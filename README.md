# 🍷 Wine Quality Binary Classification using Decision Tree

This project uses a Decision Tree classifier to predict the **quality of red wine** as either **low quality (0)** or **high quality (1)**, based on various physicochemical properties.

The project involves:
- Data preprocessing
- Binary classification transformation
- Model building using a scikit-learn pipeline
- Hyperparameter tuning with cross-validation
- Model evaluation and visualization

---

## 📁 Dataset

- **Source**: [`winequality-red.csv`](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- **Attributes**: 11 numeric input features (e.g., acidity, sugar, pH, etc.) and a quality score (0–10).
- **Target**: Original multiclass `quality` column is converted into a binary classification:
  - Class `0`: Low quality (quality ≤ 5)
  - Class `1`: High quality (quality ≥ 6)

---

## 📊 Workflow

### 1. Data Preparation
- Load and inspect the dataset
- Convert the `quality` score into binary labels
- Split data using stratified sampling to maintain class balance

### 2. Pipeline
- **StandardScaler**: Normalize feature values
- **DecisionTreeClassifier**: Train a decision tree on the scaled data

### 3. Hyperparameter Tuning
Performed using `GridSearchCV` with 5-fold `StratifiedKFold` cross-validation. The following hyperparameters are explored:
- `criterion`: `gini`, `entropy`
- `max_depth`: `None`, `5`, `10`, `15`
- `min_samples_split`: `2`, `5`, `10`
- `min_samples_leaf`: `1`, `3`, `5`
- `class_weight`: `None`, `'balanced'`

### 4. Model Evaluation
- Test set evaluation using `accuracy_score` and `classification_report`
- Confusion matrix visualization using `ConfusionMatrixDisplay`

---

## 📈 Results

Example output after training:

```text
Best Params: {'clf__class_weight': 'balanced', 'clf__criterion': 'entropy', 'clf__max_depth': 10, ...}
Best Cross-Validation Score: 0.79

Test Set Evaluation:
              precision    recall  f1-score   support

           0       0.75      0.71      0.73       210
           1       0.83      0.85      0.84       309

    accuracy                           0.80       519
   macro avg       0.79      0.78      0.79       519
weighted avg       0.80      0.80      0.80       519
