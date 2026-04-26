# Kyle Rauch

**Technical Operations Specialist (4+ years SaaS support) building AI-collaborative products in my own time.** Based in Cincinnati, OH. Comfortable with the "I'll direct AI to build the thing, then explain what we built and why" loop.

> **Open to roles** — Customer Success Manager, Implementation Specialist, Solutions Engineer, Technical Account Manager, AI Trainer / Evaluator, or AI Implementation Specialist at AI-forward SaaS companies. Cincinnati, hybrid, or remote. **Available immediately.** Reach me at [kyle.g.rauch@gmail.com](mailto:kyle.g.rauch@gmail.com).

---

## Featured projects

### [csm-account-pulse](https://github.com/kgr1115/csm-account-pulse) — CSM account-health dashboard with documented v1→v5 prompt iteration

Single-page Streamlit dashboard a CSM opens every Monday: per-account 0–100 health score (usage decay + ticket pressure + NPS) and a 3-bullet "what to focus on this week" briefing per account, every bullet citation-grounded to a specific fixture field. `DataSource` Protocol with `FixtureDataSource` as the only implementation — the README walks through the ~3–5 days of work to swap in Salesforce, plus a parallel `NotebookStore` Protocol for adding actioned-flags / notes. The interface boundary IS the architectural claim.

The portfolio piece is `evals/` — five prompt versions (v1→v5), seven result files, a methodology rubric (script-checked citation validity, schema validity, bullet count, renewal-prose accuracy + hand-graded specificity, action-orientation), and visible failure-mode-then-fix cycles: v3 closed a months/years hallucination, v4 closed a 500-day day-count hallucination ("564 days" vs actual 64) by precomputing `days_to_renewal` and requiring verbatim copy, v5 closed a citation-grammar gap that the v4 run itself surfaced. Every prompt bump ships with its eval result file in the same window.

31 tests defending specific failure modes. CI green.

### [support-triage-public](https://github.com/kgr1115/support-triage-public) — Local-first AI triage workstation for B2B SaaS support

Classify (priority / category / sentiment via Anthropic tool use, prompt-cached Haiku) → embed and retrieve top-k KB (sentence-transformers MiniLM-L6-v2 + FAISS flat-IP) → draft a citation-grounded reply (Sonnet 4.6, strict no-speculation prompt with `[KB-…]` inline citations) → suggest top-3 macros from a separate macro index. FastAPI `POST /triage` with classifier and drafter running in parallel via `asyncio.gather`. React + TypeScript workstation.

The differentiator is the clean-room ragas faithfulness scorer in `app/faithfulness.py` — decomposes each draft into atomic claims and judges each one against ticket + KB, distinguishing "paraphrasing the customer's report" from "KB-grounded product fact" so customer-acknowledgment claims aren't penalized. Strict-vs-permissive baseline shows the strict prompt buys **+27.9pp faithfulness** isolated from model and retrieval.

Honest baselines on 200 labeled synthetic tickets / 26 KB / 19 macros: category 95.0% (vs 20% random), priority 62.0% strict / **100% within-1-tier** (vs 40.5% modal), recall@3 95.8%, faithfulness 97.1%. Worst-offender analysis classifies drafter failure modes ("defining KB terms," "predicting workaround outcomes") with proposed prompt mitigations. 30 tests; CI green.

### [SiftRobust](https://github.com/kgr1115/SiftRobust) — Local-first AI inbox triage

React + FastAPI UI, multi-provider LLM layer (Anthropic · OpenAI · Google · Groq), and a safety-gated bulk-action engine that can actually touch Gmail — not just summarize it. Eval harness scoring four providers on the same 40-fixture set: 97.5% top accuracy on Groq Llama 3.3 70B at ~10x lower cost per thread than Sonnet. Three safety gates in code: dry-run by default, confidence floor, safe-category whitelist.

The interesting design problem isn't "summarize email" — it's "how do you let AI safely touch production data?" ~4,400 lines Python + ~2,400 lines TypeScript.

---

## Other portfolio work

- **[mlb-market-models](https://github.com/kgr1115/mlb-market-models)** — walk-forward backtest framework over MLB prediction markets. 14,531 gated picks · honest +/− ROI per market (Totals +1.43%, Moneyline −1.37%, Run Line −1.86% — losers published, not buried). Bayesian shrinkage, isotonic calibration (40-bin PAVA), fractional-Kelly sizing with correlated-leg deduplication. Research framework, not a product.
- **[diamond-edge](https://github.com/kgr1115/diamond-edge)** — MLB pick recommendation system · [live at diamond-edge.co](https://www.diamond-edge.co). Gradient-boosted models on real Statcast + odds data, an LLM rationale layer grounded on SHAP attributions, isotonic-calibrated probability output (ECE 0.065 → 0.0004 on run line). Refuse-to-promote retrain pipeline with variance-collapse and passthrough-trap guardrails caught a real bug.
- **[understudy](https://github.com/kgr1115/understudy)** — multi-agent job-search orchestrator. Orchestrator + Scout/Tailor/Researcher subagents fanning out in parallel, a file-based contract that lets two completely different runtimes (Claude Code slash commands / Python over the Anthropic SDK) drive the same local dashboard, and a folder-watcher auto-ingesting browser-dropped approval manifests in 2-4s. Built for my own job search — the repo doubles as the demonstration.
- **[project-generator](https://github.com/kgr1115/project-generator)** — bootstrap-and-brief tool for Claude Code projects. Deep interview scaffolds new repos (single or paired private/public) and writes a tailored `CLAUDE.md`. Successor to [ai-pipeline-scaffold](https://github.com/kgr1115/ai-pipeline-scaffold) (archived).
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
