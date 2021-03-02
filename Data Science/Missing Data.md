# How to Deal with Missing Data

### 1. Deletion
- Remove Particular Row if it has a **NULL** value for Particular Feature.
- Remove Particukar Column if it has more than 70% to 75% of **Missing Values**.
- If Missing Data is limited to Small number of **Observations**, eliminate those cases from the **Analysis**.
- Make sure that if we Delete the Data, there is no Addition of **Bias** 
- Sometimes Deleting a particular **Row** or a **Column** with no specific information is better.

> But it is always Better to Keep Data than to **Discard** it, Removing Data may lead to **Loss** of **Information**.

### 2. Imputation
- Replace the Missing Data with Mean, Median or Mode.
- Sometimes it can Add Variance in Data but better than Deleting Data.
- Continuous : Mean | Median | Mode | Multiple Imputation

### 3. Assign a Unique Category
- If Data is Categorical then assign a Unique Category for Data with Missing Values.  
- Categorical : Treat **NA** as a Category | Multiple Imputation 

### 4. Predicting the Missing Value
- Using Features which has Values, we can **Predict** the Missing Values.
- This Method will bring Better Accuracy 

### 5. Use Algorithm which Supports Missing Values
- KNN works on Principle of Distance Measure.
- KNN can be used even if there is a Null Value in the Dataset.
- KNN considers the Missing Value by taking the Majority of the K Nearest Values.
- Random Forest works well on Non Linear Data and Categorical Data.
- But it is Time Consuming Process.

Domain Knowledge can also Help us to Deal with the Missing Data.
