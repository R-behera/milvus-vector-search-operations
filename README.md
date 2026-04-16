# Radiology Report Search Hub

![Demo Screenshot](demo/screenshot.png)

## Overview

Search prior reports, imaging findings, and clinical notes to speed radiology review and case comparison workflows.

## Real-world problem

- User: Radiologists and imaging operations teams
- Problem: Radiologists need fast access to similar prior findings and historical wording without manually scanning large archives.
- Decision improved: Surface relevant prior reports and similar findings during case review.
- KPI target: Reduce review time and improve report consistency.

## Why this matters

This repo is positioned as a real product for a real team, not a framework-only demo. The goal is to show how research-backed AI, analytics, or graph systems become deployable workflows with docs, UI, screenshots, and business-facing outputs.

## Project profile

- Domain: Clinical Knowledge Search
- Project type: `rag`
- Tags: radiology, search, retrieval, healthcare

## Workflow

1. Ingest the operational context for the user and case.
2. Score risk, quality, or opportunity using the project API.
3. Compare current signals against a business baseline.
4. Generate a recommendation or operator brief for the next step.

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python scripts/bootstrap_data.py
uvicorn src.app.main:app --host 0.0.0.0 --port 8000 --reload
```

Open `http://localhost:8000/` to use the interactive application.

## Key endpoints

- `GET /`
- `GET /health`
- `GET /bootstrap`
- `GET /project`
- `POST /score`
- `POST /analyze`
- `POST /query`
- `POST /recommend`

## Documentation

- [Architecture](docs/architecture.md)
- [Evaluation](docs/evaluation.md)
- [Runbook](docs/runbook.md)
- [Innovation memo](research/innovation_memo.md)
- [Upstream audit](research/upstream_audit.md)
