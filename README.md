# mingsoonang.com

My personal portfolio website.

Built with [Hugo](https://gohugo.io/) using the [Adritian Free Hugo Theme](https://github.com/zetxek/adritian-free-hugo-theme), deployed via Cloudflare Pages.

## Stack

- **Hugo** — static site generator
- **Bootstrap 5** — UI framework, pulled via npm and mounted into Hugo's asset pipeline
- **PostCSS + Autoprefixer** — CSS processing
- **Cloudflare Pages** — hosting & CDN

## Deployment

Pushes to `main` automatically trigger a GitHub Actions workflow. It can also be triggered manually via `workflow_dispatch`.

**Workflow steps:**
1. Checkout the repo
2. Set up Hugo and install Dart Sass (required for SCSS compilation)
3. Install Node dependencies (Bootstrap, PostCSS tooling)
4. Build the site with `hugo --minify`
5. Deploy the built files to Cloudflare Pages via Wrangler (Cloudflare's CLI)
