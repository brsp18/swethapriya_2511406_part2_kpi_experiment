
Summary:

The new onboarding campaign is doing great at getting more users signed up and active. However, we have a major problem: the group using the new system generated a huge spike in customer support tickets. Because of this risk, we shouldn't launch it to everyone yet. Instead, we recommend a conditional launch—roll it out only to the user groups where it worked best, while we figure out and fix whatever is causing the support issues

Data Summary:

Total Users : 1,408 (Control: 693 / Treatment: 715)
Experiment Period: February 2025 — May 2025
Control: Existing onboarding experience
Treatment: New onboarding and activation campaign
Significance Threshold : p-value < 0.05

Primary Metrices Summary:
                
	   Avg of start_trial|Avg of visit_land_page|Avg of converted_to_paid | Avg of completed_onboarding
Control	          25.11%	     63.64%	       3.17%	     15.58%
Treatment	      29.09%	     72.59%	       6.99%	     21.26%
Grand Total 	  27.13%	     68.18%	       5.11%	     18.47%

Key finding: Conversion to paid rate more than doubled in the treatment group — the most critical business metric — and is statistically significant with high confidence.



z-Test: Two Sample for Means 		
        
                Control_converted	Treatment_converted
Mean	       : 0.031746032        	0.06993007
Known Variance : 	0.0307	            0.0651
Observations	:  693              	715
Hypothesized Mean Difference: 	0	
z	   : -3.282117895	
P(Z<=z) one-tail: 	0.000515153	
z Critical one-tail	: 1.644853627	
P(Z<=z) two-tail:	0.001030305	
z Critical two-tail	: 1.959963985	
z-Test: Two Sample for Means		
        
Conclusion from Z-Test(Two sample for means): The new onboarding campaign significantly improved conversion rate from 3.17% to 6.99% — this is not by chance.

p-value (0.0010) < 0.05 --- Statistically Significant
z-score (-3.28) > z Critical (1.95) --- Reject Null Hypothesis
The new onboarding campaign significantly improved conversion rate from 3.17% to 6.99% — this is not by chance.

Metric                              Control     Treatment
Landing Page Visit Rate:            63.64%      72.59%
Trial Start Rate:                   25.11%      29.09%
Conversion to paid rate more than doubled in the treatment group — the most critical business metric — and is statistically significant with high confidence.

Support Tickets Metric: Support tickets increased by 70% in the treatment group (p < 0.0001). This is statistically significant and must be investigated before full launch.

Segment Analysis — Conversion to Paid (By Region)
Region  Control   Treatment   Lift
North   3.45%    8.89%      +157.8% 
East    2.53%    6.40%      +152.6%
South   3.26%    7.61%      +133.3%
West    3.38%    5.03%      +48.8%
All regions improved. West showed the lowest lift — worth monitoring separately.

By Device Type:
Device          Control        Treatment   Lift
Tablet:           1.79%         7.14%      +300.0%
Mobile:           2.57%         7.34%      +185.6%
Desktop:          4.50%         6.54%      +45.4%
Insight: Mobile and Tablet users responded exceptionally well to the new experience. Desktop lift is modest.


By Plan Type:
Plan             Control        Treatment     Lift
Free:            3.05%          9.24%        +203.2%
Premium:         2.75%          6.25%        +127.1%
Basic:           3.59%          3.83%        +6.8%
Insight: Free and Premium users show strong lift. Basic plan users show minimal improvement — the new experience may not be well suited for this segment.\


Assumptions & Limitations:
- days_to_convert had 1,336 missing values — analysis limited to 72 converted users only
- device_type and traffic_source had minor missing values (18 and 24 respectively)
- Refund rate analysis is based on a very small sample (3 refunds in treatment) — not conclusive
- Experiment ran over approximately 3 months — novelty effect cannot be fully ruled out
- Trial Start Rate did not reach statistical significance — needs further investigation

Recommendations:
# Decision: Warning to have a Conditional Launch — Do Not Full Launch Yet #

1. Launch to Mobile & Tablet users can give Strongest lift and largest user base
2. Launch to Free & Premium plan users can give Highest conversion improvement
3. Launch to North, East & South regions gives Consistent strong performance
4. Hold for Basic plan users because of Minimal lift which suggests need for redesign for this segment
5. Hold for Desktop users because of Lower lift which suggests consideing a desktop-specific variant
6. Do not full launch yet because Support ticket spike must be investigated first


--------------------------------------

#Task 9: Write Recommendation Memo#

# Experiment Decision Memo

## Executive Summary

The experiment demonstrates a statistically significant improvement in the primary business outcome (paid conversion) for users exposed to the new onboarding campaign. The treatment nearly doubles the conversion rate compared with the control while also improving upstream funnel metrics such as landing page visits, trial starts, and onboarding completion.

However, there is an important tradeoff: support tickets increased by approximately 70%, which is also statistically significant. This indicates that while the new experience drives growth, it also creates additional customer support burden.

---

## North Star Metric

**Paid Conversion Rate**

| Metric               |   Control | Treatment |                  Change |
| -------------------- | --------: | --------: | ----------------------: |
| Paid Conversion Rate | **3.17%** | **6.99%** | **+120% relative lift** |

* Control: **22 conversions / 693 users**
* Treatment: **50 conversions / 715 users**

---

## KPI Tree Explanation

**North Star:** Paid Conversion Rate

Supporting KPIs:

1. **Landing Page Visit**

   Control: **63.6%**
   Treatment: **72.6%**
   Significant improvement

2. **Started Trial**

   Control: **25.1%**
   Treatment: **29.1%**
   Positive lift

3. **Completed Onboarding**

   Control: **15.6%**
   Treatment: **21.3%**
   Strong improvement

4. **Paid Conversion**

   Control: **3.17%**
   Treatment: **6.99%**
   Largest business impact

5. **Guardrail: Support Tickets**

   Control Mean: **0.219**
   Treatment Mean: **0.372**
   Approximately **70% increase**

Overall, improvements are observed throughout the conversion funnel, suggesting the onboarding campaign positively affects user activation.

---

## Experiment Result Summary

### Primary KPI

Conversion rate increased from **3.17%** to **6.99%**
Relative lift: **120%**

### Revenue

Average 30-day revenue:

Control: **51.75**
Treatment: **53.88**

Revenue also increased modestly.

### Funnel Metrics

| Metric               | Control | Treatment |
| -------------------- | ------: | --------: |
| Landing Page Visit   |   63.6% |     72.6% |
| Trial Started        |   25.1% |     29.1% |
| Completed Onboarding |   15.6% |     21.3% |
| Paid Conversion      |   3.17% |     6.99% |

---

## Hypothesis Test Interpretation

The hypothesis tests strongly support that the treatment outperformed the control.

### Conversion Rate

* t-statistic = **-3.29**
* Two-tailed p-value = **0.0010**

Since:

* **p = 0.001 < 0.05**

we reject the null hypothesis.

**Interpretation:**
The improvement in paid conversion is statistically significant and is unlikely to be due to random chance.

### Landing Page Visits

* p-value ≈ **0**

This is also highly significant, indicating the treatment substantially improves user engagement early in the funnel.

---

## Guardrail Analysis

The main guardrail metric is **support tickets**.

| Metric          | Control | Treatment |
| --------------- | ------: | --------: |
| Support Tickets |   0.219 |     0.372 |

Key findings:

* Approximately **70% increase**
* z-test:

  * **p < 0.0001**

This increase is statistically significant.

Although business metrics improved, the support burden increased considerably, which may increase operational costs and negatively affect customer experience if not addressed.

---

## Segment-Level Insight

A device-level breakdown shows improvement across all device types.

| Device  | Control | Treatment |
| ------- | ------: | --------: |
| Desktop |   4.50% |     6.54% |
| Mobile  |   2.57% |     7.34% |
| Tablet  |   1.79% |     7.14% |

**Key insight:**

* Mobile users experienced the largest improvement in paid conversion.
* Desktop users also benefited.
* Tablet users improved as well, though sample size may be smaller.

The treatment appears effective across segments rather than benefiting only a single user group.

---

# Final Recommendation

## **Continue testing**

### Rationale

**Pros**

* Paid conversion increased from **3.17% to 6.99%**
* Relative lift of approximately **120%**
* Statistically significant improvement (p ≈ 0.001)
* Better performance across the entire acquisition funnel
* Slight increase in average revenue

**Cons**

* Support tickets increased by approximately **70%**
* Guardrail metric failed with strong statistical significance (p < 0.0001)

The growth impact is compelling, but the substantial increase in customer support suggests that the onboarding experience may introduce confusion or friction that should be resolved before a full rollout.

---

## Risks and Limitations

* Increased support volume could raise operational costs.
* Higher support demand may negatively affect customer satisfaction.
* Segment analysis beyond device type (e.g., region, plan type, traffic source) should be explored before scaling.
* Revenue gains are relatively modest compared with the large increase in conversions, so longer-term customer value should be monitored.

---

## Next Steps

1. Investigate the causes of the increased support tickets.
2. Analyze support ticket categories to identify common pain points.
3. Refine the onboarding flow to reduce confusion.
4. Run a follow-up A/B test with the improved onboarding experience.
5. Monitor longer-term metrics such as customer retention, churn, and lifetime value.
6. If support ticket volume decreases while conversion gains are maintained, proceed with a broader rollout.

Overall recommendation:Continue testing.The treatment delivers a strong, statistically significant improvement in conversions, but the significant increase in support tickets should be addressed before a full launch.

