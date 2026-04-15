# Water Potability Classification: SVM vs. Random Forest

This project builds machine learning models to predict whether water is safe for human consumption based on its chemical and physical properties. The analysis compares the performance of Support Vector Machines (SVM) and Random Forest classifiers.

## Objective: 
To identify patterns in water quality data and develop classification models that distinguish between potable and non-potable water.

## Repository Structure
```
├── notebooks/
│   └── Water-Potability.ipynb    <-- Full EDA, preprocessing, and modeling
├── README.md
└── requirements.txt
```


## Dataset

The dataset contains 3,276 samples with 9 key features, including:

- pH  
- Hardness  
- Solids  
- Chloramines  
- Sulfate  
- Conductivity  
- Organic Carbon  
- Trihalomethanes  
- Turbidity  
🔗 Source: https://www.kaggle.com/datasets/adityakadiwal/water-potability

## Project Structure

- Exploratory Data Analysis and Visualization  
- Data preprocessing (outliers + missing values, normalization)  
- Model training and evaluation  
- Insights
- Results

### Exploratory Data Analysis (EDA)  and Visualization

1.  Class distribution analysis and general statistical information.
2.  Univariate  and Bivariate analysis.
3.  Understanding missing Values.
4.  Outliers

Observations: 
- ** moderate class imbalance** (with 61% non-potable samples).
- ** moderate positive skewness in feature Solids** (skewness ≈ 0.63), indicating a longer right tail and the presence of higher-value observations.
- The remaining features have negligible skewness.
- ** class overlap** in all variables.
- **missing values** (~44%) in multiple features.  
- **outliers (~11%)** using statistical analysis. 

 

### Preprocessing: 
   * Interquartile Range (IQR) capping to handle extreme values.
   * Feature/Target separation and Train-Test splitting.
   * RobustScaler normalization to mitigate outlier influence for distance-based models.
   * K-Nearest Neighbors (KNN) Imputation to handle missing data.

 ### Model training and evaluation  
   * Support Vector Machine (SVM): Comparative analysis between Linear and Radial Basis Function (RBF) kernels.
   * Random Forest: Implemented as a non-parametric baseline (scaling-independent).
   * Comparing the metrics for the SVM models and the Random Forest model. 
   * Comparing the number of true positives and false positives.



  Facts for SVM: 
- The SVM with a linear kernel was used as a baseline model.
- The SVM with RBF kernel was applied to capture non-linear decision boundaries  
- Feature scaling was applied to improve SVM performance
- Hyperparameter Tuning: Visualization of Accuracy vs. C-values and Score vs. Gamma plots for RBF optimization. 
 



##  Key Insight:
* The dataset shows significant overlap between classes and  moderated imbalance; these two facts  make classification challenging.
* Missing data and outliers have a substantial impact on model performance
* Tree-based models handle raw data more robustly compared with the SVM model. 




## Results

- Random Forest outperformed SVM for water potability prediction.

- SVM with a **linear kernel** was ineffective, failing to identify true positives, indicating that the data is not linearly separable.

- SVM with an **RBF kernel** captured non-linear decision boundaries. However, it performed well in predicting non-potable water but struggled to detect potable samples (recall = 0.33).

- By optimizing for F1-score, the Random Forest model improved recall from **0.33 (SVM)** to **0.46**, demonstrating better detection of potable water samples.


## Tools
- Python  
- Pandas  
- Scikit-learn  
- Matplotlib / Seaborn 


## Skills:


Data preprocessing, EDA, classification modeling, SVM (linear & RBF), Random Forest, model evaluation (F1-score, recall), feature scaling, and missing data imputation.


🔗  View  Full Analysis:  

---
 
