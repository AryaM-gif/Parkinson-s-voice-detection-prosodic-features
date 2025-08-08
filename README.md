# Parkinson's Voice Detection using Prosodic Features

This project aims to detect Parkinson's Disease (PwPD) using voice recordings, primarily focusing on prosodic features like pitch, energy, jitter, shimmer, etc.

---

##  Project Workflow

1. **Data Loading & Validation**
2. **Audio Preprocessing** (resampling, pre-emphasis, silence removal)
3. **Feature Extraction**
   - Global: pitch range, energy mean/std, jitter, shimmer
   - Frame-wise pitch using librosa

---

##  Statistical Analysis & Mathematical Methods

This project involves several statistical and mathematical techniques for feature validation, hypothesis testing, and correlation analysis before model training:

###  1. Hypothesis Testing

Used to evaluate whether feature distributions differ significantly between the two groups (HC vs. PwPD):

- **Shapiro-Wilk Test**: Tests whether each feature is normally distributed.
- **Levene’s Test**: Tests for equality of variances between the two groups.
- **t-test / Mann-Whitney U Test**:
  - *t-test* is used when normality & equal variance assumptions hold.
  - *Mann-Whitney U* is used for non-parametric comparison when assumptions are violated.
  - These tests determine whether the **mean or median** of a feature is significantly different between HC and PwPD.

###  2. Bonferroni Correction

Since multiple tests are conducted, Bonferroni correction is applied to adjust p-values and control the **family-wise error rate**, reducing the chance of false positives.

###  3. Correlation Analysis

Used to find relationships between features and the target label (0 = HC, 1 = PwPD):

- **Point-Biserial Correlation**: Measures the strength and direction of association between continuous features and the binary class label.
- **Correlation Matrix (Heatmap)**: 
  - Reveals multicollinearity between features.
  - Helps identify redundant or highly correlated features.

###  4. Feature Engineering Metrics

Many features rely on mathematical calculations of variation and distribution:

- **Mean, Median, Standard Deviation**: For pitch and energy.
- **Jitter & Shimmer**:
  - *Jitter*: Cycle-to-cycle variation in pitch period.
  - *Shimmer*: Cycle-to-cycle variation in amplitude.
  - Both indicate voice instability.
- **Pitch Slope**: Trend of pitch change over time, often calculated using linear regression.

###  Visualizations

- **Histograms & KDE Plots**: For distribution analysis.
- **Boxplots**: To compare spread and detect outliers.
- **Heatmaps**: For correlation between features.
- **ROC Curves**: For evaluating model performance.

---

4. **Exploratory Data Analysis (EDA)**
   - Histograms, box plots, KDEs, statistical testing

5. **Modeling Approaches**
   - HMM + MLP
   - GMM + MLP
   - RNN (LSTM-based)

6. **Evaluation**
   - Accuracy, F1-score, Confusion matrix, ROC-AUC

7. **Prediction on New Audio**

---

## 🛠️ Technologies Used

- Python, NumPy, Pandas, SciPy  
- Librosa, Parselmouth  
- scikit-learn, TensorFlow, PyTorch  
- Matplotlib, Seaborn

