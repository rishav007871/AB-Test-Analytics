# Strategic Memo Template - A/B Test Recommendation

**TO:** Head of Product & CMO  
**FROM:** Joyan Bhathena, Web Analyst  
**RE:** Variant B does not encourage more conversions  

---

## Executive Summary

We should NOT ship variant B platform-wide. Despite +82% engagement time, conversion rate dropped 7.9% and revenue per session fell 15.6%, resulting in an estimated €390K monthly revenue loss. However, variant B shows a 7.8% revenue lift for mobile users browsing small items (decor/lighting) and should be tested as a targeted mobile-only experience for those categories.

---

## Test Background

The test was to compare a Visual-first (variant) PDP vs Information-first (control). The hypothesis was that, increasing visual immersion on product pages will improve conversion by helping customers better envision products in their homes.

**Test ran:** October 1st to 27th, 2024  
**Sample size:** ~94,000 Sessions per variant  
**Key change:** 

- **Variant (B) - "Visual-First"**
  - Hero full-width image carousel (70% of viewport)
  - Sticky "Add to Cart" + "Save" buttons
  - 12-15 lifestyle photos in styled rooms
  - Condensed scannable specs
  - Room inspiration carousel
  - "Shop the Look" cross-sell feature

---

## Key Findings

### Finding #1: Overall Performance

- **Conversion Rate:** 
  - Variant A: 4.74%
  - Variant B: 4.37%
  - %Change: -7.9%

- **Average Order Value:**
  - Variant A: €872
  - Variant B: €798
  - %Change: -8.4%

- **Revenue Per Session:**
  - Variant A: €41.4
  - Variant B: €34.9
  - %Change: -15.6%

Despite higher engagement on variant B, overall it failed to convert more sessions into purchases thereby reducing the AOV and revenue per session.


### Finding #2: Higher Engagement on PDP != More Purchases

| Metric | Variant A | Variant B | Change |
|--------|-----------|-----------|--------|
| Time on PDP | 54 sec | 98 sec | +82.7% |
| Images Viewed | 4.8 | 8.1 | +68.3% |
| Add-to-Cart Rate | 16.9% | 18.6% | +10.2% |
| Cart-Abandonment Rate | 66.3% | 72% | +8.63% |
| Conversion Rate | 4.7% | 4.3% | -7.8% |

Higher engagement did NOT translate to more revenue. Variant B increased time on page by 83% and images viewed by 68%, but these gains were illusory - cart abandonment rose 8.6% and conversion fell 7.8%. Users were browsing more but buying less. 


### Finding #3: Variant B Fails on Desktop, Barely Wins on Mobile

**The Desktop Collapse:**
Variant B devastated desktop performance - conversion dropped 16.4% and revenue per session fell 23.5%, costing €419K in lost revenue. 

Why? 
Desktop users researching expensive furniture (€800+ sofas, beds) need detailed specs to make confident decisions. Variant B buried specifications in favor of lifestyle imagery, creating friction for high-consideration purchases.

**The Mobile Paradox:**
Mobile showed a slight conversion lift (+2.5%), but revenue per session still declined 7.2%. The reason: mobile users converted MORE sessions but purchased CHEAPER items. When we segment by product category, we find variant B only 
wins for small decor and lighting purchases (<€200) where decisions are visual and impulsive.

**The One Clear Winner:**
Mobile users buying small items generated 7.8% more revenue with variant B. 
This represents ~€10K in monthly incremental revenue at current traffic levels.

---

## Business Impact

### If Shipped to 100% of Traffic:

Expected RPS change: -€6.50 (from €41.40 to €34.90)
Monthly sessions: ~750,000
**Estimated monthly revenue LOSS: €390,000**

Over a year: €4.68M in lost revenue

**Confidence level:** HIGH
- Sample size is robust (94K sessions per variant)
- Patterns are consistent across segments
- Statistical significance: p < 0.001 (chi-square test on conversion rate)


### Risks of shipping variant B

1. €390K monthly revenue bleed compounds to €4.68M annually
2. Desktop users (45% of traffic) may perceive the site as "dumbed down" and switch to competitors with better product information
3. Long-term brand damage - furniture buyers expect detailed specs; visual-only experience may erode trust in high-consideration categories

---

### Primary Recommendation: DON'T SHIP - Kill Platform-Wide Rollout

**Rationale:**
1. **Massive revenue loss**: Shipping to 100% of traffic would cost €390K/month in lost revenue (€6.5 RPS decline × 750K monthly sessions)
   
2. **Desktop failure is fatal**: 45% of our traffic is desktop, and variant B destroys conversion there (-16%). We cannot ship a design that breaks the experience for half our users.
   
3. **Mobile gains are marginal**: Even where variant B "wins" (mobile), the overall RPS still declines 7.2%. The only true winner is a tiny segment (mobile + small items) representing just 8% of total revenue.

**However, there's a salvageable opportunity...**

### Alternative Path Worth Testing:

**Option 1: Mobile-Only Rollout for Small Items (Decor/Lighting)**
- **Why it might work:** This is the ONE segment where B clearly wins (+7.8% revenue)
- **Estimated impact:** +€10K/month with minimal downside risk
- **Risks:** Engineering complexity of maintaining two experiences; small absolute impact might not justify development cost

**Option 2: Iterate the Desktop Design**
- **Why it might work:** Keep the visual richness but restore spec accessibility (e.g., sticky specs panel, expandable details)
- **Risks:** Requires product team to accept their hypothesis was half-right - engagement matters, but not at the cost of information

---

**Immediate actions (this week):**
1. Present findings to product team; expect pushback on killing the project
2. Engineering to estimate cost of mobile-only implementation
3. Quantify the small-items mobile opportunity more precisely

**Follow-up analysis needed:**
1. Investigate WHY desktop users abandoned carts at higher rates - was it specs access or something else?
2. A/B test a hybrid design (visual + accessible specs) on desktop only

**If we proceed with "kill it globally":**
- Timeline: End test immediately to stop revenue bleed
- Success metric: Return to baseline 4.75% conversion rate
- Review checkpoint: Monitor desktop conversion for 2 weeks post-rollback

---

**Note to reviewers**: This recommendation is based on 4 weeks of data covering 187,974 sessions. The primary limitation is that we cannot determine WHY desktop users abandoned carts at higher rates without qualitative user research (heatmaps, session recordings, exit surveys). I recommend this as a follow-up investigation before attempting a hybrid 
desktop design.

## Appendix: Statistical Notes

Chi-Square Test on Conversion Rate:
- Observed: 4.75% (A) vs 4.37% (B)
- Sample size: 93,762 (A), 94,212 (B)
- Chi-square statistic: χ² = 67.42
- p-value: < 0.001 (highly significant)
- Conclusion: Difference is NOT due to random chance

Power Analysis:
- With 94K sessions per variant, we have 99.9% power to detect a 
  0.5% difference in conversion rate
- Our observed difference (0.38%) is well above detection threshold