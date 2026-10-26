# Day 18

## Key Learnings

## Coding
```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression, LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, mean_squared_error, r2_score, classification_report

# Load the Iris dataset
iris = load_iris()
X, y = iris.data, iris.target

# Split dataset for classification models (70% train, 30% test)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

print("=" * 60)
print("PART 1: CLASSIFICATION MODELS (Predicting Species)")
print("=" * 60)

classification_models = {
    "Logistic Regression": LogisticRegression(max_iter=200),
    "Decision Tree": DecisionTreeClassifier(random_state=42),
    "Random Forest": RandomForestClassifier(random_state=42)
}

for name, model in classification_models.items():
    model.fit(X_train, y_train)
    y_pred = model.predict(X_test)
    acc = accuracy_score(y_test, y_pred)

    print(f"\n--- {name} ---")
    print(f"Accuracy: {acc:.4f}")
    print(classification_report(y_test, y_pred, target_names=iris.target_names))

print("=" * 60)
print("PART 2: REGRESSION MODEL (Predicting Continuous Values)")
print("=" * 60)

# For Linear Regression, we use the first 3 features to predict the 4th feature (Petal Width)
X_features = X[:, :3]
y_target = X[:, 3]
X_tr, X_te, y_tr, y_te = train_test_split(X_features, y_target, test_size=0.3, random_state=42)

lin_reg = LinearRegression()
lin_reg.fit(X_tr, y_tr)
y_pred_lr = lin_reg.predict(X_te)

print(f"\n--- Linear Regression (Target: Petal Width) ---")
print(f"Mean Squared Error (MSE): {mean_squared_error(y_te, y_pred_lr):.4f}")
print(f"R-squared (R2 Score): {r2_score(y_te, y_pred_lr):.4f}")
```
<img width="636" height="622" alt="Screenshot 2026-10-26 122453" src="https://github.com/user-attachments/assets/bf637a12-c485-448e-b26e-e4cd99dd6432" />
<img width="672" height="407" alt="Screenshot 2026-10-26 122510" src="https://github.com/user-attachments/assets/b7314d1d-777d-4338-ac26-6dee64d9d9d3" />

## Random Forest Regression
Is an ensemble learning method that combines multiple decision trees to produce more accurate and stable predictions. It can be used for both classification and regression tasks, where regression predictions are obtained by averaging the outputs of several trees.
- Multiple decision trees: Builds many trees and combines their predictions.
- Ensemble approach: Reduces errors compared to a single decision tree.
- Regression prediction: Produces continuous values by averaging predictions from all trees.

### Working of Random Forest Regression
Random Forest Regression works using the bagging (Bootstrap Aggregating) technique:
- Multiple decision trees are trained on different random subsets of the dataset with replacement to train each tree.
- Each tree uses a random subset of features while splitting nodes.
- Due to this each tree learns slightly different data and features, which increases model diversity.
- The final prediction is obtained by averaging the predictions from all decision trees.

### Support Vector Machine
Support Vector Machine (SVM) is a supervised machine learning algorithm used for classification and regression tasks. It tries to find the best boundary known as hyperplane that separates different classes in the data. It is useful when you want to do binary classification like spam vs. not spam or cat vs. dog.

