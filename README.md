# Roger Li

**Data & AI Engineer** — data platforms, dbt transformations, MCP servers for LLM agents, and laboratory-automation software.

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

**Laboratory automation** — a control kernel for automated bio-pharma labs: BPMN workflow execution, parallel experiment scheduling, position-level plate occupancy with atomic reservation, device contracts, and a crash-recovery path built on idempotency keys.

**Legacy at scale** — Oracle JDBC / ODI on Hadoop, Oracle RAC 12c; worked directly with US engineering teams on throughput and latency.

---

## Stack

**Data** SQL · PostgreSQL (incl. Supabase) · MySQL · Oracle (8 yrs) · ClickHouse · DuckDB · dimensional modeling · ETL/ELT · idempotent loading · data-quality gates · source-to-report lineage · semantic/metric layers

**AI & Agents** LLM APIs (OpenAI, Claude) · RAG · vector retrieval · tool-calling / agent workflows · MCP · agent harness design (permissions, guardrails, human-in-the-loop, retries, validation) · LLM evaluation · LightGBM

**Engineering** Python (FastAPI, pandas) · REST APIs · webhooks · Kafka · Airflow · dbt · Docker · Kubernetes · GitLab CI/CD · Linux · Git

**Apps** FastAPI · React · Vue.js · Spring Boot · Python · Java 17 (JDK stdlib + PostgreSQL JDBC, no framework dependency) · BPMN · device drivers (TCP / serial)

English (professional — daily written and verbal work with US-based teams) · Chinese (native)

---

## Selected work

Together these trace one architecture: **compute (pandas) → transform (dbt) → serve to agents (MCP)** — the shape of a modern data platform, with each layer built by hand.

| Repo | What it shows |
|---|---|
| **[`dbt_quant_demo`](https://github.com/rogerlzp/dbt_quant_demo)** | A dbt project on DuckDB: staging → intermediate → mart, semantic metrics, and data-quality as first-class models. 32/32 tests pass. |
| **[`mcp_quant_server`](https://github.com/rogerlzp/mcp_quant_server)** | A read-only MCP server over the mart dbt builds — permission boundary, tool descriptions written for the model, and data quality as a callable tool. 12 contract tests + an end-to-end MCP test. |
| **[`labos`](https://github.com/rogerlzp/labos)** | An Apache-2.0 orchestration kernel for laboratory automation: BPMN workflow execution, parallel experiment scheduling, position-level plate occupancy, device contracts, plate-movement audit trail. SiLA 2 / OPC UA LADS on the roadmap. Pre-alpha. |

### Built on top of others' open source

These are **not my own projects** — they are upstream projects I contribute to, fork, or extract from. The distinction matters, so I keep it explicit.

| Upstream | My relationship |
|---|---|
| **[`PandaAI-Tech/panda_factor`](https://github.com/PandaAI-Tech/panda_factor)** (2.8k★, AGPL-3.0) | The factor platform itself is upstream's work. I contribute docs and cross-project standards to the fork [`rogerlzp/panda_factor`](https://github.com/rogerlzp/panda_factor), and run it as a dependency in my own research stack. |
| **[`PandaAI-Tech/panda_quantflow`](https://github.com/PandaAI-Tech/panda_quantflow)** (1k★) | The workflow framework I build on, in the same family of upstream projects. |

[`rogerlzp/panda_factor_core`](https://github.com/rogerlzp/panda_factor_core) is my **standalone extraction** of the upstream factor engine — a dependency-light library (`numpy` + `pandas` only) carrying the operator set, the `Factor` ABC, a strategy base layer and backtest metrics, with 12 contract tests. The upstream platform ships AGPL-3.0 and covers a much larger surface (web UI, MongoDB data hub, LLM service, deployment); this repo isolates the part that is useful on its own. **The extracted engine code is upstream's, under upstream's AGPL-3.0 licence** — my work here is the extraction, the packaging, the backtest/strategy layer and the contract tests.

---

## My own quant stack (private)

The quant strategy work itself is **not open source** — it runs against licensed and paid third-party data, and the strategy logic is the asset. What is open source above is the surrounding data engineering.

For scale, the system spans **5 repositories** (display / compute / data / factor / workflow) with **949 tables across two PostgreSQL databases**, a ClickHouse factor store of **3.28B rows**, MongoDB for factor cataloguing, and ~1.9 TiB on external storage holding research PDFs, exchange filings and primary-source documents.

The parts worth naming:

- **Data ingestion** — multi-source market and fundamental data on a daily schedule, loaded idempotently, with per-table freshness and coverage guards.
- **Financial data modelling** — point-in-time discipline on fundamentals and corporate actions, so a backtest cannot read a value that did not exist on the decision date.
- **Third-party and alternative data** — broker research PDFs, exchange disclosure filings and paid research feeds, ingested as searchable document corpora for retrieval over the original text rather than summaries.
- **Strategy research** — cross-sectional factor models, event-driven and intraday strategies, walk-forward validation, and realistic cost/fill modelling; results are recorded in a strategy ledger with the rules alongside the numbers.

---

## How I work

- **Async-first, written-obsessed** — design docs, PR descriptions, runbook-style handover
- **Deliver working, tested increments** — README, tests, and commit notes included
- **Data quality is a deliverable** — gaps should *alert*, never fail silently; a join that drops rows is a bug that must fail a test
- **I verify my own outputs** — look-ahead bias checks, coverage gates, reconciliation rules, and a test that asserts the scored row count matches the symbol count
- **Explain the design decisions** — not just what the code does, but why the boundaries are where they are
- **Credit stays accurate** — when a repo is a fork or an extraction of someone else's project, the README says so

---

## Contact

- ✉️ rogerlzp@gmail.com · +86 158-0091-1536
- 🔗 [linkedin.com/in/zhengping-li-89507315](https://linkedin.com/in/zhengping-li-89507315)
