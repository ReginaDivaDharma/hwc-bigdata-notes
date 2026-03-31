# 🐘 Big Data — A Beginner's Guide

Hey there! 👋 Welcome to this repo. Whether you're just starting out or trying to wrap your head around big data concepts, this guide is for you.

This isn't just theory — each section comes with **real projects** so you can see how everything works in practice. Think of it as a mix between a textbook and a hands-on workshop.

---

## 🗺️ What's Inside

| # | Topic | What You'll Learn | Project |
|---|---|---|---|
| 1 | [📖 Big Data Fundamentals](./01-fundamentals.md) | What is big data, the 5 Vs, Medallion Architecture | — |
| 2 | [🗄️ Big Data Storage](./02-storage.md) | Data Lakes, Warehouses, Lakehouses + vendor list | ✅ [Storage Project](./03-tools-and-processes/02-storage-project/) |
| 3 | [🔧 Tools & Processes](./03-tools-and-processes/README.md) | Ingestion, Cleaning, Analysis, Visualization | 👇 See below |

### 🔧 Tools & Processes Breakdown

| # | Step | What Happens Here | Project |
|---|---|---|---|
| 3.1 | [📥 Data Ingestion](./03-tools-and-processes/01-ingestion/README.md) | Collecting and loading data (batch, streaming, hybrid) | ✅ [Batch Ingestion Project](./03-tools-and-processes/01-ingestion/batch-project/) |
| 3.2 | [🧹 Data Cleaning](./03-tools-and-processes/03-cleaning/README.md) | Removing nulls, duplicates, standardizing formats | 🚧 Coming soon |
| 3.3 | [🔍 Data Analysis](./03-tools-and-processes/04-analysis/README.md) | Running queries and extracting insights | 🚧 Coming soon |
| 3.4 | [📊 Data Visualization](./03-tools-and-processes/05-visualization/README.md) | Dashboards, reports, and AI-ready datasets | 🚧 Coming soon |

---

## 🧭 How to Use This Repo

1. **New to big data?** Start with [📖 Fundamentals](./01-fundamentals.md) — it covers all the core concepts you need before diving in.
2. **Understand the storage landscape** in [🗄️ Big Data Storage](./02-storage.md) — lakes, warehouses, lakehouses, and when to use each.
3. **Follow the data journey** step by step in [🔧 Tools & Processes](./03-tools-and-processes/README.md) — from ingestion all the way to visualization.
4. **Try the projects** — each ✅ section has a real working project you can run and explore yourself.

---

## 🛠️ Tech Stack Used in Projects

| Tool | Purpose |
|---|---|
| Apache Kafka | Streaming ingestion |
| Apache Spark | Batch processing and cleaning |
| Huawei Cloud (OBS, DWS, DMS, SMS) | Cloud storage and ingestion |
| Python (Pandas, Dask) | Data cleaning and analysis |
| Power BI / Grafana | Visualization |

---

> 💡 **Note:** This guide is structured around Huawei Cloud but most concepts and tools are vendor-agnostic. You'll find alternatives for AWS, Azure, and GCP throughout.
