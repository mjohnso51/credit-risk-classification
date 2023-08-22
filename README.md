# credit-risk-classification

Overview of the Analysis:

	The purpose of this analyis was to create a model that accurately predicts the health of a loan.  The information we used to help develope this model include: loan size($), the interest rate, income of the borrower, debt/income ratio, number of accounts, derogatory marks and the total debt.  The final column in the .csv file is the health of the loan.  Using this information, we created a program that could predict the health of a loan based on the factors of a loan.  

	The dataset(.csv file) was split into training and testing datasets.  The training set was used to build a logistic regression model using scikit-learn.  This model was the applied to the testing dataset, in an attempt to have it predict whether a loan would be classified as healthy (0) or high-risk(1).  Using RandomOverSampler from imbalanced-learn, we were able to resample the training dataset increase the quality of our data for the logistic regression model.  Finally, we used the resampled data to build a new logistic regression model with the hopes that it would be more accurate than the first model.
	
Results:

Logistic Regression Model 1

  PRECISION - On average, the model was 92% precise (100% precise on healthy loans, 85% precise on high-risk loans)
  RECALL - On average, 95% on recall (99% recall on healthy loans, 91% on high-risk loans)

Logistic Regression Model 2	

  PRECISION - On average, the model was 99% precise (99% precise on healthy loans, 99% precise on high-risk loans)
  RECALL - On average, 99% on recall (99% recall on healthy loans, 99% on high-risk loans)

Summary:

	In my opinion, the second logistic regression model performed better.  As a bank, I would place more weight on a model being able to predict high-risk loans.  Even if it means sacrificing predicting a few healthy loans.  For a bank, it would important to avoid high-risk loans defaulting.  That is why I believe that being more accurate when predicting high-risk loans is important.