Machine Learning:
- Regression (Linear, Logistic, Descision Tree, SVM: Find optimal hyperplane with maximum margin in N dimensional space, KNN)
- Ensemble Technique: Bagging: Random Forest  | Boosting: ADABOOST (Handling class imbalance, More weights to misclassified data) GBM (Gradient Descent), XGBOOST (Regularization + GB)

- K Mean, Clustering, Hierarchical (AGNES: Agglomerative Nesting | DIANA: Divise Analysis) DBSCAN 
- PCA (Create principal components without losing information) | LDA (Maximize the seperation between 2 or more classes of data) | t-SNE (Non linear dimensional reduction)
- Association Mining (Items that frequently occurs together in a dataset) 

Metrics:
- Regression: MAE (small error) | MSE | RMSE (large error) | R2 (Coefficient of Determination, Square Correlation Coefficient | Explain variance and variability) | Adjusted R2
- Classification: Confusion Matrix (Summarize the performance/Evaluate correct and incorrect) | Accuracy | Precision | Recall (TPR & Sensitivity) | FPR & Specificity | F1 Score (Imbalanced) | ROC | AUC

Regularization: (A technique to prevent from overfitting)
- L1 (Least Absolute Shrinkage Selection Operator) Adds a penalty equal to the sum of absolute value of the slope.
- L2 (Ridge) Adds a penalty equal to the squared value of the slope.

Cross Validation: (A resampling technique used to evaluate the trained model performance on a limited dataset)
- Holdout | K Fold | Stratified K Fold | Leave one out LOOCV
- Hyperparameter Tuning: Find optimal set of parameters to train the model
- Grid Search CV: Evaluate the model with all possible combination of Hyperparameters within a predefined grid.
- Random Search CV: Randomly choose the combination of Hyperparameter values.

Gradient Descent: An optimization algorithm used while training a model | Learning Rate: Determine the step size taken in the direction of local minimum point.

Hyperparameters: Learning Rate | Batch Size | Regularization | # Epochs | # Layers | # Nodes | Activation Function

Missing Data: 
- Drop | Impute (Estimate) | Assign / Flag Unique Class / Category | Predict Missing Value | Algorithm (KNN, SVM and Random Forest)

Outlier:
- Visualization | Z Score (Extreme Value Analysis) | DBSCAN | 5 Number Summary | Sensitive (Linear, KNN, K Mean, SVM) | Insensitive (Decision Tree, Ensemble Technique)

Categorical Feature:
- Data Encoding (Nominal/No Rank: OHE, get_dummies | Ordinal: Label Encoding)

Imbalanced Dataset:
- Upsampling (Oversampling) SMOTE: Synthetic Minority Oversampling Technique and Downsampling (Undersampling)
- F1 Score | Precision | Recall | Stratified K Fold Cross Validation | Random Forest | class_weights | Collect more data

Overfitting:
- Low Bias + High Variance | Train Test Split | Apply Regularization | Apply Cross Validation | Feature Selection | Ensemble Technique.

MLOps:
- ETL (Extract, Transform, Load, Integrate)
- Data Pipeline (Validate, Clean, Preprocess, Standardize, Curate, Encode)
- Feature Engineering (Select Features, Extract Features)
- Model Development (Code, Train, Validate, Evaluate, Optimize, Fine Tune, Retrain, Hyperparameter Tuning)
- Model Deployment (Build, Deploy, Contenarize, Package)
- Monitor, Automate, Integrate, Release, Register
- Serve (API, App, UI)
- Sustenance, Infrastructure Management.
