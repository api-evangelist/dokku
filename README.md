# Dokku (dokku)

Dokku is an open-source Docker-powered self-hosted Platform-as-a-Service — often described as "the smallest PaaS implementation you've ever seen" and a self-hosted mini-Heroku. It turns a single Linux host (or a multi-host scheduler such as K3s or Nomad) into a `git push` deployment target that builds applications from Heroku-compatible buildpacks, Cloud Native Buildpacks, Nixpacks, Railpack, Dockerfiles, or pre-built Docker images. Dokku is MIT licensed, written primarily in Bash, and maintained by the Dokku organization on GitHub since 2013.

**APIs.json:** [apis.yml](https://raw.githubusercontent.com/api-evangelist/dokku/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **x-type:** opensource
- **License:** MIT
- **Primary interface:** `dokku` CLI invoked over SSH
- **Public REST/HTTP API:** None in core. The historical `dokku-api` Ruby wrapper is archived and unmaintained.

## Tags

PaaS, Self-Hosted, Docker, Containers, Buildpacks, Deployment, DevOps, Heroku Alternative, Open Source, Git Push Deploy, Kubernetes, Nomad, K3s, CLI, Plugins

## APIs

Dokku does not expose a first-party public HTTP REST API in its core distribution. Operators interact with Dokku through the `dokku` CLI, which is invoked locally on the host or remotely over SSH (`ssh dokku@host <command>`). Application deployment is performed by pushing a git remote to the Dokku host, which triggers the configured builder (buildpacks, Dockerfile, Nixpacks, Railpack, Cloud Native Buildpacks, or Lambda) and the configured scheduler (Docker local, K3s, or Nomad).

The archived `dokku/dokku-api` project previously exposed an HTTP wrapper on top of the `dokku-daemon` service but is no longer maintained and is not recommended for new deployments.

## Builders

- Cloud Native Buildpacks
- Herokuish (Heroku-compatible buildpacks)
- Dockerfile
- Nixpacks
- Railpack
- Lambda (via `lambda-builder`)
- Null

## Schedulers

- Docker Local (default, single host)
- K3s (`scheduler-k3s`, lightweight Kubernetes)
- Nomad (`dokku-scheduler-nomad`)
- Null

## HTTP Proxies

- Nginx (default)
- HAProxy
- Caddy
- Traefik
- OpenResty

## Official Plugins and Tooling

Datastores: dokku-postgres, dokku-mysql, dokku-mariadb, dokku-redis, dokku-mongo, dokku-memcached, dokku-rabbitmq, dokku-elasticsearch, dokku-couchdb, dokku-rethinkdb, dokku-clickhouse, dokku-meilisearch, dokku-typesense, dokku-solr, dokku-nats, dokku-pushpin, dokku-graphite.

Operations: dokku-letsencrypt, dokku-maintenance, dokku-http-auth, dokku-redirect, dokku-copy-files-to-image, dokku-event-listener, dokku-update, dokku-cron-restart.

Integrations: `github-action`, `gitlab-ci`, `dokku-orb` (CircleCI), `ansible-dokku`, `azure-quickstart-templates`, `homebrew-repo`.

Supporting projects: herokuish (build environment), plugn (plugin/hook system), sshcommand (SSH thin client), procfile-util, docker-image-labeler, netrc, sigil, docker-container-healthchecker, openresty-docker-proxy, compose-transpiler.

## Common Properties

- [Website](https://dokku.com)
- [Documentation](https://dokku.com/docs/)
- [Getting Started](https://dokku.com/docs/getting-started/installation/)
- [Tutorials](https://dokku.com/tutorials/)
- [Blog](https://dokku.com/blog/)
- [GitHub](https://github.com/dokku/dokku)
- [GitHub Organization](https://github.com/dokku/)
- [Releases](https://github.com/dokku/dokku/releases)
- [License (MIT)](https://github.com/dokku/dokku/blob/master/LICENSE)
- [Sponsorship](https://github.com/sponsors/dokku)
- [Dokku Pro](https://pro.dokku.com/)
- [Discord](https://discord.gg/YQjANGMZ)
- [Slack](https://slack.dokku.com/)
- [GitHub Discussions](https://github.com/dokku/dokku/discussions)

## Maintainers

- **FN:** Kin Lane
- **Email:** kinlane@gmail.com
