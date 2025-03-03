### i. Parametric Model: Logistic Regression Model

In our analysis for the year 2024, we aim to predict the chances of a driver winning the championship.

#### General Logistic Regression Model

Logistic regression is a form of regression analysis suitable for situations where the dependent variable is binary (typically 0 or 1). It predicts the probability of a given observation falling into a specific category based on one or more independent variables.

#### Interpretation

The logistic function transforms the linear combination of independent variables and their coefficients into a probability value between 0 and 1. The coefficients represent the change in the log-odds of the dependent variable for a one-unit change in the corresponding independent variable, holding all other variables constant.

#### Model Assumptions

1. **Linearity**: Assumes a linear relationship between the log-odds of the dependent variable and the independent variables.
2. **Independence**: Observations are assumed to be independent.
3. **No Multicollinearity**: Independent variables should not be highly correlated.
4. **No Outliers**: The model is sensitive to outliers.
5. **Large Sample Size**: Logistic regression performs well with large sample sizes.

### Focus on 'Champion' Variable

We focus on the 'Champion' variable in our `final_df` DataFrame, where the driver with the most points is marked as '1' and others as '0'. This model aids in predicting the likely champion of the 2024 competition.

### Output

- **Accuracy**: 0.9935

- **Confusion Matrix**:

[[154 0]

[ 1 0]]

- **Classification Report**:
  
           precision    recall  f1-score   support
        0       0.99      1.00      1.00       154
        1       0.00      0.00      0.00         1

      accuracy                           0.99       155
      macro avg       0.50      0.50      0.50       155
      weighted avg       0.99      0.99      0.99       155

- **Driver Win Probabilities**:
  
| Driver            | Win Probability |
|-------------------|-----------------|
| Max Verstappen    | 0.02966         |
| Sergio Perez      | 0.00134         |
| George Russell    | 0.000619        |
| Lance Stroll      | 0.000449        |
| Oscar Piastri     | 0.000443        |
| Lando Norris      | 0.000443        |
| Fernando Alonso   | 0.000349        |
| Charles Leclerc   | 0.000338        |
| Pierre Gasly      | 0.000334        |
| Guanyu Zhou       | 0.000328        |
| Yuki Tsunoda      | 0.000325        |
| Lewis Hamilton    | 0.000315        |
| Carlos Sainz      | 0.00031         |
| Nyck De Vries     | 0.000265        |
| Valtteri Bottas   | 0.000242        | 

Based on our model's calculations, Max Verstappen is the frontrunner for victory in 2024, boasting the highest win probability among all drivers.

### Model Assumption Validity

We must verify whether the logistic regression model fulfills all assumptions:

- **Assumption of Linearity of the Logit**: Not satisfied.
- **Assumption of Independence of Errors**: Satisfied.
- **Assumption of No Multicollinearity**: Satisfied.
- **Assumption of Binary Outcome**: Satisfied.
- **Assumption of No Outliers**: Not satisfied.

As the linearity of the logit is violated, predicting the winner using logistic regression may be less appropriate. We attempted model adjustments using Box-Cox and Log Transformation; however, due to the violation of assumptions, hypothesis testing cannot be performed effectively.

### Diagnostic Checks

We validated the assumptions and performance of our logistic regression model using various diagnostic tools, including:

- VIF computation
- Mean squared error
- R-squared metrics
- Accuracy and confusion matrix
- ROC curve analysis
- Q-Q plot of residuals

### Conclusion

The logistic regression model provides valuable insights into the prediction of race winners. However, the violations of certain assumptions indicate the need for caution in interpretation and application of results. Further refinement and exploration of alternative models may enhance predictive accuracy.

