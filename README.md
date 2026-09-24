# 📱 Impact of Social Media on Life

> A comprehensive data science project analysing how social media usage patterns affect student **mental health**, **sleep quality**, **stress levels**, and **academic performance** — powered by a real-world Kaggle dataset of 4,500 students.

---

## 📌 Table of Contents

- [Project Description](#-project-description)
- [Real-World Problem](#-real-world-problem)
- [Dataset](#-dataset)
- [Technologies Used](#-technologies-used)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [How to Run](#-how-to-run)
- [Key Findings](#-key-findings)
- [Conclusion](#-conclusion)

---

## 📖 Project Description

This project presents an end-to-end data science investigation into the multi-dimensional impact of social media on student life. Using a dataset of **4,500 students** across High School, Undergraduate, and Postgraduate levels, the analysis covers:

- **Exploratory Data Analysis (EDA)** — distribution profiles, group comparisons, platform breakdowns
- **Statistical Testing** — Pearson/Spearman correlation, ANOVA, Kruskal-Wallis, Chi-square, t-tests
- **Machine Learning — Classification** — predicting the *Overall Impact* category (Beneficial / Neutral / Negative) using Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting
- **Machine Learning — Regression** — predicting student *GPA* from social media and lifestyle features using Linear, Ridge, and Random Forest regression

All findings are grounded in statistical evidence, and every chart and metric is generated directly from the data inside the Jupyter Notebook.

---

## 🌍 Real-World Problem

Social media usage among students is rising rapidly, yet the true quantitative impact on well-being and academic outcomes remains poorly understood. Key questions this project answers:

| # | Research Question |
|---|---|
| 1 | Does increased daily social media usage measurably degrade sleep and raise stress? |
| 2 | Is late-night social media access a significant predictor of lower GPA? |
| 3 | Which platforms and behavioural patterns are most linked to negative outcomes? |
| 4 | Can a machine learning model reliably classify whether a student's overall impact is Beneficial, Neutral, or Negative? |
| 5 | How accurately can student GPA be predicted from social media and lifestyle features alone? |

---

## 📊 Dataset

| Property | Value |
|---|---|
| **Source** | [Kaggle — Social Media Impact on Life](https://www.kaggle.com/datasets/mdismielhossenabir/impact-of-social-media-on-life) |
| **File** | `Social_media_impact_on_life.csv` |
| **Rows** | 4,500 students |
| **Columns** | 16 features |
| **Target** | `Overall_Impact` (Beneficial / Neutral / Negative) |

### Feature Summary

| Feature | Type | Description |
|---|---|---|
| `Age` | Numeric | Student age (15–26) |
| `Gender` | Categorical | Female, Male, Non-Binary, Prefer not to say |
| `Academic_Level` | Ordinal | High School · Undergraduate · Postgraduate |
| `Primary_Platform` | Categorical | Most-used platform (Instagram, TikTok, YouTube, …) |
| `Daily_Usage_Hours` | Numeric | Average weekday social media hours per day |
| `Weekend_Extra_Hours` | Numeric | Extra usage on weekends |
| `Device_Type` | Categorical | Smartphone · Laptop/PC · Tablet |
| `Sleep_Duration_Hours` | Numeric | Average nightly sleep in hours |
| `Sleep_Quality_Score` | Ordinal (1–5) | Self-rated sleep quality |
| `Late_Night_Usage` | Boolean | Social media use after 10 PM |
| `Social_Comparison_Frequency` | Ordinal | Never / Rarely / Sometimes / Frequently / Always |
| `Perceived_Stress_Score` | Numeric (0–40) | Validated stress scale |
| `Mental_Health_Index` | Numeric (0–100) | Composite well-being score |
| `Academic_Performance_GPA` | Numeric | GPA on 4.0 scale |
| `Overall_Impact` | **Target** | Beneficial · Neutral · Negative |

---

## 🛠 Technologies Used

| Category | Library / Tool | Version |
|---|---|---|
| Language | Python | 3.10+ |
| Data Manipulation | pandas | 2.3.3 |
| Numerical Computing | numpy | 2.2.6 |
| Visualisation | matplotlib | 3.10.7 |
| Visualisation | seaborn | 0.13.2 |
| Statistical Analysis | scipy | 1.14.1 |
| Machine Learning | scikit-learn | 1.5.2 |
| Notebook Runtime | jupyter notebook | 7.2.2 |
| Kernel | ipykernel | 6.29.5 |

---

## 🗂 Project Structure

```
IBM project/
│
├── Social_Media_Impact_Analysis.ipynb   # Main Jupyter Notebook (all code & results)
├── Social_media_impact_on_life.csv      # Raw dataset (Kaggle)
├── requirements.txt                     # Python dependencies
└── README.md                            # Project documentation (this file)
```

---

## ⚙️ Installation & Setup

### 1 — Clone or download the repository

```bash
git clone https://github.com/your-username/social-media-impact.git
cd social-media-impact
```

### 2 — (Recommended) Create a virtual environment

```bash
# Using venv
python -m venv venv

# Activate — Windows
venv\Scripts\activate

# Activate — macOS / Linux
source venv/bin/activate
```

### 3 — Install all dependencies

```bash
pip install -r requirements.txt
```

> **requirements.txt** contains:
> `pandas==2.3.3`, `numpy==2.2.6`, `matplotlib==3.10.7`, `seaborn==0.13.2`,
> `scipy==1.14.1`, `scikit-learn==1.5.2`, `notebook==7.2.2`, `ipykernel==6.29.5`

---

## ▶️ How to Run

### Option A — Jupyter Notebook (recommended)

```bash
jupyter notebook Social_Media_Impact_Analysis.ipynb
```

Then in the browser, go to **Kernel → Restart & Run All** to execute every cell from top to bottom.

### Option B — JupyterLab

```bash
pip install jupyterlab
jupyter lab Social_Media_Impact_Analysis.ipynb
```

### Option C — VS Code

1. Open the project folder in VS Code.
2. Install the **Jupyter** extension (Microsoft).
3. Open `Social_Media_Impact_Analysis.ipynb`.
4. Select your Python interpreter/virtual environment from the kernel picker.
5. Click **Run All**.

> ⚠️ Ensure `Social_media_impact_on_life.csv` is in the **same directory** as the notebook before running.

---

## 🔍 Key Findings

### 📉 Social Media Usage & Mental Health
- Daily usage vs Mental Health Index: **r = −0.850** (p < 0.001) — the strongest correlation in the dataset.
- Every additional hour of social media use is statistically associated with a measurable decline in the composite mental well-being index.

### 😴 Social Media Usage & Sleep
- Daily usage vs Sleep Duration: **r = −0.716** (p < 0.001).
- Students with *Negative* overall impact sleep an average of **4.23 hrs/night** — nearly **3 hours less** than *Beneficial* students (7.03 hrs).

### 😰 Social Media Usage & Stress
- Daily usage vs Perceived Stress Score: **r = +0.751** (p < 0.001).
- Mean stress by group — Beneficial: **11.2** | Neutral: **22.3** | Negative: **31.1** (ANOVA F = 2,619, p < 0.001).

### 🎓 Social Media Usage & GPA
- Daily usage vs GPA: **r = −0.704** (p < 0.001).
- GPA gap between impact groups: Beneficial **3.544** vs Negative **2.555** — a difference of **~1.0 GPA point**.

### 🌙 Late-Night Usage
- **58.8%** of students use social media after 10 PM.
- Late-night users earn a mean GPA of **3.348** vs **3.547** for non-users (t = −17.91, p < 0.001) — a statistically significant 0.199-point deficit.

### 🤖 Machine Learning Results

| Model | Task | Performance |
|---|---|---|
| Random Forest | Classification (Overall Impact) | ~91% accuracy · 5-fold CV stable |
| Gradient Boosting | Classification | ~89% accuracy |
| Random Forest Regressor | GPA Prediction | R² ≈ 0.84 · RMSE ≈ 0.15 |
| Linear / Ridge Regression | GPA Prediction | R² ≈ 0.68–0.71 |

**Top predictive features** (both tasks): `Daily_Usage_Hours`, `Mental_Health_Index`, `Perceived_Stress_Score`, `Sleep_Duration_Hours`, `Late_Night_Usage`.

---

## ✅ Conclusion

This study demonstrates that **daily social media usage volume is the primary driver of adverse student outcomes**. The evidence is statistically robust across every outcome metric tested — sleep, stress, mental health, and GPA all degrade significantly as usage increases. Critically, over **81.8% of students report a net Beneficial impact**, showing that social media is not inherently harmful — the detrimental effects are concentrated in a high-usage minority.

The machine learning models confirm that student outcomes are *predictable* from observable behavioural features, achieving over 90% classification accuracy and explaining ~84% of GPA variance. This opens the door to early-warning systems that could identify at-risk students before outcomes deteriorate.

**Primary recommendation:** Limiting daily usage to under 5 hours and avoiding late-night access are the two highest-impact individual behavioural changes for protecting mental health and academic performance.

---

## 📄 License

This project is for academic and educational purposes. Dataset sourced from [Kaggle](https://www.kaggle.com/datasets/mdismielhossenabir/impact-of-social-media-on-life) under its respective licence.
