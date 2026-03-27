# 📰 NYT Data Lakehouse: Automated ETL Pipeline
**Modern Data Engineering | Medallion Architecture | Oracle Cloud Infrastructure**

## 📌 Project Overview
This project implements a scalable **Data Lakehouse** using the New York Times Archive API. It demonstrates a complete end-to-end pipeline, ingesting over 7 years of global news data (2019–2026) into **Oracle Cloud Infrastructure (OCI)**. 

By leveraging the **Medallion Architecture**, I’ve ensured that raw data is transformed into high-value business intelligence through a structured validation process.

---

## 🏗 System Architecture
The data flows through a cloud-native pipeline designed for security and cost-efficiency:

### 🥉 Bronze Layer (Raw)
* **Source:** NYT Archive API.
* **Ingestion:** Python scripts fetch monthly JSON archives.
* **Storage:** **OCI Object Storage** using Pre-Authenticated Requests (PAR).

#### **Data Source Authentication**
<p align="center">
  <img src="images/NYTimes.png" alt="NY Times API" width="800">
  <br><i>Authorized access via the NYT Developer Portal</i>
</p>

---

### 🥈 Silver Layer (Cleaned)
* **Processing:** Batch processing with **Pandas**.
* **Transformation:** Column filtering, deduplication, and data type conversion.
* **Storage:** **Apache Parquet** format for optimized performance.

#### **Cloud Storage Organization**
<p align="center">
  <img src="images/DataLake2.png" alt="OCI Bucket Structure" width="800">
  <br><i>OCI Bucket Structure with Bronze/Silver/Gold folder prefixing</i>
</p>

---

### 🥇 Gold Layer (Analytics)
* **Integration:** **Oracle DBMS_CLOUD** package.
* **Outcome:** External Tables in **Autonomous Data Warehouse (ADW)**.

#### **Final Output & Querying**
<p align="center">
  <img src="images/results.png" alt="Query Results" width="800">
  <br><i>Python Terminal execution and Data Lake results</i>
</p>

---

## 🚀 Engineering Highlights
* **Security First:** Utilized **OCI PARs** for secure API-to-Cloud communication.
* **Schema-on-Read:** Database queries Parquet files directly in Object Storage.
* **Oracle ACE Apprentice Standards:** Built entirely on the OCI Free Tier.

---

## 📂 Repository Structure
* `/python`: Python scripts for API ingestion and Parquet conversion.
* `/images`: Diagrams, screenshots, and API documentation.

---

## 🏆 About the Author
**Wellington Lacerda** *Computer Engineering Student @ UNIVESP | Oracle ACE Apprentice*
