# Classification Modeling with Churn in Telecom's Dataset
 
 ## Objective
 The main objective of the project is to Explore and analyze the data to discover key factors responsible for customer churn and come up with ways/recommendations to ensure customer retention.

## 1.0 Business and Data Understanding

I will be solving a classification problem with the Churn Telecom's Dataset. The dataset consists of cleaned customer activity data (features), along with a churn label(target) specifying whether a customer canceled the subscription.The task is to build a classifier that predicts whether a customer will ("churn") stop doing business with SyriaTel, a telecommunications company. 
In this project, i will be doing a complete machine learning workflow with classification regression, including data preparation, modeling (including hyperparameter tuning), and final model evaluation.


### 2.0 Data Preparation

The dataset contains 3333 rows (customers) and 20 columns (features). Each row represents a customer, each column contains customer’s attributes described on the column Metadata.

The dataset includes information about:
 
   * ID 
   
      * area code
      * phone number


   * Features 
   
      * state
      * account length
      * international plan
      * voice mail plan
      * number vmail messages   
      * total day minutes
      * total day calls
      * total day charge
      * total eve minutes
      * total eve calls
      * total eve charge
      * total night minutes
      * total night calls
      * total night charge
      * total intl minutes
      * total intl calls
      * total intl charge
      * number customer service calls

   * Target
   
      * churn

#### EDA
I divided the whole project in different parts and analyzed data:
Churn in accordance with state
Churn in accordance with area
Churn in accordance with international plan
Churn in accordance with voice mail plan
Churn in accordance with charges
Reltionship between minutes and charges

#### Following are the conclusions got after doing EDA on the dataset:
     * There are about 85% customers who churn out, and about 14.49% customers retained.
     *The top 2 states with the highest churn rate are TX and NJ with a churn rate of 18
     * The top 3 states with the lowest churn rate are AK,IA and HI with a churn rate of 3
     * Most of the churned customers are from 415 area.
     * While Area codes 408 and 510 had comparatively less churned customers.
     * Customers with International plan have about 42% Churn rate.
     * While customers who don't have International plan have about 11% Churn rate.
     * Churn rate is more with customer using international plan.
     * Voicemail plan seems to be popular with the customers.
     * Churn rate of Customers with Voice mail plan is about 8%.
     * While Churn rate of Customers who don't have voice mail plan is about 16%
     * Day time call chargers is a significant reason to leading to customer Churn. 
     

#### Correlation HeatMap Analysis
   According to the correlation heatmap analysis produced by the correlation matrix, the following features had the highest correlation:

    1. Total day minutes
    2. total day charges
    3. total night minutes
    4. total night chages
    5. number customer service calls
    6. total eve minutes
    7.total eve charges
    8.total international minutes
    9.total international charges    

#### Features Importance

  Feature selection process of finding and selecting the most useful features in a dataset. Unnecessary features decrease training speed, the model interpretability and the generalization performance on the test set.
   
   According to the feature importance analysis produced by the Random Forest algorithm, the following features had the highest predictive power:

    1. total_day_minutes
    2. total_day_charge
    3. number_customer_service_calls
    4. total_eve_minutes
    5. international_plan     
       	     
### 3.0 Modeling


Four models have been constructed for application in the problem of this project, namely:

        * Gradient Boosted 
        * Random Forest
        * AdaBoost
        * Logistic Regression

Their respective roc_auc_scores measures are listed below:
    
    Random Forest:    0.88
    Gradient Boosted Trees: 0.87
    AdaBoost: 0.85
    Logistic Regression: 0.67

Random Forest Classifier produced the highest roc_auc_score and the following scores:

      Accuracy: 94% labeled correctly
      Precision: 97% labeled as churn actually churned (3% were wrongly labeled as churn)
      Recall: 97% that actually churned were labeled as churn (3% of churn users were labeled as non-churn)
      
  From the error analysis we can also conclude that:
     1.The Random Forest Classification model reveals that 98% of the variability observed in the churn is explained.
     2.The extreemly low rmse of 0.1, indicates that the Random Forest Classification model is a best fit and accurately predicts the churn



### 4.0 Evaluation
    * From our metrics in the modeling stage:

         1.It was important to use a ML rather than a simpler form of data analysis because with the analysis of the vast amount of data that we had,ML did automate the entire data analysis workflow to provide deeper, faster, and more comprehensive insights. 

         2.The RandomForestClassifier had the best roc-auc score of 0.88.This is very good performance as it means that the model is as good as random.
         The insight we can get from this is that the model by the RandomForestClassifier has the ability to predict the target correctly 88% of the time

         3.Limitations in my analysis-The Dataset was imbalanced and therefore couldnt get the highest roc_auc_score of 1

         4. Recommendation to guarantee customer retention:
             - A good way to lower churn is to lower the prices as the talk time increases.
             - Have special offers for those who make more international calls.
             - Introduce free voice mail plans
             - Promote the service and its products frequently in area 415 area.





    
