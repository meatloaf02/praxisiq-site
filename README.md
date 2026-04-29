# PraxisIQ Website

Static single-page site for [praxisiq.studio](https://praxisiq.studio). Built for GitHub Pages.

## Quick deploy

1. Create a new repo on GitHub (e.g. `praxisiq-site` or `praxisiq.studio`)
2. Push these files:

```bash
cd praxisiq-site
git init
git add .
git commit -m "Initial PraxisIQ site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/praxisiq-site.git
git push -u origin main
```

3. Go to **Settings → Pages** in your GitHub repo
4. Under **Source**, select `main` branch and `/ (root)` folder
5. Under **Custom domain**, enter `praxisiq.studio`
6. Check **Enforce HTTPS** (may take a few minutes to provision)

The `CNAME` file is already included — GitHub will recognize it automatically.

## DNS (already done via Squarespace)

Your Squarespace DNS should have these records pointing to GitHub:
- `A` records pointing to GitHub's IPs:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- `CNAME` for `www` pointing to `YOUR_USERNAME.github.io`

## Contact form

The contact form uses [Formspree](https://formspree.io) for processing (free tier: 50 submissions/month). To activate:

1. Sign up at formspree.io
2. Create a new form
3. Copy your form ID (looks like `xyzabc12`)
4. Replace `YOUR_FORM_ID` in `index.html` line with your actual ID:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

Alternative: You can swap Formspree for any form backend (Netlify Forms, Basin, Google Forms embed, Calendly embed, etc.)

## Customization checklist

- [ ] Replace `YOUR_FORM_ID` in the contact form action URL
- [ ] Update LinkedIn URL in the contact section
- [ ] Personalize the About section with your background
- [ ] Replace placeholder case study metrics with real ones (or remove until ready)
- [ ] Add your Google Analytics 4 tag (paste before `</head>`)
- [ ] Add your Google Search Console verification meta tag

## Structure

```
praxisiq-site/
├── index.html    ← Entire site (single page, all CSS/JS inline)
├── CNAME         ← Custom domain for GitHub Pages
└── README.md     ← This file
```

## Brand reference

- **Fonts**: Lora (headings) + DM Sans (body) via Google Fonts
- **Primary colors**: Indigo #1B2B5B, Teal #1A9E7A, Coral #D85A30
- **Favicon**: Inline SVG "PQ" monogram (no external file needed)
- **Full brand brief**: See `PraxisIQ_Brand_Brief.docx`
