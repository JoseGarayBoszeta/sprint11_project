# sprint11_project
# Insurance Data Analysis Project

## Overview
This project involves analyzing insurance customer data to solve several machine learning tasks for Sure Tomorrow insurance company. The project explores techniques for finding similar customers, predicting insurance benefits, implementing regression models, and protecting customer data through obfuscation.

## Dataset
The dataset contains insurance customer information including:
- Gender
- Age
- Income
- Family members
- Insurance benefits received

## Tasks

### 1. Finding Similar Customers
Implemented a k-Nearest Neighbors algorithm to find similar customers:
- Compared scaled vs. unscaled data
- Tested Euclidean and Manhattan distance metrics
- Found that scaling was crucial for accurate similarity measurement

### 2. Customer Benefit Prediction
Built a classification model to predict whether a customer will receive an insurance benefit:
- Implemented kNN classification with different k values
- Compared against random baseline models
- Addressed class imbalance through:
  - Undersampling the majority class
  - Using distance-weighted kNN
- Found that distance-weighted kNN with scaled data performed best (F1=0.95)

### 3. Benefit Amount Prediction
Developed a linear regression model to predict the amount of insurance benefits:
- Implemented linear regression using normal equations
- Analyzed feature importance
- Found that age had the strongest positive influence on benefits
- Achieved R² = 0.42, indicating moderate predictive power

### 4. Data Privacy Protection
Implemented and tested a data obfuscation technique:
- Developed matrix transformation approach (X' = XP)
- Proved analytically that obfuscation doesn't affect linear regression performance
- Verified computationally that predictions remain identical
- Demonstrated recovery of original data is possible with the transformation key
- Showed that individual customer details are effectively obscured

## Key Insights
- Feature scaling is essential for distance-based algorithms like kNN
- Class imbalance can significantly affect model performance
- Linear regression with OLS isn't affected by feature scaling
- Matrix transformation provides an effective way to protect customer data without sacrificing model performance

## Technologies Used
- Python
- NumPy, Pandas
- scikit-learn
- Matplotlib/Seaborn

## Project Structure
- `insurance_analysis.ipynb`: Main notebook containing all analysis
- `data/insurance_us.csv`: Dataset (not included in repo)
- `README.md`: Project documentation
