📊 Telco Customer Churn Prediction
This project analyzes customer data to predict churn (whether a customer will leave the service) using machine learning models. The dataset used is the Telco Customer Churn dataset.

📁 Dataset
The dataset Telco-Customer-Churn.csv contains customer demographics and service usage details. The target variable is Churn, indicating whether the customer has discontinued the service.

⚙️ Steps Performed
1. Import Libraries
Used key Python libraries including:

pandas, numpy for data handling

matplotlib, seaborn for visualization

sklearn for preprocessing, modeling, and evaluation

2. Load & Preview Data
Loaded the dataset using pandas

Displayed the first few rows for a basic understanding

3. Data Cleaning
Converted TotalCharges to numeric

Handled missing values by replacing them with 0

4. Encoding
Applied LabelEncoder to convert categorical variables to numeric, excluding customerID

5. Train-Test Split
Features (X) and labels (y) were separated

Data split into 80% training and 20% testing

6. Feature Scaling
Scaled numerical columns (tenure, MonthlyCharges, TotalCharges) using StandardScaler

7. Model Training
Trained two models:

Logistic Regression

Random Forest Classifier

8. Model Evaluation
Evaluated using accuracy and classification report

Logistic Regression Accuracy: ~80%

Random Forest Accuracy: ~79%

9. Hyperparameter Tuning
Used GridSearchCV to find best parameters for both models:

Logistic Regression: C=1, solver='liblinear'

Random Forest: n_estimators=100, max_depth=10

10. Visualization
Plotted churn distribution using countplot

Compared MonthlyCharges across churned vs. retained customers using boxplot

11. Result Export
Exported final predictions of the Random Forest model to churn_predictions.csv

📝 Requirements
Python 3.x

pandas

numpy

matplotlib

seaborn

scikit-learn

Install with:

bash
Copy
Edit
pip install pandas numpy matplotlib seaborn scikit-learn
📌 Output Files
churn_predictions.csv: Contains actual and predicted values for test data.

