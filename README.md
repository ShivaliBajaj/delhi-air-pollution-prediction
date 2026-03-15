# Delhi Air Pollution Prediction (PM2.5)

## Clinical Intelligence Context

Air pollution is strongly associated with respiratory diseases including asthma, COPD, and cardiovascular complications.

This project applies machine learning to model PM2.5 levels using environmental and pollution indicators in Delhi. The objective is to demonstrate how predictive analytics can support environmental health monitoring and population-level risk awareness.

Such predictive systems can assist public health researchers, policymakers, and healthcare analysts in identifying patterns that contribute to respiratory disease risk.

## Project Overview

Air pollution is one of the most severe public health challenges in India.  
This project builds a machine learning pipeline to analyze historical air quality data and predict PM2.5 levels in Delhi.

The goal is to demonstrate how data science can support environmental health monitoring and early warning systems.

## Project Architecture

The workflow follows a structured machine learning pipeline:

1. Data Collection  
   - Delhi air pollution dataset with meteorological and pollutant indicators

2. Data Cleaning & Preprocessing  
   - Handling missing values  
   - Data normalization and preparation

3. Feature Engineering  
   - Selection of environmental and pollutant variables relevant to PM2.5

4. Model Development  
   - Linear Regression  
   - Decision Tree Regressor  
   - Random Forest Regressor

5. Model Evaluation  
   - Comparison of predicted vs actual PM2.5 levels  
   - Visualization of model performance

6. Model Interpretation  
   - Feature importance analysis to identify dominant pollution drivers

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

## Model Performance

Three regression models were evaluated for PM2.5 prediction:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

The Random Forest model performed best.

**Evaluation Metrics (Random Forest):**

- RMSE: 17.05
- MAE: 11.95
- R² Score: 0.99

These results indicate that the model captures the majority of variance in PM2.5 levels and can effectively model complex relationships between meteorological variables and pollution indicators.

## Public Health Insight

Air pollution is a major public health concern in large urban environments such as Delhi.

Feature importance analysis indicates that particulate indicators such as PM10 have the strongest influence on PM2.5 levels, while gaseous pollutants like NO₂ and SO₂ contribute secondary signals.

This suggests that particulate emissions remain a dominant driver of urban air-quality deterioration and highlights the importance of monitoring particulate matter to assess respiratory health risks.

## Visual Insights

### Random Forest Predictions vs Actual PM2.5

![Prediction Plot](figures/prediction_vs_actual.png)

This visualization compares the predicted PM2.5 levels from the Random Forest model against the actual observed values.

---

### Feature Importance

![Feature Importance](figures/feature_importance.png)

Feature importance analysis highlights which environmental variables contribute most strongly to PM2.5 prediction.

## Future Applications

This project demonstrates how environmental data can be integrated with predictive modeling to support health-focused analytics.

Potential extensions include:

- Integrating hospital admission data for respiratory illnesses
- Building early-warning systems for high pollution days
- Developing dashboards for environmental health monitoring
- Linking pollution patterns with long-term respiratory disease trends