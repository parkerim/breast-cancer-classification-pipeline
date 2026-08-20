Breast Cancer Classification Pipeline
📌 Overview

This repository contains an automated pipeline for classifying breast cancer cells as benign or malignant based on their morphological features. This project was developed as a learning exercise for machine learning. During the work, I utilized Hands-On Machine Learning with Scikit-Learn by Aurélien Géron and AI tools to build a robust architecture.

🧬 Biological Feature Engineering
Irregular morphology, asymmetrical growth, and membrane distortion are common features of cancerous cells. Instead of relying solely on raw geometric measurements, I utilized a Custom Scikit-Learn Transformer to compute biologically meaningful features:

Radius Anomaly Ratio (radius_worst / radius_mean): Captures the severity of asymmetrical growth and size deviation within the cell sample.

Shape Irregularity Index (perimeter_mean² / area_mean): A mathematical representation of membrane distortion. While a perfect circle maintains a constant ratio, malignant cells yield significantly higher variance.

The core of this project is a fully automated Transformation and Prediction Pipeline that integrates these biological insights.

📊 Model Evaluation
The model was evaluated using Stratified Train-Test splits and Cross-Validation to safely handle class imbalances and prevent data leakage.

Overall Accuracy: 97.37%
Precision (Malignant): 1.00 (Zero false positives; no healthy cells were misclassified as cancerous)
Recall (Malignant): 0.93 (Successfully identified 93% of actual malignant cases)
