# jaeyonglee0205.github.io

Personal blog, built with [Jekyll](https://jekyllrb.com) (based on [Jekyll Now](https://github.com/barryclark/jekyll-now)) and hosted on GitHub Pages.

## Writing a post

Add a Markdown file to `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: My post title
---

Post content goes here.
```

Push to `master` and GitHub Pages rebuilds the site automatically (usually within a minute or two).

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
