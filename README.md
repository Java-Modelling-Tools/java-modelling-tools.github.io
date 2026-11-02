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

## Badges and download statistics

- **Home page badges** (`layouts/partials/badges.html`): the four SourceForge
  community awards are hardcoded image URLs; the GitHub shields badges (stars,
  forks, contributors, issues, latest release, license) are toggled by
  `params.badges.enableGithub` in `hugo.toml`. They render "repo not found"
  while the `jmt` repository is private and light up automatically once it is
  public.
- **Download statistics** (`layouts/partials/download-stats.html`): Hugo fetches
  download counts from the SourceForge
  [Download Stats API](https://sourceforge.net/p/forge/documentation/Download%20Stats%20API/)
  at *build time*. The Download page embeds a compact summary
  (`mode = "summary"`); the dedicated
  [Statistics page](https://java-modelling-tools.github.io/statistics/)
  (`content/statistics.md`, `mode = "full"`) shows everything the API offers:
  all-time/last-30-days/release totals, downloads by year, the last 12 months,
  every operating system, every country, and the OS-by-country matrix. If the
  API is unreachable the build still succeeds and a note is shown instead.
  When a new release ships, update `params.releaseStats` (`version`, `folder`,
  `releaseSince`) in `hugo.toml`.

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
