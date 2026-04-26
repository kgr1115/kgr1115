# Kyle Rauch

**Technical Operations Specialist (4+ years SaaS support) building AI-collaborative products in my own time.** Based in Cincinnati, OH. Comfortable with the "I'll direct AI to build the thing, then explain what we built and why" loop.

> **Open to roles** — Customer Success Manager, Implementation Specialist, Solutions Engineer, Technical Account Manager, AI Trainer / Evaluator, or AI Implementation Specialist at AI-forward SaaS companies. Cincinnati, hybrid, or remote. **Available immediately.** Reach me at [kyle.g.rauch@gmail.com](mailto:kyle.g.rauch@gmail.com).

---

## Featured projects

### [SiftRobust](https://github.com/kgr1115/SiftRobust) — Local-first AI inbox triage

React + FastAPI UI, multi-provider LLM layer (Anthropic · OpenAI · Google · Groq), and a safety-gated bulk-action engine that can actually touch Gmail — not just summarize it. Built in ~2 weeks. Runs against a 40-thread synthetic fixture inbox out of the box, so you can see the pipeline end-to-end without OAuth setup.

Includes an eval harness scoring four providers on the same 40-fixture set (97.5% top accuracy on Groq Llama 3.3 70B). The interesting design problem isn't "summarize email" — it's "how do you let AI safely touch production data?" Three gates in code: dry-run by default, confidence floor, safe-category whitelist.

~4,400 lines Python + ~2,400 lines TypeScript.

### [understudy](https://github.com/kgr1115/understudy) — Multi-agent job-search orchestrator

Orchestrator + Scout/Tailor/Researcher subagents fanning out in parallel, a file-based contract that lets two completely different runtimes (Claude Code slash commands / Python over the Anthropic SDK) drive the same local dashboard, and a folder-watcher that rides along in a separate terminal auto-ingesting browser-dropped approval manifests in 2-4s. Status-bucket auto-reconciler keeps the spreadsheet, the dashboard, and the on-disk PDFs in sync without manual moves.

The shape is the product: an idempotent ingester with a stamped dedupe key, a kanban with one-click ◀ Back / Next ▶ buttons that drop manifests into Downloads, and an LLM-driven onboarding that replaces a scripted wizard. I built this for myself while job-searching — the repo doubles as the demonstration.

### [diamond-edge](https://github.com/kgr1115/diamond-edge) — MLB pick recommendation system · [live at diamond-edge.co](https://www.diamond-edge.co)

Gradient-boosted models on real Statcast + odds data, an LLM rationale layer **grounded on SHAP attributions** (no free-form storytelling), and a calibrated probability output. ROI 22.97% on 2024 holdout for the promoted moneyline classifier. Architecture-keyword leakage ("LightGBM," "SHAP," "gradient boost") is scrubbed both in the prompt and post-response so end-users see clean rationale copy. Shipped as free + informational — no bets placed, no funds held.

Built around four invariants the load path enforces in code: snapshot-pinned line tracking (the line at pick-creation time, not the latest live alternate), an isotonic calibrator wrapping the raw model output (ECE 0.065 → 0.0004 on run line), a refuse-to-promote retrain pipeline (variance-collapse + passthrough-trap guardrails — caught a real bug), and a "this migration hasn't been applied yet" clean-degrade banner so the admin telemetry page never crashes. Stripe checkout scaffolding for the planned paid tiers is preserved at tag `v0.1-paid-tiers`.

---

## Other portfolio work

- **[ai-pipeline-scaffold](https://github.com/kgr1115/ai-pipeline-scaffold)** — researcher → architect → implementer → tester → publisher pipeline for Claude Code projects, with scope gates, binary-signal handoffs, and safety rails (personal-data guard, bounded retry loops, explicit model routing per agent). Includes a `/begin` bootstrap that spawns new projects as paired private/public repos.
- **[mlb-market-models](https://github.com/kgr1115/mlb-market-models)** — walk-forward backtest framework over MLB prediction markets. 14,531 gated picks · honest +/− ROI per market (Totals +1.43%, Moneyline −1.37%, Run Line −1.86% — losers published, not buried). Bayesian shrinkage, isotonic calibration (40-bin PAVA), fractional-Kelly sizing with correlated-leg deduplication. Research framework, not a product.
- **[agentic-job-pipeline](https://github.com/kgr1115/agentic-job-pipeline)** — predecessor to *understudy*. Same orchestrator/subagent shape; two branches over the same file-based state machine.

---

## How I work

All featured projects are **AI-collaborative**. I specified the architecture, chose the models and features, set the evaluation methodology, and reviewed every line — Claude wrote the implementation. This is the explicit point of the work, not a footnote.

The hot skill in 2026 isn't "I can hand-implement isotonic calibration" — a senior ML engineer will out-code me. It's "I can productively direct AI to build complex systems, validate them with real numbers, and ship the result." Every project README is honest about what that collaboration looks like.

---

## Background

- **Clubessential** — Level 2 Website Support Specialist · Oct 2021 – Jan 2026 · SaaS support across websites, reservation systems, CRM, and mobile apps. Salesforce ticketing. Level 2 escalation point; collaborated with dev on root cause; client training; mentored Level 1 reps and authored knowledge-base articles.
- **Fidelity Investments** — Customer Relationship Advocate · Apr 2019 – Sep 2020 · Earned FINRA Series 7 & 63 (expired).
- **Total Quality Logistics** — Logistics Account Executive · Oct 2017 – Mar 2019 · 75+ outbound calls/day, sales targets.
- **Western Governors University** — BS IT, currently enrolled.
- **Active certs:** CompTIA Security+ · ITIL 4 Foundations.

---

## Tech I work in

Python · FastAPI · Pydantic · React · TypeScript · Next.js · Tailwind · SQLite · Supabase · Salesforce · HTML / CSS · Anthropic · OpenAI · Google Gemini · Groq · LightGBM · SHAP · isotonic calibration · pytest · Stripe

---

## Contact

[kyle.g.rauch@gmail.com](mailto:kyle.g.rauch@gmail.com) · [LinkedIn](https://www.linkedin.com/in/kyle-rauch-b2984a75/) · 513-609-7268 · Batavia, OH 45103
