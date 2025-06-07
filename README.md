# Laptop Price Prediction using Regression

![Domain](https://img.shields.io/badge/Domain-Technology-blue?style=for-the-badge)  
![Tech](https://img.shields.io/badge/Tech-Python%20%7C%20Sklearn%20%7C%20EDA-green?style=for-the-badge)  
![Project Type](https://img.shields.io/badge/Type-Machine%20Learning-yellow?style=for-the-badge)

---

##  Overview

This project uses machine learning regression techniques to predict laptop prices based on features like brand, type, CPU, GPU, screen characteristics, RAM, storage type, weight, and operating system. The analysis includes feature engineering, data cleaning, exploratory data analysis, and model building using linear, ridge, and lasso regression.

The dataset used for this project was sourced from Kaggle and consists of synthetic pricing data for over 1,200 laptops.

---

##  Objectives

- Understand how different specifications affect laptop pricing.
- Engineer meaningful features from raw data (like PPI, touchscreen, memory type).
- Build a regression model that accurately predicts laptop prices.

---

##  Technologies Used

- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn (LinearRegression, Ridge, Lasso, GridSearchCV)
- Jupyter Notebook (Kaggle environment)

---

##  Key Steps

### 1. Data Preprocessing
- Removed duplicates and nulls
- Converted units (e.g., RAM from "8GB" to integer)
- Created binary flags for touchscreen, IPS panel, and storage types
- Parsed and engineered new features like screen resolution and PPI

### 2. Exploratory Data Analysis (EDA)
- Analyzed price distribution (log transformation used for skew)
- Visualized categorical features vs price (brand, CPU, GPU, type, OS)
- Found positive correlations of price with SSD size, RAM, PPI, etc.

### 3. Feature Engineering
- Extracted processor types from full CPU descriptions
- Aggregated SSD, HDD, Flash, and Hybrid storage from memory column
- Categorized GPU vendors and OS types

### 4. Model Building
- Split data into training and testing sets (85/15)
- Trained Linear, Ridge, and Lasso regression models
- Performed 10-fold cross-validation

### 5. Model Evaluation
- **Best Model**: Lasso Regression with alpha=0.0001  
- **R² Score**: 0.8246  
- **MAE**: 0.2116 (on log-transformed prices)

---

##  Insights

- **8GB RAM**, **256GB SSD**, **Intel Core i7**, and **non-touchscreen notebooks** are the most popular affordable configurations.
- **Dell** and **Lenovo** dominate lower price ranges, while **Apple** leads high-end pricing.
- **Touchscreen** and **IPS Panel** displays significantly increase price.

---

##  Conclusion

This project demonstrates a complete pipeline from raw data to predictive modeling using regression. Feature engineering and categorical handling played a crucial role in improving model accuracy. The code is modular and ready for extension to include more advanced models like Random Forest or XGBoost.

---

 *This project was built in Python 3 using Jupyter Notebooks on Kaggle and follows best practices in data preprocessing, feature engineering, visualization, and modeling.*
