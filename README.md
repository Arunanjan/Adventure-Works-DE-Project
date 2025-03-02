# Adventure-Sales-DE-Project

# End-to-End Azure Data Engineering Project

# Abstract
This project illustrates the creation of a comprehensive data engineering pipeline using Azure technologies, including Azure Data Factory, Databricks, PySpark, and Azure Synapse Analytics. The focus is on ingesting data from APIs, processing and transforming it with Databricks and PySpark, and storing it in a structured data warehouse. The processed data is then made available for analysis and visualization. This document provides a detailed explanation of the architecture, technologies, and implementation of the project.

# 1. Introduction
Data engineering plays a pivotal role in data-driven organizations, ensuring seamless data flow, transformation, and storage. This project demonstrates a real-world example of constructing a data pipeline on the Azure platform. It follows the Medallion Architecture (Bronze, Silver, Gold layers) to manage and enhance data for analytics.

# 2. Project Architecture
The architecture of this project is organized into the following components:

Data Ingestion: Data is extracted from APIs using Azure Data Factory.
Storage: Raw data is stored in Azure Data Lake Storage Gen2 (Bronze Layer).
Data Processing: Data is cleaned and transformed using Azure Databricks and PySpark (Silver Layer).
Data Warehousing: The transformed data is loaded into Azure Synapse Analytics (Gold Layer).
Visualization: Power BI connects to Synapse Analytics to create interactive dashboards.

# 3. Technologies Used

Azure Data Factory: Orchestration and ETL tasks.
Azure Data Lake Storage Gen2: Raw data storage.
Azure Databricks & PySpark: Data cleaning and transformation.
Azure Synapse Analytics: Data warehousing and SQL analytics.
Power BI: Data visualization.

# 4. Step-by-Step Resource Creation

# 4.1 Creating a Resource Group

Navigate to the Azure Portal.
Select Create a Resource, then choose Resource Group.
Provide a unique name for the Resource Group.
Choose a Region close to your location.
Click Review + Create, then Create.

# 4.2 Creating an Azure Data Lake Storage Gen2 Account

Go to the Azure Portal and click Create a Resource.
Search for Storage Account and select Create.
Choose the previously created Resource Group.
Provide a unique name for the Storage Account.
Select the appropriate Region and set Standard performance.
In Advanced settings, enable Hierarchical Namespace for Data Lake Gen2 support.
Click Review + Create, then Create.

# 4.3 Creating Azure Data Factory

In the Azure Portal, select Create a Resource.
Search for Data Factory and click Create.
Choose the Resource Group.
Provide a name for the Data Factory.
Select a Region and leave other settings as default.
Click Review + Create, then Create.

# 4.4 Creating an Azure Databricks Workspace

In the Azure Portal, select Create a Resource.
Search for Azure Databricks and click Create.
Choose your Resource Group and provide a Workspace Name.
Select a Pricing Tier (Standard/Premium).
Click Review + Create, then Create.

# 4.5 Creating an Azure Synapse Analytics Workspace

In the Azure Portal, select Create a Resource.
Search for Azure Synapse Analytics and click Create.
Choose your Resource Group and provide a Workspace Name.
Select a Storage Account for data storage.
Enable Managed Virtual Network for enhanced security.
Click Review + Create, then Create.
4.6 Setting Up Power BI for Visualization

# Open Power BI Desktop.
Select Get Data and choose Azure Synapse Analytics.
Enter the SQL Server Name from your Synapse workspace.
Select the desired database and tables.
Load the data and begin building your visualizations.

# 5. Data Ingestion & Processing
Data is fetched from an API hosted on GitHub, containing structured CSV files. The ingestion process includes:

Extracting the data from the API using Azure Data Factory (ADF) and an HTTP connector.
Storing raw data in the Bronze Layer (Azure Data Lake Storage Gen2).
Creating linked services in ADF to establish connections between the API and storage.
# 6. ETL Pipelines with Azure Data Factory
The ETL pipeline involves the following steps:

Copy Activity: Extracts data from the API and stores it in the Bronze Layer.
Transformation Activity: Uses Databricks to clean and process the data.
Data Movement Activity: Loads the processed data into Azure Synapse Analytics.
# 7. Data Transformation using Databricks & PySpark
Data transformation involves:

Removing duplicates and null values.
Standardizing data formats.
Aggregating key data fields.
Applying business logic for deeper analytics.

# 8. Data Warehousing in Azure Synapse Analytics

The refined data is loaded into tables within Synapse Analytics.
Fact and dimension tables are set up to optimize query performance.
SQL queries are employed to fine-tune data retrieval.
#  9. Data Visualization using Power BI
Power BI is connected to Azure Synapse Analytics to create visual reports. Key steps include:

Establishing a connection between Power BI and Synapse.
Designing dashboards for insights on sales and customer data.
Adding dynamic filters and interactive elements for improved user experience.

# 10. Conclusion
This project showcases the development of an Azure-based data engineering solution. By integrating Azure Data Factory, Databricks, and Synapse Analytics, the project highlights the creation of a scalable, efficient, and production-ready data pipeline for analytics.
