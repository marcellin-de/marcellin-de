# 🛠️ GitHub Portfolio Setup — Remaining Steps

> **Prerequisite:** Run `gh auth login` in your terminal first, then execute the commands below.
>
> These commands are **non-destructive** (descriptions, topics, visibility changes). The archive commands are clearly separated and marked as **destructive** — review before running.

---

## Phase 2 — Update Descriptions & Topics (Non-Destructive)

### 1. vehicle-ecommerce-analytics

Fix the leading space in description + add missing topics:

```bash
gh repo edit marcellin-de/vehicle-ecommerce-analytics \
  --description "Production-grade analytics platform for a vehicle e-commerce marketplace. Airbyte → Snowflake (medallion) → dbt → Dagster → Elementary + Great Expectations → Power BI." \
  --add-topic great-expectations,medallion-architecture,power-bi,clv,rfm-segmentation,retention-analysis
```

### 2. crm-sales-analytics-platform

Add missing topics (description is already excellent):

```bash
gh repo edit marcellin-de/crm-sales-analytics-platform \
  --add-topic incremental-models,snapshots,data-quality,star-schema,metric-validation
```

### 3. marketing-performance-analysis

Add missing topics (description is already excellent):

```bash
gh repo edit marcellin-de/marketing-performance-analysis \
  --add-topic kpi,metabase,incremental-models,elementary-data,kpi-dashboard
```

### 4. dagster-weather-platform

Add missing topics (description is already excellent):

```bash
gh repo edit marcellin-de/dagster-weather-platform \
  --add-topic duckdb,mlops,mlflow,forecasting,ai-enrichment,huggingface
```

### 5. marcellin-portfolio

Add a description (README was already added):

```bash
gh repo edit marcellin-de/marcellin-portfolio \
  --description "Personal portfolio website — React 19, Vite 7, Tailwind CSS 4, TypeScript. Showcasing data engineering & analytics projects."
```

### 6. coingecko-modern-data-platform

Make it public + add description and topics:

```bash
gh repo edit marcellin-de/coingecko-modern-data-platform --visibility public

gh repo edit marcellin-de/coingecko-modern-data-platform \
  --description "Asset-driven crypto data platform — Dagster, DLT, ClickHouse, dbt, Great Expectations, Hugging Face AI enrichment." \
  --add-topic crypto,data-platform,dagster,clickhouse,dbt,huggingface,ai,mlops
```

### 7. Active private repos — add descriptions

```bash
gh repo edit marcellin-de/xpress \
  --description "WIP project"

gh repo edit marcellin-de/xpress-agency \
  --description "WIP — Xpress Agency"
```

---

## Phase 3 — Pin Repos (Manual)

GitHub has no API for pinning. Do this manually:

1. Go to https://github.com/marcellin-de?tab=repositories
2. Click **Customize pins**
3. Pin these 6 repos in this order:

| # | Repo | Why |
|---|------|-----|
| 1 | `crm-sales-analytics-platform` | Most complete Analytics Engineering project |
| 2 | `dagster-weather-platform` | Only project with ML/MLOps — AI differentiator |
| 3 | `marketing-performance-analysis` | Modern data stack (DLT + dbt + Dagster) |
| 4 | `vehicle-ecommerce-analytics` | Medallion architecture + observability |
| 5 | `coingecko-modern-data-platform` | Crypto + AI/HuggingFace angle |
| 6 | `marcellin-portfolio` | Personal website (has README now) |

---

## Phase 6 — Archive Obsolete Repos (Destructive — Review First)

> **Archiving ≠ deleting.** All history is preserved and reversible via `gh repo unarchive`.
>
> Only run these AFTER you've confirmed the content is superseded.

### Doublons (older versions of repos you already have public & improved)

```bash
# CRM-Sales-Analytics (private) → superseded by crm-sales-analytics-platform (public)
gh repo archive marcellin-de/CRM-Sales-Analytics --yes

# marketing-performance-analytics-platform (private) → superseded by marketing-performance-analysis (public)
gh repo archive marcellin-de/marketing-performance-analytics-platform --yes
```

### Empty scaffolds

```bash
# marcel_lin — empty scaffold, no description
gh repo archive marcellin-de/marcel_lin --yes

# lumina-data-engineering — single scaffold commit, no description
gh repo archive marcellin-de/lumina-data-engineering --yes
```

### To unarchive if needed

```bash
gh repo unarchive marcellin-de/CRM-Sales-Analytics
```

---

## Quick Start — Run Everything at Once (Non-Destructive Only)

```bash
# Phase 2: All description & topic updates
gh repo edit marcellin-de/vehicle-ecommerce-analytics --description "Production-grade analytics platform for a vehicle e-commerce marketplace. Airbyte → Snowflake (medallion) → dbt → Dagster → Elementary + Great Expectations → Power BI." --add-topic great-expectations,medallion-architecture,power-bi,clv,rfm-segmentation,retention-analysis

gh repo edit marcellin-de/crm-sales-analytics-platform --add-topic incremental-models,snapshots,data-quality,star-schema,metric-validation

gh repo edit marcellin-de/marketing-performance-analysis --add-topic kpi,metabase,incremental-models,elementary-data,kpi-dashboard

gh repo edit marcellin-de/dagster-weather-platform --add-topic duckdb,mlops,mlflow,forecasting,ai-enrichment,huggingface

gh repo edit marcellin-de/marcellin-portfolio --description "Personal portfolio website — React 19, Vite 7, Tailwind CSS 4, TypeScript. Showcasing data engineering & analytics projects."

gh repo edit marcellin-de/coingecko-modern-data-platform --visibility public
gh repo edit marcellin-de/coingecko-modern-data-platform --description "Asset-driven crypto data platform — Dagster, DLT, ClickHouse, dbt, Great Expectations, Hugging Face AI enrichment." --add-topic crypto,data-platform,dagster,clickhouse,dbt,huggingface,ai,mlops

gh repo edit marcellin-de/xpress --description "WIP project"
gh repo edit marcellin-de/xpress-agency --description "WIP — Xpress Agency"
```
