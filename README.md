# java-modelling-tools.github.io

Official website of **Java Modelling Tools (JMT)**, served at
<https://java-modelling-tools.github.io/>.

This repository is the GitHub Pages organization site for the
[Java-Modelling-Tools](https://github.com/Java-Modelling-Tools) organization.
It succeeds the legacy project site at <https://jmt.sourceforge.net/>.

## Stack

- [Hugo](https://gohugo.io/) static site generator (extended edition)
- GitHub Actions deployment to GitHub Pages (see `.github/workflows/pages.yml`)
- No theme: layouts, partials and CSS live in `layouts/` and `assets/css/`

## Local development

1. Install Hugo extended (0.169.0 or later): <https://gohugo.io/installation/>
2. Run `hugo server` and open <http://localhost:1313/>

```sh
hugo server          # live preview
hugo --minify --gc   # production build into public/
```

## Editing content

- Pages are Markdown files in `content/`
  - `content/_index.md` - home page (tool cards are configured in its
    front matter)
  - `content/tools/*.md` - the six tool pages; screenshots are configured in
    front matter
- Images, papers, and other static files live in `static/`
- Navigation is configured in `hugo.toml` (`[menu] main`)
- Styling is in `assets/css/main.css`

## Deployment

Every push to `main` triggers `.github/workflows/pages.yml`, which builds the
site with Hugo and deploys it via GitHub Actions to Pages.

## Migration notes

- The legacy site (`jmt.sourceforge.net`) was migrated page-by-page on
  02-Nov-2026: Introduction, Download, Requirements, six tool pages,
  Documentation, License.
- Binary downloads still point at SourceForge files until GitHub Releases
  take over (see the HTML comment in `content/download.md`).
- Community links (help/bugs/features) still point at SourceForge until the
  `Java-Modelling-Tools/jmt` repository becomes public (see the HTML comment
  in `layouts/partials/footer.html`).
- To redirect the old domain, replace the SourceForge "Project Web" content
  with a single page containing
  `<meta http-equiv="refresh" content="0; url=https://java-modelling-tools.github.io/">`.

## License

JMT is released under the GNU GPL v2 (see `static/License.txt`).
