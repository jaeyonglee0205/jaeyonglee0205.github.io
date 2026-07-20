# jaeyonglee0205.github.io

Personal blog, built with [Jekyll](https://jekyllrb.com) (based on [Jekyll Now](https://github.com/barryclark/jekyll-now)) and hosted on GitHub Pages.

## Writing a post

A post is a Markdown file in `_posts/` named `YYYY-MM-DD-title.md`. [`_drafts/template.md`](_drafts/template.md) has the starting front matter to copy.

**From the browser, no local setup needed:**

1. Go to this repo on github.com and press `.` (period) — that opens a full VS Code-style editor in the browser (github.dev).
2. In the `_posts/` folder, create a new file named `YYYY-MM-DD-your-title.md` (today's date, lowercase-hyphenated title).
3. Paste in the contents of [`_drafts/template.md`](_drafts/template.md), fill in the title and body.
4. Commit directly to `master` (or open a PR if you want to review the diff first).

Alternatively, the **GitHub mobile app** lets you create/edit files the same way from your phone.

Either way, GitHub Pages rebuilds the site automatically after the commit lands on `master` (usually within a minute or two).

## Enabling comments (giscus)

Comments are powered by [giscus](https://giscus.app), which stores comments as GitHub Discussions on this repo — no third-party account, no ads. One-time setup:

1. In this repo's **Settings → General → Features**, enable **Discussions**.
2. Install the [giscus GitHub App](https://github.com/apps/giscus) on this repository.
3. Go to [giscus.app](https://giscus.app), enter this repo, and copy the generated `data-repo-id` and `data-category-id` values.
4. Paste those values into the `giscus:` block in [`_config.yml`](_config.yml).

Until `repo_id`/`category_id` are filled in, the comments section is simply hidden.

## Local development

This repo doesn't track a `Gemfile` (see `.gitignore`), so create one locally the first time:

```bash
echo 'source "https://rubygems.org"' > Gemfile
echo 'gem "github-pages", group: :jekyll_plugins' >> Gemfile
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
