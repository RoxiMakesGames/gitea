# Gitea — Self-Hosted Git Server

[Gitea](https://gitea.com) instance managed through the Citadel panel via
`gitea_cplug`. Provides a self-hosted Git forge with repos, CI/CD, container
registry, and native OSID identity integration.

**Created in R13 (D116): replaces the archived Forgejo package.**

## Features

- **Citadel Panel Integration** — Deploy, start, stop, restart, and update
  Gitea directly from the Citadel panel via `gitea_cplug`.
- **Git Plugin Provider** — Auto-registers as a `git:providers` + `git:servers`
  provider so the Git plugin can browse Gitea repos alongside other sources.
- **Token-Aware Auth** — Uses `tokens_cplug` consumer API to acquire Gitea
  API tokens automatically.
- **Container Lifecycle** — Managed via `sovctl_rs_containers` extension.

## Installation

```bash
sovctl package install gitea
```

## Contents

| Component | Description |
|-----------|-------------|
| `gitea_cplug` | Citadel panel plugin — Gitea instance manager |
| `docker/compose.yaml` | Docker Compose merge fragment |
