
# Oil and Gas Prediction Project

## Project Overview

This project aims to develop a predictive model for cumulative oil output over a 12-month period based on data from 6000+ wells operated by 65 operators. The data includes characteristics such as well depth, oil in place, porosity, maturity, and structure derivative. The goal is to help investors and operators make informed decisions about drilling and exploitation of oil and its derivatives, improving production and profitability in the industry.

## Motivation

The oil and gas industry is a crucial part of the global economy, with revenues of over $7 trillion in 2022. Predictive analysis of oil production can be a valuable tool for investors and operators to make more informed decisions and improve overall production.

## Data Description & Pre-processing

The dataset consists of 6,098 observations and 23 variables, including the response variable, CumOil12Month. The independent variables can be grouped into three categories:
- **Completion**: Variables related to the completion of the well.
- **Geology**: Variables related to the geology of the reservoir.
- **Well spacing**: Variables related to the spacing of the well.

### Missing Data Handling

We used the Multivariate Imputation with Chained Equations (MICE) method to handle missing data. This advanced method accounts for uncertainty by iteratively replacing each missing data point with multiple plausible values.

### Data Transformation

Several transformations were applied to the data, including the addition of indicator variables for missing values, the removal of outliers, and the log transformation of the response variable to weigh errors from wells more evenly.

## Exploratory Data Analysis (EDA)

Initial explorations involved scatter plots, histograms, and correlograms to investigate distributions and relationships between variables. We also performed time series analysis based on completion dates.

## Modeling

### Baseline Model

A linear regression model was used as a baseline. This simple model provided a starting point for comparison and evaluation purposes.

### Regularized Models

Lasso and Ridge regressions were implemented to minimize out-of-sample errors and balance overfitting and underfitting. These models were cross-validated to identify the best hyperparameters.

### Tree-based Models

We developed several tree-based models, including Decision Trees, Random Forests, Extra Trees and XGBoost, to capture non-linear relationships and interactions between variables. Hyperparameters were fine-tuned using GridSearchCV.

## Results

The XGBoost model achieved the best performance, with a testing R-squared of 0.5106. The detailed comparison of model performances is included in the final report.

## Files

- **Oil and Gas Prediction.pdf**: The final report detailing the entire project.
- **Data/**: The directory containing the dataset used in the project.
- **Exploratory Data Analysis.pdf**: Additional project documentation.

## How to Run the Code

1. Clone the repository:
    ```sh
    git clone https://github.com/pianissix7mo/Oil-and-Gas-Prediction.git
    ```
2. Navigate to the project directory:
    ```sh
    cd Oil-and-Gas-Prediction
    ```
3. Ensure you have the required Python packages installed. You can use the `requirements.txt` file if available:
    ```sh
    pip install -r requirements.txt
    ```
4. Run the Jupyter notebooks or Python scripts in the repository to see the analysis and model training steps.

## Contributors

- Mofei Wang
- Shaoyi Li
- Sun Kim
- Christoph Wippel
- Benito D Isaac

