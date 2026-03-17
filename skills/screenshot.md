# Screenshot Skill

## Strategy
Find a browser. Use `--headless --screenshot`. No libraries needed.

## Step 1: Find a browser

```bash
# Playwright-managed browsers (any version)
find /root/.cache/ms-playwright -name "chrome" 2>/dev/null
find /home -path "*/ms-playwright/*/chrome" 2>/dev/null

# System-installed
which chromium-browser chromium google-chrome google-chrome-stable 2>/dev/null

# Other common locations
ls /snap/chromium/current/usr/lib/chromium-browser/chrome 2>/dev/null
ls /usr/lib/chromium-browser/chromium-browser 2>/dev/null
ls /opt/google/chrome/chrome 2>/dev/null
```

Pick the first one that exists and is executable.

## Step 2: Screenshot

```bash
$CHROME_PATH --headless --no-sandbox --disable-gpu \
  --screenshot=$OUTPUT_PATH --window-size=900,800 \
  file://$HTML_PATH 2>/dev/null
```

That's it. One command, zero installs.

- `--no-sandbox` is needed when running as root (common in containers)
- `--window-size=900,800` controls the viewport — 900px wide works well for diagrams
- `2>/dev/null` suppresses harmless dbus errors in headless environments
- Output is a single viewport-sized PNG (no scroll capture)

## If you need full-page scroll capture

Only then reach for playwright. Sniff for it before installing:

```bash
# Check if playwright is available globally
find /opt /usr/lib /usr/local/lib -path "*/node_modules/playwright/index.js" 2>/dev/null
which playwright 2>/dev/null

# If not found, install minimally (--no-save to avoid polluting the project)
npm install --no-save playwright-core
```

## Step 3 (last resort): Install a browser

Only if Step 1 found nothing:

```bash
# Try playwright's browser installer
npx playwright install chromium

# Or system package manager
apt-get install -y chromium-browser 2>/dev/null || apt-get install -y chromium 2>/dev/null
```
