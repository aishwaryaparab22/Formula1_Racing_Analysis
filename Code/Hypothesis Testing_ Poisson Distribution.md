### Hypothesis Testing: Poisson Distribution
Hypothesis Testing of Incident Rates Using Poisson Distribution

We test whether the number of incidents before and after the introduction of virtual safety cars in 2015 follows a Poisson distribution.

### Python Code:
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import poisson

# Load incidents data and calculate means
incidents_before_2015 = np.random.poisson(3, 100)  # Sample data for demonstration
incidents_after_2015 = np.random.poisson(2, 100)

# Plot Poisson distributions for both periods
mu_before = np.mean(incidents_before_2015)
mu_after = np.mean(incidents_after_2015)
x = np.arange(0, max(max(incidents_before_2015), max(incidents_after_2015)) + 1)

plt.hist(incidents_before_2015, bins=range(0, 10), density=True, color='blue', alpha=0.7, label='Before 2015')
plt.plot(x, poisson.pmf(x, mu_before), 'r-', lw=2, label=f'Poisson (Before 2015)')

plt.hist(incidents_after_2015, bins=range(0, 10), density=True, color='green', alpha=0.7, label='After 2015')
plt.plot(x, poisson.pmf(x, mu_after), 'k--', lw=2, label=f'Poisson (After 2015)')

plt.xlabel('Number of Incidents')
plt.ylabel('Probability Density')
plt.title('Incident Distribution Before and After 2015')
plt.legend()
plt.show()
