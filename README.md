# SCT_DS_3
# Bank Marketing Decision Tree Classifier

##  Project Overview
This project builds and evaluates a **Decision Tree Classifier** to predict whether a customer will subscribe to a **term deposit** based on their **demographic and behavioral attributes**.

The analysis uses the **Bank Marketing dataset** and includes **data preprocessing, visualization, model training, evaluation, and interpretation**.

---

##  Objective
To predict the target variable:

- **`deposit`**
  - `yes` → Customer subscribed to the term deposit
  - `no` → Customer did not subscribe

---

##  Dataset Description

- **Dataset Name:** Bank Marketing Dataset
- **Number of Records:** 11,162
- **Number of Features:** 16
- **Target Variable:** `deposit`
- **Data Source:** UCI Machine Learning Repository

###  Features
| Feature | Description |
|------|------------|
| age | Age of the customer |
| job | Type of job |
| marital | Marital status |
| education | Education level |
| default | Credit in default |
| balance | Average yearly balance |
| housing | Housing loan |
| loan | Personal loan |
| contact | Contact communication type |
| day | Last contact day |
| month | Last contact month |
| duration | Call duration |
| campaign | Number of contacts during campaign |
| pdays | Days since last contact |
| previous | Number of previous contacts |
| poutcome | Outcome of previous campaign |

---

##  Technologies Used
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

---

##  Data Preprocessing Steps
1. Loaded CSV file with correct delimiter
2. Verified dataset shape and column names
3. Handled categorical variables using **Label Encoding**
4. Encoded target variable (`deposit`: no → 0, yes → 1)
5. Checked class imbalance
6. Split data into training and testing sets with stratification

---

##  Exploratory Data Analysis (EDA)
The following visualizations were performed:

- Target class distribution
- Age vs Deposit subscription
- Balance vs Deposit
- Campaign calls vs subscription
- Duration vs subscription
- Correlation heatmap
- Feature importance visualization

---

##  Model Building

### Decision Tree Classifier
- Baseline Decision Tree
- Depth-controlled Decision Tree
- Class-weighted Decision Tree
- Hyperparameter tuned Decision Tree

Key parameters explored:
- `max_depth`
- `min_samples_split`
- `class_weight`

---

##  Model Evaluation Metrics
The models were evaluated using:

- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1-score
- ROC–AUC Score
- Cross-validation accuracy

### Best Model Performance
| Metric | Value |
|------|------|
| Accuracy | ~89% |
| ROC–AUC | ~0.87 |
| Precision (Yes) | ~0.63 |
| Recall (Yes) | ~0.42 |

---

##  Feature Importance
The most influential features in predicting subscription:

1. **duration**
2. **pdays**
3. **previous**
4. **campaign**
5. **balance**

---

##  Model Interpretation
- Longer call durations significantly increase the probability of subscription
- Fewer campaign calls are associated with higher success
- Previous successful contacts improve conversion chances

---

##  Prediction Example

```python
Prediction: YES
Probability: 77%
