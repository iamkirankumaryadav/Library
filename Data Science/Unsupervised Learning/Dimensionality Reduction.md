<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

## What is Dimensionality Reduction?
- A method to reduce the number of input features (variables) in a dataset.
- Helps make complex data easier to understand and work with.

## Why is it important?
- Datasets with too many features can make analysis and modeling difficult.
- Not all features are useful, some may be irrelevant or repetitive.
- Extra features can confuse models, complicate learning, and reduce accuracy.

## How does it work?
- The number of features (variables) should be low compared to the dataset's observations (rows).
- It transforms data into a simpler form with fewer features.
- Tries to keep the most important information while removing the rest.

## When is it useful?
- Especially helpful for algorithms that use distance calculations, like:
- Regression, K Nearest Neighbour (KNN), K Mean Clustering, and Support Vector Machine (SVM)
- Helps focus on the most meaningful features in the data.

## When to use Dimensionality Reduction?
- Too Many Features = High Cost, your model takes too long to train or uses too much memory.
- Your model performs well on training data but performs poorly on the new data due to too many features (overfitting).
- You want to visualize patterns in data with many dimensions by converting it to 2D or 3D.

## Benefits:
- **Simplified Analysis:** Analyzing data with fewer, relevant features is easier and faster.
- **Improved Accuracy:** Simplifies the model, removes noise and irrelevant data, which improves accuracy, consistency and efficiency.
- **Faster Training:** Less data means faster computation, faster training, and faster prediction/classification.
- **Improved Visualization:** Lower-dimensional data can be visualized more effectively using charts and plots.
- **Enhanced ML:** Reduced computational cost, faster model training and better accuracy + model performance.

**Feature Selection** | **Feature Extraction**
:--- | :---
Selecting a subset of the existing features in your data | Creating entirely new features from existing ones
Keeping the original dataset, but selecting the subset of important features | Transforming the original dataset and creating something entirely new.
Selects the most relevant features that best represent the data | Transforms the raw data into a new set of features that are more suitable for ML algorithms.
Improves model performance by eliminating irrelevant or redundant features | Simplifies data processing by creating more meaningful features
Reduces training time by using a smaller set of features | Improves model performance by capturing underlying patterns

## Feature Selection
- Feature selection selects the most relevant features and creates a new subset of data for building a better model with better accuracy.
- Features are selected by calculating the correlation (regression) or information gain (classification)
- Embedded methods perform feature selection as a part of the model training process (Decision Tree)
- Regularization (LASSO and Ridge) also helps in finding relevant features and reducing irrelevant features.
- Example: If you have a dataset with 30 features,
- Feature selection might help you identify the top 10 that contribute most to predicting the target variable.

### Feature Extraction
- Feature extraction identifies the most relevant features and transforms the original dataset into a new dataset. 
- Models with only the relevant features (variables) require less training data, training time, and computational resources.
- Examples: PCA (Unsupervised Numerical), LDA (Supervised Categorical Classification), and t-SNE (Non-linear)
- Example: Instead of selecting 10 out of 30 features,
- Feature extraction might create 10 new features that are combinations of the original ones. 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
