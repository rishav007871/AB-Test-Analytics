# MöbelHaus Digital - A/B Test Analysis Portfolio Project

**Author:** Joyan Bhathena  
**Role:** Web Analyst  
**Project Type:** A/B Test Evaluation & Strategic Recommendation  
**Tools Used:** Python, DuckDB (SQL), Pandas, Matplotlib, SciPy

---

## 📊 Project Overview

I analyzed a 4-week A/B test (187,974 sessions, 8,572 conversions) for a fictional Berlin-based furniture e-commerce company testing a redesigned product detail page. The product team was celebrating engagement wins (+82% time on page), but the Head of Product wanted to know: **Does this actually make money?**

**My deliverable:** A strategic recommendation memo backed by SQL analysis, statistical testing, and business impact quantification.

---

## 🎯 The Challenge

**Test Hypothesis:** Increasing visual immersion on product pages will improve conversion by helping customers better envision furniture in their homes.

**Variants:**
- **Control (A):** Traditional product page with detailed specs, standard gallery
- **Variant (B):** Visual-first redesign with 12-15 lifestyle photos, sticky CTA, condensed specs

**The Complication:** Engagement metrics looked amazing, but would this translate to revenue?

---

## 🔍 Key Findings

### 1. **Engagement ≠ Revenue**
While variant B increased engagement dramatically:
- ✅ Time on page: +82%
- ✅ Images viewed: +68%
- ✅ Add-to-cart rate: +10%

It failed where it mattered:
- ❌ Conversion rate: -7.9% (4.75% → 4.37%)
- ❌ Average order value: -8.4% (€872 → €798)
- ❌ Revenue per session: -15.7% (€41.40 → €34.90)

**Insight:** This was "engagement theater" - optimizing for vanity metrics that don't drive business value.

### 2. **Massive Device Segmentation**
The overall average masked dramatic differences:

| Device | Conversion Rate Change | Revenue Per Session Change |
|--------|------------------------|----------------------------|
| **Desktop** | -16.4% ❌ | -23.5% ❌ |
| **Mobile** | +2.5% ✅ | -7.2% ⚠️ |
| **Tablet** | -16.9% ❌ | -21.2% ❌ |

**Why:** Desktop users researching €800+ furniture purchases need detailed specs to make confident decisions. Variant B buried this information in favor of lifestyle imagery, creating friction for high-consideration purchases.

### 3. **The Mobile Paradox**
Mobile showed a conversion lift BUT revenue still declined. **Why?** 

Deeper analysis revealed mobile users converted more but bought cheaper items. When segmented by product category:
- Small items (decor/lighting <€200): **+7.8% revenue** ✅
- Large items (furniture >€800): **-7.3% revenue** ❌

**Insight:** Variant B works for impulse, visual purchases - not considered, research-driven ones.

---

## 💰 Business Impact

### If Shipped to 100% of Traffic:
- **Monthly revenue loss:** €390,000
- **Annual impact:** €4.68M
- **Statistical confidence:** 99.9% (p < 0.001, chi-square test)

### Recommendation: **DON'T SHIP GLOBALLY**

However, identified a salvageable opportunity:
- **Ship to mobile users browsing small items only:** +€10K/month potential
- **Iterate desktop design:** Test hybrid approach (visual + accessible specs)

---

## 🛠️ Technical Skills Demonstrated

### Data Analysis
- ✅ SQL query design (joins, aggregations, CTEs, window functions)
- ✅ Statistical hypothesis testing (chi-square, significance testing)
- ✅ Segmentation analysis (device, user type, product category, price range)
- ✅ Correlation analysis (engagement vs. conversion)

### Business Analysis
- ✅ Metric selection (primary, secondary, guardrail metrics)
- ✅ Trade-off evaluation (engagement vs. revenue)
- ✅ Business impact quantification (€ impact, not just percentages)
- ✅ Risk assessment and alternative path identification

### Communication
- ✅ Executive memo writing (1-page strategic recommendation)
- ✅ Data visualization (matplotlib for clear insights)

---

## 📁 Project Structure

```
mobelhaus-ab-test/
├── data/
│   ├── sessions_data.csv          # 187,974 session records
│   ├── conversions_data.csv       # 8,572 order records
│   └── engagement_data.csv        # Interaction metrics
├── analysis/
│   ├── Analysis.ipynb                  # Exploratory analysis & statisitical tests
├── deliverables/
│   ├── strategic_memo.md          # Final recommendation (1-page)
│   ├── chart1_rps_comparison.png  # Revenue per session comparison
│   ├── chart2_device_segment.png  # Device segmentation analysis
│   └── chart3_engagement_trap.png # Engagement vs. conversion scatter
└── README.md
```

---

## 🎓 What I Learned

### 1. **Averages Hide the Story**
The overall metrics showed a modest decline, but device segmentation revealed desktop was collapsing (-16% conversion) while mobile barely improved (+2.5%). **Always segment before concluding.**

### 2. **Engagement Metrics Can Be Misleading**
Time on page and image views increased significantly, but these didn't translate to purchases. **Lesson:** Define engagement as "actions that predict purchase," not passive browsing.

### 3. **Statistical Rigor Builds Credibility**
Running chi-square tests and quantifying confidence levels (99.9%) made my recommendation defensible against pushback from a product team that loved their design.

### 4. **Business Impact > Statistical Significance**
Saying "conversion dropped 0.38 percentage points" is weak. Saying "this costs €390K per month" gets action. **Always translate findings into business terms.**

### 5. **Never Just Say "No"**
I didn't just kill the test - I identified a salvageable opportunity (mobile-small items) and proposed an iteration path (hybrid desktop design). 

---

## 💼 Business Context

This project simulates a real-world scenario common in e-commerce:
- Product teams optimize for engagement without checking revenue impact
- A/B tests show "wins" on vanity metrics but losses on what matters
- Segmentation reveals the design works for some users but destroys experience for others
- The analyst must deliver tough news to stakeholders invested in the project

**Relevant to:** Web Analyst, Product Analyst, Growth Analyst, Data Analyst roles in e-commerce (especially furniture/home goods like home24, Wayfair, Westwing).

---

## 🔗 Connect

I'm actively seeking **Web Analyst / Data Analyst** roles in Berlin. If this work resonates with you:

- **LinkedIn:** https://www.linkedin.com/in/joyan-bhathena/
  
**Looking for:** Roles focused on e-commerce analytics, A/B testing, product analytics, or growth analytics.

---
---

**⭐ If you found this analysis valuable, feel free to star this repo or reach out to discuss similar projects!**
