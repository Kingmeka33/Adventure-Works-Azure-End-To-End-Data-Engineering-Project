# Building an End-to-End Data Engineering Solution with Azure ✨  

In this project, I share a **comprehensive guide** to designing an end-to-end (E2E) data engineering pipeline using **Azure's powerful tools**.  
The solution processes, transforms, and delivers data for **Business Intelligence (BI)** purposes, leveraging resources like:  

- **Azure Data Factory**  
- **Azure Databricks**  
- **Azure Synapse Analytics**  
- **Power BI**  

The data source is the **AdventureWorks dataset**, fetched directly from GitHub.  

---

## 📂 Project Overview  

This project demonstrates how to design, build, and implement a scalable data pipeline in Azure:  

1. **Data ingestion** with Azure Data Factory (ADF).  
2. **Data transformation** with Azure Databricks.  
3. **Data warehousing** with Azure Synapse Analytics.  
4. **Visualization & BI reporting** with Power BI.  

---

## 🏗️ Architecture Overview  
<img width="1263" height="670" alt="Image" src="https://github.com/user-attachments/assets/a9000c4d-5cae-4188-abce-341b655b3a3f" />

---

## ⚙️ Step 1: Setting Up the Azure Environment  

Provisioned Azure resources:  

- **Azure Data Factory (ADF):** Orchestration and automation.  
- **Azure Storage Account:** Data lake with raw (bronze), transformed (silver), and curated (gold) zones.  
- **Azure Databricks:** Data transformations and computation.  
- **Azure Synapse Analytics:** Data warehousing for BI use.  

> All resources were configured with proper **Identity and Access Management (IAM)** roles to ensure seamless integration and security.  
<img width="1919" height="812" alt="Image" src="https://github.com/user-attachments/assets/d93eea78-b4a6-4536-a14e-6b2f00fa97c8" />
---

## 🚀 Step 2: Data Pipeline with Azure Data Factory  

- **Dynamic Copy Activity:** ADF pulls data from GitHub via HTTP connector and lands it in the **bronze container** in Azure Storage.  
- **Parameterization:** Pipeline parameters ensure adaptability for data source changes.  

<img width="1919" height="817" alt="Image" src="https://github.com/user-attachments/assets/df660b74-691c-4720-af87-e2f774e0d4f2" />
<img width="1913" height="862" alt="Image" src="https://github.com/user-attachments/assets/3f340ee9-4b4f-4e88-9907-97da78000acf" />

---

## 🔄 Step 3: Data Transformation with Azure Databricks  

- **Cluster Setup:** Databricks cluster provisioned for data processing.  
- **Data Lake Integration:** Connected to Azure Storage.  

**Transformations performed:**  
- Normalized date formats.  
- Cleaned/filtered invalid records.  
- Grouped and concatenated data for usability.  

Output stored in **silver container** in **Parquet format** for efficient querying.  

![Databricks Transformation](image)  
![Silver Data Lake](image)  

---

## 📊 Step 4: Data Warehousing with Azure Synapse Analytics  

- **Connected to Silver Container** for direct queries.  
- **Serverless SQL Pools** enabled for cost-efficient querying.  
- **Database & Schema Setup:** External tables and views created for BI use.  

![Synapse SQL](image)  
![Data Models](image)  

The curated data was finally stored in the **gold container** for BI consumption.  

![Gold Data Lake](image)  

---

## 🕵️‍♂️ Step 5: Business Intelligence with Power BI  

- Connected **Power BI** to **Azure Synapse Analytics**.  
- Designed **dashboards & reports** to present actionable insights.  

![Power BI Dashboard](image)  

---

## 🌐 Key Takeaways  

✅ **Automation:** End-to-end data movement & orchestration.  
✅ **Scalability:** Handles large datasets efficiently.  
✅ **Efficiency:** Optimized with Parquet + serverless SQL pools.  
✅ **Insights:** BI dashboards for data-driven decision making.  

This project shows how modern businesses can **transform raw data into insights** using Azure’s ecosystem.  

---

## 🎉 Acknowledgment  

This project draws inspiration from an insightful repository by **[Ansh Lamba](https://github.com/anshlamba)**.  
For a detailed walkthrough, check out his **[YouTube channel](https://www.youtube.com/@anshlamba)**.  
Special thanks to Ansh for valuable resources and guidance for aspiring data engineers!  

---
