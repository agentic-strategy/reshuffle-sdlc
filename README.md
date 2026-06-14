# The System, Not the Task — Reshuffle, applied to the SDLC

An internal explainer of Sangeet Paul Choudary's *Reshuffle* (AI as coordination, not
automation) mapped onto the software development lifecycle. Ships as a single static
website plus a downloadable slide deck and whitepaper.

**Live site:** `https://<your-username>.github.io/<repo-name>/`

## Contents
| Path | What it is |
|------|------------|
| `index.html` | The website (self-contained — all CSS, JS and diagrams are inline). Light + dark themes. |
| `downloads/Reshuffle-applied-to-the-SDLC.pptx` | 20-slide deck with speaker notes. |
| `downloads/Reshuffle-applied-to-the-SDLC.docx` | The full written whitepaper. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (no Jekyll processing). |

## Deploy on GitHub Pages (simplest)

1. Create a new repository on GitHub (Public).
2. Push these files to the `main` branch (see commands below), **or** use
   GitHub's *Add file → Upload files* to drag the whole folder in.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set **Branch** to `main` and the folder to **`/ (root)`**, then **Save**.
6. Wait ~1 minute, refresh, and your site is live at the URL shown on that page.

### Push from your machine

```bash
# from inside this folder
git init
git add .
git commit -m "Reshuffle → SDLC explainer"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Or with the GitHub CLI (creates the repo and pushes in one step):

```bash
gh repo create <repo-name> --public --source=. --remote=origin --push
```

## Custom domain (optional)
In **Settings → Pages → Custom domain**, enter your domain and Save. Add a `CNAME`
record at your DNS provider pointing to `<your-username>.github.io` (or four A records
for an apex domain). GitHub provisions HTTPS automatically once DNS resolves.

## Don't want to use Git?
Drag this folder onto **Netlify Drop** (app.netlify.com/drop), **Cloudflare Pages**, or
**Vercel** — each gives you a live HTTPS URL in seconds with no command line.

---
Independent synthesis for discussion — not affiliated with or endorsed by the author.
Concepts & quotations © Sangeet Paul Choudary; diagrams are an original interpretation
of his frameworks.
