# Firefly

## Overview  
- This project uses the Firefly Algorithm to detect anomalies in the UCI Red Wine Quality dataset.  
- Anomalies are wines with extremely low quality or extremely high quality.
  - We drew the line at quality <= 3 and quality >= 8 to be considered an anomoly. 
- The dataset has 1599 samples with 12 physicochemical features such as acidity, alcohol, density, and pH. Only about 1.75 percent of the samples are anomalies, making the data highly imbalanced.  

## Method  
- Anomalies are detected using a weighted Mahalanobis distance that emphasizes the most relevant features.  
- The Firefly Algorithm optimizes feature weights and a percentile threshold to maximize cross-validated F1 score, average precision, and ROC-AUC while penalizing large weights for interpretability.  
- The algorithm simulates fireflies moving toward brighter solutions, using 80 fireflies over 60 generations with moderate randomness decay.  

## Results  
- The algorithm highlighted volatile acidity, alcohol, and density as the most important features.  
- Example metrics include precision 0.68, recall 0.71, F1 score 0.69, ROC-AUC 0.93, and average precision 0.79.  
- Visualizations include FA convergence, feature weight distribution, PCA projection highlighting anomalies, score distribution with threshold, and precision-recall curves.  

## Full Report  
For detailed explanations, mathematical justification, and all visualizations, see the `FA-report.pdf` and our Jupyter notebook file located in this repository.
