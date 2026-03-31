## Big Data Technology and Tools

In big data, there are many data processes, and within each of those processes there are many tools available to help you. Let's break down what each step does and which tools are best suited for each scenario.

---

### 1. Data Ingestion

Data ingestion is the process of collecting, importing, and loading data from various sources into a storage or processing system. Depending on your ingestion approach, different tools will serve you better. Let's break down the three types first before picking the right toolset.

#### A. Batch Ingestion

Batch ingestion means transferring data in scheduled intervals — ranging from every few hours to once a day or longer. Data is collected over a period of time and then ingested all at once on a fixed schedule, which is why it's called "batch."

This approach is ideal when you don't need instant insights, and it helps manage large volumes of data efficiently without overwhelming your system.

**Use cases:**

| # | Use Case | Description |
|---|---|---|
| a | Reporting | Collecting data periodically to generate business insights and summaries |
| b | Data Backups | Moving historical records from operational databases into a warehouse on a nightly schedule |
| c | Payroll Processing | Aggregating employee hours and transactions at the end of a pay period |
| d | ETL Pipelines | Extracting, transforming, and loading large datasets from source systems into a warehouse on a schedule |

**Tools:**

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

> **Note:** In Huawei Cloud engagements, we typically use the **Cloud Migration Service (SMS)** for batch data ingestion scenarios.

---

#### B. Real-Time / Streaming Ingestion

Real-time ingestion involves continuously collecting and processing data as it is generated. This makes it possible to gain instant insights, which is critical in time-sensitive scenarios where immediate decision-making is required.

**Use cases:**

| # | Use Case | Description |
|---|---|---|
| a | Fraud Detection | Monitoring transactions in real time to identify and respond to suspicious activity |
| b | IoT Sensors | Gathering and processing data from devices such as temperature or motion sensors in real time |
| c | Live Analytics | Powering dashboards that need minute-level updates to track key metrics |
| d | Real-Time Recommendations | Serving product or content recommendations based on a user's live behaviour |

**Tools:**

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

#### C. Hybrid Ingestion

Hybrid ingestion mixes both batch and real-time approaches to handle varied data sources and business needs within a single pipeline. This is common in large enterprises where some data requires immediate processing while other data can be deferred.

**Use cases:**

| # | Use Case | Description |
|---|---|---|
| a | E-Commerce | Real-time ingestion for live inventory and order updates, batch ingestion for end-of-day sales reporting |
| b | Healthcare | Streaming patient vitals from monitors in real time, while batch-loading historical records nightly |
| c | Financial Services | Streaming live transaction data for fraud detection, while batch-processing settlements and reconciliations |

**Tools:**

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

### 2. Data Storage

> *(See Big Data Storage section — covers Data Lakes, Data Warehouses, and Data Lakehouses)*

---

### 3. Data Cleaning / Pre-processing

Data cleaning is the step where you transform raw, messy data into something reliable and usable — by removing empty values, eliminating duplicates, fixing inconsistencies, and standardizing formats across your dataset.

Cleaning data in big data is fundamentally different from cleaning a regular database. In a traditional database you might simply drop a column or fill a null value manually. At petabyte scale with hundreds of data types coming from varied sources, that approach breaks down entirely — which is why big data cleaning relies on distributed frameworks that can process and clean data in parallel across many machines.

One common technique to speed up preprocessing is **vectorization** — instead of processing records one by one, the framework converts data into numerical arrays (ones and zeros) that the CPU or GPU can process in bulk. This saves significant time and compute resources at scale.

**Tools:**

| Tool | Vendor | Best For | Deployment |
|---|---|---|---|
| Apache Spark (with DataFrames) | Apache | Large-scale distributed cleaning and transformation | On-Premise / Cloud |
| Apache Beam | Apache | Unified batch and streaming data cleaning pipelines | On-Premise / Cloud |
| AWS Glue DataBrew | AWS | Visual, no-code data cleaning for cloud pipelines | Cloud |
| Azure Data Factory (Data Flows) | Microsoft Azure | Cleaning and transforming data within Azure pipelines | Cloud |
| Google Cloud Dataprep (by Trifacta) | Google Cloud / Trifacta | Intelligent data preparation with visual profiling | Cloud / SaaS |
| Talend Data Quality | Talend | Data profiling, deduplication, and standardization | On-Premise / Cloud |
| Informatica Data Quality | Informatica | Enterprise-grade data quality and cleansing | On-Premise / Cloud |
| Pandas + Dask | Open Source | Python-based cleaning for medium-to-large datasets | On-Premise / Cloud |
| Huawei DataArts Studio | Huawei Cloud | End-to-end data governance and cleaning on Huawei Cloud | Cloud / Server |

---

### 4. Data Analysis

Once your data is cleaned and ready, data analysis is where you start extracting meaningful insights from it. This can be as simple as running SQL queries against your cleaned dataset to answer specific business questions, or as complex as running statistical models and machine learning workloads across billions of rows.

**Tools:**

| Tool | Vendor | Best For | Deployment |
|---|---|---|---|
| Google BigQuery | Google Cloud | Serverless SQL analytics on massive datasets | Cloud |
| AWS Athena | AWS | Querying data directly in S3 using SQL | Cloud |
| Azure Synapse Analytics | Microsoft Azure | Integrated SQL and Spark-based big data analysis | Cloud |
| Apache Spark | Apache | Distributed in-memory analytics and ML workloads | On-Premise / Cloud |
| Apache Hive | Apache | SQL-based querying on Hadoop data lakes | On-Premise / Self-Hosted |
| Presto / Trino | Open Source | Fast, distributed SQL queries across multiple data sources | On-Premise / Cloud |
| Databricks | Databricks | Collaborative analytics and ML on large datasets | Cloud / SaaS |
| Snowflake | Snowflake | Cloud-native SQL analytics with multi-cluster scaling | Cloud / SaaS |
| Huawei DLI (Data Lake Insight) | Huawei Cloud | Serverless SQL and Spark analytics on Huawei Cloud | Cloud / Server |

---

### 5. Data Visualization

At this stage your cleaned, analyzed data is ready to be presented — either to stakeholders through dashboards and reports, or fed into AI models and agents for further use. This is the final step of your big data journey, where raw numbers become stories and decisions.

**Tools:**

| Tool | Vendor | Best For | Deployment |
|---|---|---|---|
| Power BI | Microsoft | Business dashboards and executive reporting | Cloud / SaaS |
| Tableau | Salesforce | Interactive visual analytics and storytelling | On-Premise / Cloud / SaaS |
| Apache Superset | Apache | Open-source dashboards on top of any SQL source | On-Premise / Self-Hosted |
| Grafana | Grafana Labs | Real-time monitoring dashboards, great for IoT and ops | On-Premise / Cloud / SaaS |
| Looker | Google Cloud | Embedded analytics and data exploration | Cloud / SaaS |
| Metabase | Metabase | Lightweight, easy-to-use BI for smaller teams | On-Premise / Cloud |
| AWS QuickSight | AWS | Cloud-native BI integrated with the AWS ecosystem | Cloud |
| Huawei DataArts Insight | Huawei Cloud | Visualization layer within the Huawei DataArts platform | Cloud / Server |
| Custom Dashboards | — | Tailored internal tools built with frameworks like D3.js, React, or Grafana | On-Premise / Cloud |

> **Note on AI / LLM Integration:** At the visualization stage, your processed datasets can also be used to train or fine-tune AI models and LLMs, or to power AI agents that interact with your data directly through natural language. Tools like Databricks, BigQuery ML, and Azure ML sit at the intersection of analysis and AI.

---

### A Note on ETL vs ELT

The big data process doesn't always follow a strict linear order. Sometimes data is processed first and stored after, or vice versa, depending on business requirements. This is where **ETL** and **ELT** come in.

- **ETL (Extract → Transform → Load):** Data is extracted from the source, cleaned and transformed first, then loaded into the destination. Best suited when data quality and structure need to be enforced before storage.

- **ELT (Extract → Load → Transform):** Data is extracted and loaded into storage first in its raw form, and transformation happens afterwards inside the storage system. Best suited for cloud-based systems and large-scale raw data where storage is cheap and compute is elastic.

**Example:** An IoT company would most likely follow **ETL** — extract sensor data (ingestion), transform and filter it immediately (preprocessing), then load it into their platform for real-time use. A data analytics company, on the other hand, might prefer **ELT** — dump everything raw into a data lake first, then transform only what they need for a specific report or model.
