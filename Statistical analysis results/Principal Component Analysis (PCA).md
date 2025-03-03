# Principal Component Analysis (PCA)

### Objective
To evaluate and rank the performance of Formula 1 drivers based on multiple performance indicators using Principal Component Analysis (PCA).

### Introduction
Principal Component Analysis (PCA) simplifies complex performance data by reducing dimensionality while retaining significant information. This analysis aims to provide a comprehensive performance score for each driver, highlighting their effectiveness and competitiveness in the racing context.

### Methodology Overview
1. **Data Preprocessing**: Data was preprocessed to calculate metrics such as overtakes, overtaken instances, and points scored. Each driver's participation in races was counted, and metrics were normalized.
2. **PCA Application**: PCA was applied to derive principal components from normalized performance metrics, and a performance score was calculated for each driver.
3. **Aggregation and Ranking**: Performance scores were aggregated by driver to rank their overall performance across races.
4. **Classification**: Drivers were classified into performance categories based on percentile thresholds.

### Results (1994-2020)

#### Weights Derived from PCA
The following weights represent the contribution of each performance metric to the variance explained by the first principal component:
- **Points**: 0.46876439
- **Driver Standings Position**: 0.54295839
- **Races Participated**: 0.42607514
- **Overtakes Count**: 0.24001883
- **Overtaken Count**: 0.23970298
- **Driver Age**: 0.17063866
- **Driver Wins**: 0.39966486

#### Performance Ratings
The performance ratings of drivers from 1994 to 2020 are as follows:

| Driver       | Performance Rating |
|--------------|--------------------|
| Hamilton     | 3.16               |
| Vettel       | 2.29               |
| Raikkonen    | 1.74               |
| Alonso       | 1.68               |
| Schumacher   | 1.28               |
| Button       | 1.16               |
| Bottas       | 1.12               |
| Massa        | 1.04               |
| Rosberg      | 0.96               |
| Webber       | 0.95               |

### Insights from the Results
1. **PCA Weights**: The weights indicate that points scored, driver standings position, and races participated are the most significant factors contributing to driver performance variance.
2. **Performance Rankings**: Lewis Hamilton consistently ranks at the top, indicating superior performance over the analyzed years, while Mark Webber ranks lowest among the listed drivers.
3. **Classification Accuracy**: The model achieves an overall accuracy of 81%, with balanced precision and recall across performance categories. This indicates reliable classification of driver performance levels.

### Results (2019-2020)

#### Weights Derived from PCA
The following weights were derived for the 2019-2020 seasons:

| Metric                  | Weight        |
|-------------------------|---------------|
| Points                  | 0.54564757    |
| Driver Standings Position| 0.54177174   |
| Races Participated      | 0.44679752    |
| Overtakes Count         | 0.0976521     |
| Overtaken Count         | 0.36945393    |
| Driver Age              | -0.2511811    |
| Driver Wins             | 0.44097969    |

#### Performance Ratings
The performance ratings of drivers for the 2019-2020 seasons are as follows:

| Driver       | Performance Rating |
|--------------|--------------------|
| Hamilton     | 4.77               |
| Bottas       | 2.55               |
| Verstappen   | 2.31               |
| Leclerc      | 1.23               |
| Ocon         | 0.69               |
| Sainz        | 0.56               |
| Vettel       | 0.48               |
| Gasly        | 0.16               |
| Perez        | 0.12               |
| Hulkenberg   | 0.02               |

### Conclusion

1. **PCA Weights:**  
   The weights derived from PCA represent the contribution of each performance metric to the overall variance in the data. The higher the weight, the more significant that metric is in explaining variations in driver performance. Notably, metrics such as Points (0.46876439), driver_standings_pos (0.54295839), and Races_Participated (0.42607514) emerged as the most influential in assessing driver performance.

2. **Performance Ratings of Drivers:**  
   The performance ratings table illustrates the relative performance of various drivers, with Hamilton achieving the highest rating (3.16), signifying exceptional performance, while Webber recorded the lowest rating (0.95). This ranking system offers a clear perspective on driver effectiveness in the competitive landscape of Formula 1.

3. **Classification Report:**  
   The model attained an overall accuracy of 81%, with commendable precision, recall, and F1-scores across all performance categories (Low, Medium, High). The results indicate a well-balanced model that performs effectively in categorizing driver performance levels. Notably, the model shows slightly enhanced proficiency in identifying "Low" performance instances compared to "Medium" and "High."

4. **PCA for Enhanced Comparability:**  
   Rather than solely serving as a tool for dimensionality reduction, PCA was instrumental in enhancing the comparability of performance metrics. By synthesizing multiple indicators into principal components, we were able to retain significant information while simplifying the analysis. This approach allows for a more straightforward comparison of drivers' performances, facilitating insights into their competitiveness.

5. **Driver Stats Relation:**  
   The underlying driver statistics—such as overtakes, points, wins, and others—are foundational for assessing driver performance. These stats were aggregated and analyzed, providing a comprehensive view of each driver's effectiveness in the racing context. The analysis conducted for the 2019 and 2020 seasons further reinforces the relevance of these performance indicators.

By utilizing PCA to enhance comparability, we gain valuable insights into the effectiveness and competitiveness of Formula 1 drivers, ultimately informing discussions on their relative standings in the sport.
![image](https://github.com/user-attachments/assets/d13d0642-68ca-460b-96fe-8b53f741bbbc)

