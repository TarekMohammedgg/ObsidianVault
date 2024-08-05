---
date: 2024-07-29
author:
  - Andrew ng
topic:
  - machine learning
  - Ai
---
Normalization in machine learning refers to the process of scaling input features to a common range or distribution, which can help improve the performance and stability of models. It involves transforming the data so that it meets certain statistical properties or falls within a specific range. Here are the key concepts:


$$x = \begin{matrix} x_{1}  \\ x_{2}

\end{matrix}  
$$

$$
\mu = \frac{1}{m} \sum_{i = 1 }^n x^{(i)}

$$

$$
\sigma^{2} = \frac{1} {m} \sum_{i =1} ^ n (x^{(i)} )^2 
$$
$$
X := x - \mu
$$

$$
x / = \sigma
$$

uses same $\mu$ and $\sigma$ to normalize test set 



![[Pasted image 20240729042055.png]]

---
### Types of Normalization 
#### 1.Min-Max Normalization 
- **Purpose**: Scales data to a fixed range, typically [0, 1].
- **Formula**: 
$$
\lvert x \rvert = \frac{x - min(x)}{max(x) - min(x) }

$$
- **Example**: If you have a feature with values ranging from 10 to 100, min-max normalization would scale these values to a range of [0, 1].
#### 2.Z-score Normalization ( standardization) 
- **Purpose**: Centers data around zero with a unit variance.
- **Formula**: 
$$
x = \frac{x - \mu }{\sigma}
$$
- **Where**: $\mu$ is the mean of the feature, and σ\sigmaσ is the standard deviation.
- **Example**: If a feature has a mean of 50 and a standard deviation of 10, standardization would transform these values such that the resulting distribution has a mean of 0 and a standard deviation of 1.

#### 3.Robust Scaling 
- **Purpose**: Normalizes data using statistics that are robust to outliers.
- **Formula**: 
$$
x = \frac{x - median(x)}{IQR(x)}
$$
- **Where**: IQR is the interquartile range (75th percentile - 25th percentile).
- **Example**: Useful when data contains outliers, as it scales based on the median and quartiles.

### Why Normalize?

1. **Improved Convergence**: Normalized data helps gradient-based optimization algorithms converge faster and more reliably. It ensures that features contribute equally to the distance metrics used in optimization.
    
2. **Enhanced Model Performance**: Many machine learning algorithms, such as gradient descent-based models and distance-based algorithms (e.g., K-Nearest Neighbors), perform better when features are on a similar scale.
    
3. **Prevent Dominance**: Without normalization, features with larger scales can dominate the learning process, leading to suboptimal performance. Normalization helps ensure that no single feature disproportionately affects the model.
    

### When to Normalize?

- **When Features Have Different Scales**: Normalization is particularly useful when your dataset features have different units or ranges.
- **Before Using Algorithms Sensitive to Scaling**: Algorithms like K-Nearest Neighbors, Support Vector Machines, and neural networks often benefit from normalization.

----
LINKS TO THIS PAGE 
```dataview
LIST FROM ([[#]]) OR outgoing([[#]]) WHERE file.name != this.file.name SORT file.name ASC 
```
