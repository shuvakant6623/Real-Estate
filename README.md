
# Boston Housing Price Prediction

This project demonstrates how to build a machine learning pipeline to predict housing prices using the Boston housing dataset. The pipeline includes data preprocessing, visualization, feature engineering, and model evaluation using Random Forest Regression.

## 📁 Dataset
The dataset (`data.csv`) contains features related to housing in Boston, including crime rate, number of rooms, property tax, etc., along with the target value `MEDV` (Median value of owner-occupied homes).

## 🧹 Data Preprocessing
1. **Data Loading & Overview**: Used `pandas` to load and inspect the dataset.
2. **Histogram Visualization**: Plotted histograms to understand feature distributions.
3. **Train-Test Split**: Used both `train_test_split` and `StratifiedShuffleSplit` based on the `CHAS` column.
4. **Correlation Analysis**: Computed and visualized correlations of features with `MEDV`.
5. **Feature Engineering**: Created new feature `TAXRM = TAX / RM`.
6. **Missing Value Handling**: Used `SimpleImputer` with the median strategy.

## 🔧 Pipeline Creation
A `Pipeline` was created using:
- `SimpleImputer` for missing value imputation.
- `StandardScaler` for feature scaling.

## 🧠 Model Training
- A `RandomForestRegressor` was trained on the preprocessed training data.
- Model was evaluated on the training set using RMSE (Root Mean Squared Error).

## 📊 Evaluation
- Cross-validation was performed using `cross_val_score` (10-fold).
- Model was tested on the final test set and evaluated using RMSE and R² score.

## 💾 Model Persistence
- Final trained model was saved using `joblib` as `predictorX.joblib`.

## ✅ Results
- Final RMSE on test set: *Reported in notebook*.
- R² Score: *Reported in notebook*.

## 📦 Libraries Used
- pandas, numpy, matplotlib, seaborn
- scikit-learn (model_selection, pipeline, ensemble, metrics, preprocessing)
- joblib

## 📌 How to Run
1. Place `data.csv` in your working directory.
2. Run the notebook or script containing this pipeline.
3. Load `predictorX.joblib` for making predictions on new data.

---