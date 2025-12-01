# 🧱 Data Engineering

> **Languages:** [English](README.md) | [العربية](README_ar.md)

Welcome to the **Data Engineering** track! Learn to design and build systems for collecting, storing, and analyzing data at scale.

## 🗺️ Roadmap

```mermaid
graph TD
    DE[Data Engineering] --> Lang[Languages]
    DE --> DB[Databases]
    DE --> Pipe[Pipelines]
    DE --> Big[Big Data]

    Lang --> Py[Python]
    Lang --> Scala
    Lang --> SQL

    DB --> Rel[Relational (Postgres)]
    DB --> NoSQL[NoSQL (Mongo/Cassandra)]
    DB --> WH[Warehousing (Snowflake)]

    Pipe --> Air[Airflow]
    Pipe --> Kafka
    Pipe --> ETL

    Big --> Spark
    Big --> Hadoop
    Big --> Cloud[AWS/GCP/Azure]
```

## 📚 Core Content

- **[Data Engineering Guide (English)](data-engineering.md)**
- **[دليل هندسة البيانات (العربية)](data-engineering_ar.md)**

## 🛠️ Projects

- **ETL Pipeline**: Build a pipeline to extract data from an API, transform it, and load it into a database.
- **Data Warehouse**: Design a schema and populate a data warehouse.
- **Real-time Streaming**: Process a stream of data using Kafka and Spark.

---

[⬅️ Back to Main Roadmap](../README.md)
