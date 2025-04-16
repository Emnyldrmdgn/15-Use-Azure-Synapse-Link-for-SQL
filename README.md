# 15-Use-Azure-Synapse-Link-for-SQL
Azure Synapse Link for SQL enables you to automatically synchronize a transactional database in SQL Server or Azure SQL Database with a dedicated SQL pool in Azure Synapse Analytics.

## 📘 Overview

This lab demonstrates how to use **Azure Synapse Link for SQL** to automatically synchronize a transactional database hosted in **Azure SQL Database** (or **SQL Server 2022**) with a **dedicated SQL pool** in **Azure Synapse Analytics**. This enables near real-time analytics on operational data without impacting the source system.

---

## 🧰 Prerequisites

- Active Azure Subscription
- Azure SQL Database (or SQL Server 2022+)
- Azure Synapse Analytics Workspace
- Dedicated SQL Pool created in Synapse
- Synapse Link feature enabled on the SQL source
- Access to Synapse Studio or Azure Data Studio

---

## 🛠️ Steps

### 1. Create an Azure SQL Database (Optional if already available)

- Go to Azure Portal → **SQL Databases** → **Create**
- Configure database and server settings
- (Optional) Use **AdventureWorksLT** sample data for testing

### 2. Create a Synapse Workspace and Dedicated SQL Pool

- In Azure Portal, go to **Azure Synapse Analytics** → **Create**
- Create a new **Dedicated SQL Pool (formerly SQL DW)**

### 3. Enable Azure Synapse Link

- Navigate to your Azure SQL Database
- Open the **Azure Synapse Link** blade
- Click **+ New Link**
- Select the Synapse Workspace and target Dedicated SQL Pool
- Choose the tables you want to replicate

### 4. Query Replicated Data in Synapse Studio

- Open **Synapse Studio**
- Go to the **Data** tab
- Expand the linked database to view synchronized tables
- Run sample queries:

``sql
SELECT TOP 100 * FROM [linked_db].[dbo].[YourTableName];


## Screenshots

![lab15](https://github.com/user-attachments/assets/d16c1b7c-9866-4e9d-b01c-c8785d6f0830)
![lab152](https://github.com/user-attachments/assets/de9e126e-94b8-4a1a-ae2f-f00b01075cb9)
![lab153](https://github.com/user-attachments/assets/a1e7eaf4-1a53-40cf-a952-c122062aa568)
![lab154](https://github.com/user-attachments/assets/00c4c53d-2138-4ccb-bcb9-5aff2a301397)

![lab155](https://github.com/user-attachments/assets/dda6c490-663a-4102-bcd5-dcb8ef1e2448)
