# Berlin Wall Digital — Official Website Starter

Production-oriented bilingual (French/English) static agency website. Zero runtime dependencies, no build step, deployable straight from Git to Netlify or GitHub Pages. Separate from Remotion and MoneyPrinterTurbo.

## Features
- Responsive dark Tech Blue design, custom vector logo, accessible mobile navigation, subtle reveal animation (reduced motion supported)
- French and English language switch, with bilingual services, company profile and project brief
- Portfolio reference to `www.lacongolaise.com` (replace mock illustration and verify portfolio permission before final publication)
- Interactive budget and project request form; no backend or database; client copies summary and opens BWD WhatsApp at `https://wa.me/243802782884`
- `netlify.toml`, privacy-aware local form handling, SEO metadata and Open Graph SVG placeholder

## Preview locally (PowerShell)
```powershell
cd C:\AI\BWD\bwd-website
py -3 -m http.server 8080
```
Open http://localhost:8080. Stop with Ctrl+C. You can also use VS Code Live Server.

## GitHub push (new repo)
Create an **empty** GitHub repository called `bwd-website`, then:
```powershell
cd C:\AI\BWD\bwd-website
git init
git add .
git commit -m "Launch BWD bilingual website"
git branch -M main
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/bwd-website.git
git push -u origin main
```
Replace YOUR_GITHUB_USERNAME. Do not run `git init` inside the existing Remotion project.

## Netlify deployment from Git
- Netlify > Add new project > Import existing project > GitHub > select bwd-website.
- Build command: **leave empty**. Publish directory: **`.`**.
- Deploy; review the preview link before attaching any custom domain.
- Connect your owned domain only after confirming ownership and current DNS records. No domain ownership is assumed.

## GitHub Pages
- For the project repository `username.github.io/bwd-website/`, use GitHub Pages > Deploy from branch > `main` / `/ (root)`. Static files do not require a workflow.
- All local asset links are relative and work under a repository subpath.

## Before real clients arrive
- Replace the placeholder CSS artwork / example case study with approved, real project imagery; no unverified client results or testimonials have been invented.
- Verify `https://www.lacongolaise.com/` is publicly reachable and that you have permission to use it as a portfolio reference.
- Review all French/English copy, chosen contact link, favicon and social preview.
- Test form copy/open flow on Android and iPhone; browsers may restrict clipboard and users must paste their brief manually.
- This is a static site: it does **not** send, store or receive inquiries; WhatsApp interaction happens in WhatsApp itself.
- If adding analytics, cookies, an actual form backend, CRM, or client-data collection later, update privacy notices and configuration accordingly.

## Files
- `index.html` — structure and initial French text
- `styles.css` — responsive layout, Tech Blue style and interactions
- `script.js` — translations, navigation, animation, form brief builder
- `assets/favicon.svg`, `assets/social-preview.svg` — vector identity
- `netlify.toml` — Netlify static-site config
