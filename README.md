# Analysing-Credit-Risk-Peer-to-Peer-lending

#Analysing-Credit-Risk-on-European-Peer-to-Peer-lending-Platform Project
First of all we understand the Peer-to-to-lending platform and then understand the data file Bondora_raw.csv on which we have to perform the whole project.
Understand the data, then perform data preprocessing then perform Exploratory Data Analysis and feature engineering the design a model using Logistic Regression and Random Forest Machine Learning models. Then work on pipeline.

#Data Understanding
Bondora_raw.csv data file contains all the data related to lending platform and we have to understand the data for Analysis credit risk that which parameters are useful for our project. In this dataset we have target variable Status and we find the status of lenders.

#Data Preprocessing
The dataset we have is Raw data so we perform some data pre-processing after which we can apply Machine Learning model on our clean data.
  i) First of all check the Null values
   (a) remove all thos features who have Null values more than 40%. Those columns are,
      ['StageActiveSince','ContractEndDate','NrOfDependants','EmploymentPosition','WorkExperience','WorkExperience','PlannedPrincipalTillDate','CurrentDebtDaysPrimary',
      'DebtOccuredOn','CurrentDebtDaysSecondary','DebtOccuredOnForSecondary','DefaultDate','PlannedPrincipalPostDefault','PlannedInterestPostDefault','EAD1','EAD2',           'PrincipalRecovery','InterestRecovery','RecoveryStage','EL_V0','Rating_V0','EL_V1','Rating_V1', 'Rating_V2','ActiveLateCategory', 'CreditScoreEsEquifaxRisk',    
      'CreditScoreFiAsiakasTietoRiskGrade','CreditScoreEeMini','PrincipalWriteOffs','InterestAndPenaltyWriteOffs','PreviousEarlyRepaymentsBefoleLoan','GracePeriodStart',       'GracePeriodEnd','NextPaymentDate','ReScheduledOn','PrincipalDebtServicingCost','InterestAndPenaltyDebtServicingCost','ActiveLateLastPaymentCategory']
   (b) Then remaining features who have null values less than 40%, drop all the rows of those fatures or replace all those rows with mean value.
  
  ii)  Then correct the syntax of those data who have mistakenly entered the wrong syntax.
  iii) Check the data types of all the features
  iv)  Remove all the date type features because in peer-to-peer platform there is no need to date type features.
  v)   Check the duplicates and remove all the duplicated values
  
  #Exploratory Data Analysis
    . Check shape of data (134529, 112)
    . Divide the categorical, numerical and boolean data into different categories
    . Add Default_Date column
    . Convert Cateorical data into Numerical
    . Perform Univariant Analysis using pie charts and density plots
    . Perform Biavariant Analysis using scatter plots and bar plots
    . Perform Multivariant Analysis using pairplot and heatmap
    
   #Feature Engineering
    . Check outliers using Boxplot and IQR
    . Out of all the features select the most relevant features for the model
    . Perform Feature scalling
    . Perform Principal Component Analysis (PCA)
    
    #Develop Machine Learning model
    . Divide the data into train and test data
    . Apply the logistic regression model and predict the target feature status
    . Accuracy of logistic regression model is 0.94
    . Then Apply Random Forest model
    . Accuracy of Random Forest Model is 0.98
    
    #Pipeline
    After model building work on pipeline. In pipeline pass two models random forest and logistic regression model.
  
