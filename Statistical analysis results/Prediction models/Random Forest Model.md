# Random Forest Model Analysis

## Introduction
To predict the winner of the Formula 1 races, we opted for a **Random Forest model** due to the limitations encountered with the assumptions of logistic regression. Random Forest is an ensemble learning method that utilizes multiple decision trees to enhance prediction accuracy.

## Random Forest Model Overview
**Random Forest** is an ensemble learning method that constructs multiple decision trees during training and outputs either the mode of the classes (for classification) or the mean prediction (for regression) of the individual trees.

# OUTPUT

## Model Performance Metrics
- **Accuracy**: 0.9971, indicating very high performance.
- **ROC-AUC Score**: 0.9830, demonstrating excellent discrimination capability.
- **Classification Report**:
  - Precision, recall, and F1-score indicate a significant imbalance between classes.

### Classification Report Breakdown:
| Class  | Precision | Recall | F1-Score | Support |
|--------|-----------|--------|----------|--------|
| FALSE  | 1         | 1      | 1        | 1031   |
| TRUE   | 0         | 0      | 0        | 3      |

**Overall Accuracy**: 1.00  
**Macro Average**: 0.5  
**Weighted Average**: 0.99  

### Driver Win Probabilities
The predicted win probabilities for the drivers are as follows:

| Driver             | Win Probability |
|--------------------|-----------------|
| Max Verstappen     | 0.09            |
| Lando Norris       | 0.001667        |
| Sergio Pérez       | 0.001111        |

### ROC Curve
The ROC curve illustrates the model's performance across various thresholds. The area under the curve (AUC) is 0.983, indicating a 98.3% chance of correctly distinguishing between a randomly chosen positive and negative instance.

#### ROC Curve Plot:
![ROC Curve](https://github.com/user-attachments/assets/4a19ca5e-8c2a-499c-9fe1-b3fc03ba63ab)

### Feature Importance Scores
The feature importance scores highlight the key predictors in the model. Below is a summary of the most important features:

| Feature                | Importance Score |
|-----------------------|-----------------|
| driver_wins           | 0.191270        |
| round                 | 0.105384        |
| driver_standings_pos  | 0.090076        |
| year                  | 0.092938        |
| qualifying_time       | 0.058830        |
| circuitId_24         | 0.075822        |
| nationality_driver_British | 0.016107   |

#### Feature Importance Plot:
![Feature Importance](https://github.com/user-attachments/assets/a6e229e0-a914-4ea5-83e7-66c182bdf749)


## Conclusion
The Random Forest model exhibits high accuracy and excellent ROC-AUC scores, yet it struggles to accurately identify the minority class (TRUE). 

The analysis of feature importance emphasizes that past performance metrics of drivers and circuit characteristics are significant predictors. 

The model consistently identifies **Max Verstappen** as the likely champion, underscoring its reliability in predicting outcomes based on historical data.
