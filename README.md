# LOCS:23 Readiness Assessment

Free compliance readiness assessment tool for UK law firms, covering all 34 LOCS:23 controls.

Built by [AiLA](https://trustaila.com) — AI automation of routine legal and compliance tasks.

## Deploy to Vercel (recommended)

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com), sign in with GitHub
3. Import this repository
4. Vercel auto-detects Vite — click **Deploy**
5. Done. You'll get a URL like `locs23-assessment.vercel.app`

To use a custom domain (e.g. `locs23.trustaila.com`):
- In Vercel project settings → Domains → Add `locs23.trustaila.com`
- Add a CNAME record in your DNS pointing to `cname.vercel-dns.com`

## Local development

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

Output goes to `dist/` — can be deployed to any static host.

## Alternative: GitHub Pages

Add to `vite.config.js`:
```js
base: '/locs23-assessment/',
```

Then use the GitHub Pages action or push `dist/` to `gh-pages` branch.

## Architecture

- Single React app, no backend
- Form submissions go to Formspree (endpoint `mjgerjao`)
- Business email validation (blocks consumer domains)
- Controller/Processor conditional paths per LOCS:23 Appendix 3
- Based on LOCS:23 Certification Standard v12.3 (© 2twenty4 Consulting Ltd)
