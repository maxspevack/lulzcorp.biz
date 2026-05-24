# lulzcorp.biz

Corporate website for LulzCorp. Hosted on GitHub Pages.

## Stack

Pure Jekyll 4.x. No build pipeline beyond `jekyll build`.

| Path | Purpose |
|------|---------|
| `index.md` | The Portfolio (front page) |
| `charter.md` | LulzCorp Charter and Tenets |
| `personnel.md` | The Federated Specialist Fleet |
| `subsidiaries/` | Operating subsidiary pages |
| `_posts/` | Filings (press releases) |
| `about.md` | Founder, Office of the Consigliere |
| `_layouts/default.html` | Layout |
| `_layouts/filing.html` | Filing layout (post pages) |
| `assets/css/lulzcorp.css` | Theme — Corporate Filing aesthetic |

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

## Publishing

Push to `main`. GitHub Action at `.github/workflows/pages.yml` builds and deploys.

In the GitHub repo settings: **Settings → Pages → Source** must be set to **GitHub Actions**.

## Image assets

`assets/img/` contains 9 persona portraits (`personnel/`), 4 subsidiary wax seals
(`seals/`, transparent PNG), the LulzCorp corporate stamp (`lulzcorp-stamp.png`,
transparent), and the social-card image (`og-image.jpg`). Favicons live at the repo
root. Assets were generated in Google AI Studio and processed locally with
ImageMagick (flood-fill for seal transparency, JPEG q85 + progressive for portraits).

## Single source of truth

`_data/subsidiaries.yml`, `_data/domains.yml`, and `_data/personnel.yml` are the
canonical registries. Templates render from these. Update once; the site re-flows.

---

*Sister site to [spevack.org](https://spevack.org). The work is for real. The wrapper is for the lulz.*
