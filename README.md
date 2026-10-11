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

## Kelp Bight

`kelp-bight.html` is a separate, unrelated prototype in this same repo: a browser-based survival game set in a fictional off-grid Alaskan fishing settlement. A short narrative prologue and a per-character arrival vignette set the scene, then you play a newcomer with one autumn (50 days, 3 action slots each, a visible day/night cycle on the map) to get ready for winter — walking around a small hand-drawn pixel-art village, chopping wood and fishing through short timing-based minigames, learning skills from six named residents, and building the kind of standing with them that shows up unasked when a storm takes out your roof. You arrive with one real skill and have to pick up the rest as the season forces your hand: hunger and cold are running stats, not just an ending checklist, so eating, keeping the stove fed, and asking for help (or trading) aren't optional flavor — they're what the days are actually about. NPCs also come to *you*: a request queue where they ask for a concrete favor (spare firewood, an extra hand hauling) with a deadline, and accepting, declining, or ignoring it all carry consequences. Scripted narrative beats mark the season's turning points (first hunger, first storm, the halfway point, winter closing in). The core thesis: self-sufficiency exists at the settlement level, never the individual level — money is fast and always tempting, but it buys nothing that lasts.

Move with WASD or the arrow keys, press E near someone or something to interact. Chopping, felling, hunting, and fishing are short interactive minigames rather than a single click; everything else (eating, learning a skill, using an NPC's gated equipment, cooking, repairs, the town trip) opens a small panel where you stand.

Open `kelp-bight.html` directly in a browser. It's a single self-contained file — React, ReactDOM, and the compiled game code are inlined, and Tailwind's output is precompiled and inlined too, so it needs no build step and no CDN access beyond an optional Google Fonts stylesheet (it falls back to system serif/monospace fonts if that's unreachable). The village art, including the day/night sky, is all hand-drawn with canvas primitives (flat shapes, no sprite sheets or external assets) at a small scale with pixelated scaling, in keeping with the no-build-step, no-dependencies spirit of this repo. All game state is in-memory only; every tunable number lives in the `BALANCE` object at the top of the script.
