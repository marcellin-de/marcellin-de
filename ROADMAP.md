# 🗺️ Data Engineering Roadmap

My learning and project roadmap to grow as a **Data Engineer / Analytics Engineer / AI Engineer**.

This roadmap builds on my existing foundations (Snowflake, dbt, Dagster, DLT, Power BI, MLflow) and targets the gaps that make the difference between *junior* and *senior* profiles.

> Legend: ✅ Built · 🚧 In progress · ⬜ Planned

---

## 📊 Current State — What I've Already Built

| Project | Stack | Demonstrates |
|---------|-------|--------------|
| [CRM Sales Analytics Platform](https://github.com/marcellin-de/crm-sales-analytics-platform) | Snowflake, dbt, Power BI | Analytics Engineering, star schema, testing |
| [Dagster Weather Intelligence Platform](https://github.com/marcellin-de/dagster-weather-platform) | Dagster, dbt, DuckDB, MLflow | Data + ML in one asset graph, MLOps |
| [Marketing Performance Analysis](https://github.com/marcellin-de/marketing-performance-analysis) | DLT, dbt, Dagster, Metabase | Modern data stack, KPI engineering |
| [Vehicle E-Commerce Analytics](https://github.com/marcellin-de/vehicle-ecommerce-analytics) | Airbyte, dbt, Dagster, Elementary | Medallion architecture, observability |

**Strengths:** batch ELT, dbt modeling, orchestration, data quality, BI.
**Gaps:** streaming, infra-as-code, cloud warehousing at scale, ML systems, vector search.

---

## 🔌 Track 1 — Data Engineering (core)

### ⬜ Project 5 — Real-Time Streaming Pipeline
- **Goal:** Ingest, process, and serve streaming data with sub-minute latency.
- **Stack:** Apache Kafka (or Redpanda), Apache Flink (or Spark Structured Streaming), a serving layer (Redis / ClickHouse).
- **Dataset idea:** Real-time NYC taxi rides, or a synthetic clickstream / IoT event stream.
- **Skills demonstrated:** Event-driven architecture, windowing, exactly-once semantics, stream processing, late data handling.
- **Estimated effort:** 3–4 weeks.

### ⬜ Project 6 — Infrastructure as Code Data Platform
- **Goal:** Provision an entire cloud data platform from version-controlled code.
- **Stack:** Terraform (or Pulumi), AWS (S3, Glue, Athena, Redshift) or GCP (BigQuery, Cloud Storage, Dataflow), GitHub Actions.
- **Skills demonstrated:** IaC, cloud architecture, environment promotion (dev/staging/prod), cost governance.
- **Estimated effort:** 2–3 weeks.

### ⬜ Project 7 — Lakehouse with Open Table Formats
- **Goal:** Build a queryable lakehouse replacing a classic warehouse for petabyte-scale economics.
- **Stack:** Apache Iceberg (or Delta Lake), Spark, Trino/Athena, S3/GCS.
- **Skills demonstrated:** Time travel, schema evolution, partition evolution, ACID transactions on object storage.
- **Estimated effort:** 2–3 weeks.

---

## 🧮 Track 2 — Analytics Engineering (depth)

### ⬜ Project 8 — dbt Semantic Layer + Metrics Platform
- **Goal:** Define metrics once, query them everywhere with consistency.
- **Stack:** dbt Cloud + Semantic Layer, MetricFlow, a headless BI consumption layer.
- **Skills demonstrated:** Governed metrics, semantic modeling, metric versioning, multi-tool consistency.
- **Estimated effort:** 1–2 weeks.

### ⬜ Project 9 — Reverse ETL & Data Activation
- **Goal:** Push computed segments back into business tools (CRM, marketing).
- **Stack:** Hightouch (or Census), dbt marts, Snowflake, a downstream tool (HubSpot / Salesforce).
- **Skills demonstrated:** Data activation, audience sync, operational analytics.
- **Estimated effort:** 1–2 weeks.

---

## 🤖 Track 3 — AI Engineering (differentiation)

### ⬜ Project 10 — Production RAG Pipeline
- **Goal:** Answer questions over a private document corpus with cited, grounded answers.
- **Stack:** LangChain (or LlamaIndex), a vector DB (pgvector / Pinecone / Weaviate), an embedding model, an LLM, an evaluation harness (RAGAS / TruLens).
- **Dataset idea:** ArXiv papers, internal docs, or product documentation.
- **Skills demonstrated:** Chunking strategies, retrieval, reranking, evaluation, prompt engineering, guardrails.
- **Estimated effort:** 3–4 weeks.

### ⬜ Project 11 — Feature Store + Online/Offline Serving
- **Goal:** Serve consistent features for both training and inference.
- **Stack:** Feast (or Tecton), an offline store (S3/BigQuery), an online store (Redis/DynamoDB), a model.
- **Skills demonstrated:** Feature engineering, point-in-time correctness, training/serving skew prevention.
- **Estimated effort:** 2–3 weeks.

### ⬜ Project 12 — End-to-End MLOps
- **Goal:** Take a model from notebook to monitored production system.
- **Stack:** MLflow (tracking/registry, already used), Kubeflow or Vertex AI Pipelines, a model server (BentoML / KServe), monitoring (Evidently / Arize).
- **Skills demonstrated:** CI/CD for ML, model registry, drift detection, automated retraining.
- **Estimated effort:** 3–4 weeks.

---

## 🎯 Suggested Execution Order

Prioritize by **portfolio impact per unit of effort** and by filling your biggest gaps:

1. **Project 5 — Streaming** → fills the biggest visible gap (no real-time yet).
2. **Project 10 — RAG** → highest market demand, strong differentiator.
3. **Project 6 — IaC** → shows senior-level cloud maturity.
4. **Project 7 — Lakehouse** → rounds out the data engineering story.
5. **Project 12 — MLOps** → extends your existing MLflow foundation.
6. Projects 8, 9, 11 → depth and polish as time allows.

---

## 📚 Learning Resources

- **Data Engineering:** *Fundamentals of Data Engineering* ( Reis & Housley )
- **Analytics Engineering:** dbt Developer Hub (docs.getdbt.com), *The Analytics Engineering Cookbook*
- **Streaming:** Kafka: The Definitive Guide, Flink documentation
- **AI Engineering:** DeepLearning.AI short courses, LangChain/LlamaIndex docs
- **System Design:** *Designing Data-Intensive Applications* ( Kleppmann )

---

_Last updated: 2026-07-24_
