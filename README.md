# Walmart Retail EDA (Python, pandas, seaborn)

Exploratory Data Analysis of Walmart weekly sales to surface seasonal patterns, store performance, volatility, and holiday effects.  
Built in **JupyterLab (Anaconda)** with **pandas**, **seaborn**, and **Matplotlib**.  
Focused on clear business questions and simple, defensible metrics (means, CV, YoY%, holiday lift).

---

## 📁 Project Structure




retail_eda/
├─ data/ # raw CSVs (Kaggle Walmart: train, features, stores, test)
├─ figs/ # exported charts (PNG)
├─ notebooks/
│ └── 01_retail_eda.ipynb
├─ README.md
└─ requirements.txt





Place the unzipped Kaggle files into `data/`:
- `train.csv`
- `features.csv`
- `stores.csv`
- (`test.csv` unused for EDA)

---

## 📊 Dataset Overview

From the Kaggle “Walmart Store Sales Forecasting” dataset.

**Summary:**
- **~420,000+ rows**
- **45 stores**
- **~99 departments**
- **Weekly data:** 2010–2012
- Economic signals: temperature, fuel price, CPI, unemployment  
- Holiday indicator + markdown campaigns

Key columns used:
`Store`, `Dept`, `Date`, `Weekly_Sales`, `IsHoliday`, `Type`, `Size`, `Temperature`, `Fuel_Price`, `CPI`, `Unemployment`.

---

## 🔍 Questions Answered (with charts)

### **Core (final set)**

---

### 1. **Department Seasonality (Dept × Month heatmap)**  
**Shows:** mean weekly sales by month per department  
**Takeaway:** holiday-sensitive depts peak in **Nov–Dec**; some depts are summer-heavy; others are flat (baseline).

### 2. **Store Size vs Average Weekly Sales (scatter; hue = Type)**  
**Shows:** relationship between physical size and typical sales  
**Takeaway:** bigger stores generally sell more, with diminishing returns; a few large underperformers merit diagnostics.

### 3. **Risk–Return by Store (mean vs CV; scatter)**  
**Shows:** performance vs volatility using **CV = std/mean**  
**Takeaway:** a “workhorse” cluster (high mean, low CV) and a “spiky” cluster (high CV) for operational focus.

---

### **Additional EDA**
- Total sales by store (leaderboard)
- Average weekly sales by store (full period & 4-week MA)
- YoY growth by store (2011 vs 2010, top/bottom)
- Holiday lift by store (% vs non-holiday)
- Department Pareto (80/20; colored ≤80%)

Each notebook cell includes a short  
**“Business Question → Answer”** commentary block.

---

## ⭐ Key Insights Summary

- Walmart’s sales are **highly concentrated**: the top ~88 departments generate **80%+** of revenue.  
- Strong **seasonality** exists for key departments (92, 38, 95, 72), peaking in **Nov–Dec**.  
- **Store type strongly explains performance**: Type A stores achieve the highest sales with lower volatility.  
- Holiday periods boost sales for most stores by **5–18%**, though a few stores show **negative lift**, indicating local issues.  
- Store size is a strong predictor of performance, though with **diminishing returns** beyond ~200,000 sq ft.  
- Year-over-year trends show **large performance gaps**, with some stores growing ~20% while others decline up to ~15%.



---

## 🧰 Environment & Setup

**Python version:** 3.10+

Create a clean environment:

```bash
# optional new Conda env
conda create -n retail_eda python=3.10 -y
conda activate retail_eda

# install deps
pip install -r requirements.txt


---





##  Author
Maysarah Aljamal
[LinkedIn](https://www.linkedin.com/in/maysarah-aljamal-97a842323/) • [GitHub](https://github.com/lachmula-cmd)


