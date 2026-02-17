## 🚀 End-to-End Azure Data Engineering Pipeline
### 📌 Project Overview

This project demonstrates the implementation of a production-style end-to-end data engineering pipeline built on Microsoft Azure. The pipeline covers data ingestion, transformation, orchestration, storage optimization, and governance using modern cloud-native tools.

The goal of this project was to simulate a real-world cloud data architecture capable of handling large-scale datasets efficiently using Azure Data Factory, Azure Databricks, and Azure Data Lake Storage Gen2, following the Medallion Architecture (Bronze, Silver, Gold).

![Successful Pipeline Run](https://github.com/user-attachments/assets/c1f77636-f2ce-41ff-88e7-208f099bff25)

### 🏗️ Architecture Design

The project follows a layered architecture to ensure scalability, maintainability, and optimized data processing:

🔹 Bronze Layer

Raw data ingestion from:

External REST APIs

Flat files

Data stored in Azure Data Lake Storage Gen2

Minimal transformation applied

Preserves source-level structure

🔹 Silver Layer

Data cleaning and transformation using PySpark

Deduplication, null handling, schema standardization

Joins and business rule implementation

Data stored in Parquet format for optimized storage and performance

🔹 Gold Layer

Business-ready, curated datasets

Aggregated and analytics-friendly tables

Stored in Delta format within Databricks Unity Catalog

Enables:

ACID transactions

Schema enforcement

Centralized governance

Time-travel capabilities

### 🔄 Data Pipeline Flow

Data ingestion orchestrated using Azure Data Factory (ADF)

Raw data stored in ADLS Gen2 (Bronze layer)

Transformations executed in Azure Databricks using PySpark

Cleaned datasets written to Silver (Parquet)

Curated tables written to Gold (Delta + Unity Catalog)

Pipelines monitored and scheduled through ADF

Secrets securely managed via Azure Key Vault

### ⚙️ Key Features

✔ End-to-end cloud data pipeline implementation

✔ Full and incremental data load logic (reduced unnecessary reprocessing by ~40%)

✔ Metadata-driven pipeline design for scalable ingestion

✔ Distributed data processing using PySpark

✔ Storage optimization using Parquet format

✔ ACID-compliant Gold layer using Delta Lake

✔ Centralized governance using Databricks Unity Catalog

✔ Secure secret management using Azure Key Vault

### 📊 Performance & Scale

Processed ~1M+ records across multiple layers

Reduced redundant processing using incremental load strategy

Improved transformation efficiency using distributed Spark execution

### 🛠️ Technologies Used

Azure Data Factory (ADF)

Azure Databricks

Azure Data Lake Storage Gen2 (ADLS Gen2)

PySpark

Delta Lake

Databricks Unity Catalog

Azure Key Vault

### 🔐 Security & Governance

Secrets and credentials stored in Azure Key Vault

Gold tables governed via Unity Catalog

Separation of storage layers for better access control

Production-style architecture design principles applied

### 📈 What I Learned

Designing scalable cloud-based data architectures

Implementing incremental ingestion strategies

Working with distributed processing using Spark

Optimizing storage using Parquet and Delta formats

Managing governance and security in a cloud data environment

Orchestrating complex workflows using Azure Data Factory


👨‍💻 Author

Aman Shinde
Aspiring Data Engineer
