
# Financial Risk Level Prediction using Supervised Learning

**Lili Zheng**  

## Executive Summary

**Project Overview and Goals:**  
This project aims to develop a reliable and interpretable machine learning system for predicting individuals' financial risk levels based on structured personal and financial data. We use four supervised classification models—Logistic Regression, Decision Tree, Random Forest, and XGBoost—to predict whether an individual falls into **Low**, **Medium**, or **High** financial risk categories.

We compare the models based on **accuracy**, **recall**, and **F1 score** to identify the best-performing model, which is then analyzed further using global and local interpretability techniques such as **feature importance** and **class probability breakdown**.

## Methodology

**Data Source:**  
The dataset, sourced from Kaggle, contains survey-style structured financial and demographic information. Each record includes features like age, income, education, loan status, and credit score, along with a labeled risk rating.

**Preprocessing:**  
- Missing values were handled.
- Categorical variables were label-encoded.
- Credit Score and Age were binned into ordinal categories.
- Train-test split was done (75% training, 25% testing).
- Target variable (`Risk Rating`) was encoded into ordinal labels (0=Low, 1=Medium, 2=High).

**Models Trained:**  
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**
- **XGBoost**

All models were trained on the same dataset and evaluated using the same metrics.

## Model Selection Summary

After comparing all models, **Random Forest** achieved the best performance in terms of overall accuracy, strong recall, and balanced F1 scores across all classes.

| Model               | Accuracy | Recall  | F1 Score |
|--------------------|----------|---------|----------|
| Logistic Regression| ~0.83    | ~0.80   | ~0.81    |
| Decision Tree      | ~0.77    | ~0.75   | ~0.76    |
| Random Forest      | **0.86** | **0.84**| **0.85** |
| XGBoost            | ~0.85    | ~0.83   | ~0.84    |

💡 Based on this analysis, **Random Forest** was selected as the final model for interpretability and application.

## Evaluation of Best Model: Random Forest

### Global Interpretability
Feature importance analysis from the Random Forest model shows that the most influential predictors of financial risk include:
- **Credit Score**
- **Annual Income**
- **Loan Amount**
- **Employment Status**
- **Age Category**

This aligns with financial domain knowledge, enhancing trust and actionability for business use.

### Local Explanation
We also evaluated the prediction probabilities for individual samples to interpret model decisions on a case-by-case basis. This helps understand how confident the model is when assigning a risk label and supports risk management applications.

### Business Implication
This model can help **banks**, **insurers**, and **fintech firms**:
- Pre-screen loan applicants
- Set interest rates based on risk profile
- Recommend financial products more effectively

## Conclusion

The Random Forest model shows excellent predictive performance and interpretability. It captures key financial indicators to make accurate and explainable predictions, making it highly applicable in real-world risk assessment systems.

## Future Work

1. **Model Improvements:**
   - Conduct hyperparameter tuning using GridSearchCV.
   - Implement ensemble techniques combining multiple models.

2. **Fairness and Bias:**
   - Assess bias across demographic groups (e.g., age, gender).

3. **Deployment:**
   - Package the model as an API for integration into web apps or financial services platforms.

4. **Feature Engineering:**
   - Add more granular credit history data and behavioral features.

5. **Explainability:**
   - Add advanced tools like **SHAP** for richer explanations once environment supports it.

## Files

- `Part1_FinancialRiskLevel.ipynb`: Data preparation, EDA, and model training
- `Part2_Evaluation_FinancialRiskLevel.ipynb`: Model evaluation, interpretation, and conclusion
- `financial_risk_assessment.csv`: Dataset used for training and testing
