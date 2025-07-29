# Customer & Sales Data Pipeline on Azure

## Description
This project implements an end-to-end data engineering pipeline to extract customer and sales data from an on-premises SQL database, transform it in the Azure cloud, and deliver actionable KPIs through a Power BI dashboard. Key metrics include gender distribution and product category sales, with dynamic filters for date, category, and gender.

## Tech Stack
- On-Premises SQL Database  
- Azure Data Factory (ADF)  
- Azure Data Lake Storage Gen2 (ADLS Gen2)  
- Azure Databricks  
- Azure Synapse Analytics  
- Power BI  
- Azure Entra ID (Active Directory)  
- Azure Key Vault  

## Setup Instructions

1. **On-Premises Setup**  
   - Install and configure Self-hosted Integration Runtime (SHIR) on your on-premises server to enable secure ADF connectivity to your SQL database.

2. **Azure Resources Deployment**  
   - Provision Azure resources:  
     - Azure Data Factory  
     - Azure Data Lake Storage Gen2  
     - Azure Databricks workspace and clusters  
     - Azure Synapse Analytics workspace and SQL pools  
     - Azure Key Vault for secrets  
     - Configure Azure Entra ID for user and service access control.

3. **Configure Secret Management**  
   - Store database credentials and storage access keys securely in Azure Key Vault.  
   - Assign managed identities to Azure services and grant necessary Key Vault access policies.

4. **Data Ingestion Pipeline**  
   - Develop ADF pipelines using SHIR to extract incremental data from the on-premises SQL database into the raw zone of ADLS Gen2.

5. **Data Transformation**  
   - Use Databricks notebooks to clean, transform, and enrich raw data stored in ADLS Gen2.  
   - Store processed data in curated Delta Lake format within ADLS Gen2.

6. **Serving Layer Setup**  
   - Create external tables or load curated data into Azure Synapse Analytics SQL pools.  
   - Optimize data models and views for Power BI consumption.

7. **Power BI Dashboard**  
   - Connect Power BI to Synapse SQL pools.  
   - Build dashboards with KPIs on gender distribution and product category sales, incorporating filters for date, category, and gender.

8. **Monitoring and Alerts**  
   - Configure Azure Monitor and Log Analytics for pipeline and cluster health monitoring.  
   - Set up alerts for pipeline failures or performance issues.

## Usage Guide

- Trigger data ingestion pipelines in ADF manually or schedule them via triggers.  
- Run Databricks notebooks as scheduled jobs or triggered via ADF activities.  
- Use Power BI to access and interact with the dashboards for real-time business insights.  
- Monitor pipeline status and logs regularly via Azure portal.

## Contribution Guidelines

- Fork the repository and create feature branches for enhancements or fixes.  
- Follow coding standards and comment your code for clarity.  
- Test changes thoroughly in development before submitting pull requests.  
- Document new features or modifications in README or relevant docs.  
- Report issues or request features via GitHub Issues.

## License

NA
