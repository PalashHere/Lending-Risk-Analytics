# Lending Risk Analytics Dashboard using Power BI & Azure

![image](https://github.com/user-attachments/assets/77cecd9d-446b-409a-a410-ca183f3f5dce)

## 🌐 Overview

This project presents an end-to-end Business Intelligence solution developed using the Lending Club loan dataset (2007-2015), containing ~890,000 loan records and 145 features. It enables data-driven decisions around borrower risk, loan performance, and regional trends.

The core objective was to transform raw lending data into actionable insights by building a scalable data pipeline with Python, Azure SQL Database, and Power BI.

## 🚀 Tech Stack

Data Processing: Python (Pandas, NumPy, SQLAlchemy)

Cloud Database: Azure SQL Database

BI Tool: Power BI (DAX, Power Query, Interactive Visuals)

Cloud Integration: pyodbc, sqlalchemy for Azure push

## 📅 Project Timeline

Raw Dataset Analysis

ETL & Sampling in Python

Cloud Database Setup (Azure SQL)

Data Modeling (Star Schema)

Data Visualization in Power BI

## 📊 Data Flow Architecture

CSV Dataset (~145 columns, 890K rows)
          ⬇️

Python (Data Cleaning, Sampling 20K rows from 2014-2018)
          ⬇️

Azure SQL (Push via SQLAlchemy)
          ⬇️

Power BI (DirectQuery Mode)
          ⬇️

Star Schema Modeling & DAX-based Visuals

## 🧱 Data Modeling: Star Schema

Fact Table:

FactLoan: Contains transactional loan data (amount, interest rate, status, DTI, etc.)

Dimension Tables:

DimDate: Derived from issue_d

DimPurpose: Loan purpose

DimState: Borrower's state

DimEmployment: Employment length

DimGrade: Grade and Subgrade

DimStatus: Loan status (e.g., Fully Paid, Charged Off)

## 📊 Key Visualizations & KPIs

KPIs:

✅ % Fully Paid Loans

❌ % Charged Off Loans

💰 Avg Loan Amount

🩸 Avg Interest Rate

✉️ Recovery Rate (Post Charge-offs)

🌍 Default % by State

## 📊 Data Cleaning Highlights

Dropped unused columns

Handled nulls in loan status & interest fields

Converted interest_rate, term, and revol_util to numeric

Extracted issue year to filter loans from 2014-2018

Sampled 20,000 rows randomly

## 🎓 Learning Outcomes

How to deploy an Azure SQL database for BI

How to clean and push large datasets using Python

How to model data into a star schema for Power BI

DAX functions for advanced KPI calculations

Best practices in dashboard UX (slicers, tooltips, navigation)

## 📢 Future Scope

Add ML-based loan default prediction module (post-PBI)

Deploy dashboard to Power BI Service

Integrate RLS (Row-Level Security) for investor segmentation

## ✨ Credits

Dataset: Lending Club - Kaggle

Inspired by multiple analytics dashboards, including Yat Shun Lee's Power BI case study

## 🙌 Let's Connect!

Feel free to fork, clone, and extend. Contributions welcome!

