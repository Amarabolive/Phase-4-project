## Introduction
Motor vehicle crashes remain a significant public safety concern in many cities across the globe. Understanding the underlying causes of traffic accidents is essential for improving road safety, optimizing traffic regulations, and informing policy decisions. With the increasing availability of open data, machine learning offers powerful tools for discovering patterns and predicting outcomes that can lead to actionable insights.

This project uses publicly available crash, vehicle, and people datasets from the City of Chicago to develop a predictive model. The goal is to analyze a wide range of factors — including vehicle information, road conditions, and driver characteristics — to identify the primary contributory cause of each accident. By modeling this problem, we aim to support traffic safety stakeholders in better understanding crash dynamics and designing targeted interventions.

## Business Understanding
Motor vehicle accidents remain a persistent and costly public safety issue in urban centers. Every year, thousands of traffic accidents result in injuries, fatalities, and significant economic losses. Understanding the primary contributory causes of these crashes can help policymakers, urban planners, and safety boards implement targeted interventions to reduce accidents.

#### Objectives
Build a model that can predict the primary contributory cause of a car accident, given information about the car, the people in the car, the road conditions etc.

#### Key Questions
1. What are the most significant factors contributing to vehicle crashes in Chicago?
2. How do weather and lighting conditions impact accident causation patterns?
3. How do driver demographics (age, gender) correlate with accident causes?

## Data Understanding
This project uses three datasets published by City of Chicago (https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if)

* Traffic Crashes-Crashes Data: Shows information about each traffic crash on city streets within the City of Chicago
* Traffic Crashes-Driver/Passenger Data: Contains information about people involved in a crash and if any injuries were sustained
* Traffic Crashes- Vehicle Data: Contains information about vehicles involved in a traffic crash

## Project Structure
```
├── student.ipynb     # Main analysis notebook
├── README.md         # Project documentation
└── /data             # Source datasets
```
## Exploratory Data Analysis
1. Loaded and merged the three datasets.
2. Understanding the data by reviewing the structure, and checking for data types.
3. Identify missing data points (NULL or NaN values) and decided on how to handle them: remove, replace with default values, or use statistical methods (e.g., mean, median, mode).
4. Identify and remove duplicate records to reduce redundancy.
5. Removed columns that were not relevant to our analysis.
6. We did a univariate and multivariate analysis of the data.

## Modeling 
We used Logistic regression for our baseline model and Random Forest Classifier as the second model and thereafter used GridSearchCV to tune our hyperparameters.

## Prerequisites
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn

Modeling: LogisticRegression, RandomForestClassifier

Evaluation: classification_report, accuracy_score, confusion_matrix
## Instructions
- Clone the repository
- on bash
- Copy code
- git clone <https://github.com/Amarabolive/Phase-4-project>
- Run student.ipynb in Jupyter Notebook or any other compatible IDE.

## Conclusion

This project focused on predicting the **Primary Contributory Cause** of vehicle crashes using traffic accident data from Chicago. The workflow involved data preprocessing, exploratory analysis, model building, and hyperparameter tuning using Logistic Regression and Random Forest classifiers.

- The **Top 5 accident causes** were:
  - *Failing to Yield Right-of-Way*
  - *Following Too Closely*
  - *Improper Lane Usage*
  - *Failing to Reduce Speed to Avoid Crash*
  - *Improper Overtaking/Passing*

- **Model Performance**

| Model                | Accuracy | Key Notes |
|---------------------|----------|-----------|
| Logistic Regression (Tuned) | 27.8%   | Better recall for certain causes but low precision overall |
| Random Forest (Tuned)       | 33.3%   | Better balance across classes, but slight accuracy drop after tuning |

- Despite tuning, accuracy remained modest due to:
  - Class imbalance
  - Overlapping feature characteristics
  - Limited discriminative power of available features

## Recommendations

**Stakeholders**
* Driver-Focused Programs: Develop public awareness and training campaigns addressing top causes.
* Targeted interventions; Focus enforcement and road safety improvements on road signage.

**Data Team**
- Handle class imbalance using other techniques
- Try advanced models like **XGBoost** or **LightGBM**
- Evaluate using additional metrics (e.g., ROC AUC, confusion matrices)

While prediction accuracy is moderate, this project highlights how **machine learning** can uncover valuable **patterns in accident causation**, providing data-driven insights for **policy makers, road safety advocates**, and **urban planners** to mitigate crash risks and improve public safety.



