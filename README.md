# Unified Production Environment — Prototype

A single-file, interactive visual prototype of the Unified Production Environment (UPE) concept: an environment that takes a project from tender/bid intake through to a fully provisioned, data-driven production environment.

## What it shows

Walking through one worked example — a bridge rehabilitation tender — across seven stages:

1. **Intake** — a tender/bid folder is dropped in.
2. **Extraction** — a pipeline of agents parses the documents, extracts entities (client, location, value, scope), classifies the discipline, and maps required capabilities.
3. **Project Profile** — the project's identity is established: name, code, client, discipline, capabilities, and tools. Either adopted directly from the spec, or inferred here.
4. **Resourcing** — the other path in: the organization's knowledge graph places the project — region, project manager, available resource pools, precedent projects, and existing software entitlements.
5. **Work Breakdown** — scope is decomposed into work packages, each tagged with the capability, resource, and tool it needs.
6. **Provisioning** — the common data environment, document management, workflows, and software configure themselves automatically.
7. **Live Environment** — the resulting production environment: KPIs, work package status, and a live activity feed.

## Viewing it

Open `index.html` directly in a browser — it's fully self-contained (no build step, no dependencies beyond Google Fonts).
