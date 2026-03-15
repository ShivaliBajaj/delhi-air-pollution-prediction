# Delhi Air Pollution Prediction (PM2.5)

## Project Overview

Air pollution is one of the most severe public health challenges in India.  
This project builds a machine learning pipeline to analyze historical air quality data and predict PM2.5 levels in Delhi.

The goal is to demonstrate how data science can support environmental health monitoring and early warning systems.

---

## Public Health Motivation

Fine particulate matter (PM2.5) penetrates deep into the lungs and bloodstream.

Long-term exposure is associated with:

• Cardiovascular disease  
• Respiratory illness  
• Reduced lung function  
• Increased mortality

Predictive models can help anticipate pollution spikes and support proactive public health interventions.

---

## Dataset

Historical air quality data for Delhi including:

• PM2.5 concentration  
• Temperature  
• Humidity  
• Wind speed  
• Other environmental indicators

Data sources include publicly available air quality datasets covering multiple years.

---

## Data Pipeline

1. Raw air quality data ingestion
2. Data cleaning and preprocessing
3. Exploratory data analysis
4. Feature engineering
5. Model training and evaluation

---

## Feature Engineering

Examples of engineered features:

• Lag features for previous pollution levels  
• Rolling averages  
• Seasonal indicators  
• Environmental variables

These features help the model capture temporal patterns in pollution dynamics.

---

## Machine Learning Model

Model used:

Random Forest Regressor

Why this model:

• Handles nonlinear relationships well  
• Robust to noisy environmental data  
• Performs well with tabular datasets

The trained model is saved in:

models/pm25_random_forest.pkl

---

## Results

The model learns relationships between meteorological conditions and pollution levels.

Evaluation metrics include:

• RMSE  
• R² score

These metrics indicate the model's ability to predict PM2.5 concentrations from environmental data.

---

## Public Health Insight

Exploratory analysis suggests pollution spikes tend to occur during winter months in Delhi.

Meteorological conditions such as lower wind speeds and temperature inversions may contribute to accumulation of particulate matter.

Machine learning models can assist in identifying patterns and forecasting risk periods.

---

## Project Structure

delhi-air-pollution-prediction

data
   raw
   processed

figures

models
   pm25_random_forest.pkl

notebooks
   01_data_cleaning_and_eda.ipynb
   02_feature_engineering.ipynb
   03_modeling_pm25_prediction.ipynb

src

README.md
requirements.txt