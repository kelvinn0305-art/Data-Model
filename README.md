# 📊 Data Modeler – Building a Normalized Star Schema Data Model

## 📌 Project Overview
This project demonstrates the creation of a **Normalized Star Schema Data Model** in **Power BI** using multiple dimension and fact tables.  
The objective is to understand relational modeling concepts such as:

- Table Relationships
- Cardinality
- Star Schema vs Snowflake Schema
- Inactive Relationships
- Data Hierarchies
- Cross Filter Directions
- Data Categories

---

# 🛠️ Tools Used

- Power BI Desktop
- Power Query
- Model View
- Matrix Visuals

---

# 📂 Dataset Overview

The project uses the following Excel files:

## 1️⃣ Sales_Fact.xlsx

### Columns
- SalesID (PK)
- CustomerID (FK)
- ProductID (FK)
- RegionID (FK)
- DateKey (FK)
- Quantity
- Revenue
- Discount

---

## 2️⃣ Customer_Dim.xlsx

### Columns
- CustomerID (PK)
- FullName
- Age
- Gender
- Segment

---

## 3️⃣ Product_Dim.xlsx

### Columns
- ProductID (PK)
- ProductName
- Category
- Subcategory
- Brand

---

## 4️⃣ Region_Dim.xlsx

### Columns
- RegionID (PK)
- Country
- State
- City

---

## 5️⃣ Date_Dim.xlsx

### Columns
- DateKey (PK)
- Date
- Month
- Quarter
- Year
- Fiscal Year

---

## 6️⃣ Returns_Fact.xlsx

### Columns
- ReturnID (PK)
- SalesID (FK to Sales_Fact)
- ReturnDateKey (FK)
- Reason

---

# 🔗 Relationships Created

| From Table | To Table | Relationship Type |
|------------|----------|-------------------|
| Sales_Fact | Customer_Dim | Many-to-One |
| Sales_Fact | Product_Dim | Many-to-One |
| Sales_Fact | Region_Dim | Many-to-One |
| Sales_Fact | Date_Dim | Many-to-One |
| Returns_Fact | Sales_Fact | Many-to-One |
| Returns_Fact | Date_Dim | Inactive Relationship |

---

# ⭐ Star Schema Design

The model follows a **Star Schema Architecture**:

- `Sales_Fact` acts as the central fact table
- Dimension tables surround the fact table
- `Returns_Fact` acts as a secondary fact table

---

# ❄️ Snowflake Schema Concept

Normalized dimensions were used to demonstrate Snowflake concepts where required.

Examples:
- Product Hierarchy
- Region Hierarchy

---

# ⚙️ Tasks Performed

## ✅ Data Import & Cleaning
- Imported data using Power Query
- Removed blank rows
- Applied proper data types
- Cleaned null values

---

## ✅ Relationship Management
- Created Primary Key & Foreign Key relationships manually
- Configured relationship cardinalities
- Used single-direction cross filtering

---

## ✅ Inactive Relationship
Created an inactive relationship:

Returns_Fact[ReturnDateKey] → Date_Dim[DateKey]

Used for return-date analysis scenarios.

---

## ✅ Data Model Enhancements

### Applied Data Formats
- Currency → Revenue
- Whole Number → Quantity
- Date → Date Columns

---

## ✅ Data Categories
Configured categories for:
- Country
- State
- City
- ProductName

---

# 🏗️ Hierarchies Created

## 📅 Date Hierarchy
Date_Dim:
- Year
- Quarter
- Month
- Date

---

## 🌍 Region Hierarchy
Region_Dim:
- Country
- State
- City

---

## 📦 Product Hierarchy
Product_Dim:
- Category
- Subcategory
- ProductName

---

# 📊 Verification Using Matrix Visual

Matrix tables were created to verify:

- Sales grouped by Product Category and Region
- Return reasons by Fiscal Year
- Revenue by Customer Segment

---

# 📚 Key Learnings

- Power Query Data Cleaning
- Fact & Dimension Table Design
- Relationship Cardinality
- Star Schema Modeling
- Snowflake Schema Concepts
- Handling Inactive Relationships
- Creating Hierarchies
- Optimizing Data Models

---

# 🚀 Conclusion

Successfully designed and implemented a scalable **Normalized Star Schema Data Model** in Power BI with:

✔ Proper relationships  
✔ Optimized filtering  
✔ Hierarchies  
✔ Inactive relationships  
✔ Verification visuals  

This project strengthens understanding of real-world Business Intelligence data modeling techniques.




