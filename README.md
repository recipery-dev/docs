<p align="center">
  <img src="public/logo.png" alt="Recipery" width="96" />
</p>

<h1 align="center">Recipery Docs</h1>

<p align="center">
  Documentation site for <a href="https://github.com/recipery-dev/recipery">Recipery</a>,
  a self-hosted recipe manager. Built with <a href="https://nimbus-docs.com">Nimbus</a>.
</p>

<p align="center">
  <a href="https://github.com/recipery-dev/docs/actions/workflows/deploy.yml"><img src="https://github.com/recipery-dev/docs/actions/workflows/deploy.yml/badge.svg" alt="Deploy"></a>
  <a href="https://docs.recipery.dev"><img src="https://img.shields.io/badge/site-docs.recipery.dev-blue" alt="Site"></a>
  <a href="https://github.com/recipery-dev/recipery"><img src="https://img.shields.io/badge/app-recipery--dev%2Frecipery-orange" alt="App repo"></a>
</p>

Live at [docs.recipery.dev](https://docs.recipery.dev) — covers
[Features](https://docs.recipery.dev/features),
[Deployment](https://docs.recipery.dev/deployment) (Docker, Cloudflare,
Kubernetes), [Storage](https://docs.recipery.dev/storage) backends, and
the [HTTP API](https://docs.recipery.dev/api/overview).

## Develop

```sh
pnpm install
pnpm dev
```

## Build

```sh
pnpm build   # static output to dist/
pnpm preview
```

A `Makefile` wraps these as `make dev`, `make build`, `make preview`,
`make typecheck`, `make lint`, and `make clean` — see `make help`.

## Deploy

Pushes to `main` build and deploy automatically to GitHub Pages via
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml). The site is
served at https://docs.recipery.dev, backed by GitHub Pages' default
`recipery-dev.github.io` host via a `CNAME` record and the `public/CNAME` file
in this repo.

On first deploy, enable Pages for this repo under **Settings → Pages →
Source → GitHub Actions**.

## Contributing

This repo holds only the documentation — for the application itself, see
[recipery-dev/recipery](https://github.com/recipery-dev/recipery). See
[`AGENT.md`](AGENT.md) for the site's file layout and authoring
conventions (frontmatter shape, adding pages, running `nimbus-docs check`).

## Attribution

This site started from the [bookhoard/docs](https://github.com/bookhoard/docs)
template (the same Nimbus docs scaffold, adapted here for Recipery).
