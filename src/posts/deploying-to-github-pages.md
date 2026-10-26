---
title: Deploying to GitHub Pages
description: How this site builds and publishes itself automatically.
date: 2026-10-15
---

This site deploys itself with a GitHub Actions workflow defined in
`.github/workflows/deploy.yml`. Every push to `main` triggers a build:

1. Eleventy builds the site into `_site/`.
2. The workflow uploads `_site/` as a Pages artifact.
3. GitHub Pages publishes it.

To turn this on for your own copy of the repo, go to **Settings → Pages** and
set the source to **GitHub Actions**. No extra configuration is needed — the
workflow handles the rest on the next push.
