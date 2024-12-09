
# InsNova Auto Insurance Claim Prediction

## Overview

This project focuses on analyzing and predicting auto insurance claims using advanced statistical models and machine learning techniques. The objective is to build robust models for predicting the frequency and severity of insurance claims, leveraging datasets containing various policyholder and vehicle attributes. The project includes techniques like **Poisson Regression**, **Multiple Linear Regression (MLR)**, and **Variable Selection** to evaluate and improve the predictive performance of models.

---

## Table of Contents

1. [Objective](#objective)  
2. [Dataset Description](#dataset-description)  
3. [Technologies Used](#technologies-used)  
4. [Methodology](#methodology)  
5. [Project Structure](#project-structure)  
6. [How to Run](#how-to-run)  
7. [Key Findings](#key-findings)  
8. [Future Enhancements](#future-enhancements)  

---

## Objective

The primary goals of this project are:  
- Predict the frequency and severity of insurance claims based on historical data.  
- Identify key factors influencing claim costs and develop actionable insights for risk management.  
- Optimize model performance using variable selection and evaluation metrics.

---

## Dataset Description

### Data Sources:
- **Training Dataset**: Contains detailed information about policyholders, vehicles, and claims.  
- **Test Dataset**: Used to validate the model's predictive performance.

### Key Variables:
- `veh_value`: Vehicle value.  
- `exposure`: Coverage exposure period.  
- `claimcst0`: Claim costs.  
- `numclaims`: Number of claims filed.  
- Categorical variables like `gender`, `veh_body`, `veh_color`, `agecat`, `area`, etc.

---

## Technologies Used

### Programming Languages:
- **R**: Data analysis, visualization, and modeling.

### Libraries:
- `ggplot2`, `dplyr`, `caret`, `e1071`

---

## Methodology

### 1. Data Cleaning and Preprocessing:
- Missing values imputed and categorical variables converted to factors.  
- Data split into training and test sets for cross-validation.

### 2. Modeling Techniques:
- **Poisson Regression**: To model claim frequency.  
- **Inverse Gaussian Regression**: To predict claim severity.  
- **Multiple Linear Regression (MLR)**: To predict overall claim costs.  
- **Variable Selection**: Forward, backward, and stepwise selection to optimize the regression model.

### 3. Evaluation Metrics:
- Normalized Gini Coefficient.  
- Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC).  
- Residual and diagnostic plots to evaluate model fit.

---

## Project Structure

```
InsNova_Auto_Insurance_Claim_Prediction/
├── data/
│   ├── InsNova_data_2023_train.csv
│   ├── InsNova_data_2023_vh.csv
├── scripts/
│   ├── InsNova_Auto_Insurance_Claim_Prediction_Frequency_Severity_Model.Rmd
│   ├── InsNova_Auto_Insurance_Claim_Prediction_MLR.Rmd
│   ├── InsNova_Auto_Insurance_Claim_Prediction_Variable_Selection.Rmd
├── reports/
│   ├── InsNova_Auto_Insurance_Claim_Prediction_Frequency_Severity_Model.pdf
│   ├── InsNova_Auto_Insurance_Claim_Prediction_MLR.pdf
│   ├── InsNova_Auto_Insurance_Claim_Prediction_Variable_Selection.pdf
├── README.md
```

---

## How to Run

### Prerequisites:
1. **Install R**:
   Download and install R from [CRAN](https://cran.r-project.org/).  
2. **Install Required Libraries**:
   Run the following command in R:
   ```R
   install.packages(c("ggplot2", "dplyr", "caret", "e1071"))
   ```

---

### Steps:

#### Run R Scripts:
1. Open each `.Rmd` file in RStudio:
   - `InsNova_Auto_Insurance_Claim_Prediction_Frequency_Severity_Model.Rmd`
   - `InsNova_Auto_Insurance_Claim_Prediction_MLR.Rmd`
   - `InsNova_Auto_Insurance_Claim_Prediction_Variable_Selection.Rmd`

2. Execute the scripts to perform analysis, build models, and generate reports.

3. Render the reports in HTML format using the `Knit` button in RStudio.

---

## Key Findings

1. **Claim Frequency**:
   - Poisson regression revealed that `exposure` and `veh_value` were significant predictors of claim frequency.  
   - Normalized Gini coefficient: **0.2868**.

2. **Claim Severity**:
   - Inverse Gaussian regression indicated that `gender`, `veh_age`, and `area` significantly impact claim severity.

3. **MLR Analysis**:
   - Forward and backward selection optimized the model by identifying key predictors like `exposure`, `veh_age`, and `driving_history_score`.

---

## Future Enhancements

1. Incorporate external factors like economic conditions or weather data to improve prediction accuracy.  
2. Apply machine learning models (e.g., Random Forest, Gradient Boosting) for comparison with regression models.  
3. Develop a dashboard to visualize claim predictions and key metrics interactively.  

