# dp-203-LA03
Transform Data with Apache Spark in Azure Databricks
This project demonstrates how to transform data using Apache Spark in Azure Databricks, a cloud-based analytics platform built on Apache Spark and hosted on Microsoft Azure. The lab covers typical ETL steps like data ingestion, cleaning, transformation, and aggregation.

🚀 Lab Summary
This lab guides users through the following steps:

1. Provision Azure Databricks Workspace
A PowerShell script provisions a Premium-tier Azure Databricks workspace.

Script repository: mslearn-databricks

Script: setup.ps1

2. Create a Cluster
A single-node cluster was created with:

Runtime: 13.3 LTS (Spark 3.4.1, Scala 2.12)

Node type: Standard_D4ds_v5

Photon acceleration enabled

Auto termination after 20 minutes of inactivity

3. Create and Configure a Notebook
Notebook Name: Transform data with Spark

Connected to the created cluster

4. Ingest Data
Used shell commands to download .csv files from GitHub into /dbfs/spark_lab

Files include order data from 2019, 2020, and 2021

5. Define Schema and Load Data
Used pyspark.sql.types.StructType to define a custom schema

Loaded CSV data into a DataFrame

6. Clean the Data
Removed duplicate rows

Recalculated and type-casted the Tax column as float

7. Filter and Explore Data
Selected customer details

Counted total and distinct customers

Filtered customers who ordered a specific item (Road-250 Red, 52)

8. Aggregate and Group Data
Grouped by Item and calculated total quantity

Grouped by year of OrderDate to count orders

9. Use SQL in Databricks
Created a temporary view: salesorders

Ran SQL queries to calculate GrossRevenue per year using %sql magic

10. Clean Up
Terminated the compute cluster to avoid extra Azure costs

📂 Folder Structure
yaml
Kopyala
Düzenle
.
├── setup.ps1              # Script to provision Databricks workspace
├── TransformDataNotebook  # Notebook created in Azure Databricks
├── /spark_lab             # Directory containing CSV data files
│   ├── 2019.csv
│   ├── 2020.csv
│   └── 2021.csv
📌 Requirements
Microsoft Azure subscription with sufficient quota

Azure CLI or PowerShell

Basic familiarity with PySpark and SQL

🧠 Concepts Covered
Apache Spark dataframes

Data ingestion from cloud storage

Schema definition and data type casting

Deduplication and null value handling

Data aggregation and filtering

Using Spark SQL with %sql magic commands

ScreenShots:

![Screenshot 2025-04-22 at 15 02 05](https://github.com/user-attachments/assets/a25d44e8-1709-481d-a0fa-7aacba2cab4a)
![Screenshot 2025-04-22 at 15 00 56](https://github.com/user-attachments/assets/b19bab1a-4608-4b07-8f77-3990edcb6d4b)
![Screenshot 2025-04-22 at 14 59 44](https://github.com/user-attachments/assets/29311713-c3a2-4d45-ab0a-ca484e5cbdd7)
![Screenshot 2025-04-22 at 14 55 15](https://github.com/user-attachments/assets/9374713b-3e08-4c1b-b7f0-632ae641e3b4)

![Screenshot 2025-04-22 at 14 59 20](https://github.com/user-attachments/assets/e8b59056-4f72-46d5-8de4-880ac8cddf92)
![Screenshot 2025-04-22 at 14 55 09](https://github.com/user-attachments/assets/74c5b53f-88a4-4053-bcf3-bb66f9e24b41)
![Screenshot 2025-04-22 at 14 57 38](https://github.com/user-attachments/assets/ba76b539-41bd-469e-a474-bd353fbfa160)
![Screenshot 2025-04-22 at 14 54 45](https://github.com/user-attachments/assets/9d483a73-75ce-4c27-83d1-18f33147b663)

![Screenshot 2025-04-22 at 14 53 41](https://github.com/user-attachments/assets/2ac5db2f-33f2-45fb-893e-311fb1ed2ac0)
![Screenshot 2025-04-22 at 14 56 36](https://github.com/user-attachments/assets/f202cdae-64ff-482b-a3d4-2d420006a2d6)



✅ Completion
This lab was successfully completed. The notebook now contains examples of:

PySpark-based data transformation

SQL queries on Spark data

Data exploration techniques in Databricks
