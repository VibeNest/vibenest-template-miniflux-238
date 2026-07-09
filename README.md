# VibeNest Template: Miniflux

This is a thin VibeNest-ready deploy adapter for [Miniflux](https://github.com/miniflux/v2).

It does not fork or modify Miniflux. The repo provides a self-contained compose recipe:

- official image: `miniflux/miniflux:latest`
- app port: `8080`
- bundled PostgreSQL 16 service
- automatic migrations and first admin creation
- public service named `app` so Coolify/VibeNest can bind the template domain to the web container consistently.

## VibeNest notes

One-click deploy stays disabled until smoke confirms PostgreSQL bootstrap, migrations and the public login page work without manual steps. The first version uses compose Postgres so the template is self-contained; a managed Postgres recipe can replace it later.

## Upstream

- Product: https://github.com/miniflux/v2
- Docker docs: https://miniflux.app/docs/docker.html
- Database docs: https://miniflux.app/docs/database.html
