# nandishounak.github.io

Personal academic portfolio site for Shounak Nandi, built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

Live at https://nandishounak.github.io

## Structure

```
_config.yml           Site metadata, plugins, social links
_layouts/default.html  Shared page shell (nav, header, footer, theme toggle)
index.md              Home / About page
research.md           Research interests, experience, publications, skills, awards
talks.md              Conference talks and posters
news.md               Chronological updates
stats.md              Quick numeric snapshot (kept in sync manually with research.md/talks.md)
assets/css/           Site-wide and page-specific styles
assets/img/           Profile photo, favicon
assets/CV.pdf         Downloadable CV
```

Each content page is Markdown with front matter (`layout`, `title`, `permalink`, `description`); most of the page body is hand-written HTML for layout control (experience entries, publication lists, stat grids, etc.), styled by `assets/css/site.css` and `assets/css/research-compact.css`.

## Local development

Requires Ruby + Bundler.

```bash
gem install bundler jekyll
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Deployment

Pushing to `main` triggers GitHub Pages' built-in Jekyll build, so no CI configuration is needed.
