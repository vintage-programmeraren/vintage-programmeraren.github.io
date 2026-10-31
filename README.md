# Jekyll blog starter for GitHub Pages

## Getting started

1. Create a GitHub repository. For a user site, name it `YOUR-USERNAME.github.io`.
2. Copy these files into the repository.
3. Edit `_config.yml` and set `url`, `baseurl`, `title`, and `author`.
4. Edit or remove the sample post in `_posts/`.
5. In GitHub, open **Settings → Pages** and configure publishing from your branch/root (or use GitHub Actions if prompted).

## Writing posts

Create Markdown files in `_posts/` using this filename pattern:

`YYYY-MM-DD-your-post-slug.md`

Add YAML front matter at the top. Example:

```yaml
---
layout: post
title: "My new post"
date: 2026-11-05 10:00:00 +0100
tags:
  - programming
  - notes
categories:
  - Development
description: "A short summary."
---
```

The archive groups posts by month automatically. The tags page lists tags and their posts automatically. No month or tag folders need to be created.

## Notes

- Jekyll's built-in `site.posts` collection powers the home page and archive.
- `jekyll-feed` generates an RSS feed.
- `jekyll-seo-tag` adds common SEO metadata.
- GitHub Pages supports only a defined set of plugins. If you add plugins, check the GitHub Pages plugin list first.
- For a project site (not `YOUR-USERNAME.github.io`), set `baseurl` to `"/repository-name"`.
