# Day 16

## Key Learnings

### Supervised Learning

### Linear Regression 
Linear Regression is a fundamental supervised learning algorithm used to model the relationship between a dependent variable and one or more independent variables. It predicts continuous values by fitting a straight line that best represents the data.
- Independent variable (input): Hours studied because it's the factor we control or observe.
- Dependent variable (output): Exam score because it depends on how many hours were studied.

Linear regression uses the independent variable to predict the dependent variable.

### Interpretation of the Best-Fit Line
- Slope (m): The slope indicates how much the dependent variable changes for every one-unit increase in the independent variable. For example, if the slope is 5, then y increases by 5 units for every 1-unit increase in x.
- Intercept (b): The intercept represents the predicted value of y when x = 0. It’s the point where the line crosses the y-axis.

### Types of Linear Regression
### 1. Simple Linear Regression
Simple linear regression is used when we want to predict a target value (dependent variable) using only one input feature (independent variable). It assumes a straight-line relationship between the two.

### 2. Multiple Linear Regression
Multiple linear regression involves more than one independent variable and one dependent variable.

### Logistic Regression 
Logistic Regression is a supervised machine learning algorithm used for classification problems. Unlike linear regression, which predicts continuous values it predicts the probability that an input belongs to a specific class.

### Types
### 1. Binomial Logistic Regression: 
Used when the dependent variable has only two possible categories, such as Yes/No, Pass/Fail, or 0/1. It is the most common type and is used for binary classification tasks.
### 2. Multinomial Logistic Regression: 
Used when the dependent variable has three or more unordered categories. For example, classifying animals as cat, dog, or sheep. It extends logistic regression to handle multiple classes.
### 3. Ordinal Logistic Regression: 
Used when the dependent variable has three or more categories with a natural order, such as Low, Medium, and High. It considers the ranking of categories during prediction.

### Decision Tree 
A decision tree is a supervised learning algorithm used for both classification and regression tasks. It has a hierarchical tree structure which consists of a root node, branches, internal nodes and leaf nodes. It works like a flowchart that helps in making step-by-step decisions, where:
- Internal nodes represent attribute tests
- Branches represent attribute values
- Leaf nodes represent final decisions or predictions.

### 1. Information Gain
Information Gain tells us how useful a question (or feature) is for splitting data into groups. It measures how much the uncertainty decreases after the split. A good question will create clearer groups and the feature with the highest Information Gain is chosen to make the decision.
- Entropy: It is the measure of uncertainty of a random variable, it characterizes the impurity of an arbitrary collection of examples. The higher the entropy more the information content.

### 2. Gini Index
Gini Index is a metric to measure how often a randomly chosen element would be incorrectly identified. It means an attribute with a lower Gini index should be preferred. Sklearn supports “Gini” criteria for Gini Index and by default it takes “gini” value.

### Random Forest
Random Forest is an ensemble learning method that combines multiple decision trees to produce more accurate and stable predictions. It can be used for both classification and regression tasks, where regression predictions are obtained by averaging the outputs of several trees.

### K‑Nearest Neighbor (KNN)
Is a simple and widely used machine learning technique for classification and regression tasks. It works by identifying the K closest data points to a given input and making predictions based on the majority class or average value of those neighbors.
- Classifies data based on similarity with nearby data points
- Uses distance metrics like Euclidean distance to find nearest neighbors

### Naive Bayes 
Is a machine learning classification algorithm that predicts the category of a data point using probability. It assumes that all features are independent of each other. Naive Bayes performs well in many real-world applications such as spam filtering, document categorization and sentiment analysis.

### Support Vector Machine (SVM)
Is a supervised machine learning algorithm used for classification and regression tasks. It tries to find the best boundary known as hyperplane that separates different classes in the data. It is useful when you want to do binary classification like spam vs. not spam or cat vs. dog.


