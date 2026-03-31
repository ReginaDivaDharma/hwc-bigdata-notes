# 🧹 Data Cleaning / Pre-processing

> Garbage in, garbage out. This step is where raw, messy data gets turned into something reliable and usable.

---

Data cleaning means removing empty values, eliminating duplicates, fixing inconsistencies, and standardizing formats across your dataset.

Cleaning data in big data is fundamentally different from cleaning a regular database. In a traditional database you might drop a column or fill a null value manually — easy. At petabyte scale with hundreds of data types coming from varied sources, that approach breaks down entirely. Big data cleaning relies on **distributed frameworks** that process and clean data in parallel across many machines simultaneously.

One common technique to speed up preprocessing is **vectorization** — instead of processing records one by one, the framework converts data into numerical arrays that the CPU or GPU can crunch in bulk, saving significant time and compute at scale.

## Tools

| Tool | Vendor | Best For | Deployment |
|---|---|---|---|
| Apache Spark (DataFrames) | Apache | Large-scale distributed cleaning and transformation | On-Premise / Cloud |
| Apache Beam | Apache | Unified batch and streaming cleaning pipelines | On-Premise / Cloud |
| AWS Glue DataBrew | AWS | Visual, no-code data cleaning for cloud pipelines | Cloud |
| Azure Data Factory (Data Flows) | Microsoft Azure | Cleaning and transforming data within Azure pipelines | Cloud |
| Google Cloud Dataprep | Google Cloud / Trifacta | Intelligent data prep with visual profiling | Cloud / SaaS |
| Talend Data Quality | Talend | Data profiling, deduplication, and standardization | On-Premise / Cloud |
| Informatica Data Quality | Informatica | Enterprise-grade data quality and cleansing | On-Premise / Cloud |
| Pandas + Dask | Open Source | Python-based cleaning for medium-to-large datasets | On-Premise / Cloud |
| Huawei DataArts Studio | Huawei Cloud | End-to-end data governance and cleaning | Cloud / Server |

> 🚧 **Project coming soon** — a hands-on cleaning example using Apache Spark on a messy real-world dataset.

---

⬅️ [Back to Ingestion](../01-ingestion/README.md) | ➡️ [Next: Data Analysis](../04-analysis/README.md)
