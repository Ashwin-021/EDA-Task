# 🏥 Healthcare Admissions Analysis

Exploratory data analysis and machine learning on a preprocessed hospital admissions dataset (~55,000 patient records). The project looks at patient demographics, medical conditions, billing, length of stay and test results to uncover patterns in hospital care.

---

## 📂 Dataset

**File:** `healthcare_preprocessed.csv`
**Size:** 54,966 rows × 18 columns, no missing values

| Column | Type | Description |
|---|---|---|
| `Name` | text | Patient name |
| `Age` | int | Patient age (13 – 89) |
| `Gender` | categorical | Male / Female |
| `Blood_Type` | categorical | A+, A-, B+, B-, AB+, AB-, O+, O- |
| `Medical_Condition` | categorical | Arthritis, Diabetes, Hypertension, Obesity, Cancer, Asthma |
| `Admission_Date` | date | Date of admission |
| `Doctor` | text | Attending doctor |
| `Hospital` | text | Hospital name |
| `Insurance_Provider` | categorical | Cigna, Medicare, UnitedHealthcare, Blue Cross, Aetna |
| `Billing_Amount` | float | Amount billed for the stay |
| `Room Number` | int | Room number (101 – 500) |
| `Admission_Type` | categorical | Elective, Urgent, Emergency |
| `Discharge_Date` | date | Date of discharge |
| `Medication` | categorical | Lipitor, Ibuprofen, Aspirin, Paracetamol, Penicillin |
| `Test_Results` | categorical | Normal, Abnormal, Inconclusive |
| `Length_of_Stay` | int | Days between admission and discharge (1 – 30) |
| `Age_Group` | categorical | 0-18, 19-30, 31-45, 46-60, 61-75, 76+ |
| `Admission_Urgency` | categorical | Mirrors `Admission_Type` |

---

## 🎯 Objectives

- Understand the distribution of patients by age, gender, condition and insurer
- Analyse how billing relates to condition, admission type and length of stay
- Compare test results across conditions, medications and age groups
- Build baseline models, for example:
  - **Regression:** predict `Billing_Amount` or `Length_of_Stay`
  - **Classification:** predict `Test_Results` or `Admission_Type`

---

## 🛠️ Tech Stack

- Python 3
- pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn
- Jupyter Notebook

---

## 📁 Project Structure

```
healthcare-admissions-analysis/
│
├── data/
│   └── healthcare_preprocessed.csv
├── notebooks/
│   └── analysis.ipynb
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/healthcare-admissions-analysis.git
cd healthcare-admissions-analysis

# 2. (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook notebooks/analysis.ipynb
```

Quick load:

```python
import pandas as pd

df = pd.read_csv("data/healthcare_preprocessed.csv", parse_dates=["Admission_Date", "Discharge_Date"])
print(df.shape)
df.head()
```

---

## ⚠️ Data Notes

Things worth knowing before modelling:

- **Name casing is inconsistent** (e.g. `Bobby JacksOn`). Normalise with `.str.title()` if names are used.
- **Negative `Billing_Amount` values** exist (minimum is about -2,008). Treat them as errors or refunds and decide how to handle them.
- **`Admission_Urgency` duplicates `Admission_Type`**. Drop one to avoid redundancy or target leakage.
- **`Age_Group` includes `0-18`**, but the minimum age is 13, so the group only covers teenagers.
- **Categories are almost perfectly balanced**, which suggests the data is synthetic. Findings may not reflect real-world healthcare patterns.
- `Length_of_Stay` is derived from the admission and discharge dates, so exclude it when predicting those dates.

---

## 📊 Results

> Add your findings here: key plots, model metrics and insights.

---

## 🔮 Future Work

- Hyperparameter tuning and cross-validation
- Try tree-based models (Random Forest, XGBoost)
- Build an interactive dashboard with Streamlit
- Time-series analysis of admissions

---

## 📜 License

This project is licensed under the MIT License. See `LICENSE` for details.

---
