# Employee Data ETL Pipeline with Cloud Composer & Data Fusion

## 🛠 Overview
This repository contains an **ETL pipeline** built with:
- **Apache Airflow (Cloud Composer)** to orchestrate jobs.
- **Google Cloud Storage (GCS)** to store raw data.
- **Cloud Data Fusion** to transform and load data into **BigQuery**.
- **BigQuery** as the final data warehouse.
- **Looker** for visualization.

### **📌 Workflow**
1. **Extract Data (Python Script)**
   - `extract.py` generates **dummy employee data** using the `Faker` library.
   - Saves data as a CSV file in **Google Cloud Storage (GCS)**.

2. **Run Airflow DAG**
   - `dag.py` triggers:
     - `extract.py` to generate and upload data.
     - **Cloud Data Fusion Pipeline** to transform & load data into BigQuery.

3. **Analyze & Visualize**
   - Looker connects to **BigQuery** for visualization.

---

## 🚀 **Project Structure**
![image](https://github.com/user-attachments/assets/a38fefce-47b1-454a-b6ea-e4471f5c19aa)
