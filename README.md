# 🏎️ **The Formula for Victory: Analyzing F1 Through Data**

## Table of Contents
1. [🚀 Project Overview](#-project-overview)
2. [🏁 Project Goals](#-project-goals)
3. [📊 Data Sources](#-data-sources)
4. [🔧 Tools & Techniques](#-tools--techniques)
   - [🏎️ Logistic Regression](#-1-logistic-regression)
   - [🚥 Random Forest](#-2-random-forest)
   - [🏆 Principal Component Analysis (PCA)](#-3-principal-component-analysis-pca)
   - [📉 Chi-Square and Poisson Analysis](#-4-chi-square-and-poisson-analysis)
5. [🔮 Key Results](#-key-results)
   - [🏆 2024 Champion Prediction](#-2024-champion-prediction)
   - [🔢 Driver Performance Index (DPI)](#-driver-performance-index-dpi)
   - [🛑 Casualty Trends](#-casualty-trends)
   - [🧮 Correlation Insights](#-correlation-insights)
6. [📊 Data Visualization Highlights](#-data-visualization-highlights)
7. [📈 Applications and Future Work](#-applications-and-future-work)

## 🚀 Project Overview
Formula 1 racing is more than just fast cars; it's a sport where strategy, precision, and data converge to determine the champion. **The Formula for Victory** project dives deep into the complex world of Formula 1 by analyzing decades of racing data to uncover the key factors that influence success on the track.

Leveraging historical data from 1994 to 2023, this project utilizes advanced statistical methods and machine learning models to predict outcomes, evaluate driver performance, and assess the impact of safety innovations. With detailed exploration of driver metrics, constructor performance, and race trends, we aim to provide a comprehensive view of Formula 1 that goes beyond the checkered flag.

Whether you’re a die-hard F1 fan curious about what makes drivers like **Lewis Hamilton** and **Max Verstappen** stand out, or a data science professional looking to explore predictive modeling in a real-world context, this project has something for everyone. Through our analysis, we strive to answer key questions: **Who will be the next champion? What factors determine victory? How has safety changed the game?**

Join us as we take you behind the data and reveal the intricate statistics that power the pinnacle of motorsport.

---

## 🏁 Project Goals
Our analysis focuses on key elements of Formula 1 that define its competitive edge. We aim to:
- **Predict the 2024 F1 Season Champion** using historical data and machine learning models.
- **Evaluate Driver Performance** across various metrics like wins, podiums, and standings.
- **Analyze Constructor Dominance**, uncovering which teams consistently lead the pack.
- **Study Casualty Trends** and assess the impact of safety innovations like virtual safety cars.
- **Explore Correlations** between variables like driver age, points scored, and race positions.

---

## 📊 Data Sources
We use a diverse range of datasets sourced from reliable platforms to fuel our analysis:

- [Formula 1 Official Website](https://www.formula1.com)
- [Ergast API](https://ergast.com/mrd/)
- [Kaggle Formula 1 Dataset](https://www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020)

These datasets include race results, driver standings, constructor standings, qualifying times, weather conditions, and safety data spanning from **1994 to 2023**.

---

## 🔧 Tools & Techniques
Here’s a breakdown of the models and statistical methods that drive our analysis:

### 🏎️ 1. **Logistic Regression**:
We initially used Logistic Regression to predict the 2024 champion based on variables like wins, podium finishes, and qualifying times. However, due to assumption violations, we turned to more robust methods.

### 🚥 2. **Random Forest**:
A powerful ensemble method that builds multiple decision trees to improve prediction accuracy. This model provided us with a more reliable prediction for the 2024 season champion.

### 🏆 3. **Principal Component Analysis (PCA)**:
Used to analyze driver performance across multiple metrics, PCA enhances comparibility by combining multiple performance metrics into a single score, offering a **Driver Performance Index (DPI)**.

### 📉 4. **Chi-Square and Poisson Analysis**:
For casualty analysis, we applied chi-square goodness-of-fit tests and Poisson distribution modeling to assess whether virtual safety cars (introduced in 2015) have significantly reduced casualties in Formula 1.

---

## 🔮 Key Results

### 🏆 **2024 Champion Prediction**:
According to our **Random Forest Model**, **Max Verstappen** is predicted to win the 2024 season, with a **10.9% win probability**—the highest among all drivers.

### 🔢 **Driver Performance Index (DPI)**:
By applying **PCA**, we evaluated driver performance and ranked **Lewis Hamilton** as the top performer in the 1994–2023 dataset, followed closely by **Sebastian Vettel** and **Kimi Raikkonen**.

### 🛑 **Casualty Trends**:
Our analysis shows a **significant reduction in casualties** post-2015, thanks to the introduction of **virtual safety cars**, which has improved race safety substantially.

### 🧮 **Correlation Insights**:
- There is a **negative correlation** between driver standings position and points, indicating that drivers with lower (better) positions tend to score higher points.
- **Driver age** shows a weak positive correlation with points scored, suggesting that experience contributes slightly to performance.

---

## 📊 Data Visualization Highlights
Our analysis isn't just about numbers—it's also about bringing data to life! Check out our visualizations for insights:

- **Driver Wins by Nationality**: Which countries dominate the F1 circuit?
- **Constructor Dominance**: See the ongoing rivalry between Ferrari, Mercedes, Red Bull, and McLaren.
- **Casualty Trends**: Visualize how safety measures have reduced risks in the sport.

---

## 📈 Applications and Future Work
This analysis not only provides insight into Formula 1 but can also be expanded to other fields:

- **Predictive Modeling**: Use this framework to predict outcomes in other sports or competitive industries.
- **Safety Innovations**: With more data on car technology and racing conditions, future models could improve predictions on race outcomes and safety measures.
- **Sustainability Research**: Formula 1 is pushing toward carbon neutrality by 2030. Future work could include analysis of the environmental impact of these changes.

## 🗂️ Repository Structure

- `README.md`: Overview and documentation of the entire project.
- `Data/`: Contains all raw, cleaned, and processed datasets.
  - `README.md`: Documentation for the data directory.
  - `final_df.csv`: The final dataset used for analysis.
  - `raw data.rar`: Compressed raw data files.
- `Code/`: Collection of markdown files detailing the analysis processes.
  - `Data Preprocessing.md`: Explanation of the data cleaning and preprocessing steps.
  - `Driver Performance Index (Using PCA).md`: Analysis of driver performance using PCA.
  - `Hypothesis Testing: Poisson Distribution.md`: Poisson distribution hypothesis testing for incident rates.
  - `Prediction Modelling.md`: Overview of the prediction models used.
- `Statistical Analysis Results/`: Contains outputs from the statistical analysis.
  - `Prediction Models/`: Outputs and evaluations from various prediction models.
    - `Logistic Regression Model.md`: Detailed explanation of the logistic regression model.
    - `Random Forest Model.md`: Detailed explanation of the Random Forest model.
  - `Principal Component Analysis (PCA).md`: Full breakdown of the PCA analysis.
  - `Hypothesis testing.md`: Results and interpretation of hypothesis tests.
  - `Data Visualizations.md`: Collection of all charts and graphs.
  - `Key Findings.md`
- `PPT F1 Project.pdf`: Project presentation summarizing the findings and analysis.
