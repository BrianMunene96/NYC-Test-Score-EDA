# 🗽 Exploring NYC Public School SAT Scores

> Statistical analysis of New York City public school SAT performance to identify top schools and borough-level trends.  
> Completed as part of the **DataCamp Python Data Analysis** track.

---

## 📋 Project Overview

Every year, American high school students take SATs — standardised tests measuring literacy, numeracy, and writing skills, each section scored out of 800. This project analyses NYC public school SAT data to uncover which schools perform best and how performance varies across the city's five boroughs. The insights are relevant to policymakers, researchers, and parents alike.

---

## 🎯 Objectives

- Find all schools where the average math score is **≥ 640** (80% of the 800-point maximum)
- Identify the **top 10 schools** by combined SAT score (math + reading + writing)
- Determine which **NYC borough** has the greatest **standard deviation** in combined SAT scores

---

## 🗂️ Dataset

**`schools.csv`** — NYC public school SAT results with the following fields:

| Column | Description |
|--------|-------------|
| `school_name` | Name of the school |
| `borough` | NYC borough (Manhattan, Brooklyn, Queens, Bronx, Staten Island) |
| `building_code` | Unique building identifier |
| `average_math` | Average SAT math score (max 800) |
| `average_reading` | Average SAT reading score (max 800) |
| `average_writing` | Average SAT writing score (max 800) |
| `percent_tested` | Percentage of students who sat the SAT |

---

## 🛠️ Tools & Libraries

- **Python 3**
- **pandas** — filtering, grouping, aggregation, and feature engineering
- **NumPy** — statistical calculations (mean and standard deviation)

---

## 🔍 Approach

1. Load dataset and preview with `.head()`
2. Filter schools with `average_math >= 640` → sorted DataFrame `best_math_schools`
3. Engineer `total_SAT` column by summing all three section scores → extract top 10 → `top_10_schools`
4. Group by borough, compute mean and std dev of `total_SAT`, append school counts → isolate borough with max std dev → `largest_std_dev`

---

## 📊 Key Outputs

| Variable | Description |
|----------|-------------|
| `best_math_schools` | Schools scoring ≥ 640 in math, sorted descending |
| `top_10_schools` | Top 10 schools by combined SAT total |
| `largest_std_dev` | Borough with the highest SAT score variability (+ stats) |

---

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/nyc-schools-sat-analysis.git
cd nyc-schools-sat-analysis
pip install pandas numpy
jupyter notebook notebook.ipynb
```

---

## 📁 Repository Structure

```
├── schools.csv           # Dataset
├── schoolbus.jpg         # Project header image
├── notebook.ipynb        # Analysis notebook
└── README.md
```

---

*Project completed on the [DataCamp](https://www.datacamp.com) platform.*
