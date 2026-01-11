# 🛠 ML Mini Project – End-to-End (Algorithm → Model → Deployment)

> **Author:** Vishwanath (VishwaOps)  
> **Audience:** ML Beginners | MLOps Aspirants | Professionals  
> **Goal:** Hands-on ML project connecting **algorithm → model → deployment** in a simple, practical way

---

## 📌 Why This Project?

- Consolidates all previous topics:
  - ML basics
  - Algorithms
  - Model creation
  - Model evaluation
  - Deployment (MLOps focus)
- Helps understand **real-world ML workflow**

---

## 🔁 Project Overview

**Problem:** Predict whether a customer will buy a product based on historical data

**Steps:**
1. Data Collection
2. Data Cleaning & Preprocessing
3. Feature Selection
4. Algorithm Selection
5. Model Training
6. Model Evaluation
7. Model Saving
8. Deployment via API (FastAPI + Docker)
9. Testing & Monitoring

---

## 1️⃣ Data Collection

- Use a **CSV dataset** (customer data with features like Age, Income, Browsing History, etc.)
- Tools: pandas

```python
import pandas as pd
data = pd.read_csv('customer_data.csv')
data.head()
```

---

## 2️⃣ Data Cleaning & Preprocessing

- Handle missing values
- Convert categorical variables
- Normalize/scale if needed

```python
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data['Gender'] = le.fit_transform(data['Gender'])
```

---

## 3️⃣ Feature Selection

- Select features that matter for prediction
- Example: Age, Income, Browsing_Time

```python
X = data[['Age','Income','Browsing_Time']]
y = data['Purchased']
```

---

## 4️⃣ Algorithm Selection

- Use **Logistic Regression** for binary classification (yes/no)
- Can try **Random Forest** for better accuracy

```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)
model = LogisticRegression()
model.fit(X_train, y_train)
```

---

## 5️⃣ Model Evaluation

- Check performance using **accuracy**

```python
from sklearn.metrics import accuracy_score
predictions = model.predict(X_test)
accuracy_score(y_test, predictions)
```

---

## 6️⃣ Model Saving

- Save trained model for deployment

```python
import joblib
joblib.dump(model, 'customer_purchase_model.pkl')
```

---

## 7️⃣ Deployment (FastAPI + Docker)

**FastAPI Example:**
```python
from fastapi import FastAPI
import joblib
import pandas as pd

app = FastAPI()
model = joblib.load('customer_purchase_model.pkl')

@app.post('/predict')
def predict(data: dict):
    df = pd.DataFrame([data])
    prediction = model.predict(df)
    return {'prediction': int(prediction[0])}
```

**Dockerfile Example:**
```
FROM python:3.12-slim
WORKDIR /app
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . ./
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```

---

## 8️⃣ Testing & Monitoring

- Test API with Postman
- Add logging for input/output
- Monitor model accuracy over time

---

## 🎯 Key Learning Points

- Algorithm → Model → Deployment workflow
- Data preprocessing & feature selection
- Choosing the right algorithm for problem type
- Saving & loading models
- Simple API deployment using FastAPI
- Dockerize ML application
- Monitoring models in production

---



### ⭐ Support VishwaOps
Star ⭐ the repo and follow **VishwaOps** for practical ML & MLOps hands-on learning

