Integrated Analytics with Azure Synapse End-to-End Analysis

![image](https://github.com/jaisbhavana/-Integrated-Analytics-with-Azure-Synapse-End-to-End-Project/blob/main/Olympic%20data%20flow.png)


**Tools Used in the Project** <br>
The tools covered in this project are: <br>

**Azure Data Factory
Azure Data Lake Storage Gen2
Azure Databricks
Azure Synapse Analytics
Azure Key Vault
Azure Active Directory (AAD)** <br>

Use Case
The project's use case involved building an end-to-end data solution that included the following steps:

**Data Ingestion:** <br>
Ingest tables from an on-premise SQL Server database using Azure Data Factory. This step required admin-level access to portal.azure.com and identifying the directory containing the Azure subscription.

**Data Storage:** <br>
Store the ingested data in Azure Data Lake Storage. This cloud-based storage solution allows for the storage and management of large volumes of structured and unstructured data.

**Data Transformation:** <br>
Utilize Azure Databricks to transform the raw data into a cleaner and more usable format. Databricks notebooks were used for data cleansing and enrichment.

**Data Loading:** <br>
Load the refined data into Azure Synapse Analytics (formerly SQL Data Warehouse). Azure Synapse Analytics provides a platform for large-scale data warehousing and analytics.

**Dashboard Creation:** <br>
Integrate Microsoft Power BI with Azure Synapse Analytics to create an interactive dashboard for data visualization and exploration.

**Monitoring and Governance:** <br>
Ensure proper governance and security by using Azure Active Directory (AAD) and Azure Key Vault.

**Permissions for Azure Synapse Analytics Workspace** <br>
To effectively use Azure Synapse Analytics for Integrated Data Analytics in the Azure subscription, the project required permissions as follows:

An Azure Synapse Analytics Workspace resource was provisioned.
Admin-level access to portal.azure.com was needed.
The directory containing the subscription was identified at the top right corner of the portal with the User ID. <br><br>


**Problem Statement 1: Data Exploration with Azure Synapse Analytics** <br><br>

The project began by exploring the data analytics workspace using Azure Synapse Analytics. Access to the following services was ensured:<br>

Azure Synapse Analytics, formerly SQL Data Warehouse, was introduced as a cloud-based analytics service designed for large-scale data warehousing and integration.<br>
Data was ingested into Azure Synapse through the Built-in copy task option.<br>
Data source type: All.<br>
A new connection was created with various configurations, including file format and destination settings.<br>
Task settings were specified. <br><br>

**Problem Statement 2: Azure Data Lake Storage Gen2 Exploration** <br>
Azure Data Lake Storage Gen2 (ADLS Gen2) was explored as a cloud-based data lake storage solution designed to store and manage large volumes of data. The exploration involved:

Navigating the Data hub to locate and analyze the data ingested into the Azure Synapse workspace.<br>
Executing SQL code to find the TOP 100 rows from the New SQL Script in the workspace.<br>
Addressing column name issues by modifying the SQL code.<br>
Updating the query to select specific columns for analysis.<br>
Configuring chart views for data visualization.<br> <br>

**Problem Statement 3: Data Analysis with Azure Synapse Analytics Spark Pool** <br> <br>
Azure Synapse Analytics Spark pool was introduced as a resource within Azure Synapse Analytics that provides an Apache Spark-based big data processing environment. The focus was on data analysis using Spark:
<br>
Creating a new Spark pool with specified settings.<br>
Creating a notebook to load data into a DataFrame using PySpark (Python) language.<br>
Executing code for data analysis. <br>
Applying similar chart view configurations used in the SQL pool for data visualization. <br>
The project leveraged these tools and methods to build an end-to-end data solution, demonstrating the capabilities of Azure services for data integration, transformation, analysis, and visualization. <br>

**Here is the PPT END TO END PROJECT:
[Microsoft Azure Project.pdf]**
(https://github.com/jaisbhavana/Azure_End_to_End_Project/files/12445575/Microsoft.Azure.Project.pdf)
