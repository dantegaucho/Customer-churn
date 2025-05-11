# Customer Churn Prediction
![Booth](images\phone-booth.jpg)

This project applies the CRISP-DM methodology to predict customer churn.

## Contents
- [Overview](#contents) 
- [Business Understanding](#business-understanding)
- [Data Understanding](#data-understanding)
- [Data Preparation](#data-preparation)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Deployment](#deployment)

---
## Overview

This project focuses on predicting customer churn for SyriaTel, a telecommunications provider, using machine learning techniques. The model used is a classification model since the target is binary. By analyzing the data, plans and packages, usage patterns, and service history, the project aims to identify customers at risk of leaving SyriaTel soon. The workflow follows the CRISP-DM methodology, covering business understanding, data exploration and model development, evaluation, and deployment. The ultimate goal is to provide actionable insights to reduce churn, loss of revenue and improve customer retention.

---

## Business Understanding

![Center](images\call_center.png)

The goal is to identify customers likely to leave SyriaTel soon, enabling proactive retention strategies and reducing revenue loss.
Find the factors affecting customer satisfaction leading to churn. Understand the patterns and packages/ plans at high risk of churn.

### *Objectives*

* What is the overall churn rate?
* Which package plans have customers at high risk of leaving?
* What factors contribute to high rate of customer churn?

## Data Understanding

- The data used is collected from customer records, usage, and service history of SyriaTel, a telecommunications company found in a dataset from Kaggle [click here](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)
- Initial exploration includes summary statistics, churn distribution and  relationship between features.
![churn](images\churn_distribution.png)
This is the distribution of churn and loyal customers, churn(True) and  Loyal customers(False).

- The dataset has class imbalance as one class contains 85.51% of churn distribution when the other contains 14.49%.

## Data Preparation

- Encoded categorical variables using one-hot encoding
- Scaled numerical features using standard scaler
- Split data into training and test sets.

## Modeling
Here, two classification model algorithms are built;
1. Logistic Regression as the base model
2. Decision trees as the second model for performance comparison.
- Used cross-validation for feature selection in tuning the model.
- Tuned hyperparameters for optimal performance but tuning did not improve performance. The original tree model performed better.

## Evaluation

- Evaluated models using accuracy, precision, recall, and ROC-AUC.
- Selected the Decision tree model for its exemplary perfomance on predicting unseen data. Here is a classification model, Decision tree confusion matrix.
![Confusion_matrix](images\tree_matrix.png)
The model performance:
 - f1_score = 0.77,
 - recall = 0.78,
 - precision = 0.77,
 - accuracy = 0.93,

---
### Conclusion

Churn predictors are pointed below using two visualizations.
![Summary](images\churn_summary.png)

![Features](images\churn_features.png)

* High number of customer service calls show dissatisfaction and a potential churn.
* Customers with an international plan are more likely to churn, and those who make more customer service calls also show a higher tendency to leave, indicating dissatisfaction with the service.
* Customers who actively use voicemail services tend to be more loyal. 
* The models show that accuracy is high due to class imbalance, recall for the minority (churn) class is improved after applying SMOTE. 
* Feature importance analysis confirms that customer service calls, international plan, and usage patterns are significant predictors of churn.

---
## Recommendations

- Offering incentives or tailored packages to these segments, as well as promoting voicemail plan usage, may help increase satisfaction and retention.
- SyriaTel should focus on improving customer service quality especially customers who call for support or help, this would reduce churn and loss of revenue
- There should be a special consideration to customers with international plans as they have a high chance of leaving.

**Next Steps**
- Stay update with real-time industry data and new technology to adjust to new ideas.
- Marketing team should focus on customer acquisition and retention methods like content marketing and loyalty rewards.


---



---

## Usage

1. Clone the repository.
2. Install dependencies.
3. Run the notebook or script to train and evaluate the model.

---

