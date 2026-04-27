# hugo-tools.github.io

Source for the hugo-tools landing page at <https://hugo-tools.github.io/>.

A small Hugo site that lists every project under the
[hugo-tools](https://github.com/hugo-tools) org so newcomers find them
all from one URL. Built with no external theme — all layouts live in
`layouts/`.

## Add a project

```bash
hugo new --kind project projects/<your-project>
```

That scaffolds `content/projects/<your-project>/index.md` with the
front-matter the project card expects: name, repo URL, one-line
description, status, install hint, language tag.

## Run locally

```bash
hugo server -D
```

Open <http://localhost:1313>.

## Deploy

GitHub Pages, deployed by `.github/workflows/deploy.yml` on push to
`main`. The repo's Pages source must be set to **GitHub Actions**
(Settings → Pages) — one-time toggle.
