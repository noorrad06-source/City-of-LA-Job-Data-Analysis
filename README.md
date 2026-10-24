# City of Los Angeles Job Bulletins Data Extraction & Analysis

An end-to-end data engineering and exploratory analysis pipeline designed to process unstructured municipal job bulletin text files into structured, actionable insights.

---

## 📌 Project Overview
Municipal job bulletins are issued as unstructured text documents containing critical employment criteria—salary ranges, education requirements, experience levels, license needs, and exam types. This project automates the parsing, normalization, and quantitative analysis of these text bulletins using Python, Regular Expressions, and Natural Language Processing (`spaCy`).

---

## 📊 Key Empirical Findings

### Q1: Best Job for a Non-Experienced Job Seeker
- **Top Role:** **Harbor Engineer** ($151,442.00 entry salary) requiring minimal prior municipal experience and baseline degree credentials.
- **Secondary High-Yield Roles:**
  - **Marine Environmentalist:** $102,458.00
  - **Environmental Specialist:** $92,895.00

---

### Q2: School Type vs. Entry Compensation
Higher educational attainment directly correlates with higher entry compensation across municipal roles.

| School Type | Average Entry Salary | Median Entry Salary |
| :--- | :---: | :---: |
| **University** | **$96,724.79** | **$87,278.00** |
| **High School + Trade** | $91,999.22 | — |
| **College** | $88,985.43 | — |
| **Vocational / Technical** | $62,023.64 | — |

---

### Q3: Peak Recruitment Period
- **Busiest Month:** **March (Month 3)** leads posting activity with **68 active bulletin releases**, followed closely by **July** and **October**.

---

### Q4: Experience vs. Educational Level Correlation
- **Statistical Correlation:** Required experience length demonstrates a statistically significant positive rank correlation with salary (Spearman $\rho = 0.2107$, $p = 2.73 \times 10^{-8}$).
- **Insight:** Educational credentials serve as initial baseline qualifiers, whereas documented years of experience dictate step-level compensation increases across pay grades.

---

### Q5: Top Fresh Graduate Feeder Roles
- **Most Frequent Feeder Roles:**
  1. **Electrical Craft Helper** (11 occurrences)
  2. **Administrative Clerk** (9 occurrences)

---

## 📁 Repository Structure

```text
City-of-LA-Job-Data-Analysis/
├── data/                    # Unstructured job bulletin text files (.txt)
├── notebooks/               # Jupyter/Colab notebooks for analysis & EDA
├── src/                     # Modular Python parsing scripts
│   ├── extractor.py         # Main extraction pipeline
│   └── text_utils.py        # Regex and NLP helper routines
├── tests/                   # Automated unit tests
├── .gitignore               # Git exclusions file
├── requirements.txt         # Project dependencies
└── README.md                # Project documentation