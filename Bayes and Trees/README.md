# NTHU Machine Learning Projects

This repository contains implementations of machine learning models for medical data classification tasks, including custom implementations of various algorithms and comprehensive analyses of results.

## Projects Overview

### 1. Patient Treatment Classification

In this project, I implemented and analyzed tree-based models to classify patients based on hematological parameters:

**What I did:**
- Implemented Decision Tree, Random Forest, and Gradient Boosting models
- Performed parameter tuning using GridSearchCV to find optimal model configurations
- Conducted feature importance analysis to identify the most influential blood markers
- Applied feature selection techniques to create more efficient models
- Compared performance between models with default parameters, tuned parameters, and selected features

**What I learned:**
- Parameter tuning significantly improves simple models like decision trees (+6% accuracy)
- Random Forest provides the best balance of performance and robustness for this dataset
- Feature selection can enhance or reduce performance depending on the model type
- THROMBOCYTE count is the most important predictor for treatment classification

**Key Results:**
- Random Forest achieved the best performance (0.74 accuracy with feature selection)
- Gradient Boosting was less sensitive to parameter tuning than other models
- Decision Trees benefited most from parameter optimization

### 2. Prescription Prediction

In this project, I built custom implementations of Naive Bayes and Decision Tree algorithms from scratch:

**What I did:**
- Implemented Naive Bayes and Decision Tree classifiers without using external libraries
- Applied information theory concepts (entropy, information gain) for decision tree construction
- Analyzed model performance on prescription prediction based on symptoms
- Visualized the decision tree structure to understand the classification logic

**What I learned:**
- Naive Bayes outperforms Decision Trees for this small medical dataset (0.67 vs 0.33 accuracy)
- The "naive" assumption of feature independence works well for this medical context
- Dataset size significantly impacts model performance, especially for complex models
- Decision trees struggle with small datasets due to overfitting
- Information gain effectively identifies the most relevant features for classification

**Key Findings:**
- Weight Loss was identified as the most informative feature for prescription decisions
- With limited data, simpler models (Naive Bayes) often outperform more complex ones
- The entropy of the prescription variable was 0.985, showing high initial uncertainty

## Repository Contents

- `HW (Bayes and Trees)/`
  - `Patient Treatment/`
    - `112031508_Decision_Tree.ipynb`: Decision tree implementation and analysis
    - `112031508_Gradient_Boosting.ipynb`: Gradient boosting implementation and analysis
    - `112031508_Naive_Bayes.ipynb`: Naive Bayes implementation
    - `112031508_Random_Forest.ipynb`: Random forest implementation and analysis
    - `training_set.csv`: Hematological dataset for patient treatment
  - `Prescription Prediction/`
    - `112031508_HW_answers.pdf`: Homework submission
    - `11320BAI500200_HW_Bayes_Tree.pdf`: Project description and requirements

## Model Performance Summary

| Project | Model | Accuracy | Key Insight |
|---------|-------|----------|-------------|
| Patient Treatment | Decision Tree (Default) | 0.64 | Prone to overfitting |
| Patient Treatment | Decision Tree (Tuned) | 0.70 | +6% improvement with tuning |
| Patient Treatment | Random Forest | 0.74 | Best overall performance |
| Patient Treatment | Gradient Boosting | 0.72 | Strong baseline performance |
| Prescription | Naive Bayes | 0.67 | Works well with feature independence |
| Prescription | Decision Tree | 0.33 | Limited by small dataset size |

## Technical Skills Demonstrated

- Custom implementation of machine learning algorithms
- Application of information theory concepts
- Feature importance analysis and feature selection
- Parameter tuning and model optimization
- Handling categorical data in machine learning
- Model comparison and evaluation techniques
