# House Price Prediction Analysis

This repository contains the deliverables for the **House Price Prediction** regression modeling project, completed during Week 1 of the data science internship at XYlofy.

## 🎯 Problem Statement
Real estate buyers and sellers often rely on guesswork or outdated comparisons to estimate a property's fair value. The goal of this project is to build a regression model that predicts house prices based on physical property features—such as size, number of rooms, location, amenities, and furnishing status—and identify which features most strongly influence the price.

## 📦 Dataset
The dataset utilized is Housing.csv, consisting of 545 residential properties with 13 features:
- **Numerical Features**: rea (square footage), edrooms, athrooms, stories, parking.
- **Binary/Categorical Features**: mainroad, guestroom, asement, hotwaterheating, irconditioning, prefarea, urnishingstatus.

## 🛠️ Requirements & Installation
To run this project locally, ensure you have Python 3.x installed along with the following packages:
`ash
pip install pandas numpy scikit-learn matplotlib seaborn reportlab nbformat ipykernel
`

## 🚀 How to Execute
To regenerate the analysis, charts, executed notebook, and PDF report, run:
`ash
python build_project.py
`
Alternatively, you can open and run the Jupyter notebook nalysis.ipynb cell-by-cell.

## 📊 Model Performance Comparison
An 80/20 train/test split was used. We trained a **Multiple Linear Regression** model and a **Random Forest Regressor**:

| Evaluation Metric | Linear Regression (Best Fit) | Random Forest Regressor |
| :--- | :--- | :--- |
| **Mean Absolute Error (MAE)** | ,043.40 | ,022,560.05 |
| **Root Mean Squared Error (RMSE)** | ,324,506.96 | ,401,496.84 |
| **R² Score (Variance Explained)** | **0.6529** | **0.6114** |

### Key Findings
1. **Dominant Feature**: The physical size of the property (rea) is the strongest price driver, accounting for ~46.8% of the Random Forest feature importance.
2. **Layout Preferences**: The count of athrooms is over **twice as important** as edrooms (15.2% vs 6.4%). Adding bathrooms is significantly more lucrative than simply adding bedrooms.
3. **Comfort Amenities**: The presence of irconditioning is a powerful price driver (~6.3% importance).
4. **Model Choice**: Linear Regression achieved a higher ^2$ score (.6529$) than Random Forest (.6114$), showing that housing relationships are largely linear and parametric models generalize better on this sample size.

## 📁 Repository Structure
- [analysis.ipynb](analysis.ipynb): The complete Jupyter Notebook with loaded data, cleaning steps, training code, evaluations, and visualizations.
- [Housing.csv](Housing.csv): Sourced Kaggle dataset.
- [summary.pdf](summary.pdf): A beautifully structured 1-page PDF report compiling results and strategic recommendations.
- [charts/](charts/): Folder containing all 4 generated PNG charts:
  - price_distribution.png: Histogram showing house price distribution.
  - correlation_heatmap.png: Correlation matrix of features with price.
  - ctual_vs_predicted.png: Scatter plot comparing model predictions.
  - eature_importance.png: Feature weight importance scores bar chart.
