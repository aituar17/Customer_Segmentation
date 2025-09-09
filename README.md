# 🛒 Customer_Segmentation with RFM and KMeans

## 📌 Project Overview
This project applies RFM (Recency, Frequency, Monetary) analysis and KMeans clustering to segment customers of an online retail store. The goal is to help the business design targeted marketing strategies and improve customer retention by identifying distinct customer personas.

## 📊 Dataset
- **Source:** [Kaggle E-commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
- **Period:** Dec 2010 – Dec 2011
- **Size:** ~540,000 rows, 8 variables
- **Key Fields:**
  - `InvoiceNo` - transaction number
  - `CustomerID` - unique customer ID
  - `InvoiceDate` - date of purchase
  - `Quantity` - number of items purchased
  - `UnitPrice` - price per item
  - `Country` - customer’s country

## 🛠️ Methodology
1. **Data Cleaning**
   - Removed missing `CustomerID` values
   - Excluded cancelled orders (`InvoiceNo` starting with “C”)
   - Kept only positive `Quantity` and `UnitPrice`
   - Created `TotalPrice = Quantity × UnitPrice`
2. **Feature Engineering (RFM)**
   - 
4. **Preprocesing**
5. **Clustering**



