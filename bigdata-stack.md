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
| Apache Nifi | Apache | On-Premise / Cloud |
| AWS Glue | AWS | Cloud |
| Azure Data Factory | Microsoft Azure | Cloud |
| Google Cloud Dataflow | Google Cloud | Cloud |
| Talend | Talend | On-Premise / Cloud / SaaS |
| Informatica PowerCenter | Informatica | On-Premise / Cloud |
| Huawei Cloud Migration Service (SMS) | Huawei Cloud | Cloud / Server |

> **Note:** In Huawei Cloud engagements, we typically use the **Cloud Migration Service (CMS)** for batch data ingestion scenarios.

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

> *(See Big Data Storage section above — covers Data Lakes, Data Warehouses, and Data Lakehouses)*

---

### 3. Data Cleaning

*(Coming soon)*

---

### 4. Data Analysis

*(Coming soon)*

---

### 5. Data Visualization

*(Coming soon)*

---

### A Note on ETL vs ELT

The big data process doesn't always follow a strict linear order. Sometimes data is processed first and stored after, or vice versa, depending on the business requirement. This is where the concepts of **ETL** and **ELT** come in.

- **ETL (Extract → Transform → Load):** Data is extracted from the source, cleaned and transformed first, and then loaded into the destination system. Best suited when data quality and structure need to be enforced before storage.

- **ELT (Extract → Load → Transform):** Data is extracted and loaded into storage first in its raw form, and transformation happens afterwards inside the storage system. Best suited for cloud-based systems and large-scale raw data where storage is cheap.

**Example:** An IoT company would most likely follow **ETL**, because it needs constant real-time updates — extract the sensor data (ingestion), transform it immediately (preprocessing/filtering), and then load it into their platform for instant use.
