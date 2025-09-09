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
    - **Recency:** days since last purchase
    - **Frequency:** number of unique invoices
    - **Monetary:** total spend
3. **Preprocesing**
    - Applied log-transform to reduce skewness
    - Standardized features using `StandardScaler`
4. **Clustering**
    - Used **Elbow Method** and **Silhouette** Score to test cluster counts
    - Fit KMeans clustering for **k = 3 and k = 4**
    - Compared profiles to choose the most actionable segmentation

## 📈 Results & Insights
- **Cluster Profiles (k = 3)**
    | Cluster  | Persona | Characteristic  | Suggested Action |
    | ------------- | ------------- | ------------- | ------------- |
    | 0  | Regular Shoppers  | Recency ~46 days, 3–4 orders, ~$1.4k spend  | Upsell with bundles or seasonal campaigns  |
    | 1  | VIP / Loyal High-Value  | Very recent (~13 days), 14 orders, ~$8k spend  | Reward with loyalty perks, exclusive offers  |
    | 2  | At-Risk / Dormant  | Long inactive (~161 days), ~1 order, ~$350 spend  | Win-back discounts, targeted reactivation  |
- **Cluster Profiles (k = 4)**

## 💡 Business Implications
- **VIPs →** loyalty perks, exclusive rewards
- **Regular Shoppers →** upsell and seasonal offers
- **At-Risk Customers →** win-back campaigns
- **New Customers →** onboarding and engagement

## ⚖️ Limitations & Next Steps
- KMeans assumes spherical clusters; alternative methods (DBSCAN, hierarchical) could reveal different patterns
- RFM ignores product categories; future work could add **product-level or seasonality features**
- Deploying a **Streamlit app** or **Tableau dashboard** would make this segmentation interactive for business users

## 🛠️ Tech Stack
- **Python:** pandas, numpy, scikit-learn, seaborn, matplotlib
- **Clustering:** KMeans
- **Visualization:** seaborn, matplotlib
