# 🧠 Employee Performance Prediction using Machine Learning

> An HR Analytics project that uses machine learning to predict employee performance ratings based on workplace factors — built with real-world relevance to organizations in Kenya and beyond.

---

## 📌 Project Overview

This project applies supervised machine learning to classify employee performance ratings (2, 3, or 4) using a dataset from **INX Future Inc**. The goal is to help HR departments proactively identify performance trends, optimize promotion decisions, and improve workforce productivity.

**Target Variable:** `PerformanceRating` (ordinal: 2 = Low, 3 = Good, 4 = Excellent)

---

## 🏢 Business Problem

Organizations lose productivity and revenue due to undetected underperformance and missed high-performer recognition. Predictive analytics empowers HR teams to:

- Identify at-risk employees before performance drops
- Target training investments where they matter most
- Make data-backed promotion and compensation decisions
- Improve employee retention by understanding satisfaction drivers

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| **Source** | INX Future Inc HR Dataset |
| **File** | `INX_Future_Inc_Employee_Performance_CDS_Project2_Data_V1.8.xls` |
| **Records** | ~1,200 employees |
| **Features** | 28 columns (demographics, job info, satisfaction scores, experience) |
| **Target** | `PerformanceRating` (3 classes) |

**Key Features Used:**
- Age, Gender, Marital Status, Education Background
- Department, Job Role, Business Travel Frequency
- Job Satisfaction, Environment Satisfaction, Work-Life Balance
- Salary Hike Percentage, Training Times Last Year
- Total Work Experience, Years at Company, Years in Current Role

---

## 🔧 Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.9 | Core language |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | ML modeling & evaluation |
| Joblib | Model serialization |

---

## 🔄 Project Pipeline

```
Data Loading → Data Cleaning  → EDA → Preprocessing → Model Training → Evaluation → Insights
```

### Step-by-Step:
1. **EDA** — Distribution of ratings, correlation heatmaps, department-wise analysis
2. **Data Cleaning** — Checked for duplicates, nulls, and outliers via boxplots
3. **Feature Engineering** — Experience binning (Early/Mid/Senior/Veteran career)
4. **Preprocessing** — StandardScaler (numerical) + OneHotEncoder (categorical) via ColumnTransformer
5. **Modeling** — Logistic Regression, Random Forest, Gradient Boosting
6. **Tuning** — GridSearchCV with 5-fold cross-validation
7. **Evaluation** — Accuracy, Precision, Recall, F1, Confusion Matrix, Feature Importance

---

## 📈 Model Results

| Model | Accuracy | F1 Score |
|-------|----------|---------|
| **Gradient Boosting** | **93.3%** | **93.2%** |
| Tuned Random Forest | 92.1% | 91.8% |
| Random Forest | 91.7% | 91.3% |
| Logistic Regression | 82.5% | 81.7% |

> ✅ **Best Model: Gradient Boosting** — 93.3% accuracy on the test set.

---

## 💡 Key Insights

- **Environment Satisfaction** is one of the strongest predictors of performance — employees in comfortable, well-managed environments consistently rate higher.
- **Salary Hike Percentage** shows a strong positive correlation with performance, suggesting compensation is a significant motivator.
- **Training frequency** contributes meaningfully — employees trained 2–3 times per year tend to perform better.
- **Total Work Experience alone** is NOT a strong predictor — performance is shaped by role fit, satisfaction, and team dynamics more than raw experience.
- **Department differences** exist but are moderate — Sales and Development departments show slightly higher average performance ratings.

---

## 📋 Business Recommendations

1. **Invest in environment quality** — workspace conditions, team culture, and managerial relationships directly impact ratings.
2. **Link salary hikes to performance reviews** — competitive compensation keeps high performers motivated.
3. **Standardize training programs** — 2–3 targeted trainings per year is the sweet spot.
4. **Don't over-rely on experience** — use satisfaction scores and engagement metrics, not just tenure, when making promotion decisions.
5. **Flag low-satisfaction employees early** — job satisfaction and work-life balance scores can serve as early warning signals.

---

## 🗂️ Repository Structure

```
employee-performance-prediction/
│
├── Employee_Performance_Prediction.ipynb   # Main Jupyter notebook
├── INX_Future_Inc_Employee_Performance_... # Dataset (Excel file)
├── employee_performance_model.pkl          # Saved trained model
├── requirements.txt                        # Python dependencies
└── README.md                               # This file
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/Walpapa/employee-performance-prediction.git
cd employee-performance-prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook Employee_Performance_Prediction.ipynb
```

### 4. (Optional) Load the saved model
```python
import joblib
model = joblib.load("employee_performance_model.pkl")
# model.predict(new_employee_data)
```

---

## 📦 requirements.txt

```
numpy
pandas
matplotlib
seaborn
scikit-learn
openpyxl
xlrd
joblib
jupyter
```

---

## 🌍 Relevance to Kenyan Organizations

Banks, insurance firms, SACCOs, NGOs, and government institutions in Kenya can directly apply this framework to:
- Replace subjective annual appraisals with data-backed scoring
- Identify departments needing management intervention
- Optimize training budgets with measurable ROI

---

## 👤 Author

**Philip Walpole Opolo**
- 📧 philipwopolo@gmail.com
- 🐙 [GitHub](https://github.com/Walpapa)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
