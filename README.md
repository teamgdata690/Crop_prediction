#  Crop Recommendation System for Improving Crop Yeild

##  Project Overview

This project aims to build a machine learning pipeline to:
1. **Classify soil nutrient levels** to assess soil health.
2. **Predict crop yield** using regression models based on soil conditions.

The goal is to support data-driven decision-making for farmers, agronomists, and agricultural planners by providing accurate predictions and soil recommendations.

---

##  Data Sources

The project uses a combination of soil and crop datasets from global and national sources:

- **USDA Crop Data** – [https://www.nass.usda.gov/Data_and_Statistics/](https://www.nass.usda.gov/Data_and_Statistics/)
- **USDA Soil Survey** - [https://websoilsurvey.sc.egov.usda.gov/app/](https://websoilsurvey.sc.egov.usda.gov/app/)


Data includes:
- Soil characteristics (State, Year, pH, organic matter, texture, etc.)
- Crop information (State, Year, crop type, yield, etc.)

---

##  Methods

###  Data Cleaning & Preprocessing
- Removed nulls and outliers using **IQR-based** and later **group-based imputation** methods.
- Standardized column names and units across multiple datasets.
- Created new features such as **soil fertility class** and **soil texture** based on thresholds.

###  Exploratory Data Analysis (EDA)
- Distribution plots, heatmaps, line charts, and boxplots to identify trends and relationships.
- Fertility and texture classification based on scientific thresholds.
- Regional and crop-wise yield comparison.

###  Machine Learning Models

#### 1. **Soil Nutrient Classification (Classification)**
- Random Forest Classifier
- XGBoost Classifier

#### 2. **Crop Yield Prediction (Regression)**
- Random Forest Regressor
- XGBoost Regressor
- Evaluation using RMSE, and R² Score

---

##  Key Results

| Task                        | Best Model         | R² Score / Accuracy | Key Features                      |
|----------------------------|--------------------|---------------------|-----------------------------------|
| Soil Nutrient Classification | Random Forest  classifier    | 100%                 | Soil texture               |
| Soil Nutrient Classification | XGB  classifier    | 83%                 | Soil Fertility           |
| Crop Yield Prediction       | XGB Regressor  | 94.5 (R²)             | Crop Yeild     |
| Crop Yeild Prediction       | Random Forest Regressor | 95.4 (R²)    | Crop Yeild                   |


