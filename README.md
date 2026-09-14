# Aethera Sphere — Website

A 5-page marketing site for Aethera Sphere (Social-Emotional Learning, Emotional
Intelligence and wellbeing programs), built as plain HTML/CSS/JS so it can be
deployed directly to GitHub Pages — no build step required.

## Pages

- `index.html` — Home
- `about.html` — Who We Are (mission, vision, who we serve)
- `programs.html` — What We Do (focus areas + our approach)
- `founder.html` — Founder & CEO
- `contact.html` — Contact

Shared styles live in `assets/css/styles.css`, shared behavior in
`assets/js/main.js`, and the logo lives in `assets/img/logo.jpeg`.

## Run it locally

No build tools needed. From this folder, either:

- Open `index.html` directly in a browser, or
- Serve it locally (recommended, avoids any local-file quirks):

  ```bash
  python3 -m http.server 8000
  ```

  then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a new GitHub repository and push this folder's contents to it:

   ```bash
   git init
   git add .
   git commit -m "Aethera Sphere website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch".
4. Choose the **main** branch and **/ (root)** folder, then **Save**.
5. GitHub will publish the site at:
   `https://<your-username>.github.io/<your-repo>/`

Because every internal link and asset path in this project is relative (no
leading `/`), the site works correctly both at the root of a domain and in a
GitHub Pages project subpath — no path edits needed.

### Custom domain (optional)

If you want a custom domain, add a `CNAME` file at the project root containing
just your domain name (e.g. `www.aetherasphere.com`), then point your DNS at
GitHub Pages per GitHub's documentation.

## Editing content

All page copy is plain text inside each `.html` file — search for the section
you want to change (e.g. "Ten places where growth begins") and edit directly.
Colors, fonts and spacing are controlled by CSS custom properties at the top
of `assets/css/styles.css` under `:root`.

## Notes

- Fonts (Fraunces + Karla) load from Google Fonts via `<link>` tags in each
  page's `<head>` — an internet connection is needed for them to load; the
  site falls back to system serif/sans-serif fonts otherwise.
- The hero illustration and small icons are hand-built inline SVG, so no
  image-generation service or external icon library is required.
- The contact form uses a `mailto:` submission (no backend). If you'd like a
  real hosted form (with a database or email delivery), consider a service
  like Formspree or Getform and swap the `<form action>` — ask if you'd like
  help wiring one up.
