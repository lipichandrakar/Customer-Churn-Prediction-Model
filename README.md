# 📊 Telco Customer Churn Prediction

This project analyzes customer data to predict churn (whether a customer will leave the service) using machine learning models. The dataset used is the **Telco Customer Churn** dataset.

---

## 📁 Dataset

The dataset `Telco-Customer-Churn.csv` contains customer demographics and service usage details.  
The target variable is **`Churn`**, indicating whether the customer has discontinued the service.

---

## ⚙️ Steps Performed

### 1. **Import Libraries**
Used essential Python libraries:
- `pandas`, `numpy` for data handling
- `matplotlib`, `seaborn` for visualization
- `scikit-learn` for preprocessing, modeling, and evaluation

### 2. **Load & Preview Data**
- Loaded dataset using `pandas`
- Displayed sample data using `.head()`

### 3. **Data Cleaning**
- Converted `TotalCharges` to numeric using `pd.to_numeric`
- Filled missing values with `0`

### 4. **Encoding**
- Applied `LabelEncoder` to convert categorical features to numeric
- Skipped the `customerID` column

### 5. **Train-Test Split**
- Separated features (`X`) and target (`y`)
- Used `train_test_split` with 80/20 split and `stratify` on `y`

### 6. **Feature Scaling**
- Scaled numerical columns: `tenure`, `MonthlyCharges`, and `TotalCharges`
- Used `StandardScaler` for normalization

### 7. **Model Training**
Trained two machine learning models:
- **Logistic Regression**
- **Random Forest Classifier**

### 8. **Model Evaluation**
Used `accuracy_score` and `classification_report`:
- **Logistic Regression Accuracy**: ~80%
- **Random Forest Accuracy**: ~79%

### 9. **Hyperparameter Tuning**
Performed tuning with `GridSearchCV`:
- Best Logistic Regression params: `C=1`, `solver='liblinear'`
- Best Random Forest params: `n_estimators=100`, `max_depth=10`

### 10. **Visualization**
- **Churn Distribution** using `sns.countplot`
- **Monthly Charges by Churn** using `sns.boxplot`

### 11. **Result Export**
- Saved predictions to `churn_predictions.csv`

---

## 📝 Requirements

Install required libraries with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
