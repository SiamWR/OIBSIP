# Car Price Prediction with Machine Learning

## Project Overview

This project builds regression models to predict used car selling prices based on vehicle characteristics such as brand, age, mileage, fuel type, and transmission.

The project follows an end-to-end machine learning workflow including data cleaning, feature engineering, exploratory data analysis, model training, comparison, and evaluation.

---

## Dataset

**Dataset:** Car Details v3 (Vehicle Dataset from Cardekho)

The dataset contains used car information including:

- Car name
- Manufacturing year
- Selling price
- Kilometers driven
- Fuel type
- Transmission
- Mileage
- Engine details
- Power
- Seats

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Workflow

### 1. Data Cleaning
- Handled missing values
- Removed duplicate records
- Standardized inconsistent categorical values

### 2. Feature Engineering
- Calculated car age from manufacturing year
- Extracted car brand from the car name
- Converted mileage and vehicle specifications into usable numerical features

### 3. Exploratory Data Analysis
Performed analysis using:

- Selling price distribution
- Selling price vs fuel type analysis
- Selling price vs car age relationship
- Feature correlation heatmap

### 4. Machine Learning Models

Trained and compared:

- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor

### 5. Model Evaluation

Models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### 6. Feature Importance Analysis

Identified the most influential features affecting car selling prices.

---

## Results

Multiple regression models were trained and compared using standard regression evaluation metrics. The best-performing model is "Random Forest Regressor",  was selected based on the R² score.

---

## How to Run

1. Clone/download this repository.
2. Install required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
