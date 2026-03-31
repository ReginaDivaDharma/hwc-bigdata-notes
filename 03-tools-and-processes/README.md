# 🔧 Big Data Tools & Processes

> Now that we know where data lives, let's talk about what happens to it. This section walks through the full data journey — from the moment data is collected to the moment it becomes a dashboard or an AI model.

---

## The Big Data Journey
```
📥 Ingest  →  🗄️ Store  →  🧹 Clean  →  🔍 Analyse  →  📊 Visualize
```

Each step has its own tools, patterns, and gotchas. Click into any section below to dive deeper.

---

## Sections

| Step | Topic | Projects |
|---|---|---|
| 1 | [📥 Data Ingestion](./01-ingestion/README.md) — Batch, Streaming, Hybrid | ✅ [Batch Project](./01-ingestion/batch-project/) |
| 2 | 🗄️ Data Storage — Lakes, Warehouses, Lakehouses | ✅ [Storage Project](./02-storage-project/) |
| 3 | [🧹 Data Cleaning](./03-cleaning/README.md) — Dedup, nulls, standardization | 🚧 Coming soon |
| 4 | [🔍 Data Analysis](./04-analysis/README.md) — SQL, Spark, ML workloads | 🚧 Coming soon |
| 5 | [📊 Data Visualization](./05-visualization/README.md) — Dashboards, BI, AI | 🚧 Coming soon |

---

## ETL vs ELT — Which Order Do You Follow?

The big data process doesn't always follow a strict linear order. Sometimes data is processed first and stored after, depending on business needs. This is where **ETL** and **ELT** come in.

| | ETL | ELT |
|---|---|---|
| **Full name** | Extract → Transform → Load | Extract → Load → Transform |
| **When to use** | When data quality must be enforced before storage | When storage is cheap and you want flexibility |
| **Best for** | Real-time, IoT, strict compliance | Cloud analytics, data lakes, exploration |
| **Example tools** | Apache NiFi, Informatica, Talend | Spark, BigQuery, Databricks |

**Real-world example:**
- An **IoT company** would likely use **ETL** — extract sensor data, filter and clean it immediately, then load only the good data into their platform.
- A **data analytics company** would likely use **ELT** — dump everything raw into a data lake first, then transform only what's needed for a specific report or model later.

---

⬅️ [Back to Storage](../02-storage.md) | Start with [📥 Data Ingestion](./01-ingestion/README.md) ➡️
