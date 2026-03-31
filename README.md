• Loan Default Prediction & Risk Segmentation  
---  
  
• Project Overview  
---

  This project aims to build a Machine Learning model to predict whether a customer is likely to default on a loan. It helps financial institutions make data-driven loan approval decisions and reduce credit risk.

• Objective  
---
 -Identify customers eligible for loan approval  
 -Detect potential defaulters  
 -Perform customer risk segmentation  
 -Support business decision-making in lending
 
• Dataset  
---
-The project uses multiple datasets:  
  -application_train.csv – Customer application data  
  -bureau.csv – Credit history from other institutions  
  -bureau_balance.csv – Monthly bureau records  
  -previous_application.csv – Past loan applications  
  -POS_CASH_balance.csv – POS/Cash loan history  
  -credit_card_balance.csv – Credit card usage  
  -installments_payments.csv – Repayment history

• Data Preprocessing  
---
  -Merged multiple datasets using keys (SK_ID_CURR, SK_ID_BUREAU)  
  -Handled missing values (removed columns with >50% missing)  
  -Feature Engineering:  
  -CREDIT_INCOME_RATIO  
  -DEBT_CREDIT_RATIO  
  -Encoded categorical variables  
  -Cleaned and prepared dataset for modeling

• Exploratory Data Analysis  
---
  -Dataset is imbalanced (~8% defaulters)  
  -Higher default risk observed in:  
   -Low income customers  
   -High credit-to-income ratio  
  -Strong predictors:  
   -External credit scores (EXT_SOURCE)  
   -Payment behavior

• Models Used  
---
  Logistic Regression  
  Random Forest  
  XGBoost  
  LightGBM (Best Model)
 
• Model Performance  
---
 Model	                        ROC-AUC  
 Logistic Regression             0.62  
 Random Forest	                 0.73  
 XGBoost	                       0.76  
 LightGBM	                       0.76

• Threshold Optimization  
---
  Used Youden’s J Statistic  
  Best Threshold ≈ 0.498
  
• Evaluation Metrics  
---
  Accuracy: 73%  
  Approval Rate: 70%  
  Default Detection Rate: 67%  
  Precision (Default): 18%

• Key Insights  
---
  Model successfully detects majority of defaulters  
  Maintains high loan approval rate  
  External credit scores are most important features  
  Financial stability strongly impacts loan approval
   
• Customer Risk Segmentation  
---
  Segment	Description  
   Low Risk	Safe customers → Approve  
   Medium Risk	Moderate → Manual review  
   High Risk	Risky → Reject  
   
• Business Recommendations  
---
   Approve low-risk customers  
   Apply stricter policies for medium-risk  
   Reject or secure high-risk customers  
   Use model for automated credit decisioning
 
• Business Impact  
---
  Reduces financial losses    
  Improves approval strategy  
  Enables risk-based decision making  
 
• Technologies Used  
---
  Python  
  Pandas, NumPy  
  Scikit-learn  
  LightGBM  
  Matplotlib, Seaborn
 
• Project Structure  
---
  Loan-Default-Prediction/  
  │  
  ├── data/  
  ├── notebooks/  
  ├── model/  
  ├── loan_model.pkl  
  ├── scaler.pkl  
  ├── threshold.pkl  
  ├── README.md  

• Author  
---
  Pandhari Mane  
  Data Science Enthusiast  
