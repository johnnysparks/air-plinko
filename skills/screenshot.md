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
  --screenshot=$OUTPUT_PATH --window-size=${WIDTH},${HEIGHT} \
  file://$HTML_PATH 2>/dev/null
```

One command, zero installs.

- `--no-sandbox` is needed when running as root (common in containers)
- `2>/dev/null` suppresses harmless dbus errors in headless environments

## Avoiding clipped content

`--screenshot` captures exactly the viewport — no scroll. So the `--window-size` height must cover the full page content or it gets clipped.

**Since we author these HTML files, we control the height.** Best practices:

1. **Set the viewport to match the content.** When writing the diagram HTML, note the total height and use that as `--window-size` height. A little extra is fine — background color fills the gap.

2. **Design diagrams with a fixed height in mind.** Use CSS like `body { min-height: 100vh; }` and lay out content to fill a known viewport (e.g. 900×1400).

3. **If you're unsure of the height,** overestimate with `--window-size=900,2000`. The extra background pixels add minimal file size and can be visually ignored.

4. **For the cleanest results,** add a sizing hint to the HTML itself:
   ```html
   <!-- screenshot: 900x1400 -->
   ```
   Then parse it before screenshotting:
   ```bash
   SIZE=$(grep -oP 'screenshot: \K\d+x\d+' $HTML_PATH)
   WIDTH=${SIZE%x*}; HEIGHT=${SIZE#*x}
   ```

## Step 3 (last resort): Install a browser

Only if Step 1 found nothing:

```bash
npx playwright install chromium
# or
apt-get install -y chromium-browser 2>/dev/null || apt-get install -y chromium 2>/dev/null
```
