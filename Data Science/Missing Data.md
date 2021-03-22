# How to Deal with Missing Data

<h3><a href="#del">Drop</a> | <a href="#impute">Impute</a> | <a href="#assign">Assign</a> | <a href="#predict">Predict</a> | <a href="#algo">Algorithm</a></h3>

<h3 name="del"> 1. Deletion or Drop</h3>

- Remove **Particular Row** if it has a **NULL** value for **Particular Feature**.
- Remove **Particular Column** ( **Missing Values** > `70%` )
- If Missing Data is limited to Small number of **Observations**, eliminate those cases from the **Analysis**.
- Sometimes Deleting a particular **Row** or a **Column** with no specific information is better.

> But it is **Better** to Keep Data than to **Discard** it, Removing Data may lead to **Loss** of **Information**.

<h3 name="impute"> 2. Imputation</h3>

- Replace the **Missing Data** with **Mean**, **Median** or **Mode**.
- Sometimes it can Add **Variance** in Data but Better than deleting.

<h3 name="assign"> 3. Assign a Unique Category ( Categorical Data ) | Flag a Numeric Value</h3>

- If Data is **Categorical** then assign a **Unique Category** for Data with Missing Values.   

<h3 name="predict"> 4. Predicting the Missing Value</h3>

- **Predict** the Missing Values with the Help of other Existing Data.
- This method will bring **Better Accuracy**. 

<h3 name="algo"> 5. Use Algorithm which Supports Missing Values</h3>

- KNN works on Principle of **Distance Measure**.
- KNN can be used even if there is a **Null Value** in the Dataset.
- KNN considers the Missing Value by taking the **Majority** of the K Nearest Values.
- **Random Forest** works well on **Non Linear** and **Categorical Data**.

> **Domain Knowledge** can also help us to Deal with the **Missing Data**.
