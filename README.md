# LOCS:23 Gap Analysis — AiLA

Self-assessment tool for law firms evaluating their readiness against the LOCS:23 certification standard — the ICO-approved data protection certification scheme for legal services providers.

## What it covers

34 controls across 5 sections matching the LOCS:23 standard (V12.3):

1. Governance (Section 8.1)
2. Data Subject Rights (Section 8.2)
3. Operational Privacy (Section 8.3)
4. Third Parties (Section 8.4)
5. Monitor & Review (Section 8.5)

## How it works

The assessment adapts to your firm's profile. An intake screen captures: organisation name, controller/processor status, firm size, and practice areas. Questions are tailored based on these answers — controller-only controls are flagged, and help text adjusts for firm size and practice area (e.g. firms handling criminal or family law receive specific guidance on special category data).

Each control is assessed through yes/no questions against the standard's requirements. The sidebar shows live compliance scoring per section with an overall percentage.

## Report output

- Overall compliance score with section-by-section breakdown
- Status per control: compliant, partial, or gap
- Auto-generated action plan identifying gaps, recommended actions, priority level, and GDPR article references
- Formspree integration for lead capture

## Tech stack

- React 18
- Vite
- No backend — runs entirely in the browser
- Deployed on Vercel

## Local development

```bash
npm install
npm run dev
```

## Deployment

Push to GitHub, connect repo to Vercel. Auto-deploys on every commit.

## Sources

- LOCS:23 Standard V12.3 (2twenty4 Consulting / Tim Hyman)
- UK GDPR Articles 5–39
- Data Protection Act 2018
- ICO guidance for data controllers and processors

## Related

- [DSAR Readiness Assessment](https://dsar-readiness.vercel.app/) — assesses DSAR handling capability
- [ICO Accountability Assessment](https://ico-accountability.vercel.app/) — assessment against the ICO's full Accountability Framework

---

© AiLA AI Ltd · [trustaila.com](https://trustaila.com)# LOCS:23 Readiness Assessment

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
