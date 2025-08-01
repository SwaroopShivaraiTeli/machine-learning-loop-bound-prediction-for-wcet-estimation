# machine-learning-loop-bound-prediction-for-wcet-estimation
# 🔁 Automated Loop Iteration Prediction using Machine Learning  
### Repository: `machine-learning-loop-bound-prediction-for-wcet-estimation`

## 📘 Overview  
This project presents a machine learning-based solution to the problem of **loop iteration prediction**, a crucial aspect in **Worst-Case Execution Time (WCET)** estimation for real-time and embedded systems. By analyzing key loop characteristics, the model can automatically classify whether a loop is:

- A **small-iteration loop** (e.g., fewer than 10 cycles)
- A **nested loop** (i.e., one loop contained within another)

This automation helps reduce manual analysis effort in embedded code timing evaluations.

---

## 💡 Motivation  
Traditional WCET analysis tools require manual loop annotations or static assumptions, which can be:
- Time-consuming
- Error-prone
- Overly conservative

**Machine learning** offers a scalable alternative by learning loop behavior patterns from data — enabling more adaptive, intelligent WCET estimation workflows.

---

## 📊 Dataset Description
- **Size:** 300 synthetic loop samples  
- **Features:**
  - `initial_value` – Loop counter start
  - `increment` – Loop step value
  - `exit_condition` – Loop termination value
  - `nesting_level` – Depth of nesting
- **Labels:**
  - `label_small_iter`: 1 if loop executes < 10 times
  - `label_nested`: 1 if loop is nested

Synthetic data ensures full control, balance, and interpretability.

---

## 🧠 Models Used
- **Random Forest Classifier**  
  - F1-score: ~92% on small-iteration detection  
  - Robust and interpretable
- **K-Nearest Neighbors (KNN)**  
  - F1-score: ~84%  
  - Used as a baseline model

---

## 📈 Results Summary  
- Random Forest outperformed KNN  
- Features like `exit_condition` and `increment` were most predictive  
- Demonstrated high accuracy for both target labels  
- Validated ML as a viable assistant for WCET loop analysis  
