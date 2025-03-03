## 1. Casualty Analysis Using Poisson Distribution

### Introduction
In this analysis, we employ a statistical approach to compare incident rates before and after 2015 using hypothesis testing based on the Poisson distribution. The Poisson distribution is particularly suited for modeling count data, representing the number of events occurring within a fixed interval of time or space. This method is apt for incidents that occur independently and at a constant rate.

In 2015, Virtual Safety Cars (VSCs) were introduced. A VSC is a racing control procedure that reduces the speed of all cars to a mandated limit without deploying the physical safety car, whereas a Safety Car (SC) leads the race vehicles at a reduced speed during hazardous conditions.

### Hypothesis Testing
- **Null Hypothesis (H0):** There is no significant difference in incident rates before and after 2015.
- **Alternative Hypothesis (H1):** There is a significant difference in incident rates before and after 2015.

![image](https://github.com/user-attachments/assets/578080ed-9cef-41f0-a34e-b9b9d16caec0)

### Output
- **Test Statistic:** 37.46
- **P-value:** 0.0000

### Conclusion
Reject the null hypothesis. The incident rates before and after 2015 are significantly different.

### Interpretation
The test statistic of 37.46 indicates a large deviation from the expected mean under the null hypothesis. 

The p-value of 0.0000 is far below the significance threshold (\(\alpha = 0.05\)), leading us to reject the null hypothesis. This analysis concludes that there is a statistically significant difference in incident rates before and after 2015, suggesting that the introduction of Virtual Safety Cars brought about a significant shift in the pattern or frequency of incidents.

## 2. Spearman Correlation Coefficient Analysis

### **Hypotheses for Driver Standing Position and Points:**
  - **Null Hypothesis (H0):** There is no significant association between driver_standings_pos and driver_points.
  - **Alternative Hypothesis (H1):** There is a significant association between driver_standings_pos and driver_points (i.e., if driver_standings_pos is small, driver_points are high).

**Significance Level:** 0.05

#### Output
- **Spearman Correlation Coefficient:** -0.7968
- **P-value:** 0.0

#### Interpretation
The Spearman correlation coefficient of approximately -0.797 suggests a strong negative monotonic relationship between driver_points and driver_standings_pos. 

The p-value indicates statistical significance, allowing us to reject the null hypothesis.

### 3.**Association between Driver Age and Driver Points:**
   - **Null Hypothesis (H0):** There is no significant association between driver_age and driver_points.
   - **Alternative Hypothesis (H1):** There is a significant association between driver_age and driver_points.

**Significance Level:** 0.05

#### Output
- **Spearman Correlation Coefficient:** 0.1407
- **P-value:** 2.997 × 10^-24

#### Interpretation
The Spearman correlation coefficient of approximately 0.141 indicates a weak positive relationship between driver_points and driver_age. The very low p-value suggests statistical significance, allowing us to reject the null hypothesis.

### 4. **Association between Driver Wins and Weather (Cloudy):**
   - **Null Hypothesis (H0):** There is no significant association between driver_wins and weather_cloudy.
   - **Alternative Hypothesis (H1):** There is a significant association between driver_wins and weather_cloudy.

**Significance Level:** 0.05

#### Output
- **Spearman Correlation Coefficient:** -0.0107
- **P-value:** 0.4434

#### Interpretation
The Spearman correlation coefficient of approximately -0.01 suggests a weak negative relationship between driver_wins and weather_cloudy. The p-value is greater than 0.05, providing strong evidence to fail to reject the null hypothesis, indicating no significant association between driver_wins and weather conditions.
