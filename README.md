# Phase-4-project
This is end of phase project on model interpretability
Model Interpretability
This project explores the interpretability of a machine learning classification model trained on a dataset related to traffic crashes in the City of Chicago. The main goal is to understand how the model makes predictions and what features contribute most to the outcome, with a focus on predicting the primary contributory cause of traffic crashes.

## 📁 Project Structure
Notebook: student.ipynb
This is the main Jupyter notebook that walks through data preprocessing, model training, and interpretability analysis.

Dataset: Assumes the use of the Chicago Traffic Crashes dataset (available from the City of Chicago open data portal).

## 🚀 Key Objectives
Train a machine learning model on crash-related features.

Predict the Primary Contributory Cause of each traffic crash.

Use model interpretability tools to understand the influence of various features.

## 🛠️ Tools & Libraries
pandas, numpy – Data manipulation

scikit-learn – Machine learning modeling

matplotlib, seaborn – Data visualization

shap – SHAP (SHapley Additive exPlanations) for interpreting model predictions

## 🔍 Features Used
Crash-level attributes: CRASH_HOUR, CRASH_DAY_OF_WEEK, POSTED_SPEED_LIMIT, etc.

Environmental factors: LIGHTING_CONDITION, WEATHER_CONDITION, ROADWAY_SURFACE_COND

Location context: TRAFFIC_CONTROL_DEVICE, PRIM_CONTRIBUTORY_CAUSE, etc.

## 🧠 Model Training
A RandomForestClassifier is trained on labeled crash data.

Label encoding is used for categorical variables.

The model is evaluated using accuracy and a classification report.

## 🔎 Model Interpretability
Feature Importance is evaluated using both the Random Forest's built-in importance and SHAP values.

SHAP Summary Plots show how each feature impacts the model's predictions.

Helps decision-makers understand which crash attributes most strongly predict different contributory causes.

## 📊 Results Summary
The model achieves reasonable performance but highlights the complex nature of attributing crash causes.

SHAP visualizations identify top contributing features like LIGHTING_CONDITION, POSTED_SPEED_LIMIT, and TRAFFIC_CONTROL_DEVICE.

## 📌 How to Use
Install required packages:

bash
Copy
Edit
pip install pandas numpy scikit-learn matplotlib seaborn shap
Open the notebook:

bash
Copy
Edit
jupyter notebook "Model Interpretability.ipynb"
Execute cells sequentially for a full analysis pipeline.

## 📚 References
City of Chicago Traffic Crash Data
