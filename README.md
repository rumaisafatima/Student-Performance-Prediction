<p align="center">
  <img src="https://img.shields.io/badge/Student%20Performance%20Prediction-Machine%20Learning-000000?style=for-the-badge&logo=python&logoColor=white">
</p>

<p align="center">
  🔥 Predict Your Path — Empower Your Success 🔥
</p>

---

<p align="center">
  <img src="images/actual_vs_predicted_exam_score.png" width="750">
</p>

---

# 🎯 Student Performance Prediction & Insights Using ML

This project builds a Machine Learning model to **predict student exam scores** using their learning behavior and academic environment.  
It helps explore **how different factors influence student success**, enabling early academic support and performance improvement strategies.

---

## 📌 Motivation

Educational performance is not random — it is influenced by:
- Study discipline
- Motivation
- Family and school support
- Available learning resources

Using real-world features, this model provides **data-driven predictions** — making performance evaluation **timely and actionable**.

---

## 🧠 Project Objectives

✔ Predict a student’s upcoming exam score  
✔ Identify key contributors to high or low performance  
✔ Visualize behavior-to-performance relationships  
✔ Provide a repeatable ML pipeline for academic analytics  

---

## 📊 Dataset Description

The dataset includes **behavioral, academic, and resource availability indicators**:

| Category | Features |
|---------|----------|
| Academic Factors | Hours_Studied, Previous_Scores, Grades |
| School Support | Teacher_Quality, Attendance |
| Home Support | Parental_Involvement, Parental_Education_Level, Family_Income |
| Personal Impact | Motivation_Level, Peer_Influence, Learning_Disabilities |
| Environment | Access_to_Resources, Extracurricular_Activities |

Target variable:
Exam_Score (0–100 scale)



---

## 🔍 Data Preprocessing Steps

✅ Handled missing values (median filling)  
✅ Standardized categories (lowercase, removed spaces)  
✅ Dropped weak correlation features (Sleep Hours, Physical Activity)  
✅ Ordinal & One-Hot Encoding for categorical variables  
✅ Converted boolean values to numeric (1/0)

---

## 📈 Exploratory Data Analysis

Some key visual insights:

<p align="center">
  <img src="images/feature_correlation_exam_score.png" width="700">
</p>

📌 **Strong positive impact**  
- Hours Studied  
- Attendance  
- Previous Scores  
- Motivation Level  

📌 **Weak impact**  
- Sleep Hours  
- Physical Activity  

These were removed from model training to improve performance.

---

## 🤖 Machine Learning Models Trained

We evaluated:

| Model | Train R² | Test R² | MAE | RMSE | Notes |
|-------|------|-----|-----|------|------|
| **Linear Regression** ✅ | ~0.65 | ~0.70 | ~0.99 | ~2.04 | ✅ Best performer |
| Polynomial Regression (Degree 2 + Ridge) | ~0.66 | ~0.70 | ~1.01 | ~2.05 | Slight overfit |
| Polynomial Regression (Degree 3 + Ridge) | ~0.68 | ~0.67 | ~1.10 | ~2.15 | Overfitting |

✅ Final selected model: **Linear Regression**  
📌 Most stable + accurate generalization

---

## 🚀 Model Performance Demonstration

<p align="center">
  <img src="images/actual_vs_predicted_exam_score.png" width="750">
</p>

The predicted scores closely follow the real exam results, showing **high reliability**.

---

## 🛠️ Tech Stack

| Component | Technology |
|---------|-------------|
| Language | Python |
| Data & ML | Pandas, NumPy, Scikit-Learn |
| Visualization | Matplotlib, Seaborn |
| Deployment Ready | Joblib model files |
| Version Control | Git & GitHub |

---

## 📦 Repository Structure
📦 Student-Performance-Prediction
│
├─ data/
│ └─ StudentPerformanceFactors.csv
│
├─ images/
│ ├─ actual_vs_predicted_exam_score.png
│ ├─ exam_scores_distribution.png
│ ├─ student_grades_distribution.png
│ ├─ extracurricular_participation_distribution.png
│ ├─ access_to_resources_distribution.png
│ └─ feature_correlation_exam_score.png
│
├─ models/
│ ├─ best_model.pkl
│ └─ feature_order.json
│
├─ Student_Performance_Prediction.ipynb
├─ requirements.txt
├─ README.md
└─ LICENSE


---

## ▶️ How to Run

### Install Requirements
```bash
pip install -r requirements.txt

Open Notebook
jupyter notebook Student_Performance_Prediction.ipynb

🙌 Author

Rumaisa Fatima
Machine Learning & Data Science Enthusiast
📌 GitHub: https://github.com/rumaisafatima

