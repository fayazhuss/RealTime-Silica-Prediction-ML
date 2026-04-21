Real-Time Mining Quality Prediction 🛠️⛏️

📌 Project Overview

In the mining industry, quality control (measuring Silica concentration) is traditionally a slow process, with lab results often taking up to 1 hour. This delay makes it difficult to adjust the process in real-time. This project leverages machine learning to predict quality using sensor data, providing instant feedback to prevent material waste and optimize production.

📊 The Dataset
This project uses the "Quality Prediction in a Mining Process" dataset from Kaggle.

Records: 700,000+ rows of industrial data.

Features: 22 sensor readings (Air flow, Pulp pH, Starch flow, etc.).

Target: % Silica Concentrate (The primary impurity to be minimized).

🚀 Key Insights

Through Exploratory Data Analysis (EDA), I identified several critical patterns:

Inverse Relationship: A strong negative correlation between Iron concentrate and Silica concentrate, confirming the metallurgical logic.

Operational Drivers: Feature importance analysis revealed that % Silica Feed and Ore Pulp pH are the most significant predictors of the final output quality.

🤖 Machine Learning Model

Given the non-linear nature of industrial sensor data, I implemented a Random Forest Regressor.

Performance Metrics:
R-Squared ($R^2$) Score: 0.9636 (96.3% Accuracy)
Mean Squared Error (MSE): 0.0460

🛠️ Installation & Usage

Clone the repository:

Bash
git clone https://github.com/YOUR_USERNAME/Mining-Quality-Predictor.git

Install the required dependencies:

Bash
pip install pandas seaborn scikit-learn matplotlib

Open and run the Mining_Analysis.ipynb notebook in Jupyter or Google Colab.

💡 Business Impact
Eliminated Lab Latency: Instead of waiting 1 hour, operators get quality updates every 20 seconds.

Cost Optimization: Improved control over chemical reagents (Amina & Starch) based on real-time silica trends.

Proactive Adjustments: Allows for immediate intervention if the quality starts to deviate from the target.

Technical Challenge Handled:
"The raw data used commas as decimal separators. I performed custom pre-processing to convert strings to floats before modeling, ensuring data integrity for the 700k+ records."

Author: Fayaz Hussain

Dataset Source: Kaggle - Quality Prediction in a Mining Process https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process
