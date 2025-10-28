


<h1 align="center">📊 Student Performance Prediction & Insights Using Machine Learning</h1>

<p align="center">
  <strong>Analyze. Predict. Improve.</strong><br>
  A Machine Learning solution that predicts student exam scores while uncovering key academic success factors.
</p>

---

## 🔍 Project Overview

Educational performance is shaped by multiple behavioral and environmental influences.  
This project builds a predictive model that uses real student data to:

✅ Predict exam scores using measurable attributes  
✅ Analyze which factors most influence student success  
✅ Help schools & parents make informed academic support decisions  

The workflow includes complete **Data Cleaning ➜ EDA ➜ Feature Engineering ➜ Model Training ➜ Model Evaluation ➜ Deployment Artifacts**.

---

## 📁 Dataset Description

| Aspect | Detail |
|-------|--------|
| Source | Provided dataset (*StudentPerformanceFactors.csv*) |
| Sample Size | 6,600+ student records |
| Target Variable | `Exam_Score` (Continuous) |
| Feature Types | Numerical, Boolean & Ordinal Categorical |

Key Features include:

- Study discipline: `Hours_Studied`, `Motivation_Level`, `Tutoring_Sessions`
- Support system: `Parental_Involvement`, `Teacher_Quality`
- Resources: `Internet_Access`, `Access_to_Resources`
- Lifestyle: `Sleep_Hours`, `Physical_Activity`
- Past performance: `Previous_Scores`

➡ Goal: **Regression prediction**  
➡ Grading bands (A/B/C) created for interpretability, not modeling

---

## 🧹 Data Preprocessing Pipeline

| Step | Why? |
|------|-----|
| Remove low-correlation features | Reduce noise: `Gender`, `School_Type`, `Distance_from_Home`, `Learning_Disabilities` |
| Standardize boolean text | Fix inconsistent values (`yes/no/true/false/1/0`) |
| Ordinal encoding | Convert ranked categories into meaningful integers |
| One-Hot Encoding | Handle Peer Influence categories |
| Impute missing values | Median strategy to retain distribution integrity |

Except `Exam_Score`, **all columns become numeric** for ML input. ✅

---

## 🔎 Exploratory Data Analysis (EDA) — Key Findings

📌 Insights visualized inside `/images/`:

| Visualization | Interpretation |
|--------------|----------------|
| `exam_scores_distribution.png` | Scores heavily clustered around medium range — grade inflation unlikely |
| `student_grades_distribution.png` | Majority of students fall in “C” grade → performance improvement needed |
| `extracurricular_participation_distribution.png` | Active involvement correlates with higher academic performance |
| `access_to_resources_distribution.png` | Students with better learning tools perform better |
| `feature_correlation_exam_score.png` | **Top predictors**: Attendance ➜ Hours Studied ➜ Previous Scores |
| `actual_vs_predicted_exam_score.png` | Predictions follow real scores with minimal deviation |

➡ Attendance and study effort drive performance the strongest.

---

## 🤖 Machine Learning Models

| Model | Purpose | Result |
|------|---------|--------|
| Linear Regression | Baseline — Check linear relationships | ✅ Best performing model |
| Polynomial Regression (Degree 2 & 3) | Capture complex relationships | ❌ Overfitting + Higher RMSE |

Performance Snapshot (approx.):

| Model | Train R² | Test R² | RMSE | Conclusion |
|------|---------|---------|------|-----------|
| Linear Regression | 0.65 | 0.70+ | ~2.04 | ✅ Chosen model |
| Polynomial (d=2) | 0.69 | 0.70 | ~2.05 | Slight overfit |
| Polynomial (d=3) | 0.67 | 0.67 | ~2.14 | High variance |

✅ **Final choice: Linear Regression** — Generalizes best, simplest deployment.

---

## 💡 Model Outputs Saved for Deployment

Saved under `/models/`:

```

best_model.pkl          → final ML model
feature_order.json      → preserves column alignment

```

This allows fast prediction without retraining.

---

## 🗂 Repository Structure

```

Student-Performance-Prediction
│
├─ data/
│   └─ StudentPerformanceFactors.csv
│
├─ images/
│   ├─ exam_scores_distribution.png
│   ├─ student_grades_distribution.png
│   ├─ extracurricular_participation_distribution.png
│   ├─ access_to_resources_distribution.png
│   ├─ feature_correlation_exam_score.png
│   └─ actual_vs_predicted_exam_score.png
│
├─ models/
│   ├─ best_model.pkl
│   └─ feature_order.json
│
├─ Student_Performance_Prediction.ipynb
├─ requirements.txt
├─ README.md
└─ LICENSE

````

---

## 🔧 Installation & Execution

### ✅ Requirements Installation
```sh
pip install -r requirements.txt
````

### ✅ Run Notebook Analysis & Training

```sh
jupyter notebook Student_Performance_Prediction.ipynb
```

Notebook includes:
✔ Data cleaning
✔ EDA
✔ Visualization
✔ Model training + evaluation



## 🧑‍💻 Author

Rumaisa Fatima
Machine Learning + Data Science Enthusiast
📍 Based in Pakistan 🇵🇰
🔗 GitHub: [https://github.com/rumaisafatima](https://github.com/rumaisafatima)

---

## 📄 License

This project is licensed under the **MIT License** — open for academic & research use.

---

> *Data-driven decisions build stronger futures.*
> Let students grow with the right insights at the right time.






