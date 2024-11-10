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
