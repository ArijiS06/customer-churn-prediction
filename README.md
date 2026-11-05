# Customer Churn Prediction & Retention Analytics

### Python | Machine Learning | Data Analytics

## Project Overview

This project applies machine learning to predict customer churn in the telecommunications industry. Using a dataset containing 7,043 customer records, I analysed customer behaviour, developed predictive classification models and investigated how churn risk estimates could support customer retention decisions.

The project demonstrates an end to end data science workflow, combining data cleaning, exploratory analysis, feature engineering, machine learning and business analytics.

## Business Problem

Customer churn occurs when customers discontinue their relationship with a company, resulting in potential lost revenue.

The objective was to develop a model capable of identifying customers at higher risk of leaving, helping a telecommunications provider prioritise retention efforts.

## Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- GitHub

## Project Methodology

**1. Data Cleaning and Preparation**

Imported and examined customer records, corrected numerical data types and investigated missing values.

**2. Exploratory Data Analysis**

Analysed churn patterns across customer tenure, contract types, internet services, payment methods and technical support.

**3. Machine Learning**

Developed Logistic Regression and Random Forest classification pipelines using categorical encoding, numerical scaling and an 80/20 training test split.

**4. Model Evaluation**

Compared models using five fold cross validation, measuring ROC-AUC, recall and precision.

**5. Customer Risk Analysis**

Ranked held out customers by predicted churn probability, identified high risk groups and evaluated the concentration of actual churners among the 100 highest risk customers.

**6. Business Impact Simulation**

Modelled the potential value of a hypothetical retention campaign using assumptions about contact costs, retention effectiveness and customer value.

## Key Results

| Metric | Result |
|---|---|
| Selected model | Logistic Regression |
| Cross-validation ROC-AUC | 0.846 |
| Cross-validation recall | 54.8% |
| Cross-validation precision | 65.8% |
| Actual churners among top 100 risk-ranked customers | 74 |
| Churn rate among top 100 | 74% |
| Overall test-set churn rate | 26.54% |
| Top 100 lift | 2.79× |

Logistic Regression slightly outperformed Random Forest in average cross validation ROC-AUC (0.846 versus 0.842).

The model identified 74 actual churners among the 100 highest risk test customers, resulting in a churn rate approximately 2.79 times the overall test-set rate.

## Feature Importance

Permutation importance analysis identified the following as the five most important features for model performance:

1. Customer tenure
2. Internet service
3. Contract type
4. Monthly charges
5. Total charges

Tenure was the strongest predictor in the selected model. Feature importance reflects contribution to predictive performance, not causal impact.

## Financial Simulation

A hypothetical campaign targeting the 100 highest risk customers was evaluated.

| Financial Metric | Estimated Value |
|---|---:|
| Campaign cost | £2,000 |
| Expected customers retained | 14.8 |
| Estimated retention value | £4,440 |
| Estimated net benefit | £2,440 |

These results depend on assumed costs, customer value and a 20% retention success rate among would-be churners. They are illustrative projections, not measured business outcomes.

## Business Recommendations

The analysis suggests that churn prediction models could help businesses:

- Prioritise customers with high estimated churn probabilities.
- Investigate customer experience among groups associated with elevated churn.
- Target limited retention resources more efficiently.
- Test the effectiveness of personalised retention interventions.

## Limitations

The dataset is a fictional sample and may not represent a live customer population.

Predictive relationships do not establish causation, and the dataset cannot measure whether retention offers would actually prevent customers from leaving.

Model performance would require further validation on fresh customer data. The held-out test set was also inspected during development, so its reported results should be interpreted with that limitation.

## How to Run the Project

1. Download `Customer_Churn_Prediction.ipynb`.
2. Open the notebook using Google Colab.
3. Run the cells in order, starting with the dataset import.
4. Review the visualisations, model evaluations and business findings.

The notebook imports the publicly available IBM Telco Customer Churn dataset.

## Future Improvements

- Evaluate model probability calibration.
- Optimise classification thresholds using business costs.
- Test additional algorithms and hyperparameters.
- Validate the model on fresh customer data.
- Evaluate retention effectiveness through controlled experiments.
