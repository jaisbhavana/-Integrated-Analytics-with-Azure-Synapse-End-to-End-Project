                                                  Integrated Analytics with Azure Synapse End-to-End Analysis




The tools that are covered in this project are: 

1. Azure Data Factory 
2. Azure Data Lake Storage Gen2 
3. Azure Databricks 
4. Azure Synapse Analytics 
5. Azure Key vault 
6. Azure Active Directory (AAD) and

The use case for this project involved building an end-to-end solution by ingesting tables from an on-premise SQL Server database using Azure Data Factory. The data was then stored in Azure Data Lake. We utilized Azure Databricks to transform the raw data into a cleaner format. After that, Azure Synapse Analytics was used to load the refined data. Finally, Microsoft Power BI was integrated with Azure Synapse Analytics to create an interactive dashboard. For monitoring and governance, Azure Active Directory (AAD) and Azure Key Vault were used.

Give Permission for Azure Synapse Analytics workspace

 

                                                                   
 

In this project, we covered the following tools:
Permissions were granted for the Azure Synapse Analytics workspace as follows:

To utilize Azure Synapse Analytics for Integrated Data Analytics in the Azure subscription, an Azure Synapse Analytics Workspace resource was provisioned. Admin-level access to portal.azure.com was required. The directory containing the subscription was identified at the top right corner of the portal with the User ID.




                                                                          Problem Statement 1:

The task involved exploring the data analytics workspace using Azure Synapse Analytics. Prior to commencing work, access to the following services was ensured:

Azure Synapse Analytics, formerly SQL Data Warehouse, is a cloud-based analytics service offered by Microsoft Azure. It combines enterprise data warehousing and Big Data analytics into a single integrated platform. It's designed to handle large-scale data warehousing and integration, allowing organizations to analyze and gain insights from vast amounts of data.

Data was ingested into Azure Synapse through the Built-in copy task option, with 'run once now' selected. The following steps were completed to ingest data and query the uploaded data:

Source type: All
A new connection was created with the following inputs:
Name: Any name
Description: Dependent on the given name
Connect via integration runtime
Base URL Data link for the workspace
Source Dataset:

https://raw.githubusercontent.com/MicrosoftLearning/DP-900T00A-Azure-Data-Fundamentals/master/Azure-Synapse/products.csv

Server certificate validation was enabled
Anonymous Authentication type was selected
Default settings were maintained in various configurations, including File format as Delimited text, column delimiter as Comma (,), Row Delimiter as Line feed (\n), First row as header as Selected, and Compression type as none. The destination type was set to ADLS Gen 2, utilizing the existing storage account created on the Azure portal during workspace configuration.

Before commencing work, the following settings were ensured:

Task name: Any given name
Task Description: Aligned with the task name
Fault tolerance: Default
Enable logging: Unchecked
Enable staging: Unchecked



                                                                              Problem Statement 2:
                                                                              
Azure Data Lake Storage Gen2 (ADLS Gen2) is a cloud-based data lake storage solution provided by Microsoft Azure. It is designed to store and manage large volumes of data, including structured, semi-structured, and unstructured data, with enhanced performance, scalability, and security features.


Exploration of the Data hub involved clicking on linked to expand ADLS Gen2 and locating the xyz.csv files on the page. The data ingested into the Azure Synapse workspace was analyzed and queried using SQL code.

The objective was to find the TOP 100 rows from the New SQL Script in the workspace. Before running the code, the connection was set to built-in, with the database as master. The code was executed, and the result datasets were examined.

A column name issue was identified, displaying column names as c1, c2, c3, and c4. To resolve this, "HEADER_ROW = TRUE" was added to the code before "AS [result]," and the code was rerun, resulting in corrected column names. The query was then updated to select the category and count as ProductNumbers. The properties of SQL Script 1 were updated to reflect this change, and the modified code was published.

In the Develop hub, the published code was selected, and it was ensured that it was set as Built-in SQL pool. The code was run again to access the total number of products. Changes were made to the chart view:

Chart type: Column
Category Column: Category
Legend (series) columns: Number of products (or custom name)
Legend position: Bottom-center
Legend (series) label: Blank
Legend (series) minimum value: Blank
Legend (series) maximum value: Blank
Category label: Blank



                                                                      Problem Statement 3:
An Azure Synapse Analytics Spark pool is a resource within the Azure Synapse Analytics service that provides an Apache Spark-based big data processing environment. It allows you to perform advanced data processing, analytics, and machine learning tasks on large datasets using the power of Spark, a widely used open-source data processing and analytics engine.                                                                      

Data analysis using the Spark pool was the focus. SQL is commonly used for structured datasets, but languages like Python are effective for data analysis.


Moving to the Manage hub, the Apache Spark pool was selected. A new Spark pool was created with the following inputs:

Apache Spark pool name: Any chosen name
Node Size Family: Default
Node Size: Default
Autoscale: Enabled
Number of nodes: 3-5
In the Synapse workspace, xyz.csv was right-clicked, and a new notebook was created. The notebook was set to load into a DataFrame using PySpark (Python) language. The code was executed, generating a dataset similar to previous operations in the SQL pool. However, this time, Python syntax utilizing the Spark pool was used.

The chart view was accessed, and the same commands applied in the SQL pool were repeated.



Here is the PPT END TO END PROJECT:
[Microsoft Azure Project.pdf]
(https://github.com/jaisbhavana/Azure_End_to_End_Project/files/12445575/Microsoft.Azure.Project.pdf)
