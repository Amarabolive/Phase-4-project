# Phase-4-project
This is end of phase project on model interpretability
Model Interpretability
This project explores the interpretability of a machine learning classification model trained on a dataset related to traffic crashes in the City of Chicago. The main goal is to understand how the model makes predictions and what features contribute most to the outcome, with a focus on predicting the primary contributory cause of traffic crashes.

## Key Objectives
Train a machine learning model on crash-related features.

Predict the Primary Contributory Cause of each traffic crash.

Use model interpretability tools to understand the influence of various features.
                                                     
## Data Sources
- **Traffic Crashes - Crashes**
- **Traffic Crashes - Vehicles**
- **Traffic Crashes - People**
Dataset: Assumes the use of the Chicago Traffic Crashes dataset (available from the City of Chicago open data portal).

## Project Structure
Notebook: student.ipynb
This is the main Jupyter notebook that walks through data preprocessing, model training, and interpretability analysis

## Tools & Libraries
pandas, numpy – Data manipulation

scikit-learn – Machine learning modeling

matplotlib, seaborn – Data visualization

shap – SHAP (SHapley Additive exPlanations) for interpreting model predictions

## Steps Performed

### Data Processing
#Import the necessary packages

### Data Merging and Preparation
crashes dataset

### Data Cleaning and Feature Engineering
(Numeric columns)

### Model Development
- Logistic Regression
- Random Forest Classifier

### Evaluation Metrics
- Accuracy: ~30.6%
- Confusion Matrix: Visualized with heatmaps
- Classification Report: Precision, Recall, and F1-Score for top 5 crash causes

## Top 5 Most Frequent Crash Causes
- Unable to Determine
- Failing to Yield Right-of-Way
- Following Too Closely
- Improper Overtaking/Passing
- Failing to Reduce Speed to Avoid Crash

## Key Takeaways
- Models are more effective at identifying general patterns than specific crash causes.
- “Unable to Determine” is a dominant but vague category.
- Random Forest and Logistic Regression performed similarly.

## Project Structure
```
├── student.ipynb     # Main analysis notebook
├── README.md         # Project documentation
└── /data             # Source datasets
```
## Authors & License
This project is based on public data provided by the City of Chicago.
