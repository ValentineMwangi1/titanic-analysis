# titanic-analysis

---

## Project Objectives

- Understand the Titanic dataset and its features
- Perform thorough data cleaning
- Explore how different features relate to survival
- Build and evaluate a machine learning model (logistic regression)
- Derive actionable insights from the results

---

##  Dataset Description

This dataset includes data for passengers on the Titanic. Below are the key columns used:

| Feature       | Description                                       |
|---------------|---------------------------------------------------|
| Survived      | Target variable (0 = No, 1 = Yes)                 |
| Pclass        | Passenger Class (1 = 1st, 2 = 2nd, 3 = 3rd)       |
| Name          | Name of the passenger                             |
| Sex           | Gender                                            |
| Age           | Age in years                                      |
| SibSp         | Siblings/spouses aboard                           |
| Parch         | Parents/children aboard                           |
| Ticket        | Ticket number                                     |
| Fare          | Ticket fare                                       |
| Cabin         | Cabin number (many missing values)                |
| Embarked      | Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

##  Step 1: Data Cleaning

Performed the following:

- Dropped irrelevant columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Filled missing `Age` with **median**
- Filled missing `Embarked` with **mode**
- Converted categorical features:
  - `Sex`: male → 0, female → 1
  - `Embarked`: S → 0, C → 1, Q → 2

---

## Step 2: Exploratory Data Analysis (EDA)

Using `seaborn` and `matplotlib`, we explored:

- **Survival by gender**: Females had higher survival rates
- **Survival by class**: 1st-class passengers survived more
- **Age distribution**: Survivors tended to be younger
- **Correlation heatmap**: Found relationships between variables

Visualizations used:
- Countplots for gender, class, and embarked
- Age histogram
- Correlation heatmap

---

## Step 3: Model Building (Logistic Regression)

Used **Logistic Regression** from `scikit-learn`.

- Selected features: `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`
- Split data into **80% training** and **20% testing**
- Trained logistic regression model

---

## Step 4: Model Evaluation

Model was evaluated using:

- **Accuracy**: ~78%
- **Confusion matrix**: TP, FP, TN, FN breakdown
- **Classification report**: Precision, recall, F1-score

---

## Key Insights

- **Sex** and **Pclass** are the strongest survival predictors
- Being female and/or in first class increased survival chances significantly
- Logistic regression gives decent baseline performance; other models like Random Forest or XGBoost could improve results

---

##  Tools Used

- **Python**
- **Pandas** & **NumPy** for data handling
- **Seaborn** & **Matplotlib** for EDA
- **Scikit-learn** for ML modeling
- **Jupyter Notebook / Google Colab** for development

---

##   Author
Valentine Njeri
Nairobi, Kenya
 Aspiring Data Analyst | Skilled in Python, Excel, Power BI & Data Visualization
Open to internships and remote opportunities
Email: njerivalentine6@gmail.com
