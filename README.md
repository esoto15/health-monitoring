# Understanding Stress Predictors Among Students Using Machine Learning and Explainable AI

## Dependencies
[![Pandas](https://img.shields.io/badge/pandas-1.3.3-blue)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-1.21.4-blue)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/matplotlib-3.4.3-blue)](https://matplotlib.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-0.24.2-blue)](https://scikit-learn.org/)
[![SciPy](https://img.shields.io/badge/scipy-1.7.3-blue)](https://www.scipy.org/)

## How to Run
1. Clone the repository.
2. Ensure dependencies are installed (`pip install -r requirements.txt`).
3. Run `python main.py`.

## Abstract
As student stress levels continue to rise, identifying and understanding the underlying causes is essential for promoting academic success and mental well-being. 
This project leverages machine learning and explainable AI (XAI) to analyze a wide range of factors impacting student stress, such as self-esteem, mental health history, social dynamics, and academic pressures. 
Unlike traditional models, which may offer limited interpretability, our approach prioritizes transparency, enabling us to pinpoint the most influential predictors of stress in a clear, interpretable manner. 
By uncovering these key stress drivers, this research aims to provide valuable insights for educational institutions to develop targeted interventions and foster a more supportive learning environment for students.

## Feature Selection
We applied ANOVA (Analysis of Variance) and the Chi-Square Test to identify the most significant features associated with the target variable, stress_level. Both tests assess the relationship between each feature and the target, with higher scores indicating stronger associations.

The results from both tests highlighted sleep quality and blood pressure as the most significant features. These two variables showed the highest scores, suggesting they are strongly correlated with stress levels in the dataset.

## Predictive Modeling Assessment
We assessed the performance of three models—Linear Regression, Decision Tree Regressor, and Random Forest Regressor—using R-Squared (R²), Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE). These metrics were applied to the actual and predicted results from each model.

The Linear Regression model achieved an R² value of 0.67, with a MAE of 0.33, an MSE of 0.22, and an RMSE of 0.47. While the model explained 67% of the variance in the target variable, the error metrics indicated that it was not as effective in predicting stress levels compared to the other models.

The Decision Tree Regressor delivered a stronger performance, with an R² of 0.82, a MAE of 0.14, an MSE of 0.12, and an RMSE of 0.35. These results suggested that the Decision Tree model was much better at capturing the complexity of the data, showing improved accuracy over Linear Regression in all metrics.

The Random Forest Regressor showed similar results to the Decision Tree Regressor, with an R² value of 0.82, a MAE of 0.14, an MSE of 0.12, and an RMSE of 0.35. These results reinforced the robust predictive power of the Random Forest model, which is well-suited for handling more complex datasets due to its ensemble learning approach.

In conclusion, both the Decision Tree Regressor and Random Forest Regressor outperformed Linear Regression in terms of predictive accuracy, with Random Forest slightly edging out Decision Tree in general robustness. Given the similar performance between Decision Tree and Random Forest, either could be used, with Random Forest offering the added benefit of being less prone to overfitting.

## SHAP (SHapley Additive exPlanations)
This section delves into SHAP (SHapley Additive exPlanations) analysis, uncovering how individual features impact our models' predictions. SHAP values serve as a unified measure of feature importance.
![image](https://github.com/user-attachments/assets/a93e7d78-3957-4474-a7a0-bd2c5caa185e)

This SHAP summary plot shows the impact of sleep_quality and blood_pressure on the model's predictions. Each point represents a data instance, with the x-axis indicating SHAP values (feature impact on the prediction) and color showing feature values (blue for high, pink for low). For sleep_quality, high values generally push the prediction higher, while low values decrease it. The effect of blood_pressure is more varied, with both high and low values affecting the prediction in mixed directions. Overall, sleep_quality has a more consistent influence, while blood_pressure shows a more distributed impact across different SHAP values.
