# Classification Modelling with Churn in Telecom's Dataset
## Overview
I will be solving a classification problem with the Churn Telecom's Dataset. The dataset consists of cleaned customer activity data (features), along with a churn label(target) specifying whether a customer canceled the subscription.The task is to build a classifier that predicts whether a customer will ("soon") stop doing business with SyriaTel, a telecommunications company. 

In this project, i will be doing a complete machine learning workflow with classification regression, including data preparation, modeling (including hyperparameter tuning), and final model evaluation.

### Business and Data Understanding

The dataset contains 3333 rows (customers) and 20 columns (features). Each row represents a customer, each column contains customer’s attributes described on the column Metadata.

The dataset includes information about:

- state, string. 2-letter code of the US state of customer residence
- account length, numerical. Number of months the customer has been with the current telco provider
- area code, string="area_code_AAA" where AAA = 3 digit area code.
- international plan, (yes/no). The customer has international plan.
- voice mail plan, (yes/no). The customer has voice mail plan.
- number vmail messages, numerical. Number of voice-mail messages.
- total day minutes, numerical. Total minutes of day calls.
- total day calls, numerical. Total minutes of day calls.
- total day charge, numerical. Total charge of day calls.
- total eve minutes, numerical. Total minutes of evening calls.
- total eve calls, numerical. Total number of evening calls.
- total eve charge, numerical. Total charge of evening calls.
- total night minutes, numerical. Total minutes of night calls.
- total night calls, numerical. Total number of night calls.
- total night charge, numerical. Total charge of night calls.
- total intl minutes, numerical. Total minutes of international calls.
- total intl calls, numerical. Total number of international calls.
- total intl charge, numerical. Total charge of international calls
- number customer service calls", numerical. Number of calls to customer service
- churn, (yes/no). Customer churn - target variable.


### Modeling
