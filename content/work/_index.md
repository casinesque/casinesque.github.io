---
title: "Work"
layout: "Work"
summary: "This is the space about everything i find interesting"
alt: "Cover image"
caption: "Welcome"
draft: false
relative: false
aliases:
  - /work/
---

A collection of things I've built, broken, fixed, and learned from. I care about doing
things right, declarative, automated, and open where it can be. Most of this lives on
[GitHub](https://github.com/casinesque).

## Projects

Things I've designed and built from the ground up.

### Ovatta
My first real Go project, a configuration anonymization tool aimed at making it safe
to share infrastructure configs (think public-administration compliance / EU data
governance use cases). It's where I'm learning Go properly, by building something real.

[→ Repository](https://github.com/casinesque/ovatta)


### Spoon River Poems

When I was younger, I read this book and it stayed with me for years.
That's why i built this project, a random "Spoon River Poems" generator.
It's my small way of keeping this masterpiece alive and sharing it with anyone who might discover it for the first time.

[→ Repository](https://github.com/casinesque/spoonriverpoems)

https://spoonriverpoems.pages.dev/

## Open Source Contributions

Contributions to tools I use, projects I admire, and things I've tripped over and fixed.


- **[OpenChamber](https://github.com/openchamber/openchamber/pull/1986)** — Added a
  `docker_build_and_push` CI job to the release workflow (builds and publishes the image
  to GHCR on every release, with pinned + `latest` tags), and fixed a pre-existing
  Dockerfile bug that broke the build entirely. *(open, under review — 6.5k★ repo)*

- **[Qdrant Helm Chart](https://github.com/qdrant/qdrant-helm/pull/484)** — Added support for `namespaceOverride`, allowing chart resources to be deployed into a custom namespace instead of always using the Helm release namespace.
  *(open)*

- **[pfnet-research/gcp-workload-identity-federation-webhook](https://github.com/pfnet-research/gcp-workload-identity-federation-webhook/pull/141)** —
  Made the mutating webhook's `failurePolicy` and `reinvocationPolicy` configurable via
  `values.yaml` instead of being hardcoded, without breaking existing installs.
  *(merged, shipped in v0.6.1)*

- **[guerzon/vaultwarden](https://github.com/guerzon/vaultwarden/pull/233)** — Fixed a
  Helm template context bug (`.` vs `$`) that broke `helm template`/upgrade whenever
  additional ingress hostnames were configured. *(merged)*

- **[Hetzner CSI Driver](https://github.com/hetznercloud/csi-driver)** — Renamed Helm
named templates with a `hetzner` prefix to resolve `bitnami/common` library
collisions in umbrella charts. *(merged)*

- **[Cribl helm-charts](https://github.com/criblio/helm-charts/pull/249)** — Fixed a
  `readonly` → `readOnly` casing bug that silently mounted the host root filesystem
  read-write instead of read-only, and added a unit-test assertion to lock it down.
  *(open)*

- **[griffinskudder/updater](https://github.com/griffinskudder/updater/pull/155)** —
  Replaced a hardcoded `GOARCH=amd64` in the Dockerfile with `ARG TARGETARCH`, enabling
  multi-arch (arm64) builds via `docker buildx`. *(open)*

- **[terraform-proxmox-sdn](https://github.com/hybridops-tech/terraform-proxmox-sdn/pull/32)** — Added Terraform `validation` blocks to catch invalid Proxmox SDN naming at plan time instead of failing late against the live API.
*(open)*

- **[StellarSend/backend](https://github.com/StellarSend/backend/pull/19)** — Added a
  `.dockerignore` to shrink the build context and keep `.git/`, build artifacts, and
  `.env` out of Docker images. *(open)*


## Professional

Day-to-day I work as an SRE/Cloud/DevOps engineer, building and operating cloud
infrastructure across multiple providers and platforms.

**Platforms & multi-cloud** — Kubernetes in production across managed and
self-managed setups: **EKS**, **AKS**, **OpenShift**, and **Hetzner** bare-metal
(a deliberate choice for cost control and digital sovereignty, keeping workloads
on European infrastructure). Day-to-day work spans cluster operations, workload
reliability, pipeline orchestration, and designing infrastructure architectures
end to end across **AWS** and **Azure**.

**Infrastructure as Code & GitOps** — Infrastructure defined and managed with
**Terraform**, application and cluster config delivered through **Helm** and
GitOps workflows. I care about reproducible, reviewable infrastructure.

**CI/CD** — Pipelines built and maintained in **GitLab CI**, covering builds,
tests, artifact publishing deployments and environment management.

**Tooling & automation** — **Python** and Bash for internal tooling and
automation of repetitive operational tasks.

**Observability & Operations** — Monitoring and log aggregation with **Elastic**
**Grafana**, basically the **ELK stack**. I care about closing the DevOps loop: acting
on what monitoring tells us, not just collecting it — feeding measurements back
into capacity planning, alerting thresholds, and architecture decisions.

**Cost & Platform Efficiency** — **Kubernetes optimization** (resource tuning,
cluster right-sizing), **Artifactory** management for artifacts and dependencies,
and light **FinOps**, keeping an eye on cost and trimming waste where it makes
sense.

**Ways of working** — Autonomous, task-driven work with self-prioritization based
on impact and urgency, tracked in Jira. Beyond my own scope, I support other teams
and customers with custom solutions when standard tooling doesn't fit the need.

## Homelab

No PRs, no guidelines, no blast radius to worry about, just a Proxmox + k8s 
cluster where I get to break things on purpose. Cluster API, Kubernetes operators, self-hosted
tools, wireguard tunnels.. the more the better.