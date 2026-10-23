# GRID — Local Evaluation

GRID is a legal-practice management platform (cases, tasks, workflows, document
management, and an AI assistant) delivered as a licensed cloud product at
**https://grid.ia.br**.

This repository contains everything you need to **run GRID on your own machine for
evaluation**: a prebuilt, compiled backend image, the obfuscated web app, and a
`docker-compose.yml` that brings the whole stack up with one command. It does **not**
contain source code — see [LICENSE.md](LICENSE.md).

> **Evaluation build.** This local build is a self-contained trial. It is not connected
> to the GRID cloud, stores everything in its own local database, and is capped (see
> **[Trial limits](#trial-limits)**). The full product — multi-tenant cloud, unlimited
> cases, team/ownership scopes, integrations, and the full AI tier — runs only on a
> **licensed** GRID instance. See **[Going beyond the trial](#going-beyond-the-trial)**.

---

## Requirements

- **Docker** with the Compose plugin (`docker compose`, v2). Docker Desktop on
  macOS/Windows, or Docker Engine on Linux.
- **~6 GB RAM** free (the optional local AI model needs ~2 GB of that), **~5 GB disk** for
  images, the local database, and the ~1 GB AI model.
- Ports **8080** (web) and **3307** (database, optional) free on your machine.
- Architecture: images are published for **linux/amd64** and **linux/arm64**
  (Apple Silicon, ARM servers). Docker picks the right one automatically.

No Python, Node, or MySQL install is needed — everything runs in containers. The first
`docker compose up` pulls the images and fetches the local AI model once (internet needed
that first time only); afterwards it runs fully offline.

---

## Quick start

```bash
# 1. Get this repository
git clone https://github.com/grid-ia/GRID.git
cd GRID

# 2. Create your local settings from the sample (safe defaults; edit if you like)
cp .env.sample .env

# 3. Start GRID
docker compose up -d

# 4. Watch it come up (first run pulls images and seeds the database — a few minutes)
docker compose logs -f grid
```

When the log shows the backend is listening, open:

> **http://localhost:8080**

Sign in with the evaluation administrator account created on first boot:

| Field    | Value                 |
|----------|-----------------------|
| User     | `admin@grid.local`    |
| Password | `admin` *(you will be asked to change it on first login)* |

Stop the stack with `docker compose down`. Your data is preserved in a Docker volume
between runs; `docker compose down -v` erases it and starts fresh.

---

## What you can do in the trial

- Create and manage **cases, people, parties, and tasks**.
- Use the **Kanban task board** and the **workflow** steps.
- **Import a spreadsheet** (`/admin/import`) to create a table and load your own data,
  then browse and edit it through generated screens.
- Attach documents (**GED**) and try the AI document analysis.
- Chat with the built-in **AI assistant**. The trial runs a small **local** language model
  (no API key, no cost) so the assistant answers out of the box; it is intentionally limited.
  The model is fetched once on first start and then runs offline. Supply your own provider
  key in `.env` for full answers (see comments in `.env.sample`). Don't need the assistant?
  `docker compose stop mini-llm-engine mini-llm-download` to free its memory.

## Trial limits

The evaluation build runs as a **trial** with built-in caps:

- **10 active cases per user.** Creating an 11th is refused with a message explaining the
  limit; deleting a case frees a slot. (This is the same `cases` allowance the product
  meters — in the trial it is fixed at 10 and cannot be raised locally.)
- **Single local tenant**, no cloud sync, no multi-firm separation.
- **Local AI model only** unless you add your own provider key.
- **No outbound integrations** (webhooks/n8n/e-mail delivery are cloud features).

These caps are part of the compiled build; they are what makes the trial free to use for
evaluation. Removing or circumventing them is not permitted (see [LICENSE.md](LICENSE.md)).

---

## Configuration

Everything is driven by `.env` (copied from [`.env.sample`](.env.sample)). The sample
ships working defaults for a local trial; the values most people change:

| Variable                 | Default        | What it does                                        |
|--------------------------|----------------|-----------------------------------------------------|
| `GRID_HTTP_PORT`         | `8080`         | Port the web app is served on.                      |
| `MYSQL_ROOT_PASSWORD`    | `grid-eval`    | Local database root password.                       |
| `GRID_AI_PLATFORM_*`     | *(empty)*      | Your own LLM provider/key for the full AI assistant.|
| `GRID_AI_LOCAL_FALLBACK` | `true`         | Use the bundled local model when no key is set.     |

---

## Troubleshooting

- **Port already in use** — change `GRID_HTTP_PORT` in `.env` and `docker compose up -d`
  again.
- **Database not ready / backend restarts a few times on first boot** — normal: the
  backend waits for the database to finish seeding, then starts. Follow
  `docker compose logs -f grid`.
- **Apple Silicon** — supported natively; no Rosetta needed.
- **Reset everything** — `docker compose down -v` removes the database volume and the next
  `up` reseeds from scratch.

---

## Manuals

Step-by-step guides (Portuguese) are in [`docs/`](docs/):

- [Trial guide](docs/guia-avaliacao.md) — start here: what the evaluation limits, the first day step by step, and how to leave it.
- [User manual](docs/manual-usuario.md) — day-to-day use: cases, tasks, documents, search.
- [Administrator manual](docs/manual-administrador.md) — users, access, tenant settings.
- [Builder manual](docs/manual-construtor.md) — spreadsheet import and the dictionary editor.

---

## Going beyond the trial

The trial shows the product; it is not the product. The licensed GRID service adds the
multi-tenant cloud, unlimited (metered) cases, team and ownership scopes, document storage
tiers, integrations, the full AI tier, and support — hosted and kept current for you.

- **Product & licensing:** https://grid.ia.br
- **Contact:** see the site.

---

## License

Use of this evaluation build is governed by **[LICENSE.md](LICENSE.md)** — a proprietary
evaluation license. In short: you may run and evaluate GRID locally for free within the
built-in limits; you may not modify, redistribute, reverse-engineer, or circumvent the
build's protections or limits. All rights reserved.

© 2026 Ricardo Voyceik (VOYCEIK.NET).
