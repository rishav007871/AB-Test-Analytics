# MöbelHaus Digital - A/B Test Analysis Portfolio Project

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![SQL](https://img.shields.io/badge/SQL-DuckDB-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple)
![Matplotlib](https://img.shields.io/badge/Visualization-Matplotlib-green)
![SciPy](https://img.shields.io/badge/Statistics-SciPy-blue)

| **Field** | **Details** |
|------------|-------------|
| **Author** | Rishav Dey |
| **Role** | Associate Data Engineer |
| **Project Type** | A/B Test Evaluation & Strategic Recommendation |
| **Tools Used** | Python, DuckDB (SQL), Pandas, Matplotlib, SciPy |

---

# 📑 Table of Contents

- [📊 Project Overview](#-project-overview)
- [🎯 The Challenge](#-the-challenge)
- [🔍 Key Findings](#-key-findings)
- [💰 Business Impact](#-business-impact)
- [🛠️ Technical Skills Demonstrated](#️-technical-skills-demonstrated)
- [⚙️ Tech Stack](#️-tech-stack)
- [📁 Project Structure](#-project-structure)
- [🎓 What I Learned](#-what-i-learned)
- [💼 Business Context](#-business-context)
- [🔗 Connect](#-connect)

---

# 📊 Project Overview

This project analyzes a four-week A/B experiment conducted for a fictional Berlin-based furniture e-commerce company. The objective was to determine whether a redesigned product detail page improved business performance or merely increased engagement metrics.

Using SQL, Python, statistical hypothesis testing, and business impact analysis, I evaluated whether the experiment should be rolled out to all users.

**Business Question:**

> Does the redesigned product page actually increase revenue, or does it simply improve engagement metrics?

**Deliverable:**

A strategic recommendation memo backed by SQL analysis, statistical testing, and quantified business impact.

---

# 🎯 The Challenge

**Test Hypothesis**

Increasing visual immersion on product pages will improve conversion by helping customers better visualize furniture in their homes.

### Variants

- **Control (A):** Traditional product page with detailed specifications and a standard image gallery.
- **Variant (B):** Visual-first redesign with lifestyle images, sticky CTA, and condensed specifications.

### The Complication

Although engagement metrics improved dramatically, the key question remained:

**Did those improvements actually increase revenue?**

---

# 🔍 Key Findings

## 1. Engagement ≠ Revenue

Variant B improved engagement:

- ✅ Time on Page: **+82%**
- ✅ Images Viewed: **+68%**
- ✅ Add-to-Cart Rate: **+10%**

However, core business metrics declined:

- ❌ Conversion Rate: **-7.9%**
- ❌ Average Order Value: **-8.4%**
- ❌ Revenue per Session: **-15.7%**

**Insight**

The redesign optimized vanity metrics rather than business outcomes.

---

## 2. Device Segmentation Changed Everything

| Device | Conversion Rate Change | Revenue per Session |
|---------|-----------------------|---------------------|
| Desktop | -16.4% ❌ | -23.5% ❌ |
| Mobile | +2.5% ✅ | -7.2% ⚠️ |
| Tablet | -16.9% ❌ | -21.2% ❌ |

Desktop users purchasing expensive furniture required detailed specifications before purchasing.

The redesign buried those specifications, increasing friction during the buying process.

---

## 3. The Mobile Paradox

Although mobile conversion increased slightly, overall revenue still declined.

Further segmentation showed:

- Small Items (< €200): **+7.8% Revenue**
- Large Furniture (> €800): **-7.3% Revenue**

**Insight**

The redesign benefited impulse purchases but negatively affected high-consideration purchases.

---

# 💰 Business Impact

### If Released to 100% of Traffic

- Monthly Revenue Loss: **€390,000**
- Annual Revenue Impact: **€4.68 Million**
- Statistical Confidence: **99.9% (p < 0.001)**

## Final Recommendation

❌ **Do NOT ship globally.**

Instead,

- Deploy only for mobile users browsing small-ticket products.
- Continue iterating on desktop using a hybrid design.

---

# 🛠️ Technical Skills Demonstrated

### Data Analysis

- SQL (DuckDB)
- Window Functions
- CTEs
- Aggregations
- Statistical Hypothesis Testing
- Chi-Square Testing
- Segmentation Analysis
- Correlation Analysis

### Business Analysis

- KPI Selection
- Revenue Impact Analysis
- Experiment Evaluation
- Executive Recommendation
- Product Analytics

### Communication

- Executive Reporting
- Data Storytelling
- Business Recommendations
- Data Visualization

---

# ⚙️ Tech Stack

- Python
- DuckDB (SQL)
- Pandas
- Matplotlib
- SciPy
- Jupyter Notebook

---

# 📁 Project Structure

```text
mobelhaus-ab-test/
├── data/
│   ├── sessions_data.csv
│   ├── conversions_data.csv
│   └── engagement_data.csv
│
├── analysis/
│   └── Analysis.ipynb
│
├── deliverables/
│   ├── strategic_memo.md
│   ├── chart1_rps_comparison.png
│   ├── chart2_device_segment.png
│   └── chart3_engagement_trap.png
│
└── README.md
```

---

# 🎓 What I Learned

### Averages Hide the Story

Overall metrics can conceal major behavioral differences across customer segments.

---

### Engagement Isn't Always Success

Higher engagement does not necessarily translate into higher revenue.

Business metrics should always remain the primary success criteria.

---

### Statistics Build Confidence

Quantifying statistical significance strengthens recommendations and stakeholder confidence.

---

### Business Impact Matters Most

Communicating financial impact is far more persuasive than simply reporting percentage changes.

---

### Good Analysts Don't Just Reject Ideas

Rather than simply rejecting the redesign, I identified a targeted rollout strategy that preserved potential gains.

---

# 💼 Business Context

This project simulates a realistic e-commerce experimentation workflow where analysts must evaluate whether product changes generate measurable business value.

It demonstrates:

- A/B Test Evaluation
- Product Analytics
- Customer Segmentation
- Revenue Analysis
- Executive Decision Support
- Statistical Experimentation

Relevant for roles including:

- Data Analyst
- Associate Data Engineer
- Product Analyst
- Growth Analyst
- Business Intelligence Analyst

---

# 🔗 Connect

If you'd like to discuss this project or collaborate on analytics and data engineering work:

- **LinkedIn:** *www.https://www.linkedin.com/in/rishavdey2000/*

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

Feedback and suggestions are always welcome.
