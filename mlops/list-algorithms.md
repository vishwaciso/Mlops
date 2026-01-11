# 🧠 Complete ML Algorithms Reference Table | VishwaOps

> **Author:** Vishwanath (VishwaOps)  
> **Audience:** Beginners | ML Learners | MLOps Aspirants | Professionals  
> **Goal:** One-stop global reference for **all popular ML algorithms, purpose, usage, and when/how to choose**

---

| # | Algorithm | Type | Purpose | When to Use | How to Use (Globally) | Pros | Cons |
|---|-----------|------|--------|------------|----------------------|------|------|
| 1 | Linear Regression | Supervised | Predict numeric values | Prices, sales, temperature | `sklearn.linear_model.LinearRegression()` | Simple, fast, interpretable | Only linear data |
| 2 | Logistic Regression | Supervised | Predict categorical values | Spam, churn, fraud | `sklearn.linear_model.LogisticRegression()` | Fast, interpretable, baseline | Struggles with complex patterns |
| 3 | Decision Tree | Supervised | Regression & classification | When interpretability is needed | `sklearn.tree.DecisionTreeClassifier()` / `Regressor()` | Easy to explain, non-linear | Overfits easily |
| 4 | Random Forest | Supervised (Ensemble) | Regression & classification | Large datasets, complex data | `sklearn.ensemble.RandomForestClassifier()` | High accuracy, reduces overfitting | Slower, less interpretable |
| 5 | Gradient Boosting (XGBoost/LightGBM) | Supervised (Ensemble) | Regression & classification | Tabular data, competitions | `xgboost.XGBClassifier()` | High accuracy, handles missing | Slower training |
| 6 | Support Vector Machine (SVM) | Supervised | Classification & regression | Small-medium datasets, high features | `sklearn.svm.SVC()` | Works well in high dimensions | Slow for large data |
| 7 | K-Nearest Neighbors (KNN) | Supervised | Classification & regression | Local patterns, simple | `sklearn.neighbors.KNeighborsClassifier()` | Simple, no training | Slow on large datasets |
| 8 | K-Means Clustering | Unsupervised | Group similar items | Customer segmentation, anomaly detection | `sklearn.cluster.KMeans()` | Fast, simple | Need to define clusters |
| 9 | Hierarchical Clustering | Unsupervised | Tree-like grouping | Data exploration | `scipy.cluster.hierarchy.linkage()` | Visual, interpretable | Slow for large datasets |
| 10 | DBSCAN | Unsupervised | Cluster & detect noise | Outlier detection, spatial data | `sklearn.cluster.DBSCAN()` | Detects non-linear clusters | Needs tuning eps/min_samples |
| 11 | Isolation Forest | Unsupervised (Anomaly) | Detect anomalies/outliers | Fraud, intrusion detection | `sklearn.ensemble.IsolationForest()` | Efficient for high-dim data | Not always precise |
| 12 | PCA | Unsupervised (Dimensionality Reduction) | Reduce dimensions | Feature reduction, noise removal | `sklearn.decomposition.PCA()` | Reduces complexity | Interpretability lost |
| 13 | Neural Networks (MLP) | Supervised/Deep Learning | Complex pattern learning | Images, text, complex relationships | `keras.Sequential()` / `torch.nn.Module()` | High flexibility | Needs lots of data & compute |
| 14 | Convolutional Neural Networks (CNN) | Deep Learning | Image/video recognition | Image classification, object detection | `keras.layers.Conv2D()` | High accuracy for images | Requires GPU, complex |
| 15 | Recurrent Neural Networks (RNN/LSTM) | Deep Learning | Sequence prediction | Time series, NLP | `keras.layers.LSTM()` | Captures sequences | Vanishing gradient, slow |
| 16 | Reinforcement Learning | Reinforcement | Learn via trial & error | Games, robotics | OpenAI Gym + `stable-baselines3` | Learns optimal policies | Needs environment & compute |
| 17 | Naive Bayes | Supervised | Probabilistic classification | Text classification, spam | `sklearn.naive_bayes.MultinomialNB()` | Simple, works well with text | Assumes feature independence |
| 18 | AdaBoost | Supervised (Ensemble) | Boost weak learners | Classification | `sklearn.ensemble.AdaBoostClassifier()` | Reduces bias | Sensitive to noisy data |
| 19 | CatBoost | Supervised (Ensemble) | Regression & classification | Categorical-heavy data | `catboost.CatBoostClassifier()` | Handles categorical well | Less popular than XGBoost |
| 20 | LightGBM | Supervised (Ensemble) | Regression & classification | Large datasets, high performance | `lightgbm.LGBMClassifier()` | Very fast, scalable | Less interpretable |

---

## ✅ Global Usage Notes

1. **Start simple:** Linear/Logistic Regression, Decision Trees
2. **Evaluate performance:** Accuracy, RMSE, precision, recall
3. **Scale based on dataset:** Simple → Ensemble → Deep Learning
4. **Ensemble methods** for higher accuracy
5. **Deep Learning** only for large/complex datasets (images, text, sequences)
6. **Unsupervised methods** for clustering/exploration
7. **Anomaly detection** for fraud/security tasks

---

### ⭐ Support VishwaOps
Star ⭐ the repo and follow **VishwaOps** for practical ML & MLOps learning

