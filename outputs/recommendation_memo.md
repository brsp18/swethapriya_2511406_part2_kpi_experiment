
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