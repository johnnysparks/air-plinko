# Screenshot Skill

## Strategy
Don't hardcode paths. Sniff the environment for what's available. Only install as a last resort.

## Step 1: Find a browser

Search for a usable Chromium/Chrome binary in this order:

```bash
# Playwright-managed browsers (any version)
find /root/.cache/ms-playwright -name "chrome" -o -name "chromium" 2>/dev/null | head -5
find /home -path "*/ms-playwright/*/chrome" 2>/dev/null | head -5

# System-installed browsers
which chromium-browser chromium google-chrome google-chrome-stable 2>/dev/null

# Snap / flatpak / other locations
ls /snap/chromium/current/usr/lib/chromium-browser/chrome 2>/dev/null
ls /usr/lib/chromium-browser/chromium-browser 2>/dev/null
ls /opt/google/chrome/chrome 2>/dev/null
```

Pick the first one that exists and is executable.

## Step 2: Find a browser automation library

Search for playwright or puppeteer that can drive the browser:

```bash
# Global node_modules (check multiple node version paths)
find /opt -path "*/node_modules/playwright/index.js" -o -path "*/node_modules/playwright-core/index.js" 2>/dev/null
find /usr/lib -path "*/node_modules/playwright*/index.js" 2>/dev/null
find /usr/local/lib -path "*/node_modules/playwright*/index.js" 2>/dev/null

# Check if playwright CLI is on PATH (tells us the package exists somewhere)
which playwright 2>/dev/null && dirname $(which playwright)/../lib/node_modules/playwright

# Also check for puppeteer as a fallback
find /opt -path "*/node_modules/puppeteer*/index.js" 2>/dev/null
find /usr/lib -path "*/node_modules/puppeteer*/index.js" 2>/dev/null
```

Require from whatever path resolves. Prefer `playwright` > `playwright-core` > `puppeteer`.

## Step 3: If nothing found — install minimally

Only after the searches above come up empty:

```bash
# Try playwright-core first (smaller, no bundled browsers — we already found one)
npm install --no-save playwright-core

# If no browser was found either, install playwright (includes browser download)
npm install --no-save playwright && npx playwright install chromium
```

Use `--no-save` to avoid polluting the project's package.json.

## Screenshot Script

Once you've resolved `PLAYWRIGHT_PATH` (the require path) and `CHROME_PATH` (the binary):

```js
const { chromium } = require(PLAYWRIGHT_PATH);

async function screenshot(htmlPath, outputPath, width = 900, height = 800) {
  const browser = await chromium.launch({
    executablePath: CHROME_PATH  // omit if playwright found its own browser
  });
  const page = await browser.newPage({ viewport: { width, height } });
  await page.goto(`file://${htmlPath}`);
  await page.waitForTimeout(500);
  await page.screenshot({ path: outputPath, fullPage: true });
  await browser.close();
}
```

If neither playwright nor puppeteer are available, a bare Chromium can still screenshot:

```bash
# Last resort — no automation library needed
$CHROME_PATH --headless --disable-gpu --screenshot=$OUTPUT_PATH --window-size=900,800 file://$HTML_PATH
```

## Key Notes
- Use `fullPage: true` to capture the entire scrollable content
- Set viewport width to control layout (900px works well for diagrams)
- Always use absolute `file://` paths for local HTML files
- The `--headless --screenshot` fallback produces a single viewport-sized PNG (no fullPage scroll), but it works with zero dependencies
