# quartenson-legal

Static legal pages for Quartenson mobile applications, hosted on GitHub Pages.

## Pages

| Page | File | Description |
|------|------|-------------|
| Homepage | `index.html` | Landing page with links to all legal pages |
| Privacy Policy | `privacy-policy.html` | Privacy policy covering Firebase, AdMob, subscriptions |
| Terms & Conditions | `terms-and-conditions.html` | Terms of use for apps and subscriptions |

## Tech Stack

- Plain HTML, CSS, and minimal vanilla JS
- No build step, no framework, no dependencies
- Responsive / mobile-friendly
- Automatic dark mode via `prefers-color-scheme`

## Repository Structure

```
quartenson-legal/
├── index.html                  # Homepage
├── privacy-policy.html         # Privacy policy
├── terms-and-conditions.html   # Terms & conditions
├── css/
│   └── style.css               # Shared stylesheet
└── README.md
```

## Deploying to GitHub Pages

### Option A – Deploy from the `main` branch root (recommended)

1. Push this repository to GitHub (or ensure it is already there).
2. Go to **Settings → Pages** in the repository on GitHub.
3. Under **Source**, choose:
   - **Branch:** `main` (or whichever branch holds the files)
   - **Folder:** `/ (root)`
4. Click **Save**.
5. GitHub will publish the site at `https://<your-org>.github.io/quartenson-legal/`
   within a minute or two.

### Option B – Deploy from a `gh-pages` branch

```bash
# From the repository root, push directly to gh-pages
git subtree push --prefix . origin gh-pages
```

Then configure Pages to use the `gh-pages` branch (root folder) in Settings.

### Option C – Custom domain

1. Complete Option A or B above.
2. Add a `CNAME` file to the repository root containing your domain, e.g.:
   ```
   legal.quartenson.com
   ```
3. Point your DNS to GitHub Pages (`185.199.108.153` etc.) as described in the
   [GitHub Pages custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Updating Content

All legal content lives directly in the HTML files — no build step needed.

1. Edit the relevant `.html` file.
2. Update the **"Last updated"** date in the `<p class="page-meta">` element.
3. Commit and push — GitHub Pages will redeploy automatically.

## Contact Placeholders

The following email placeholders are used across the pages. Replace them with real
addresses before publishing:

| Placeholder | Used in |
|-------------|---------|
| `quartenson.support@gmail.com` | Privacy Policy |
| `quartenson.support@gmail.com` | Homepage, Terms, footer |

## License

Content is proprietary to Quartenson. Code/structure may be reused freely.