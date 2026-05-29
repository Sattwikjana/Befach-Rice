# Befach Diet &amp; Diabetic White Rice — Landing Page

A premium, fully self-contained marketing landing page for **Befach Diet &amp; Diabetic White Rice** (GI 50, lab-validated low-glycemic Sona Masoori rice). A Befach Wellness brand.

> Single static HTML page — no build step, no framework, no dependencies. Deploys to any static host in seconds.

## What's inside

```
.
├── index.html              # the entire landing page (inline CSS + JS)
├── befach-rice/            # all images + lab-report PDFs
│   ├── *.jpg / *.png       # product shots, lifestyle creatives, logo, charts
│   └── reports/            # 8 lab-report PDFs (GI, amylose, heavy metals, AJFN paper, etc.)
├── vercel.json             # Vercel static config + asset caching headers
├── netlify.toml            # Netlify publish config
└── 404.html                # branded fallback
```

The page is 100% static: open `index.html` in any browser and it works offline (fonts load from Google Fonts CDN).

## Sections

Hero · trust strip · GI bar chart · "Why choose" 6-benefit grid · Befach-vs-normal comparison · field-to-plate story · interactive glucose simulator · the science · 8 downloadable lab reports · nutrition facts · heavy-metal safety · published research (AJFN 2019) · awards · India→Global exports · 2-SKU shop · verified Amazon/Flipkart reviews · doctors · find-your-pack quiz · cooking steps · creative marquee · FAQ · final CTA · footer.

## Run locally

No build needed. Either:

```bash
# Option A — just open it
open index.html

# Option B — serve it (recommended, so /befach-rice/ absolute paths resolve)
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

This is a static site — pick any host. **No build command, output/publish directory is the repo root.**

### Render (recommended — `render.yaml` included)
1. [dashboard.render.com](https://dashboard.render.com) → **New → Static Site** (or **New → Blueprint** to use `render.yaml`)
2. Connect this repo → Render auto-detects the blueprint:
   - Build command: *(none)* · Publish directory: `.`
3. **Create** → live at `https://befach-rice.onrender.com` in ~1 min
4. **Settings → Custom Domains** → add your domain → Render shows the exact DNS record to add at GoDaddy

### Vercel
1. Import this repo at [vercel.com/new](https://vercel.com/new)
2. Framework preset: **Other** · Build command: *(empty)* · Output dir: *(leave default / root)*
3. Deploy → add your custom domain under **Settings → Domains**

`vercel.json` is already included (handles asset caching).

### Netlify
1. New site from Git → pick this repo
2. Build command: *(empty)* · Publish directory: `.`
3. Deploy → add domain under **Domain management**

`netlify.toml` is already included.

### Cloudflare Pages
1. Create a Pages project from this repo
2. Build command: *(empty)* · Build output directory: `/`
3. Deploy → add custom domain

### GitHub Pages
1. Repo **Settings → Pages**
2. Source: **Deploy from a branch** → branch `main` → folder `/ (root)`
3. For a custom domain, add it under Pages settings (GitHub will create a `CNAME` file)

## Editing

Everything is in `index.html`:
- **Copy / prices** — search the text directly (e.g. `₹600`, `4.5 KG Pack`)
- **Images** — swap files in `befach-rice/`, keep the same filename, or update the `src` paths
- **Lab reports** — drop PDFs into `befach-rice/reports/`
- **Colours** — CSS custom properties at the top of the `<style>` block (`--orange`, `--cocoa`, `--gold`, etc.)
- **GI chart** — edit the `.gibar` bars in the chart section
- **Reviews** — the `.tcard` blocks in the "Real verified reviews" section

## Brand &amp; compliance

- Manufactured by **Befach 4X Private Limited**, Hyderabad
- FSSAI Lic No. **13620014000587** · FDA Reg No. **1600103515**
- GI tested by **UniQ Nutri Bio-Sciences LLP** (NABL-accredited, ISO 26642:2010) — **GI = 50**
- Disclaimer: *Befach Low-GI Rice is not a medicine and does not replace prescribed treatment. Always follow your doctor's advice.*

---

© Befach Wellness · A Befach 4X Private Limited company · Made in India
