# 📥 Data Ingestion

> The first step of the big data journey — collecting, importing, and loading data from various sources into your storage or processing system.

---

## Types of Ingestion

| Type | When to Use |
|---|---|
| [A. Batch](#a-batch-ingestion) | When you don't need instant insights — scheduled, high-volume loads |
| [B. Real-Time / Streaming](#b-real-time--streaming-ingestion) | When you need instant insights — continuous data flow |
| [C. Hybrid](#c-hybrid-ingestion) | When you need both depending on the data source |

---

## A. Batch Ingestion

Batch ingestion transfers data in scheduled intervals — every few hours, daily, or longer. Data is collected over a period of time and then ingested all at once on a fixed schedule.

This is ideal when you don't need instant insights and helps manage large volumes of data without overwhelming your system.

### Use Cases

| # | Use Case | Description |
|---|---|---|
| a | Reporting | Collecting data periodically to generate business insights and summaries |
| b | Data Backups | Moving historical records from operational databases into a warehouse nightly |
| c | Payroll Processing | Aggregating employee hours and transactions at the end of a pay period |
| d | ETL Pipelines | Loading large datasets from source systems into a warehouse on a schedule |

### Tools

| Tool | Vendor | Deployment |
|---|---|---|
| Apache Sqoop | Apache | On-Premise / Self-Hosted |
| Apache NiFi | Apache | On-Premise / Cloud |
| AWS Glue | AWS | Cloud |
| Azure Data Factory | Microsoft Azure | Cloud |
| Google Cloud Dataflow | Google Cloud | Cloud |
| Talend | Talend | On-Premise / Cloud / SaaS |
| Informatica PowerCenter | Informatica | On-Premise / Cloud |
| Huawei Cloud Migration Service (SMS) | Huawei Cloud | Cloud / Server |

> 💡 In Huawei Cloud engagements, we typically use **Cloud Migration Service (SMS)** for batch ingestion scenarios.

### ✅ Project — Batch Ingestion
> See how batch ingestion works in practice with a real working example.
> 👉 [View the Batch Ingestion Project](./batch-project/)

---

## B. Real-Time / Streaming Ingestion

Real-time ingestion continuously collects and processes data as it is generated — making instant insights possible. This is critical in time-sensitive scenarios where immediate decision-making is required.

### Use Cases

| # | Use Case | Description |
|---|---|---|
| a | Fraud Detection | Monitoring transactions in real time to identify suspicious activity |
| b | IoT Sensors | Processing data from devices like temperature or motion sensors in real time |
| c | Live Analytics | Powering dashboards that need minute-level metric updates |
| d | Real-Time Recommendations | Serving product or content suggestions based on live user behaviour |

### Tools

| Tool | Vendor | Deployment |
|---|---|---|
| Apache Kafka | Apache | On-Premise / Cloud |
| Apache Flink | Apache | On-Premise / Cloud |
| Apache Spark Streaming | Apache | On-Premise / Cloud |
| AWS Kinesis | AWS | Cloud |
| Azure Event Hubs | Microsoft Azure | Cloud |
| Google Cloud Pub/Sub | Google Cloud | Cloud |
| Confluent Platform | Confluent | On-Premise / Cloud / SaaS |
| Huawei DMS (Distributed Message Service) | Huawei Cloud | Cloud / Server |

---

## C. Hybrid Ingestion

Hybrid ingestion mixes both batch and real-time approaches within a single pipeline. Common in large enterprises where some data needs immediate processing while other data can wait.

### Use Cases

| # | Use Case | Description |
|---|---|---|
| a | E-Commerce | Real-time for live inventory updates, batch for end-of-day sales reports |
| b | Healthcare | Streaming patient vitals in real time, batch-loading historical records nightly |
| c | Financial Services | Streaming transactions for fraud detection, batch-processing settlements |

### Tools

| Tool | Vendor | Deployment |
|---|---|---|
| Apache NiFi | Apache | On-Premise / Cloud |
| Apache Kafka + Spark | Apache | On-Premise / Cloud |
| AWS Glue + Kinesis | AWS | Cloud |
| Azure Data Factory + Event Hubs | Microsoft Azure | Cloud |
| Google Cloud Dataflow | Google Cloud | Cloud |
| Cloudera Data Platform (CDP) | Cloudera | On-Premise / Hybrid |
| Huawei DMS + Cloud Migration Service | Huawei Cloud | Cloud / Server |

---

⬅️ [Back to Tools & Processes](../README.md) | ➡️ [Next: Data Cleaning](../03-cleaning/README.md)
