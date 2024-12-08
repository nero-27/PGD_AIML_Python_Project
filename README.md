# PGD_AIML_Python_Project
Salifort Motors Project

# Salifort Motors Employee Retention Analysis

This project analyzes employee retention at Salifort Motors using a dataset containing various employee-related metrics. The goal is to understand the factors contributing to employee turnover and build a predictive model to classify whether an employee is likely to leave.

## Dataset Overview

The dataset contains the following columns:

| Column Name            | Values              | Description                                                                 |
|------------------------|---------------------|-----------------------------------------------------------------------------|
| `satisfaction_level`   | 0 to 1              | Employee satisfaction level (0 = not satisfied, 1 = very satisfied).        |
| `last_evaluation`      | 0 to 1              | Employee's last evaluation score.                                           |
| `number_project`       | Positive Integer    | Number of projects completed by the employee.                               |
| `average_monthly_hours`| Positive Integer    | Average monthly hours spent by the employee.                                |
| `time_spend_company`   | Positive Integer    | Number of years the employee has spent at the company.                      |
| `work_accident`        | 0 or 1              | Whether the employee had a work-related accident (0 = no, 1 = yes).         |
| `promotion_last_5years`| 0 or 1              | Whether the employee was promoted in the last 5 years (0 = no, 1 = yes).    |
| `department`           | Class (e.g., Sales)| Department of the employee.                                                 |
| `salary`               | low, medium, high  | Employee's salary bracket.                                                  |
| `left`                 | 0 or 1              | Target variable: 0 = stayed, 1 = left.                                      |

## Project Steps

1. **Data Exploration and Cleaning**  
   - Inspected dataset structure and checked for missing values and duplicates.
   - Renamed columns to follow a standardized naming convention.
   - Removed duplicate rows to ensure data consistency.

2. **Exploratory Data Analysis (EDA)**  
   - Analyzed the distribution of key variables using boxplots and histograms.
   - Examined relationships between features and the target variable (`left`).
   - Visualized key trends such as project hours vs. retention.

3. **Model Building**  
   - Built a predictive model using the `XGBoost` classifier to classify whether an employee is likely to leave.
   - Created new features, including the project-to-hours ratio, to enhance the model's predictive power.
   - Used one-hot encoding for categorical variables (e.g., `salary`).

4. **Evaluation**  
   - Evaluated the model on accuracy, precision, recall, and F1 score:
     - **Accuracy**: 97.87%
     - **Precision**: 95.78%
     - **Recall**: 91.20%
     - **F1 Score**: 93.43%
   - Plotted the confusion matrix to visualize classification performance.

## Tools and Technologies

- **Programming Language**: Python
- **Libraries**: 
  - Data Analysis: `pandas`, `NumPy`
  - Visualization: `matplotlib`, `seaborn`
  - Machine Learning: `XGBoost`, `sklearn`
- **Data Handling**: Preprocessing and cleaning using Python.
- **Model Evaluation**: Metrics such as accuracy, precision, recall, and F1 score.

## Results and Insights

- High satisfaction levels correlate strongly with retention.
- Employees with excessively high or low project workloads are more likely to leave.
- Time spent at the company shows a nonlinear relationship with turnover.

