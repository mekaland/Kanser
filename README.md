# Breast Cancer Classification with K-Nearest Neighbors (KNN)

This project demonstrates the use of a K-Nearest Neighbors (KNN) classifier to predict breast cancer diagnoses based on a dataset. Below are the key components and steps involved in the analysis.

---

## Dataset

The dataset contains 569 instances with 31 columns:
- **Target**: Indicates diagnosis (M = Malignant, B = Benign). Encoded as 1 (M) and 0 (B).
- **Features**: 30 numerical attributes describing various properties of the cells.

---

## Libraries Used

- `pandas`: Data manipulation and analysis.
- `numpy`: Numerical computations.
- `seaborn` and `matplotlib`: Data visualization.
- `scikit-learn`: Machine learning algorithms and preprocessing tools.
- `warnings`: To suppress unnecessary warnings.

---

## Workflow

### 1. **Data Preprocessing**

- Loaded data from the CSV file.
- Dropped irrelevant columns (`id` and `Unnamed: 32`).
- Renamed the `diagnosis` column to `target`.
- Encoded target labels: Malignant (`M`) as 1, Benign (`B`) as 0.
- Checked for missing values (none found).

### 2. **Exploratory Data Analysis (EDA)**

- Visualized target distribution:
  - **357 Benign** (Class 0).
  - **212 Malignant** (Class 1).
- Correlation analysis:
  - Identified features highly correlated with the target.
  - Visualized relationships among selected features using a clustermap.

### 3. **Outlier Detection**

- Applied the `LocalOutlierFactor` method to detect potential outliers.

### 4. **Data Splitting and Scaling**

- Split data into training and testing sets (70% training, 30% testing).
- Standardized features using `StandardScaler`.

### 5. **K-Nearest Neighbors (KNN) Classifier**

- Trained a KNN model with `n_neighbors=4`.
- Evaluated model performance on the test set.

---

## Results

- **Accuracy**: 96.49%
- **Confusion Matrix**:
  ```
  [[106   2]
   [  4  59]]
  ```
  - True Negatives: 106
  - False Positives: 2
  - False Negatives: 4
  - True Positives: 59

---

## Key Files

- **`data.csv`**: The dataset used for the analysis.
- **Python Script**: Implements the workflow outlined above.

---

## How to Run

1. Ensure the required libraries are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
2. Load the dataset (`data.csv`) into the project directory.
3. Execute the script.

---

## Conclusion

The KNN classifier achieved high accuracy in predicting breast cancer diagnoses. Future improvements could include hyperparameter tuning using GridSearchCV or exploring other machine learning models to compare performance.

---
