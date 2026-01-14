# ❤️ Heart Disease Diagnostic System 

### **A Comparative Machine Learning Study**
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Project-Hackathon%20Ready-green)]()

## 📌 1. Project Objective
The goal is to provide a data-driven approach to medical diagnosis. Using the UCI Heart Disease dataset, I developed a classification system to predict presence of heart disease with high recall, ensuring that high-risk patients are not overlooked.

---

## 📊 2. Final Model Performance
After extensive cross-validation and tuning, the **Random Forest** model provided the most stable results.

| Metric | Score | Note |
| :--- | :--- | :--- |
| **Accuracy** | **88.52%** | Overall correct predictions |
| **Precision** | **0.87** | Quality of positive predictions |
| **Recall** | **0.90** | Ability to find all positive cases |
| **F1-Score** | **0.88** | Balanced harmonic mean |



---

## 🛠️ 3. Technical Implementation

### **Data Processing**
* **Scaling:** Applied `StandardScaler` to ensure features like `chol` (cholesterol) and `thalach` (heart rate) didn't dominate the models.
* **Leakage Prevention:** Used a robust train-test split before any fitting occurred.

### **Model Comparison & Tuning**
I compared three distinct mathematical approaches to the problem:
1. **Logistic Regression:** Used as a linear baseline.
2. **K-Nearest Neighbors (KNN):** Tuned via `RandomizedSearchCV` for optimal $k$ and distance metrics.
3. **Random Forest:** Tuned via `GridSearchCV` to optimize tree depth and ensemble size.

---

## 🔬 4. Clinical Insights (Feature Importance)
The model identified the following attributes as the strongest indicators of heart disease. This "Black Box" transparency is vital for medical acceptance:

1. **cp (Chest Pain Type):** The most significant predictor.
2. **thalach (Max Heart Rate):** Patients with lower max heart rates during exercise showed higher risk.
3. **ca (Number of Major Vessels):** Number of vessels colored by fluoroscopy.



---

## 📈 5. Visual Evaluation
I utilized **ROC-AUC Curves** to ensure the model maintains a high True Positive Rate while keeping False Positives low. The Area Under the Curve (AUC) of ~0.92 indicates excellent separability.



---

## 💻 6. How to Run

1. **Clone & Install:**
   ```bash
   git clone [https://github.com/your-username/heart-disease-ml.git](https://github.com/your-username/heart-disease-ml.git)
   cd heart-disease-ml
   pip install pandas numpy matplotlib seaborn scikit-learn
