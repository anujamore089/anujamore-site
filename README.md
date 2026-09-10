# anujamore.com

A single-file personal site. No build step, no framework — just `index.html`.

## Edit

Everything lives in `index.html`. Each section is marked with a comment
(`<!-- ===== HERO ===== -->`, `ABOUT`, `HIGHLIGHTS`, `AI PROJECTS`, `CONTACT`).

- **Photo:** replace `<div class="hero-photo">A</div>` with
  `<div class="hero-photo"><img src="photo.jpg" alt="Anuja More"></div>` and drop `photo.jpg` next to `index.html`.
- **New highlight / project:** copy one `<a class="card">…</a>` block and change the link, tag, title, and blurb.
- **Colors:** change `--accent` (and `--accent-ink`, `--accent-soft`) in the `:root` block at the top.

## Deploy on Cloudflare Pages (about 5 minutes)

1. Create a GitHub repo (e.g. `anujamore-site`) and push this folder.
2. In the Cloudflare dashboard: **Workers & Pages → Create → Pages → Connect to Git**, pick the repo.
3. Build settings: Framework preset **None**, build command **(leave empty)**, output directory **/**.
4. Click **Save and Deploy**. You get a `*.pages.dev` URL immediately.
5. **Custom domain:** Pages project → **Custom domains → Set up a custom domain** → enter your domain.
   Because the domain is registered at Cloudflare, DNS is added automatically and HTTPS is on by default.

Every later `git push` redeploys automatically.

### Alternative: no GitHub

**Workers & Pages → Create → Pages → Upload assets** and drag this folder in. Re-upload to update.
