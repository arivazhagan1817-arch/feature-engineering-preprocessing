# Feature Engineering & Preprocessing Pipeline

## Project Overview
This project demonstrates a reusable machine learning preprocessing pipeline using Python and Scikit-Learn. The Ames Housing dataset is used to predict house sale prices.

## Dataset
- **Source:** OpenML
- **Dataset ID:** 42165
- **Rows:** 1,460
- **Original columns:** 81
- **Target variable:** `SalePrice`

## Tools and Libraries
- Python
- Pandas
- Scikit-Learn
- Matplotlib
- Jupyter Notebook

## Project Workflow
1. Load and explore the dataset.
2. Separate input features and the target variable.
3. Split the data into training and testing sets before preprocessing.
4. Identify numerical and categorical features.
5. Handle missing numerical values using median imputation.
6. Scale numerical features using `StandardScaler`.
7. Handle missing categorical values using most-frequent imputation.
8. Apply `OneHotEncoder` to categorical features.
9. Combine preprocessing steps using `ColumnTransformer` and `Pipeline`.
10. Train a `RandomForestRegressor`.
11. Evaluate the model and visualize feature importance.

## Model Results
- **Mean Absolute Error (MAE):** 17,750.58
- **R² Score:** 0.8877
- **Processed training features:** 1,168 rows × 286 features
- **Processed testing features:** 292 rows × 286 features

These results are from one train/test split and should not be interpreted as a guarantee of performance on future data.

## Feature Importance
The most important features in the trained Random Forest model were:
1. `OverallQual`
2. `GrLivArea`
3. `TotalBsmtSF`
4. `2ndFlrSF`
5. `BsmtFinSF1`

Feature importance indicates relative importance in this trained model; it does not establish causation.

## Project File
- `Feature_Engineering_Preprocessing.ipynb` — Jupyter Notebook containing the preprocessing pipeline, model evaluation, and feature importance visualization.

## How to Run
1. Install Python and Jupyter Notebook.
2. Install the required libraries:
   ```bash
   pip install pandas scikit-learn matplotlib scipy liac-arff
   ```
3. Open `Feature_Engineering_Preprocessing.ipynb` in Jupyter Notebook.
4. Run the notebook cells in order.

## Conclusion
This project demonstrates how to build a reusable preprocessing pipeline for mixed numerical and categorical data while reducing data leakage by splitting the dataset before fitting preprocessing transformations.
