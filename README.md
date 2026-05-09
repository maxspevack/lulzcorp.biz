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

Persona portraits, the LulzCorp seal, and other illustrations are pending generation
via Google AI Studio. CSS-stubbed placeholders in the meantime.

---

*Sister site to [spevack.org](https://spevack.org). The work is for real. The wrapper is for the lulz.*
