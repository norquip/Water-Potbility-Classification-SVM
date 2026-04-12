# Water Potability Classification: SVM vs. Random Forest

This project explores the Water Potability dataset to predict whether water is safe for human consumption based on its chemical properties. The analysis compares the performance of Support Vector Machines (SVM) and Random Forest classifiers.

Objective: Develop a predictive model to determine water potability using physical and chemical features, including pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, and Turbidity.



## Repository Structure
```
├── notebooks/
│   └── Water-Potability.ipynb    <-- Full EDA, preprocessing, and modeling
├── README.md
└── requirements.txt
```


## Dataset and Methodology

The dataset consists of 3,276 entries and 9 features. The analysis was conducted following the machine learning pipeline:

1. Exploratory Data Analysis (EDA): Statistical profiling, class distribution analysis, and correlation mapping.

2. Outlier Management: Applied Interquartile Range (IQR) capping to handle extreme values.

3. Preprocessing:
   * Feature/Target separation and Train-Test splitting.
   * RobustScaler application to mitigate outlier influence for distance-based models.
   * K-Nearest Neighbors (KNN) Imputation to handle missing data.

4. Modeling:
   * Support Vector Machine (SVM): Comparative analysis between Linear and Radial Basis Function (RBF) kernels.
   * Random Forest: Implemented as a non-parametric baseline (scaling-independent).

5. Hyperparameter Tuning: Visualization of Accuracy vs. C-values and Score vs. Gamma plots for RBF optimization.


##  Key Insight:
* Solids and Conductivity 
* This dataset has around 44 % of missing values and 11 % of outliers.


##  Key Outcomes



##  Recommendations




##  Tools

* Language: Python  (sklearn, seaborn, matplotlib, scipy.stats)

* Skills:
 **Key Result:**
🔗 
* View  Full Analysis:  

---
 
