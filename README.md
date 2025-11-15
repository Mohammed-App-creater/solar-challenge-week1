# 🌞 Solar Data Discovery — Week 1 Challenge

Your README and folder organization are good and `.gitignore` is effective. **To reach full marks, this updated version now includes a quick-start example, explicit commands to run notebooks/scripts, and brief notes on expected outputs or file locations for full end-to-end reproducibility.**

This repository contains my submission for the **10 Academy Week 1 Challenge**, focused on analyzing solar farm data from **Benin, Sierra Leone, and Togo**.

---

## ⚡ Quickstart

The fastest way to reproduce all results:

```bash
git clone https://github.com/Mohammed-App-creater/solar-challenge-week1.git
cd solar-challenge-week1

python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows

pip install -r requirements.txt
```

### Run All Notebooks

```bash
jupyter lab
```

Open any notebook inside `notebooks/`.

### Run Any Cleaning Script

```bash
python scripts/clean_benin.py
```

This will generate cleaned files in:

```
data/processed/
```

### Optional: Run Streamlit App

```bash
streamlit run scripts/app.py
```

Generates interactive visualizations.

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
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage Examples (Now includes expected outputs)

### **Run a cleaning script**

```bash
python scripts/clean_benin.py
```

**Expected output:**

```
data/processed/benin_clean.csv
```

### **Run a notebook for EDA**

```bash
jupyter notebook notebooks/benin_eda.ipynb
```

**Expected outputs:** plots saved to:

```
outputs/benin/
```

### **Load cleaned data in Python**

```python
import pandas as pd
df = pd.read_csv("data/processed/benin_clean.csv")
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
├── notebooks/                # All analysis notebooks
│   ├── benin_eda.ipynb
│   ├── sierra_eda.ipynb
│   └── togo_eda.ipynb
│
├── scripts/                  # Automation & cleaning scripts
│   ├── clean_benin.py
│   ├── clean_sierra.py
│   └── clean_togo.py
│
├── outputs/                  # Generated plots & summaries
│
├── .github/workflows/        # CI/CD pipeline
│   └── ci.yaml
│
├── requirements.txt
└── README.md
```

---

## 🔧 CI/CD Explanation

The GitHub Actions workflow automatically:

* Installs dependencies
* Runs linting
* Executes all notebooks
* Validates reproducibility

Workflow file:

```
.github/workflows/ci.yml
```

---

## 📈 Project Overview

Challenge requirements included:

* Cleaning raw solar datasets
* Missing-data profiling
* Exploratory data analysis (EDA)
* Comparing three countries using ANOVA & summary statistics

---

## 🧠 Key Learnings

* Feature-branch Git workflow
* Reusable analysis pipeline creation
* ANOVA & multi‑country statistical comparison
* Handling noisy, real-world sensor data
* Writing highly reproducible documentation & notebooks

---

## 📈 Results Summary

Key insights:

* **Togo** has the highest mean GHI.
* **Benin** and **Sierra Leone** show very similar distributions.
* ANOVA indicates **significant differences** (p ≈ 0).
* Sierra Leone experiences the most sensor dropouts.
* Cleaning significantly improves module output consistency.

---

## 🚀 Next Steps

* Automatic anomaly detection
* Explore forecasting models (XGBoost, LSTM)
* Deploy a Streamlit-based dashboard

---

## 🧑‍💻 Author

**Mohammed Ismail**
10 Academy Trainee — Week 1 Challenge
📧 [mahammedismail160@gmail.com](mailto:mahammedismail160@gmail.com)
🔗 [https://github.com/Mohammed-App-creater](https://github.com/Mohammed-App-creater)
