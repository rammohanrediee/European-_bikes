# 🏍️ European Motorbike Price Prediction

This project uses machine learning models to predict the price of motorbikes based on real-world data from European listings.  
It demonstrates how to handle messy data, perform exploratory data analysis, and build a price prediction model.

---

## 📊 Dataset Overview
- **Source:** Web-scraped data from European motorbike listings  
- **Target Variable:** Price of the motorbike  
- **Key Features:**
  - `make_model`: The brand and model of the motorbike  
  - `mileage`: Total distance traveled  
  - `power`: Engine power  
  - `fuel`: Type of fuel (e.g., Gasoline, Electric)  
  - `gear`: Transmission type (e.g., Manual, Automatic)  
  - `offer_type`: Status of the listing (e.g., Used, Demonstration)  

---

## 📋 Table of Contents
1. [Data Cleaning & Preprocessing](#data-cleaning--preprocessing)  
2. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
3. [Model Building](#model-building)  
4. [Evaluation & Results](#evaluation--results)  
5. [Suggested Screenshots](#suggested-screenshots)  

---

## 🧹 Data Cleaning & Preprocessing

- **Handling Missing Values:**  
  Used `SimpleImputer` with:
  - Median strategy for numerical features  
  - Constant value (`'Unknown'`) for categorical features  

- **Outlier Treatment:**  
  - Extreme values in **price**, **mileage**, and **power**  
  - Capped at **1st and 99th percentiles**  

- **Feature Engineering:**  
  - Created `price_segment` feature:  
    - **Floor Market** (< €5000)  
    - **Budget Market** (> €5000)  

---

## 📈 Exploratory Data Analysis (EDA)

Explored distributions, correlations, and segmentations to understand the dataset better.

---

## 🤖 Model Building

Three regression models were trained and tuned using **RandomizedSearchCV**:

1. Random Forest Regressor  
2. Gradient Boosting Regressor  
3. CatBoost Regressor  

---

## 📊 Evaluation & Results

- Models were evaluated using:  
  - **Mean Absolute Error (MAE)**  
  - **R-squared (R²)**  

- The best-performing model was selected based on accuracy and consistency.



🚀 This project is a practical example of applying **data cleaning, EDA, feature engineering, and ML modeling** to real-world messy data.
