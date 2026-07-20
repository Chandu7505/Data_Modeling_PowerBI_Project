# 📊 Power BI Data Modeling Project

## 📖 Overview

This project focuses on transforming a large and complex dataset into a clean, efficient, and scalable Power BI data model. The objective is to build a well-structured star schema by identifying business entities, creating dimensions and fact tables, standardizing data, and optimizing the model for reporting and performance.

---
---

# 🖼️ Data Model Comparison

The following comparison shows how the original data model was transformed into a clean, optimized **Star Schema**.

<table>
<tr>
<td align="center"><b>Initial Data Model</b></td>
<td align="center"><b>Final Data Model</b></td>
</tr>

<tr>
<td>

<img width="1411" height="728" alt="Initial data Model" src="https://github.com/user-attachments/assets/a6e93a91-c65e-4d1e-8c10-6db3cf19e756" />


</td>

<td>

<img width="1712" height="732" alt="Final Data Model" src="https://github.com/user-attachments/assets/32043afa-60f6-4151-81d2-cce4c73116e8" />



</td>
</tr>
</table>

**Key Improvements**

- Simplified relationship structure
- Implemented a Star Schema design
- Built reusable dimension tables
- Optimized fact tables
- Improved model readability
- Enhanced query performance
- Reduced model complexity

---

# 🎯 Project Objectives

- Explore and understand the dataset before making changes.
- Identify business entities, facts, and dimensions.
- Build reusable dimension tables.
- Create optimized fact tables.
- Improve model performance by removing unnecessary data.
- Follow consistent naming conventions and modeling standards.
- Implement Row-Level Security (RLS).
- Build a scalable and maintainable Power BI data model.

---

# 🏗️ Data Modeling Process

The project follows four structured phases.

## Phase 1: Dataset Preparation & Exploration

Before modifying the data, the dataset is explored to understand:

- Business domain
- Business entities
- Facts and dimensions
- Relationships between tables
- Data quality

Understanding the dataset before making changes helps prevent modeling mistakes and ensures an accurate data model.

---

## Phase 2: Dimension Building

Every dimension is created using the same three-step approach.

### 1. Collect Tables

Identify all tables that describe the same business entity and group them together.

Example:

Customer
- Customer Master
- Customer Address
- Customer Contact

↓

One Customer Dimension

---

### 2. Combine Tables

Merge or append tables whenever necessary.

Typical transformations include:

- Merge tables
- Append tables
- Split columns
- Merge columns
- Remove duplicate records
- Drop unnecessary columns
- Remove unused tables

---

### 3. Clean and Standardize

Each dimension follows common standards.

#### Naming Standards

- Use `snake_case`
- Meaningful table names
- Meaningful column names
- Standard key names
- Friendly names for reporting

Example

```
customer_key
product_key
order_date
sales_amount
```

#### Data Cleaning

- Remove unnecessary columns
- Remove unused tables
- Standardize text capitalization
- Create surrogate keys when required
- Ensure every column has a business purpose

This improves:

- Model readability
- Storage efficiency
- Report performance
- Ease of maintenance

---

# 📈 Phase 3: Fact Table Development

Fact tables contain measurable business events.

To identify a fact table, ask:

> **"Where do the numbers come from?"**

Examples of measures:

- Sales
- Quantity
- Profit
- Cost
- Orders

A fact table stores measurements, while dimensions provide descriptive context.

---

## Modeling Principles

### Dimension

A dimension describes the business.

Examples:

- Customer
- Product
- Date
- Region
- Employee

### Fact

A fact records business events.

Examples:

- Sales
- Orders
- Shipments
- Transactions

> **A Dimension describes. A Fact grows.**

---

## Factless Fact Tables

A fact table can exist without numeric measures.

These are called **Factless Fact Tables**, where only business events are recorded.

---

## Junk Dimensions

Small, unrelated flags and indicators are grouped into a **Junk Dimension** to simplify the model.

---

## Data Validation

After every major transformation:

- Validate totals
- Verify row counts
- Compare source totals
- Confirm business metrics

This ensures the model remains accurate throughout development.

---

## Protect the Core Model

Only include the facts and dimensions required for reporting.

Avoid adding unnecessary tables because they can:

- Reduce performance
- Increase storage
- Complicate relationships
- Confuse report users

For special business requirements, create a separate model instead of modifying the core model.

---

# ✨ Phase 4: Model Polishing

Apply consistent modeling standards across the project.

## Naming Convention

### Tables

```
fact_sales
fact_orders

dim_customer
dim_product
dim_date
```

### Keys

```
customer_key
product_key
date_key
```

### Measures

```
Total Sales
Total Orders
Total Quantity
Average Price
Total Customers
```

---

# 📅 Date Dimension

A dedicated Date Dimension is created and connected to the appropriate fact tables.

This enables:

- Time Intelligence
- Year-over-Year Analysis
- Month-to-Date Reporting
- Quarter Analysis
- Trend Analysis

---

# 🔒 Row-Level Security (RLS)

The model includes Row-Level Security (RLS) to restrict data access based on user roles.

Security is applied only where required to avoid unnecessary complexity and preserve model performance.

Before deployment, security is validated by testing the model from the perspective of different users.

---

# ⚡ Performance Optimization

The model is optimized by:

- Removing unnecessary columns
- Removing unused tables
- Reducing model size
- Eliminating duplicate data
- Using clean relationships
- Building reusable dimensions
- Following star schema design

---

# 🛠️ Technologies Used

- Microsoft Power BI Desktop
- Power Query
- DAX
- Star Schema Modeling
- Row-Level Security (RLS)

---

# 📂 Project Structure

```
PowerBI-Data-Modeling/
│
├── Data/
│   └── raw_tables.xlsx
│
├── PowerBI/
│   └── Data_Modeling_PowerBI_Project.pbix
│
├── Images/
│   ├── Data_Model.png
│   └── Dashboard.png
│
└── README.md
```

---

# 📌 Key Features

- Structured Star Schema
- Optimized Dimension Tables
- Clean Fact Tables
- Standard Naming Convention
- Data Cleaning & Transformation
- Performance Optimization
- Date Dimension
- Reusable Measures
- Row-Level Security
- Business-Oriented Data Model

---

# 📄 Conclusion

This project demonstrates a complete end-to-end Power BI data modeling process, from understanding the raw data to building a clean, scalable, and secure analytical model. By following structured modeling practices, consistent naming conventions, and performance optimization techniques, the final model is easy to maintain, efficient for reporting, and suitable for future business growth.
