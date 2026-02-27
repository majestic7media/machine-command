# THE MACHINE™ COMMAND — System Status

## Configuration

- **Event Handler:** localhost:3002 (thepopebot 1.2.72-beta.11)
- **LLM Provider:** NVIDIA NIM (openai-compatible)
- **LLM Model:** deepseek-ai/deepseek-r1
- **GitHub Repo:** majestic7media/machine-command
- **Pi Runner:** ubuntu-latest (GitHub-hosted)
- **Auto-Merge:** enabled
- **Allowed Paths:** logs, config, app, components, .pi, .github

## Active Crons

- `ping` — every 5 min — heartbeat command
- `daily-brief` — 8am daily — Pi job: morning status summary
- `memory-consolidation` — 10pm daily — Pi job: end-of-day log review
- `workspace-health` — every 4 hours — repo health command

## Dashboards

- http://localhost:3000 — Vanilla dashboard (ttt-dashboard)
- http://localhost:3001 — JARVIS Next.js
- http://localhost:3002 — THE MACHINE COMMAND (this)
- http://localhost:18789 — OpenClaw gateway UI

## THE MACHINE Context

- **Workspace:** B:\TTT_MACHINE\ (on Ty's local Windows machine — NOT accessible to Pi)
- **Podcast:** Truth Through Tribulation (TTT) — Ty + Addie's story
- **Addie Grace** — Ty's daughter, central to everything
- **OpenClaw** — AI gateway running in Docker (model squad: NVIDIA + OpenRouter)

## Notes for Pi

Pi runs in GitHub Actions (ubuntu-latest) — it cannot access B:\TTT_MACHINE directly.
Pi's working directory is the machine-command GitHub repo at /job.
All Pi deliverables go in logs/{JOB_ID}/ and get auto-merged via PR.
