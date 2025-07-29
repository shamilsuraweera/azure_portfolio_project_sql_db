# Customer & Sales Data Pipeline on Azure

A production-ready data engineering pipeline to ingest, transform, and visualize customer and sales data from an on-premises SQL database. The solution delivers actionable KPIs in a Power BI dashboard using a modern Azure data lakehouse architecture.

## 📦 Tech Stack
- On-Premises SQL Database
- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks
- Azure Synapse Analytics
- Power BI
- Entra ID (Azure Active Directory)
- Azure Key Vault

## ⚙️ Setup Instructions

1. **Provision Azure resources**  
   Deploy ADF, ADLS Gen2, Databricks, Synapse Analytics, Key Vault, and configure Entra ID.

2. **Configure connectivity**  
   - Install Self-hosted Integration Runtime (SHIR) to connect ADF securely to the on-premises SQL database.
   - Create linked services in ADF for source and sink connections.

3. **Set up secret management**  
   Store database credentials and keys in Azure Key Vault; configure managed identities for ADF and Databricks.

4. **Build data pipeline**  
   - Use ADF to copy raw data into the `/raw` layer in ADLS.
   - Develop Databricks notebooks to clean, transform, and aggregate data into `/cleansed` and `/curated` zones.

5. **Serve and visualize**  
   - Create Synapse SQL views over curated data.
   - Connect Power BI to Synapse to build dashboards with filters by date, product category, and gender.

## 🚀 Basic Usage
- Trigger the ADF pipeline to ingest fresh data.
- Run Databricks jobs to process and update curated datasets.
- Refresh the Power BI dashboard to view updated KPIs:
  - Gender distribution
  - Product category sales
  - Time-based trends

## 🤝 Contribution Guidelines
Contributions are welcome.  
Please fork the repository, create a new feature branch, and open a pull request.
