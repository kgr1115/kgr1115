Kyle Rauch

Technical Operations Specialist (4+ years SaaS support) building AI-collaborative products in my own time. Based in Cincinnati, OH. Comfortable with the "I'll direct AI to build the thing, then explain what we built and why" loop.

Open to roles — Solutions Engineer, Technical Account Manager, Implementation Consultant, or Customer Success Engineer at AI-forward SaaS companies. Cincinnati, hybrid, or remote. Available immediately. Reach me at kyle.g.rauch@gmail.com.

Featured projects
SiftRobust — Local-first AI inbox triage
React + FastAPI UI, multi-provider LLM layer (Anthropic · OpenAI · Google · Groq), and a safety-gated bulk-action engine that can actually touch Gmail — not just summarize it. Built in ~2 weeks. Runs against a 40-thread synthetic fixture inbox out of the box, so you can see the pipeline end-to-end without OAuth setup.
Includes an eval harness scoring four providers on the same 40-fixture set (97.5% top accuracy on Groq Llama 3.3 70B). The interesting design problem isn't "summarize email" — it's "how do you let AI safely touch production data?" Three gates in code: dry-run by default, confidence floor, safe-category whitelist.
~4,400 lines Python + ~2,400 lines TypeScript.

mlb-market-models — Walk-forward backtest framework
14,531 gated picks across 2018–2026 with a proper 2018–22 train / 2023–25 test split. Totals model cleared the gate at +1.43% ROI / 53.3% win rate across 4,842 picks; honest negative findings published on the two markets that didn't clear (Moneyline −1.37%, Run Line −1.86%).
Bayesian shrinkage for small-sample pitchers, isotonic regression calibration (40-bin PAVA), and fractional-Kelly sizing with correlated-leg deduplication. Not a shipped product — a research framework I run on my own. The repo doubles as a record of the process: what worked, what didn't, and why.

How I work
Both featured projects are AI-collaborative. I specified the architecture, chose the models and features, set the evaluation methodology, and reviewed every line — Claude wrote the implementation. This is the explicit point of the work, not a footnote.
The hot skill in 2026 isn't "I can hand-implement isotonic calibration" — a senior ML engineer will out-code me. It's "I can productively direct AI to build complex systems, validate them with real numbers, and ship the result." Both READMEs are honest about what that collaboration looks like.

Background

Clubessential — Level 2 Website Support Specialist · Oct 2021 – Jan 2026 · SaaS support across websites, reservation systems, CRM, and mobile apps. Salesforce ticketing. Level 2 escalation point; collaborated with dev on root cause; client training.
Fidelity Investments — Customer Relationship Advocate · Apr 2019 – Sep 2020 · Earned FINRA Series 7 & 63 (expired).
Total Quality Logistics — Logistics Account Executive · Oct 2017 – Mar 2019 · 75+ outbound calls/day, sales targets.
Western Governors University — BS IT, currently enrolled.
Active certs: CompTIA Security+ · ITIL 4 Foundations.


Tech I work in
Python · FastAPI · Pydantic · React · TypeScript · Tailwind · SQLite · Salesforce · HTML / CSS · Anthropic · OpenAI · Google Gemini · Groq · pytest

Contact
kyle.g.rauch@gmail.com · LinkedIn · 513-609-7268 · Batavia, OH 45103
