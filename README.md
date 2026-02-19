# End-to-End Data Warehouse Solution (Medallion Architecture)

## 🏗️ Architecture Overview
This project implements a robust **Medallion Architecture** (Bronze, Silver, Gold) within a SQL Server environment. It automates the flow of data from raw sources to business-ready reporting layers, ensuring high data quality and optimized performance for downstream consumption.

## 📁 Project Structure

### 1. Data Sources
*   **Systems:** CRM and ERP systems.
*   **Object Type:** CSV Files.
*   **Interface:** Automated file-in-folder ingestion logic.

### 2. Data Warehouse Layers

#### 🥉 Bronze Layer (Raw Data)
*   **Process:** Initial ingestion using **Stored Procedures**.
*   **Load Type:** Batch Processing (Full Load via Truncate & Insert).
*   **Data State:** Unaltered, as-is raw data stored in SQL Tables for historical traceability.

#### 🥈 Silver Layer (Cleaned & Standardized)
*   **Process:** Data refinement via **Stored Procedures**.
*   **Transformations:** 
    *   Data Cleansing & Standardization.
    *   Data Normalization.
    *   Creation of Derived Columns & Data Enrichment.
*   **Data State:** Trustworthy, standardized tables ready for integration.

#### 🥇 Gold Layer (Business-Ready)
*   **Process:** Optimized for reporting using **SQL Views**.
*   **Transformations:** 
    *   Complex Data Integrations & Aggregations.
    *   Implementation of specific Business Logic.
*   **Data Models:** Supports **Star Schema**, Flat Tables, and Aggregated Tables for high-performance BI.

### 3. Consumption Layer
The architecture serves three primary business functions:
*   **BI & Reporting:** Interactive Power BI dashboards for strategic decision-making.
*   **Ad-Hoc Analysis:** Direct SQL access for custom queries.
*   **Machine Learning:** Structured datasets prepared for predictive modeling.

## 🛠️ Technical Stack
*   **Database:** MS SQL Server
*   **Logic:** T-SQL (Stored Procedures & Views)
*   **Data Ingestion:** CSV-to-SQL Batch Processing
*   **Data Modeling:** Dimensional Modeling (Star Schema)
*   **BI Tool:** Power BI

## 🚀 Key Achievements
*   Reduced data latency by implementing efficient **Batch Processing** workflows.
*   Ensured 100% data consistency by moving business logic from report layers to the **Gold Layer** SQL views.
*   Implemented scalable ETL processes capable of handling multi-source data enrichment.

---
*Developed by Nikesh Anand - Power BI & Data Specialist*
