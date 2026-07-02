# Financial Transactions Data Warehouse & Fraud Analytics

An end-to-end Data Engineering and Business Intelligence project that builds a complete Data Warehouse for financial transactions and fraud analytics using the Microsoft BI Stack.

The project demonstrates the full data pipeline starting from raw CSV/JSON files, passing through ETL using SSIS, building a Star Schema Data Warehouse in SQL Server, creating a semantic model with SSAS Tabular, and finally delivering interactive Power BI dashboards.

---

## Project Architecture

Raw Files (CSV / JSON)
        │
        ▼
ODS Layer (Raw Data)
        │
        ▼
STG Layer (Data Cleansing & Transformation)
        │
        ▼
Data Warehouse (Star Schema)
        │
        ▼
SSAS Tabular Model
        │
        ▼
Power BI Dashboard

---

##  Data Sources

https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets?

The project uses five source files:

- Users.csv
- Cards.csv
- Transactions.csv
- TrainFraudLabel.json
- MCC.json

The dataset contains:

- Customer Information
- Payment Cards
- Financial Transactions
- Fraud Labels
- Merchant Category Codes (MCC)

---

##  Data Warehouse Design

### Fact Table

- FactTransactions

### Dimension Tables

- DimClients
- DimCards
- DimMerchant
- DimDate
- DimMCC
- DimFraud

The warehouse follows a **Star Schema** design to support high-performance analytical queries.

---

##  ETL Process (SSIS)

The ETL pipeline consists of three layers:

### 1. ODS Layer

- Import raw CSV & JSON files
- Preserve original data

### 2. Staging Layer

Data cleansing including:

- Trim spaces
- Data type conversion
- Currency cleaning
- ZIP code formatting
- Null handling
- Description cleaning
- Business transformations

### 3. Data Warehouse Layer

- Load dimension tables
- Generate surrogate keys
- Lookup transformations
- Load FactTransactions

---

##  SSAS Tabular Model

A semantic model was built using SQL Server Analysis Services (SSAS).

Features include:

- Relationships
- Calculated Columns
- DAX Measures
- Optimized reporting model

---

##  Power BI Dashboard

The dashboard contains six pages:

- Home
- Executive Overview
- Transactions Analysis
- Fraud Analysis
- Customer Analysis
- Cards Analysis

KPIs include:

- Total Transactions
- Transaction Amount
- Fraud Rate
- Fraud Amount
- Fraud Clients
- Fraud Cards
- Merchant Performance

---

##  Business Questions Answered

Examples include:

- Monthly transaction trends
- Fraud trends over time
- Fraud by merchant category
- Fraud by location
- Customer spending behavior
- Card performance
- Income vs Spending
- Fraud by Card Brand
- Merchant performance

---

## 🛠️ Technologies Used

- SQL Server
- SSIS
- SSAS Tabular
- Power BI
- DAX
- SQL

---

##  Repository Structure

```
Financial-Transactions-DWH/
│
├── Data/
│   ├── Users.csv
│   ├── Cards.csv
│   ├── Transactions.csv
│   ├── MCC.json
│   └── TrainFraudLabel.json
│
├── Database/
│   ├── Create Database.sql
│   ├── Star Schema.sql
│   └── Stored Procedures.sql
│
├── SSIS/
│   ├── ODS.dtsx
│   ├── STG.dtsx
│   └── DWH.dtsx
│
├── SSAS/
│
├── Power BI/
│   └── Financial Transactions.pbix
│
├── Images/
│
├── Documentation/
│   └── Project Documentation.pdf
│
└── README.md
```

---

##  Dashboard Preview

> Add dashboard screenshots inside the **Images** folder.

Example:

- Overview
- Transactions
- Fraud Analysis
- Clients
- Cards

---

##  Author

**Mohamed Saber**

Data Engineer | Data Analyst

LinkedIn:
https://www.linkedin.com/in/mohamed-saber-b0a1231b3/
