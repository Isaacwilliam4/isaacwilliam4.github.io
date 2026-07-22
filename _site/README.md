# isaacwilliam4.github.io

Personal site for Isaac Peterson — built with Jekyll and served via GitHub Pages.

## Structure

- `index.html`, `about.md`, `resume.html`, `publications.html`, `projects.html` — top-level pages
- `_projects/` — project collection (one Markdown file per project, rendered with the `project` layout)
- `_layouts/` — page templates (`default.html`, `project.html`)
- `_includes/` — shared partials (e.g. `nav.html`)
- `_config.yml` — site config (title, collections, defaults)
- `_site/` — generated output; not edited by hand, rebuilt from the source files above

## Local development

Requires Ruby and Bundler.

```bash
sudo apt install ruby-rubygems ruby-dev build-essential
gem install --user-install bundler
```

Bundler installs gems into your home directory with `--user-install`, so avoid `sudo` on `bundle`/`gem` from here on — running Bundler as root pollutes the system gem path with root-owned files. Install dependencies into a project-local folder instead:

```bash
bundle config set --local path 'vendor/bundle'
bundle install
bundle exec jekyll serve
```

Then visit http://localhost:4000. `jekyll serve` rebuilds `_site/` automatically on file changes.

To do a one-off build without serving:

```bash
bundle exec jekyll build
```

## Deployment

Pushing to `main` publishes automatically via GitHub Pages.
