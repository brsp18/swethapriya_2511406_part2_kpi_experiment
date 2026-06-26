hypothesis_test_notes.md

Hypothesis Testing Notes: Onboarding & Activation Campaign

This document outlines the formal hypothesis testing framework used to evaluate whether the new onboarding and activation campaign experience should be launched to all users. Each metric tested is connected directly to the business decision of full launch, partial launch, or rollback.
NOTE: Standard Significance Level α (Alpha) = 0.05
A p-value below 0.05 means there is less than a 5% probability the observed difference occurred by chance. This is the industry-standard threshold for A/B testing decisions

------

1. Primary Metric : Paid Conversion Rate

Null Hypothesis (H₀)
The new onboarding campaign has no effect on paid conversion rate. Any observed difference between Control and Treatment is due to random chance
H₀: Conversion Rate (Treatment) = Conversion Rate (Control)

Alternate Hypothesis (H₁)
The new onboarding campaign increases paid conversion rate compared to the existing experience.
H₁: Conversion Rate (Treatment) > Conversion Rate (Control)

    Control_converted	Treatment_converted
Mean	0.031746032	0.06993007
Known Variance	0.0307	0.0651
Observations	693	715
Hypothesized Mean Difference	0	
z	-3.282117895	
P(Z<=z) one-tail	0.000515153	
z Critical one-tail	1.644853627	
P(Z<=z) two-tail	0.001030305	
z Critical two-tail	1.959963985	
z-Test: Two Sample for Means

Paid Conversion Rate = Users converted to paid / Total users in group		
Control Group: 3.19%
Treatment Group: 7.04%
Conclusion: p-value = 0.0005 < 0.05 → Reject H₀. The new campaign significantly improved paid conversion rate from 3.19% to 7.04%. This is statistically significant and practically meaningful. The campaign should be launched subject to guardrail metric resolution.

------

2. Secondary Metric — Onboarding Completion Rate
Null Hypothesis (H₀)
The new campaign has no effect on onboarding completion rate.
H₀: Onboarding Completion Rate (Treatment) = Onboarding Completion Rate (Control)

Alternate Hypothesis (H₁)
The new campaign increases onboarding completion rate.
H₁: Onboarding Completion Rate (Treatment) > Onboarding Completion Rate (Control)

Onboarding Completion Rate = Users who completed onboarding / Total users
Control Group: 15.65%
Treatment Group: 21.13%

 p-value = 0.0061 < 0.05 → Reject H₀. Onboarding completion significantly improved. This supports the conversion rate finding and confirms the new experience is more effective at guiding users through activation.

----
3. Secondary Metric — Landing Page Visit Rate
Null Hypothesis (H₀)
The new campaign has no effect on landing page visit rate.
H₀: Landing Page Visit Rate (Treatment) = Landing Page Visit Rate (Control)

Alternate Hypothesis (H₁)
The new campaign changes landing page visit rate in either direction.
H₁: Landing Page Visit Rate (Treatment) ≠ Landing Page Visit Rate (Control)

        Control-visited_landing_page	Treatment-visited_landing_page
Mean	0.636363636	0.725874126
Known Variance	0.0307	0.0651
Observations	693	715
Hypothesized Mean Difference	0	
z	-7.693894971	
P(Z<=z) one-tail	7.10543E-15	
z Critical one-tail	1.644853627	
P(Z<=z) two-tail	1.42109E-14	
z Critical two-tail	1.959963985	
p-value (two-tail): ~0.0000
z-score: -7.69

p-value ≈ 0.0000 < 0.05 → Reject H₀. The new campaign significantly increased landing page visits — the funnel entry point is stronger in the Treatment group.

----
4. Secondary Metric — Trial Start Rate

Null Hypothesis (H₀)
The new campaign has no effect on trial start rate.
H₀: Trial Start Rate (Treatment) = Trial Start Rate (Control)

Alternate Hypothesis (H₁)
The new campaign changes trial start rate.
H₁: Trial Start Rate (Treatment) ≠ Trial Start Rate (Control)

Trial Start Rate = Users who started trial / Total users
Control Group: 25.07%	
Treatment Group: 29.01%
p-value (two-tail): 0.0929
p-value = 0.0929 > 0.05 → Fail to Reject H₀. The improvement in trial start rate is not statistically significant. While the Treatment group started more trials, this could be due to random variation. This metric needs further monitoring in future experiment iterations.

-----

5. Guardrail Metric — Support Ticket Rate

Null Hypothesis (H₀)
The new campaign has no effect on support ticket volume.
H₀: Support Ticket Rate (Treatment) = Support Ticket Rate (Control)

Alternate Hypothesis (H₁)
The new campaign changes support ticket volume.
H₁: Support Ticket Rate (Treatment) ≠ Support Ticket Rate (Control)
p-value (two-tail): < 0.0001
Treatment avg: 0.375 tickets/user vs Control 0.220

p-value < 0.0001 < 0.05 → Reject H₀. The guardrail is breached. Support tickets increased significantly in the Treatment group. This is the primary blocker for a full launch. The root cause must be identified and resolved before scaling the new experience to all users.


____________


Test inputs — Control 3.19% (n=690), Treatment 7.04% (n=710)
Test output — z-score: -3.28
p-value — one-tail: 0.0005, two-tail: 0.0011
Decision rule — Reject H₀ if p-value < 0.05
Business interpretation — Campaign significantly improved conversion, supports launch

1. Paid Conversion Rate: p-value:0.0005. Reject H. Launch supported.

2. For Onboarding Completion: p-value: 0.0061. Reject H₀. Activation improved.

3. For Landing Page Visit: p-value: ~0.0000. Reject H₀. Funnel entry improved.

4. For Trial Start Rate: p-value: 0.0929. Fail to Reject H₀. Monitor.

5. For Support Tickets (Guardrail): p-value: <0.0001. Guardrail breached.

_________


Task 8: Evaluate Guardrail Metrics

Support Ticket Rate : BREACHED — +69.6% increase (p=0.000028) HIGH RISK
Revenue Quality: BREACHED — -52.7% per converter (p=0.0106) HIGH RISH
Refund Rate: MONITOR — 6% of converters refunded vs 0% MEDIUM
Engagement Score : SAFE — +10.4% improvement (p<0.0001) None 
Days to Convert : SAFE — 2.46 days faster (p=0.0036) None
Segment-Level Decline : SAFE — no declines (Basic plan low +7.2%) LOW RISK

Final Decision:
The file clearly states the recommendation is not based only on conversion improvement:

"Primary metric says:  Launch — conversion rate doubled"
"Guardrail metrics say: Do not fully launch yet"

Two guardrails breached:
Support tickets critically elevated
Revenue quality significantly declined