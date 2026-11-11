# Catographer landing

Astro 5 + Tailwind v4 static site, deployed to GitHub Pages at `https://disin8.github.io/catographer/`.

## Develop
```
npm install
npm run dev
npm run build
```

## Before going live
1. `src/config.ts` → set `APP_STORE_URL` (the button switches from "Coming soon" to a real link automatically).
2. Optional: add real screenshots to `public/assets/screens/` and swap `PhoneMockup` in `Hero.astro` / `HowItWorks.astro` for `<img>`.
3. Review legal text in `src/pages/privacy.astro`, `terms.astro`, `support.astro`.

## Deploy
Push to `main` of the repo that hosts the site; Settings → Pages → Source: **GitHub Actions**
(workflow: `.github/workflows/static.yml`). `package-lock.json` must be committed (`npm ci`).

The app links to `/catographer/privacy/`, `/terms/`, `/support/` — these paths are preserved.
If this replaces the old `docs/` folder in the app repo, switch Pages source only after the first successful deploy.
