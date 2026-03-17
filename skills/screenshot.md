# Screenshot Skill

## Primary Method: Playwright (confirmed working)

Playwright is globally installed at `/opt/node22/lib/node_modules/playwright` with Chromium.

```javascript
const { chromium } = require('/opt/node22/lib/node_modules/playwright');
(async () => {
  const browser = await chromium.launch();
  const page = await browser.newPage({ viewport: { width: 1200, height: 900 } });
  await page.goto('file://' + __dirname + '/diagram.html');
  await page.waitForTimeout(2000); // allow Three.js / CSS animations to render
  await page.screenshot({ path: 'diagram.png' });
  await browser.close();
})();
```

### Key Notes
- **Must use absolute path** to module: `require('/opt/node22/lib/node_modules/playwright')`
- `require('playwright')` does NOT work (not in local node_modules)
- Use `file://` protocol with absolute paths for local HTML files
- Wait at least 2s for Three.js scenes to initialize
- Default viewport 1200×900 works well for 3D diagrams
- Chromium runs headless by default — no display server needed

## Fallback Method: Direct Chrome CLI

```bash
$CHROME_PATH --headless --no-sandbox --disable-gpu \
  --screenshot=$OUTPUT_PATH --window-size=${WIDTH},${HEIGHT} \
  file://$HTML_PATH 2>/dev/null
```

- `--no-sandbox` needed when running as root
- `2>/dev/null` suppresses dbus errors

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
