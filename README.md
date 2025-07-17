# 🛒 E-Commerce Invoice Prediction with Machine Learning

This project aims to predict the **total invoice amount** in an e-commerce dataset using various machine learning regression models. The dataset contains real-world transaction data from an online UK-based retail store.

## 📁 Dataset
- **Source**: [Kaggle - E-Commerce Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
- The dataset includes:
  - Invoice numbers and dates
  - Product descriptions and quantities
  - Unit prices
  - Customer and country info

## ⚙️ Project Workflow

### 1. Data Preprocessing
- Dropped missing values (`CustomerID`, `Description`)
- Converted date column to datetime format
- One-hot encoded the `Country` feature
- Created new features:
  - `TotalPrice = Quantity × UnitPrice`
  - Temporal features: `Year`, `Month`, `Day`, `Hour`, `Weekday`
  - Aggregated features: `TotalProductQuantity`, `TotalInvoiceQuantity`, `TotalInvoicePrice`

### 2. Models Applied
- `Linear Regression`
- `Random Forest Regressor`
- `XGBoost Regressor`
- `LightGBM Regressor`

### 3. Evaluation Metrics
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**

## 📊 Results

| Model                  | R² Score | MAE    | MSE      |
|------------------------|----------|--------|----------|
| Linear Regression      | 0.74     | 633.85 | 1.33M    |
| Random Forest Regressor| 0.99     | 39.97  | 27.4K    |
| XGBoost Regressor      | 0.96     | 229.65 | 190K     |
| LightGBM Regressor     | 0.96     | 219.52 | 193K     |

✅ **Random Forest Regressor** outperformed the others with over 99% accuracy.

