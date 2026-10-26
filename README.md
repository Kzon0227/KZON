# KZON Blog

A static blog built with [Eleventy](https://www.11ty.dev/), written in
Markdown, and deployed for free on GitHub Pages.

## Local development

```bash
npm install
npm run serve
```

This starts a local server (usually at `http://localhost:8080`) and rebuilds
on every file change.

## Writing a post

Add a new Markdown file to `src/posts/`, e.g. `src/posts/my-new-post.md`:

```markdown
---
title: My New Post
description: A one-line summary shown on the homepage.
date: 2026-11-01
---

Your post content goes here, in Markdown.
```

Posts are sorted by `date`, newest first, and appear automatically on the
homepage.

## Deploying to GitHub Pages

A GitHub Actions workflow (`.github/workflows/deploy.yml`) builds and
publishes the site automatically on every push to `main`.

To enable it on your repository:

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Push to `main` (or run the workflow manually from the **Actions** tab).

The site will be published at `https://<your-username>.github.io/<repo-name>/`.

If you're deploying to a user/organization root site (a repo named
`<your-username>.github.io`) or a custom domain, edit
`.github/workflows/deploy.yml` and set `PATH_PREFIX: "/"` instead of the
repository-name prefix.

## Project structure

```
src/
  _includes/layouts/   Nunjucks layouts (base page, post page)
  posts/                Blog posts (Markdown)
  css/                  Stylesheet
  index.njk             Homepage (lists all posts)
  about.md              About page
eleventy.config.js      Eleventy configuration
.github/workflows/      GitHub Actions deploy workflow
```
