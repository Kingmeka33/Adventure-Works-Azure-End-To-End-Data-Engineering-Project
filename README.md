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
<img width="1910" height="822" alt="Image" src="https://github.com/user-attachments/assets/fa956e32-1b19-4665-a852-a10faee53904" />

---

## 🔄 Step 3: Data Transformation with Azure Databricks  

- **Cluster Setup:** Databricks cluster provisioned for data processing.  
- **Data Lake Integration:** Connected to Azure Storage.
  <img width="1913" height="866" alt="Image" src="https://github.com/user-attachments/assets/40d2ddb8-bafc-4093-adae-6b233b7e82e1" />

**Transformations performed:**  
- Normalized date formats.  
- Cleaned/filtered invalid records.  
- Grouped and concatenated data for usability.  

Output stored in **silver container** in **Parquet format** for efficient querying.  

<img width="1911" height="863" alt="Image" src="https://github.com/user-attachments/assets/8a610908-11b8-4a15-92a4-b08dde483ef5" />
<img width="1909" height="759" alt="Image" src="https://github.com/user-attachments/assets/23a2d1c3-ded5-49c4-9f0b-dce50a0ec1da" />
---

## 📊 Step 4: Data Warehousing with Azure Synapse Analytics  

- **Connected to Silver Container** for direct queries.  
- **Serverless SQL Pools** enabled for cost-efficient querying.  
- **Database & Schema Setup:** External tables and views created for BI use.  

<img width="1918" height="817" alt="Image" src="https://github.com/user-attachments/assets/8f33f031-022a-4a4d-a3ea-b78bef024469" />

<img width="1919" height="818" alt="Image" src="https://github.com/user-attachments/assets/f9382e4a-8649-4ff8-8ec4-d239789fa7c5" />



The curated data was finally stored in the **gold container** for BI consumption.  

<img width="1919" height="753" alt="Image" src="https://github.com/user-attachments/assets/2f2b2631-4293-4a9e-82d8-90394fb4c535" />

---

## 🕵️‍♂️ Step 5: Business Intelligence with Power BI  

- Connected **Power BI** to **Azure Synapse Analytics**.  
- Designed **dashboards & reports** to present actionable insights.  

<img width="1919" height="1017" alt="Image" src="https://github.com/user-attachments/assets/5f89de07-96de-422c-a374-9f8a085e253c" /> 

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
