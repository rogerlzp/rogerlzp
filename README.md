# Roger Li

**Data & AI Engineer** — data platforms, dbt transformations, and MCP servers for LLM agents.

Currently building production data infrastructure in quant research: **900M+ factor rows across 120+ factors**, multi-source API ingestion with idempotent loading, and automated freshness/coverage gates that **alert on gaps instead of failing silently**.

📍 Shanghai, China (UTC+8) · Open to Remote — worldwide / APAC / Europe
⏱ Can cover **4–6 hours with US Eastern (ET) core hours** (≈ 21:00–01:00 Beijing); flexible to EU core hours. No relocation or visa sponsorship required.

---

## What I build

**Data platforms** — 15 source systems (~1TB) → ClickHouse OLAP (**-50% query time**), 300+ reports/APIs, end-to-end lineage and reconciliation rules, ownership of the metric layer for four downstream teams.

**Transformation layers** — dbt models (staging → intermediate → mart), semantic metrics with explicit weights, data-quality tests as first-class models rather than spreadsheets.

**Agent access layers** — read-only MCP servers exposing a data mart to LLM agents, with permission boundaries, tool descriptions written for model consumption, and data quality exposed as a callable tool.

**AI-assisted data engineering** — LLM agent workflows (Claude / GPT APIs + tool calling) that draft, refactor and **verify** pipeline code against a change log and validation checklist. This is the same discipline as an agent evaluation harness: the agent's output is checked, not trusted.

**RAG** — 200k+ policy documents, vector retrieval, 1,000+ active users.

**Quant research** — LightGBM cross-sectional ranking with **walk-forward splits and look-ahead bias checks**; event-driven backtester with realistic cost and fill assumptions.

**Legacy at scale** — Oracle JDBC / ODI on Hadoop, Oracle RAC 12c; worked directly with US engineering teams on throughput and latency.

---

## Stack

**Data** SQL · PostgreSQL (incl. Supabase) · MySQL · Oracle (8 yrs) · ClickHouse · DuckDB · dimensional modeling · ETL/ELT · idempotent loading · data-quality gates · source-to-report lineage · semantic/metric layers

**AI & Agents** LLM APIs (OpenAI, Claude) · RAG · vector retrieval · tool-calling / agent workflows · MCP · agent harness design (permissions, guardrails, human-in-the-loop, retries, validation) · LLM evaluation · LightGBM

**Engineering** Python (FastAPI, pandas) · REST APIs · webhooks · Kafka · Airflow · dbt · Docker · Kubernetes · GitLab CI/CD · Linux · Git

**Apps** FastAPI · React · Vue.js · Spring Boot · Python

English (professional — daily written and verbal work with US-based teams) · Chinese (native)

---

## Selected work

Together these trace one architecture: **compute (pandas) → transform (dbt) → serve to agents (MCP)** — the shape of a modern data platform, with each layer built by hand.

| Repo | What it shows |
|---|---|
| **[`panda_factor`](https://github.com/rogerlzp/panda_factor)** | The full quant factor platform: 103 operators, factor authoring engine, analysis workflow, web UI, data hub, LLM service. ~5 years of built-in market data, nightly ingestion from Tushare / RiceQuant / Xuntou / Tqsdk. |
| **[`panda_factor_core`](https://github.com/rogerlzp/panda_factor_core)** | The factor engine extracted as a dependency-light library — `operators.py`, the `Factor` ABC, and a `backtest/` module. 12 contract tests. |
| **[`dbt_quant_demo`](https://github.com/rogerlzp/dbt_quant_demo)** | A dbt project on DuckDB: staging → intermediate → mart, semantic metrics, and data-quality as first-class models. 32/32 tests pass. |
| **[`mcp_quant_server`](https://github.com/rogerlzp/mcp_quant_server)** | A read-only MCP server over the mart dbt builds — permission boundary, tool descriptions written for the model, and data quality as a callable tool. 12 contract tests + an end-to-end MCP test. |

---

## How I work

- **Async-first, written-obsessed** — design docs, PR descriptions, runbook-style handover
- **Deliver working, tested increments** — README, tests, and commit notes included
- **Data quality is a deliverable** — gaps should *alert*, never fail silently; a join that drops rows is a bug that must fail a test
- **I verify my own outputs** — look-ahead bias checks, coverage gates, reconciliation rules, and a test that asserts the scored row count matches the symbol count
- **Explain the design decisions** — not just what the code does, but why the boundaries are where they are

---

## Contact

- ✉️ rogerlzp@gmail.com · +86 158-0091-1536
- 🔗 [linkedin.com/in/zhengping-li-89507315](https://linkedin.com/in/zhengping-li-89507315)
