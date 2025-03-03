## Logistic Regression for Predicting the F1 Champion

We use logistic regression to predict the Formula 1 champion, considering features such as qualifying time, driver age, and weather conditions.

### Python Code:
```python
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report, accuracy_score, roc_auc_score, roc_curve
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
data = pd.read_csv('final_df.csv')

# Define the target variable
data['champion'] = data.groupby('year')['driver_points'].transform(lambda x: (x == x.max()).astype(int))

# Convert boolean columns to integers and ensure the target variable is binary (0 or 1)
bool_columns = data.select_dtypes(include=['bool']).columns
data[bool_columns] = data[bool_columns].astype(int)

# Define features
features = ['grid', 'driver_wins', 'weather_warm', 'weather_cold', 'weather_dry', 'weather_wet', 'weather_cloudy', 'qualifying_time', 'driver_age', 'podium']
X_train, X_test, y_train, y_test = train_test_split(data[features], data['champion'], test_size=0.3, random_state=42)

# Standardize the features
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# Train logistic regression model
logit_model = LogisticRegression(max_iter=1000, solver='liblinear', penalty='l2').fit(X_train_scaled, y_train)

# Predict on test set and evaluate
y_pred = logit_model.predict(X_test_scaled)
y_pred_proba = logit_model.predict_proba(X_test_scaled)[:, 1]
print(classification_report(y_test, y_pred))
print("Accuracy:", accuracy_score(y_test, y_pred))
print("AUC-ROC Score:", roc_auc_score(y_test, y_pred_proba))

# Plot ROC Curve
fpr, tpr, thresholds = roc_curve(y_test, y_pred_proba)
plt.plot(fpr, tpr, label=f'AUC = {roc_auc_score(y_test, y_pred_proba):.2f}')
plt.plot([0, 1], [0, 1], 'r--')
plt.xlabel('False Positive Rate')
plt.ylabel('True Positive Rate')
plt.title('ROC Curve')
plt.legend(loc='lower right')
plt.show()
````
## Random Forest for Predicting F1 Season Outcome

A Random Forest model is used to predict the probability of each driver winning the upcoming season based on historical data.

### Python Code:
```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report, roc_auc_score, roc_curve
import seaborn as sns
import matplotlib.pyplot as plt

# Load dataset and drop unnecessary columns
df = pd.read_csv('final_df.csv')
df = df.drop(['weather', 'status', 'raceId', 'resultId', 'points', 'driverId', 'constructorId'], axis=1)

# Define target variable and features
df['champion'] = df.groupby('year')['driver_points'].transform(lambda x: (x == x.max()).astype(bool))
X = df.drop(columns=['driver_points', 'champion', 'driver'])
y = df['champion']

# Split data and scale features
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# Train RandomForest model
rf_classifier = RandomForestClassifier(random_state=42)
rf_classifier.fit(X_train, y_train)

# Make predictions and evaluate
y_pred = rf_classifier.predict(X_test)
y_prob = rf_classifier.predict_proba(X_test)[:, 1]
print("Accuracy:", accuracy_score(y_test, y_pred))
print("ROC-AUC Score:", roc_auc_score(y_test, y_prob))

# Plot ROC Curve
fpr, tpr, thresholds = roc_curve(y_test, y_prob)
plt.plot(fpr, tpr, label=f'AUC = {roc_auc_score(y_test, y_prob):.2f}')
plt.plot([0, 1], [0, 1], 'r--')
plt.xlabel('False Positive Rate')
plt.ylabel('True Positive Rate')
plt.title('ROC Curve')
plt.legend(loc='lower right')
plt.show()
