# Task 5 — Sales Prediction Using Python

## Project Overview
This project builds regression models to predict product sales based on advertising expenditure across TV, Radio, and Newspaper channels. It follows a complete machine learning workflow including data inspection, exploratory data analysis, model training, evaluation, residual analysis, and feature-importance analysis.

## Objective
Build a regression model that predicts product sales based on advertising spend across different media channels (TV, Radio, Newspaper)

## Tech Stack
- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn
- Jupyter Notebook

## Dataset
The Advertising Sales dataset contains 200 observations and four relevant variables:
- `TV` — TV advertising spend
- `Radio` — Radio advertising spend
- `Newspaper` — Newspaper advertising spend
- `Sales` — Product sales

No missing or duplicate rows were found.

## Workflow
Dataset → Data Cleaning → EDA → Train/Test Split → Linear Regression → Random Forest → Model Evaluation → Best Model → Residual Analysis → Feature Importance → Conclusion

## Exploratory Data Analysis
- Null-value and duplicate checks
- Descriptive statistics
- Pairplot of all features
- Sales vs. TV scatter plot
- Sales vs. Radio scatter plot
- Sales vs. Newspaper scatter plot
- Correlation matrix heatmap

## Models
- **Linear Regression** — baseline model
- **Random Forest Regressor** — additional model

Both models were evaluated using MAE, RMSE, and R² score.

## Model Performance

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 1.4608 | 1.7816 | 0.8994 |
| **Random Forest** | **0.6287** | **0.7572** | **0.9818** |

Random Forest achieved the best overall test performance with an R² of **0.9818**, MAE of **0.6287**, and RMSE of **0.7572**.

## Feature Importance
TV advertising had the highest predictive importance, followed by Radio and Newspaper. This represents predictive importance within the Random Forest model and not causal impact.

## Residual Analysis
The residuals were generally scattered around zero without a strong systematic pattern, indicating that the Random Forest model captured the main relationship between advertising spend and sales reasonably well.

## Repository Structure

```text
OIBSIP/
└── DataScience-Task5-SalesPrediction/
    ├── Task5_Sales_Prediction.ipynb
    ├── Advertising.csv
    ├── README.md
    └── outputs/
        ├── model_comparison.csv
        └── figures/
            ├── pairplot.png
            ├── sales_vs_tv.png
            ├── sales_vs_radio.png
            ├── sales_vs_newspaper.png
            ├── correlation_heatmap.png
            ├── residual_plot.png
            └── feature_importance.png
