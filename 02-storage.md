# 🗄️ Big Data Storage

> Where does all that data actually live? This section breaks down the three main storage types you'll encounter in big data systems.

---

## Table of Contents

- [Data Lakes](#1-data-lakes)
- [Data Warehouses](#2-data-warehouses)
- [Data Lakehouses](#3-data-lakehouses)

---

## 1. Data Lakes

A data lake is a low-cost storage environment designed to handle massive amounts of raw structured or unstructured data. You don't need to clean the data yet — it stays in its native format. This is ideal when volume, variety, and velocity are high and performance or quality isn't a priority yet.

Data lakes are commonly used to support AI training, machine learning, and big data analytics. They can also act as a general-purpose staging area where raw data waits before being moved to other applications.

**Think of it as:** a giant dumping ground where everything goes in first, questions asked later. 🪣

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

## 2. Data Warehouses

Data warehouses are built to support analytics, business intelligence (BI), and data science. They aggregate data from many sources into a central hub with a strict schema enforced — meaning data must be clean and structured before it goes in. This makes storage costs higher, but queries much faster and more reliable.

Rather than storing everything, warehouses store a curated subset of big data that's ready for business users, analysts, and reporting tools to query directly.

**Think of it as:** a well-organized library where everything is catalogued and easy to find. 📚

| Vendor | Product / Service | Deployment |
|---|---|---|
| AWS | Amazon Redshift | Cloud |
| Google Cloud | BigQuery | Cloud |
| Microsoft Azure | Azure Synapse Analytics | Cloud |
| Microsoft | Microsoft Fabric (Fabric SQL) | Cloud / SaaS |
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

> 💡 **Bonus — Data Marts:** A data mart is a smaller, department-focused version of a data warehouse. It stores cleaned, structured data but serves only one specific department (e.g. Marketing or Finance), whereas a data warehouse serves the entire organization.

---

## 3. Data Lakehouses

A data lakehouse is an emerging hybrid solution that combines the best of both worlds — the cheap, flexible storage of a data lake with the powerful querying capability of a data warehouse — all in a single platform. This eliminates the need to maintain two separate systems and is quickly becoming the modern standard.

**Think of it as:** the best of both worlds — store everything cheaply, query it powerfully. 🏆

| Vendor | Product / Service | Deployment |
|---|---|---|
| Databricks | Databricks Lakehouse Platform | Cloud / SaaS |
| AWS | AWS Lake Formation + Athena | Cloud |
| Google Cloud | BigQuery + BigLake | Cloud |
| Microsoft | Microsoft Fabric | Cloud / SaaS |
| Huawei Cloud | DataArts FabricSQL | Cloud / Server |
| Cloudera | Cloudera Data Platform (CDP) | On-Premise / Hybrid |
| Snowflake | Snowflake (with Iceberg Tables) | Cloud / SaaS |
| Apache | Apache Iceberg + Spark | On-Premise / Self-Hosted |
| Apache | Apache Hudi | On-Premise / Self-Hosted |
| Delta Lake (Linux Foundation) | Delta Lake | On-Premise / Self-Hosted |
| IBM | IBM watsonx.data | Cloud / On-Premise |
| Starburst | Starburst Galaxy | Cloud / SaaS |
| Dremio | Dremio Lakehouse Platform | On-Premise / Cloud |

---

⬅️ [Back to Fundamentals](./01-fundamentals.md) | ➡️ [Next: Tools & Processes](./03-tools-and-processes/README.md)
