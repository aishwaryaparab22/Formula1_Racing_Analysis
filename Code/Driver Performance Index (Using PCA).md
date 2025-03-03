##  Driver Performance Index (Using PCA)

We apply Principal Component Analysis (PCA) to calculate a composite **Driver Performance Index (DPI)** based on overtakes, wins, and standings.
In this study, we aim to evaluate and rank the performance of Formula
1 drivers based on multiple performance indicators. By applying data normalization,
Principal Component Analysis (PCA), and statistical aggregation, we develop a
comprehensive performance score for each driver. 

### Python Code:
```python
import pandas as pd
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

# Load dataset containing driver performance metrics
data = pd.read_csv('dpi_f1.csv')

# Normalize features
scaler = StandardScaler()
features = ['Overtakes_Count', 'Overtaken_Count', 'points', 'driver_standings_pos', 'driver_wins']
X = scaler.fit_transform(data[features])

# Apply PCA to combine features into one performance index
pca = PCA(n_components=1)
data['Performance_Index'] = pca.fit_transform(X)

# Display top drivers based on performance index
top_drivers = data[['Driver', 'Performance_Index']].sort_values(by='Performance_Index', ascending=False)
print(top_drivers)
```
