[العربي](./06-data-engineering_ar.md)

# <a name="-6-data-engineering"></a>📊 Chapter 6: Data Engineering

## 1. What is it?

Data Engineering is the discipline that focuses on building and maintaining the "infrastructure" for data. A data engineer is the "plumber" or "road engineer" of the data world; they don't analyze data to extract knowledge, but rather build robust and reliable systems to collect, transport, store, and transform massive amounts of data, making it ready for use by data scientists and analysts.

## 2. What does the specialist do?

* Building Data Pipelines: Designing and building automated systems to move data from its sources (like applications, databases, sensors) to its final destination (like a data warehouse).
* Designing Data Models: Structuring and organizing data in databases or data warehouses to be easy to query and analyze.
* ETL/ELT Processes: Implementing Extract, Transform, and Load (ETL) or Extract, Load, and Transform (ELT) processes.
* Ensuring Data Quality and Reliability: Making sure the data is accurate, complete, and available when needed.
* Managing Big Data: Using specialized tools to handle data that is too large, fast, or diverse to be processed by traditional methods.

## 3. Sub-domains

* ETL Engineering: Focusing on building traditional ETL processes.
* Data Pipeline Engineering: Focusing on building more modern and interactive data pipelines.
* Big Data Engineering: Specializing in tools like Spark and Hadoop.
* Analytics Engineering: A modern role that sits between a data engineer and a data analyst, focusing on transforming data within the data warehouse to be ready for direct analysis.

## 4. Expanded Key Concepts

* `Data Pipeline`: The entire process of moving data from source to destination.
* `ETL vs. ELT`:
  * `ETL`: Extract, then Transform (on an intermediate server), then Load to the final destination.
  * `ELT`: Extract, then Load to the final destination (like a cloud data warehouse), then Transform it there to leverage the warehouse's power.
* `Data Warehouse`: A large database optimized for complex analytical queries. It contains structured and historical data.
* `Data Lake`: A repository for storing massive amounts of data in its raw form (structured, unstructured, etc.) without needing to structure it beforehand.
* `Data Modeling`: The process of designing the data structure. The most famous models in data warehouses are the Star Schema and Snowflake Schema.
* `Batch vs. Stream Processing`:
  * `Batch`: Processing large amounts of data at specific time intervals (e.g., every hour).
  * `Stream`: Processing data instantly as it arrives.

## 5. Expanded Tools & Technologies

* Programming Languages: Python (most common), SQL (essential and very important), Scala, Java.
* Big Data Processing Tools: Apache Spark, Apache Hadoop.
* Data Streaming Tools: Apache Kafka, Apache Flink.
* Cloud Data Warehouses: Google BigQuery, Amazon Redshift, Snowflake.
* Pipeline Orchestration Tools: Apache Airflow, Prefect, Dagster.
* Transformation Tools: dbt (Data Build Tool).

## 6. In-Depth Workflow

Project: Build a nightly pipeline to collect sales data from the application's database and load it into a data warehouse for analysis.

 1. Planning: The data engineer decides to pull sales data from the production PostgreSQL database every night, clean it, and then load it into Google BigQuery.
 2. Orchestration: They use Apache Airflow to create a "DAG" (Directed Acyclic Graph) that describes the process steps.
 3. Extract Task: They write a Python script (which will be a task in Airflow) that connects to the production PostgreSQL database and extracts all sales made in the previous day.
 4. Transform Task: They write another Python script (a subsequent task in Airflow) using the Pandas library. This script cleans the data (e.g., standardizing product names) and enriches it (e.g., adding the profit margin for each sale).
 5. Load Task: They write a third script that takes the clean data and loads it into the designated table in BigQuery.
 6. Scheduling and Monitoring: They schedule this DAG to run automatically every night at 2 AM. Airflow monitors the process, and if any step fails, it sends an alert to the engineer.
 7. Documentation: The engineer documents the data sources, the transformations performed, and the structure of the tables in BigQuery so that data analysts can easily understand and use it.

## 7. Common Job Roles

* Data Engineer: The general role.
* Big Data Engineer: Specializes in big data tools.
* Cloud Data Engineer: Specializes in data tools on a specific cloud platform (AWS, GCP, Azure).
* Analytics Engineer: Focuses on the transformation (T) stage within the data warehouse.

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Airflow`** | An open-source tool for orchestrating, scheduling, and monitoring data pipelines. |
| **`API`** | Application Programming Interface, a common source for fetching data. |
| **`Big Data`** | A term for data characterized by large Volume, high Velocity, and variety. |
| **`DAG`** | Directed Acyclic Graph, the basic concept for defining workflows in tools like Airflow and Spark. |
| **`Data Governance`** | The set of policies and standards to ensure data quality and security. |
| **`Data Lineage`** | Tracking the path of data from its original source through all transformations to its final destination. |
| **`Data Mart`** | A smaller data warehouse focused on a specific department in a company (like marketing or sales). |
| **`dbt`** | A popular tool that enables analytics engineers to transform data in a data warehouse using SQL. |
| **`Hadoop`** | A big data framework, consisting mainly of the distributed file system `HDFS` and the processing engine `MapReduce`. |
| **`Idempotent`** | A property of an operation that, if performed multiple times, gives the same result as if performed once. This is an important property in data pipelines. |
| **`Kafka`** | An event streaming platform used to transport massive amounts of data in real-time. |
| **`OLAP`** | Online Analytical Processing, a type of database designed for complex analytical queries (like data warehouses). |
| **`OLTP`** | Online Transaction Processing, a type of database designed for fast daily operations (like application databases). |
| **`Orchestration`** | Organizing and coordinating multiple tasks in a data pipeline. |
| **`Parquet`** | A popular columnar file format for storing big data, known for its efficiency in compression and querying. |
| **`Schema`** | A blueprint that describes the structure of data in a database or table. |
| **`Snowflake`** | A very popular modern cloud data warehouse. |
| **`Spark`** | A distributed, high-performance processing engine for big data, much faster than Hadoop MapReduce. |
| **`SQL`** | The primary query language for interacting with databases and data warehouses. |

</details>

[⬆️ Back to Table of Contents](README.md)

