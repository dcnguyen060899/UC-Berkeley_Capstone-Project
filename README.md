# UC-Berkeley_Capstone-Project - Final Report to Stakeholders

## Objective
The goal of this analysis was to predict the length of stay (LOS) for hospital patients and identify the key factors influencing these predictions. By understanding these factors, we aim to optimize hospital resource allocation, improve patient care, and enhance operational efficiency.

## Data Overview
The dataset contains 31,844 records with 18 features, including:
- Demographic information (e.g., Age, City Code)
- Hospital-specific information (e.g., Hospital Type, Ward Type)
- Clinical information (e.g., Severity of Illness, Type of Admission)
- Length of Stay (target variable)

## Data Preprocessing
- Handled missing values in `Bed Grade` and `City_Code_Patient` by imputing the mode.
- Converted categorical variables using one-hot encoding.
- Mapped `Stay` to numerical values for modeling purposes.

## Exploratory Data Analysis
### Key Findings:
1. **Length of Stay Distribution**: The target variable `Stay` shows a right-skewed distribution with most patients staying between 0-10 days.
2. **Correlation Matrix**: Identified moderate correlations between `Stay` and features like `Admission_Deposit`, `Visitors with Patient`, and `Age`.

### Visualizations:
- **Correlation Heatmap**: Showed relationships between features and the target variable.
- **Feature Distributions**: Plotted histograms and scatter plots to understand the distribution and relationships of key features with `Stay`.

## Modeling
### Baseline Model:
- **Linear Regression**: Achieved an R-squared value of 0.394, indicating moderate predictive power.

### Advanced Models:
- **Random Forest Regressor**:
  - Mean Absolute Error: 11.77
  - R-squared: 0.438
- **Gradient Boosting Regressor**:
  - Mean Absolute Error: 11.50
  - R-squared: 0.458
- **XGBoost Regressor**:
  - Mean Absolute Error: 11.51
  - R-squared: 0.454

### Feature Importance:
- Identified `Visitors with Patient`, `Ward_Type_Q`, and `Admission_Deposit` as key features influencing LOS.

## SHAP Analysis
### SHAP Values:
- Provided insights into the impact of each feature on individual predictions.
- Key Features:
  - **Visitors with Patient**: Strongly correlated with longer stays.
  - **Ward_Type_Q**: Associated with shorter stays.
  - **Severity of Illness** and **Type of Admission**: Significant clinical predictors.

## Cluster Analysis
### PCA and K-Means Clustering:
- Performed PCA for dimensionality reduction and K-Means clustering to group patients.
- Identified three clusters with distinct characteristics in terms of LOS, Ward Type, and number of visitors.

### Cluster Insights:
- **Cluster 0**: Longest average stay, balanced presence of Ward_Type_Q.
- **Cluster 1**: Intermediate stay length, fewer patients in Ward_Type_Q.
- **Cluster 2**: Shortest average stay, distinct patient characteristics.

## Policy Simulation: Visitor Management
- **Visitor Threshold**: Simulated a policy limiting visitors to 5 or fewer.
- **Impact**:
  - Reduced total LOS by approximately 10.53%.
  - Highlights the potential of visitor management in optimizing hospital stays.

## Recommendations
1. **Enhance Social Support**:
   - Implement programs to increase visitor engagement and support for patients.
2. **Optimize Ward Practices**:
   - Analyze ward-specific protocols to identify best practices and areas for improvement.
3. **Focus on Critical Clinical Features**:
   - Prioritize resources and attention to patients with severe illnesses or traumatic admissions to optimize their stay and recovery process.

## Conclusion
The analysis provides a comprehensive understanding of the factors influencing hospital length of stay. By leveraging these insights, healthcare providers can improve patient outcomes and hospital efficiency through targeted interventions and optimized practices. Implementing visitor management policies and optimizing ward-specific practices can significantly reduce LOS, benefiting both patients and hospital operations.

## Visual Attachments
The following visualizations support the findings and recommendations:
1. **Correlation Heatmap**: Illustrates relationships between features and LOS.
2. **SHAP Summary Plots**: Visualize the impact of key features on LOS predictions.
3. **Cluster Analysis Plots**: Highlight distinct patient groups based on LOS, Ward Type, and visitors.
4. **Policy Simulation Charts**: Show the potential impact of visitor management on reducing LOS.

Thank you for your attention. I am available for any questions or further discussions on the findings and recommendations.

---
**Data Scientist**
[Duy Nguyen]
