
# Employee Turnover Prediction & Retention Strategy

## Problem

Employee turnover leads to increased hiring costs, lost productivity, and disruption in team performance.
The goal of this project is to not only predict which employees are likely to leave, but also identify why and recommend targeted retention strategies.

## Objective

* Build a machine learning model to predict employee turnover
* Identify key drivers of attrition
* Segment employees by risk level
* Provide actionable retention strategies based on predicted risk

## Dataset

* HR employee dataset
* Features include satisfaction level, evaluation scores, workload (projects, hours), tenure, department, and salary

## Tools & Technologies

* Python (Pandas, NumPy)
* Scikit-learn
* Matplotlib / Seaborn
* Jupyter Notebook

---

## Approach

### Exploratory Data Analysis (EDA)

* Analyzed relationships between satisfaction, workload, and turnover
* Identified workload imbalance patterns (underutilized vs overworked employees)
* Used correlation analysis and visualizations to understand key drivers

## Visualizations

### Correlation Heatmap
![Correlation Heatmap](turnover_heatmap.png)

The heatmap shows how different features relate to employee turnover.

---

### Project Count by Employee Turnover
![Project Count](turnover_project_count.png)

Employees with very low or very high project counts show higher turnover patterns.

---

### ROC Curve Comparison
![ROC Curve](turnover_roc_curve.png)

This compares model performance and shows how well each model predicts employee turnover.
### Key EDA Insights

* Employees working too few or too many projects had higher turnover
* Lower satisfaction levels strongly correlated with attrition
* Workload and performance metrics are interconnected drivers

---

### Modeling

* Built multiple classification models:

  * Logistic Regression
  * Random Forest
  * Gradient Boosting

* Applied 5-fold cross-validation

* Evaluated models using precision, recall, and F1-score

### Metric Selection

Recall was prioritized because the business goal is to minimize missed turnover cases.
Failing to identify at-risk employees results in lost opportunities for intervention.

### Model Performance

* Logistic Regression: Recall = 82%
* Gradient Boosting: Recall = 94%
* Random Forest: Recall = 97% (Best Model)

Random Forest was selected due to its ability to capture the highest number of at-risk employees.

---

## Risk Segmentation Strategy

Employees were segmented based on predicted turnover probability:

* **Safe (Green): < 20%**
* **Low Risk (Yellow): 20% – 60%**
* **Medium Risk (Orange): 60% – 90%**
* **High Risk (Red): > 90%**

This allows the company to move from reactive to proactive retention planning.

---

## Recommendations & Business Actions

### Safe Zone (Green)

Employees are stable but should not be ignored

* Maintain engagement through recognition and growth opportunities
* Continue performance support and career progression

### Low Risk (Yellow)

Early signs of disengagement

* Increase manager check-ins
* Provide career development opportunities
* Improve team involvement and engagement

### Medium Risk (Orange)

Clear signs of potential turnover

* Identify dissatisfaction drivers (role fit, workload)
* Adjust workload and improve work-life balance
* Introduce targeted retention conversations

### High Risk (Red)

Employees are highly likely to leave

* Implement personalized retention plans
* Reassess compensation, role alignment, or team placement
* Act immediately to prevent loss of high-value employees

---

## Business Impact

* Enables early identification of at-risk employees
* Supports targeted retention strategies instead of one-size-fits-all approaches
* Reduces hiring and training costs
* Improves workforce stability and productivity

---

## Key Takeaway

This project goes beyond prediction by combining machine learning with actionable business strategy, helping organizations make smarter, data-driven decisions about employee retention.
