# 🎓 Students Performance Analysis

Exploratory data analysis (EDA) of exam scores for 1,000 students, looking at how background factors such as parental education, lunch type and test preparation relate to performance in math, reading and writing.

---

## 📂 Dataset

**File:** `StudentsPerformance_csv_EDA.csv`
**Size:** 1,000 rows × 8 columns, no missing values, no duplicate rows

| Column | Type | Description |
|---|---|---|
| `gender` | categorical | female (518) / male (482) |
| `race/ethnicity` | categorical | Anonymised groups A to E |
| `parental level of education` | categorical | some high school, high school, some college, associate's degree, bachelor's degree, master's degree |
| `lunch` | categorical | standard (645) / free/reduced (355) |
| `test preparation course` | categorical | none (642) / completed (358) |
| `math score` | int | 0 – 100 (mean ≈ 66.1) |
| `reading score` | int | 17 – 100 (mean ≈ 69.2) |
| `writing score` | int | 10 – 100 (mean ≈ 68.1) |

---

## 🎯 Objectives

- Understand the distribution of scores in each subject
- Compare performance across gender, lunch type, parental education and ethnicity group
- Measure the effect of the test preparation course
- Check how strongly the three subject scores are correlated
- (Optional) Build a simple model to predict a score from the background features

---

## 🛠️ Tech Stack

- Python 3
- pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (for the optional modelling step)
- Jupyter Notebook

---

## 📁 Project Structure

```
students-performance-eda/
│
├── data/
│   └── StudentsPerformance_csv_EDA.csv
├── notebooks/
│   └── eda.ipynb
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/students-performance-eda.git
cd students-performance-eda

# 2. (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook notebooks/eda.ipynb
```

Quick load:

```python
import pandas as pd

df = pd.read_csv("data/StudentsPerformance_csv_EDA.csv")
df["average score"] = df[["math score", "reading score", "writing score"]].mean(axis=1)
df.head()
```

---

## 🔍 Suggested Analysis

- Histograms and box plots of each score
- Group-wise averages, for example `df.groupby("lunch")["math score"].mean()`
- Heatmap of the correlation between math, reading and writing scores
- Count plots of the categorical features
- Pass/fail or grade bands built from the average score

---

## ⚠️ Data Notes

- Column names contain spaces and a slash. Rename them (e.g. `math_score`) to make coding easier.
- A few very low scores (a math score of 0, for example) are outliers. Check them before deciding whether to keep them.
- `race/ethnicity` is given as anonymised groups, so avoid drawing conclusions about real populations.
- This is a well-known public teaching dataset and is likely synthetic. Treat findings as practice, not as evidence about real students.
- The data shows correlation only. It cannot show that a factor causes better or worse scores.

---

## 📊 Results

> Add your findings here: key plots and insights.

---

## 🔮 Future Work

- Regression models to predict scores
- Statistical tests (t-test, ANOVA) for group differences
- Interactive dashboard with Streamlit

---

## 📜 License

This project is licensed under the MIT License. See `LICENSE` for details.
