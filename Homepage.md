# 📦 Big Data Fundamentals
> A beginner-friendly guide to understanding big data concepts and Huawei's big data ecosystem.

---

## 📖 Table of Contents

- [What is Big Data?](#what-is-big-data)
- [The 5 Vs of Big Data](#the-5-vs-of-big-data)
- [The Medallion Architecture](#the-medallion-architecture)
  - [🥉 Bronze Layer](#-bronze-layer)
  - [🥈 Silver Layer](#-silver-layer)
  - [🥇 Golden Layer](#-golden-layer)
- [Common Big Data Architecture Terms](#common-big-data-architecture-terms)

---

## What is Big Data?

At its core, **big data** is exactly what its name implies — a collection of enormous amounts of data in one space.

When your data grows to a massive scale, traditional databases start to struggle. You might find yourself asking:

- *How do I maximize performance at this scale?*
- *How do I process this data fast enough?*

That's where **big data tools** come in. Instead of relying on conventional databases, these tools are built to handle large volumes of data with great speed and efficiency.

---

## The 5 Vs of Big Data

Not sure if your data qualifies as "big data"? A good rule of thumb is to evaluate it against the **5 Vs** — the key characteristics that define big data:

| # | Characteristic | Description |
|---|---------------|-------------|
| 1 | **Volume** | The sheer size of the data — typically ranging from **terabytes to petabytes**, far exceeding what traditional storage systems are built for. |
| 2 | **Velocity** | The speed at which data is generated, received, and needs to be processed — including **real-time** streaming scenarios. |
| 3 | **Variety** | The diversity of data formats: **structured** (databases), **semi-structured** (JSON, XML), and **unstructured** (images, videos, audio). |
| 4 | **Veracity** | The **accuracy, quality, and trustworthiness** of the data — how reliable is it? |
| 5 | **Value** | The **business benefit** you extract from the data — whether that's generating insights, cleaning data for AI training, or powering dashboards. |

> 💡 **Tip:** Whether your data qualifies as "big data" ultimately depends on your company's specific needs. Use the 5 Vs as a guide, not a strict rulebook.

---

## The Medallion Architecture

Big data solutions are commonly organized into **three layers**, known as the **Medallion Architecture**. Each layer serves a distinct purpose in the journey from raw data to business value.
```
Raw Data In
    │
    ▼
┌─────────────────────────────────────────────────────────┐
│  🥉  BRONZE LAYER  — Raw / Unprocessed Storage          │
│       (Cheap bucket storage: JSON, CSV, logs, etc.)     │
└────────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────┐
│  🥈  SILVER LAYER  — Cleaned & Structured Data          │
│       (ETL/ELT: filter, validate, fix nulls)            │
└────────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────┐
│  🥇  GOLDEN LAYER  — Business-Ready Data                │
│       (Dashboards, reports, stakeholder-facing)         │
└─────────────────────────────────────────────────────────┘
                         │
                         ▼
               Insights / AI / Reports
```

---

### 🥉 Bronze Layer

**The "dirty data" zone** — this is where your raw data lands first.

- Data arrives in its **original, unprocessed form**
- Multiple formats are accepted: CSV, JSON, Parquet, logs, etc.
- Stored in **low-cost bucket storage** (e.g., object storage services)
- **No transformation is done here** — the goal is simply to capture everything

> Think of it as an inbox that accepts everything without judgment.

---

### 🥈 Silver Layer

**The processing zone** — this is where data gets cleaned and structured.

- **Validates** data quality and consistency
- **Cleans** data: removes duplicates, fixes null values, standardizes formats
- **Transforms** data using **ETL** (Extract, Transform, Load) or **ELT** (Extract, Load, Transform) pipelines
- Outputs organized, reliable datasets ready for analysis

> Think of it as the editorial desk — raw content gets reviewed, corrected, and structured.

---

### 🥇 Golden Layer *(Single Source of Truth)*

**The presentation zone** — your cleanest, most reliable data lives here.

- Contains **fully processed, business-ready data**
- Used to power **dashboards, reports, and stakeholder presentations**
- Serves as the **single source of truth** for your organization
- Data at this layer is summarized, curated, and ready to tell a story

> Think of it as the published report — polished, accurate, and ready to share.

---

## Big Data Storage

Beyond the Medallion Architecture, there are several other terms and concepts you'll commonly encounter in big data systems, especially around data storage itself. According to IBM, big data storage can be divided into three main types.

---

### 1. Data Lakes

A data lake is a low-cost storage environment designed to handle massive amounts of raw structured or unstructured data. You don't need to clean the data yet, so it is still in its native format. This is ideal where volume, variety, and velocity are high, and performance or quality is not a priority yet. Data lakes prioritize flexibility and low cost, making them ideal for storing vast amounts of raw data.

Data lakes are commonly used to support AI training, machine learning, and big data analytics. They can also serve as general-purpose spaces for all big data, which can be moved from the lake to different applications as needed.

**Cloud Examples:**

| Vendor | Product / Service | Deployment |
|---|---|---|
| AWS | Amazon S3 | Cloud |
| Microsoft Azure | Azure Data Lake Storage (ADLS) | Cloud |
| Google Cloud | Cloud Storage | Cloud |
| Huawei Cloud | Object Storage Service (OBS) | Cloud / Server |
| Oracle | Oracle Object Storage | Cloud |
| MinIO | MinIO | On-Premise / Self-Hosted |
| Apache | Apache Hadoop HDFS | On-Premise / Self-Hosted |
| Dell | Dell ECS (Elastic Cloud Storage) | On-Premise / Hybrid |
| IBM | IBM Cloud Object Storage | Cloud / On-Premise |
| Alibaba Cloud | Alibaba OSS (Object Storage Service) | Cloud |

---

### 2. Data Warehouses

Data warehouses are built to support data analytics, business intelligence (BI), and data science efforts. They aggregate data from many sources into a central hub. Because warehouses enforce a strict schema, storage costs can be high. Rather than being a general-purpose big data storage solution, warehouses are mainly used to make a specific subset of big data readily available to business users for BI and data analysis. Data warehouses focus on structure and speed, providing highly efficient querying for formal reporting.

**Cloud Examples:**

| Vendor | Product / Service | Deployment |
|---|---|---|
| AWS | Amazon Redshift | Cloud |
| Google Cloud | BigQuery | Cloud |
| Microsoft Azure | Azure Synapse Analytics | Cloud |
| Huawei Cloud | Data Warehouse Service (DWS) | Cloud / Server |
| Snowflake | Snowflake Data Warehouse | Cloud / SaaS |
| Oracle | Oracle Exadata / Autonomous Data Warehouse | On-Premise / Cloud |
| Greenplum | Greenplum Database | On-Premise / Hybrid |
| IBM | IBM Db2 Warehouse | On-Premise / Cloud |
| Teradata | Teradata Vantage | On-Premise / Cloud |
| SAP | SAP BW/4HANA | On-Premise / Cloud |
| Vertica | Vertica Analytics Platform | On-Premise / Cloud |
| ClickHouse | ClickHouse | On-Premise / Cloud / SaaS |
| Alibaba Cloud | AnalyticDB | Cloud |


> **Bonus — Data Marts:** A data mart is essentially a smaller version of a data warehouse. It stores cleaned, structured data but serves only one specific department (e.g., Marketing or Finance), whereas a data warehouse can serve the entire company or multiple departments simultaneously.

---

### 3. Data Lakehouses

A data lakehouse is an emerging hybrid solution that combines the best of both data lakes and data warehouses — the cheap storage of a lake with the powerful querying capability of a warehouse — into a single platform, reducing system fragmentation. Lakehouses are a relatively recent development but are becoming increasingly popular because they eliminate the need to maintain two separate data systems.

**Cloud Examples:**

| Vendor | Product / Service | Deployment |
|---|---|---|
| Databricks | Databricks Lakehouse Platform | Cloud / SaaS |
| AWS | AWS Lake Formation | Cloud |
| Huawei Cloud | DataArts FabricSQL | Cloud |
| Google Cloud | BigLake | Cloud |
| Microsoft Azure | Microsoft Fabric | Cloud / SaaS |
| Cloudera | Cloudera Data Platform (CDP) | On-Premise / Hybrid |
| Snowflake | Snowflake (with Iceberg Tables) | Cloud / SaaS |
| Apache | Apache Iceberg + Spark | On-Premise / Self-Hosted |
| Apache | Apache Hudi | On-Premise / Self-Hosted |
| Delta Lake (Linux Foundation) | Delta Lake | On-Premise / Self-Hosted |
| IBM | IBM watsonx.data | Cloud / On-Premise |
| Starburst | Starburst Galaxy | Cloud / SaaS |
| Dremio | Dremio Lakehouse Platform | On-Premise / Cloud ||
