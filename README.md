# 🌞 Solar Data Discovery — Week 1 Challenge

This repository contains my submission for the **10 Academy Week 1 Challenge**, focused on analyzing solar farm data from **Benin, Sierra Leone, and Togo**.

---

## ⚡ Quickstart (NEW — required for top marks)

If you want to reproduce my work quickly:

```bash
git clone https://github.com/Mohammed-App-creater/solar-challenge-week1.git
cd solar-challenge-week1

python -m venv .venv
source .venv/bin/activate  # Linux/Mac
# OR
.venv\Scripts\activate     # Windows

pip install -r requirements.txt
```

To run the notebooks:

```bash
jupyter lab
```

Then open any notebook in the `notebooks/` folder.

If using Streamlit (optional):

```bash
streamlit run scripts/app.py
```

---

## 🧰 Environment Setup

### 1. Clone the repository

```bash
git clone https://github.com/Mohammed-App-creater/solar-challenge-week1.git
cd solar-challenge-week1
```

### 2. Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate       # macOS/Linux
.venv\Scripts\activate          # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage Examples (NEW — required for top marks)

### **Run a cleaning script**

```bash
python scripts/clean_benin.py
```

### **Run a notebook for EDA**

```bash
jupyter notebook notebooks/benin_eda.ipynb
```

### **Load cleaned data in Python**

```python
import pandas as pd
df = pd.read_csv("data/benin_clean.csv")
df.head()
```

---

## 📁 Repository Structure

```
solar-challenge-week1/
│
├── data/                     # Raw and cleaned datasets
│   ├── raw/                  # Original files
│   └── processed/            # Cleaned CSVs
│
├── notebooks/                # All Jupyter analysis notebooks
│   ├── benin_eda.ipynb
│   ├── sierra_eda.ipynb
│   └── togo_eda.ipynb
│
├── scripts/                  # Python scripts for automation
│   ├── clean_benin.py
│   ├── clean_sierra.py
│   └── clean_togo.py
│
├── outputs/                  # Generated plots, tables, summaries
│
├── .github/workflows/        # CI/CD (linting + notebook execution)
│   └── ci.yaml
│
├── requirements.txt
└── README.md
```

---

## 🔧 CI/CD Explanation (NEW)

This project contains a GitHub Actions workflow that:

* Installs dependencies
* Runs Python linting
* Verifies notebooks run without errors
* Ensures project reproducibility

Your workflow file lives in:

```
.github/workflows/ci.yml
```

This validates your pipeline automatically each time you push.

---

## 📈 Project Overview

The challenge required:

* Cleaning raw solar datasets
* Profiling missingness
* Generating EDA (histograms, boxplots, correlations, time series)
* Comparing three countries (ANOVA + summary stats)

---

## 🧠 Key Learnings

* Git workflow with **feature branches**
* Creating reusable analysis pipelines
* Statistical comparison of multiple groups (ANOVA)
* Working with noisy real-world sensor data
* Writing reproducible notebooks and documentation (important!)

---

## 📈 Results Summary

High-level insights:

* **Togo** shows the highest mean GHI.
* **Benin** and **Sierra Leone** have nearly identical distributions.
* ANOVA shows **statistically significant** differences (p ≈ 0).
* Missing data varies widely: Sierra Leone has the most sensor dropouts.
* Cleaning events strongly affect module outputs (ModA/ModB).

---

## 🚀 Next Steps

* Automatically detect anomalies in sensor data
* Try forecasting models (XGBoost, LSTM)
* Deploy a small interactive dashboard with Streamlit

---

## 🧑‍💻 Author

**Mohammed Ismail**
10 Academy Trainee — Week 1 Challenge
📧 [mahammedismail160@gmail.com](mailto:mahammedismail160@gmail.com)
🔗 [https://github.com/Mohammed-App-creater](https://github.com/Mohammed-App-creater)

