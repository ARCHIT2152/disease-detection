# 🩺 Disease Detection System Using Machine Learning
### Diabetes Prediction | B.Tech CSE Mini Project


## 📌 About the Project

This is a beginner-level machine learning project that predicts whether a patient is **diabetic or non-diabetic** based on medical features like glucose level, BMI, age, and more.

Built as part of my **Introduction to Machine Learning** coursework in **B.Tech CSE (2nd Year)**.

The project trains and compares **4 classification models** on the Pima Indians Diabetes Dataset and picks the best performer.

---

## 📂 Repository Structure

```
📦 diabetes-disease-detection
 ┣ 📓 Disease_Detection_Diabetes.ipynb   ← Main Jupyter Notebook
 ┣ 📄 diabetes.csv                       ← Dataset
 ┗ 📄 README.md                          ← You are here
```

---

## 📊 Dataset

**Source:** Pima Indians Diabetes Dataset  
**Records:** 768 patients  
**Features:** 8 medical attributes + 1 target variable

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skinfold thickness (mm) |
| Insulin | 2-hour serum insulin (mu U/ml) |
| BMI | Body mass index |
| DiabetesPedigreeFunction | Diabetes likelihood based on family history |
| Age | Age in years |
| **Outcome** | **Target — 1 = Diabetic, 0 = Non-Diabetic** |

---

## 🔬 What's Inside the Notebook

1. **Introduction** — What is diabetes and why ML can help with early detection
2. **Library Imports** — pandas, numpy, matplotlib, seaborn, sklearn, xgboost
3. **Data Loading** — Load and explore the dataset (shape, info, describe)
4. **Data Cleaning** — Handle impossible zero values using median imputation
5. **EDA (Exploratory Data Analysis)** — 5 visualizations with observations
   - Class distribution countplot
   - Correlation heatmap
   - Age distribution
   - BMI distribution
   - Glucose vs Outcome boxplot
6. **Feature Selection** — Separate features (X) and target (y)
7. **Train-Test Split** — 80/20 split with stratification
8. **Feature Scaling** — StandardScaler applied for LR and SVM
9. **Model Training** — 4 models trained and evaluated
10. **Accuracy Comparison** — Results table + bar chart
11. **Conclusion** — Key findings
12. **Future Scope** — Ideas for improvement and deployment

---

## 🤖 Models Used

| Model | Parameters Used |
|---|---|
| Logistic Regression | `max_iter=1000` |
| Random Forest | `n_estimators=100, max_depth=5` |
| SVM | `kernel='rbf', C=1, gamma='scale'` |
| XGBoost | `n_estimators=100, max_depth=3, learning_rate=0.1` |

---

## 📈 Results

| Model | Accuracy |
|---|---|
| Logistic Regression | ~78% |
| SVM | ~79% |
| Random Forest | ~82% |
| **XGBoost** | **~84%** ✅ |

> XGBoost achieved the highest accuracy among all four models.

---

## 🔑 Key Findings

- **Glucose** is the strongest predictor of diabetes (highest correlation with Outcome)
- **BMI** and **Age** are also significant risk indicators
- Ensemble models (Random Forest, XGBoost) outperformed simpler models (LR, SVM)
- Replacing impossible zero values with column medians improved data quality

---

## 🛠️ How to Run

**1. Clone the repository**
```bash
git clone https://github.com/your-username/diabetes-disease-detection.git
cd diabetes-disease-detection
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter
```

**3. Launch Jupyter Notebook**
```bash
jupyter notebook Disease_Detection_Diabetes.ipynb
```

**4. Run all cells** — `Kernel → Restart & Run All`

> Make sure `diabetes.csv` is in the same folder as the notebook.

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
jupyter
```

---

## 🚀 Future Scope

- Deploy the model as a web app using **Streamlit** or **Flask**
- Train on a larger and more diverse dataset
- Add more health parameters (cholesterol, activity level, diet)
- Explore deep learning approaches
- Handle class imbalance using SMOTE
