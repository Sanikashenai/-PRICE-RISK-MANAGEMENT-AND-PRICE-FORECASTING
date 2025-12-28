# 🚀 Price Risk Management & Forecasting

This project demonstrates a complete data engineering and analytics lifecycle—from multi-source ingestion to machine learning-based price forecasting—all unified within the **Microsoft Fabric** environment.

---

## 🏗️ The Architecture


https://github.com/user-attachments/assets/236ea05a-8b52-4755-9e0c-44c3398a3733


The project follows a modern "Medallion" or "Lakehouse" architecture pattern, ensuring data is cleaned, modeled, and ready for high-performance reporting.

### Core Workflow:

1. **Ingestion:** Multi-modal data intake (Upload, Shortcuts, Data Pipelines).
2. **Storage:** Unified OneLake storage using the **Lakehouse** and **SQL Warehouse**.
3. **Transformation:** Conversion of raw CSV/JSON to optimized Delta Parquet tables.
4. **Modeling:** Establishing a Star Schema in the SQL Analytics Endpoint.
5. **Visualization:** Interactive Power BI reports for global order distribution.

---

## 📥 Stage 1: Data Ingestion Strategies

A robust data platform must handle diverse data types. In this project, we utilize three distinct data structures:

| Data Type | Format Used | Description |
| --- | --- | --- |
| **Structured** | `.csv`, `.parquet`, `.xlsx` | Tabular data with a fixed schema; ready for immediate SQL querying. |
| **Semi-Structured** | `.json` | Nested key-value pairs; flexible but hierarchical. |
| **Unstructured** | `.txt` | Raw character streams; requires parsing for insights. |

### Ingestion Methods Employed:
<img width="1486" height="603" alt="image" src="https://github.com/user-attachments/assets/4aaeef47-76ed-4b49-ad06-87d23920fc1e" />

* **Direct Upload:** Quick ingestion of local CSV files directly into the Lakehouse "Files" section.
* **OneLake Shortcuts:** Live virtualization of data from the **Data Warehouse** into the **Lakehouse**, avoiding data duplication.
* **Data Factory Pipelines:** Orchestrated movement of data for automated, recurring loads.
* **Dataflow Gen2:** Low-code "Power Query" experience to clean data before it hits the table layer.

---

## 🛠️ Stage 2: Data Engineering & Transformation

Once the data is in OneLake, we transition from raw files to high-performance tables.

### 1. From Files to Delta Tables

Using the **"Load to Tables"** feature, we convert raw CSVs into optimized Delta Lake tables. This allows for:

* **ACID Transactions:** Ensuring data integrity.
* **Time Travel:** Querying previous versions of the data.
* **Performance:** Faster read/write speeds for large datasets.

### 2. The SQL Analytics Endpoint

By shifting the Lakehouse to **SQL Analytics Mode**, we unlock a full T-SQL experience. Here, we:

* Define **Primary and Foreign Key relationships** between Fact and Dimension tables.
* Write complex **DAX measures** for aggregate functions (e.g., Total Revenue, YoY Price Variance).

---

## 📊 Stage 3: Analytics & Visualization

The final layer turns raw data into business intelligence.

* **Geospatial Analysis:** Visualizing total orders by country to identify high-risk price zones.
* **Temporal Trends:** Analyzing order volume by month to detect seasonality.
* **Real-time Connection:** Utilizing **Direct Lake** mode in Power BI for near-instant reporting on Lakehouse data without the need for manual refreshes.

---

## 🔮 Future Enhancements (Price Forecasting)

To complete the "Risk Management" aspect, the next phase involves:

* **Synapse ML:** Training a Time-Series model in a Fabric Notebook.
* **Forecasting:** Predicting price volatility for the next 6 months.
* **Automated Alerts:** Using Data Activator to trigger emails if prices exceed a specific risk threshold.

---

**Would you like me to help you draft the Python code for a Fabric Notebook to handle the Price Forecasting (ML) part of this project?**
