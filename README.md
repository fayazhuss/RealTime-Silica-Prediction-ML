# Real-Time Mining Quality Prediction 🛠️⛏️

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange?style=flat&logo=scikit-learn)
![Accuracy](https://img.shields.io/badge/R²%20Score-96.3%25-brightgreen?style=flat)
![Dataset](https://img.shields.io/badge/Dataset-700K%2B%20rows-yellow?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat)

> **Predicting iron ore silica concentration in real-time using machine learning on industrial flotation sensor data — replacing 1-hour lab delays with instant predictions.**

---

## 📌 The Problem

In the mining industry, measuring Silica concentration (quality control) traditionally requires lab testing — a process that takes **up to 1 hour**. During this time:

- Operators cannot react to quality changes
- Chemical reagents are wasted
- Material quality deviates undetected

This project solves that by using **live sensor data + machine learning** to predict quality **every 20 seconds**.

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| Source | [Kaggle — Quality Prediction in a Mining Process](https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process) |
| Size | 700,000+ rows of industrial sensor data |
| Features | 22 sensor readings (Air flow, Pulp pH, Starch flow, etc.) |
| Target | % Silica Concentrate (primary impurity to minimize) |

> **Data Challenge:** Raw data used commas as decimal separators. Custom preprocessing was applied to convert 700k+ string values to floats before modeling.

---

## 🔍 Key Findings (EDA)

- **Inverse Relationship** — Strong negative correlation between Iron concentrate and Silica concentrate, confirming metallurgical logic
- **Top Predictors** — Feature importance analysis revealed that `% Silica Feed` and `Ore Pulp pH` are the most significant drivers of final output quality
- **Non-linear patterns** — Sensor data showed complex, non-linear behavior, guiding the choice of ensemble modeling

---

## 🤖 Model Performance

**Algorithm: Random Forest Regressor**

| Metric | Score |
|--------|-------|
| R² Score | **0.9636 (96.3%)** |
| Mean Squared Error (MSE) | 0.0460 |

Random Forest was chosen due to the non-linear nature of industrial sensor data and its ability to handle high-dimensional feature spaces robustly.

---

## 💼 Business Impact

| Before | After |
|--------|-------|
| Lab results in ~60 minutes | Predictions every 20 seconds |
| No real-time intervention | Immediate process adjustments |
| Chemical reagents wasted | Optimized Amina & Starch usage |
| Reactive quality control | Proactive quality control |

---

## 🛠️ How to Run

**1. Clone the repository**
```bash
git clone https://github.com/fayazhuss/RealTime-Silica-Prediction-ML.git
cd RealTime-Silica-Prediction-ML
```

**2. Install dependencies**
```bash
pip install pandas numpy seaborn scikit-learn matplotlib jupyter
```

**3. Run the notebook**
```bash
jupyter notebook Mining_Analysis.ipynb
```
Or open directly in [Google Colab](https://colab.research.google.com/).

---

## 📁 Project Structure

```
RealTime-Silica-Prediction-ML/
│
├── Mining_Analysis.ipynb    # Main analysis & ML notebook
├── README.md                # Project documentation
└── data/                    # Dataset (download from Kaggle)
```

---

## 🧰 Tech Stack

- **Python** — Core language
- **Pandas & NumPy** — Data manipulation & preprocessing
- **Matplotlib & Seaborn** — Exploratory data visualization
- **Scikit-learn** — Machine learning (Random Forest Regressor)
- **Jupyter Notebook** — Development environment

---

## 👤 Author

**Fayaz Hussain**
Freelance Data Analyst | Dubai, UAE

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://linkedin.com/in/fayaz-hussain-1273bb361)
[![GitHub](https://img.shields.io/badge/GitHub-fayazhuss-black?style=flat&logo=github)](https://github.com/fayazhuss)
[![Email](https://img.shields.io/badge/Email-Contact-red?style=flat&logo=gmail)](mailto:fayazhussainkhaskheli@gmail.com)

---

*⭐ If you found this project useful, please consider giving it a star!*
