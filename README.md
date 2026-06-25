# swethapriya_2511406_part2_kpi_experiment

# Task 1: Understand the Business Problem

1. What decision needs to be made?

We need to decide what to do with our new onboarding experience: launch it to everyone, use it to completely replace the old flow, or scrap it and stick with what we had before. To make the right call, we ran an A/B test where we split users into two groups—one stayed on the original setup, while the other tried out the new experience.

2. Who the decision impacts?

Based on the experiment setup, this decision impacts New Users, Product Team, Marketing Team, Company's leadership and Maintanance team.
- New users: New Users decision depends on their first impression, engagement, and how likely they are to convert or subscribe.
- Product Team: Product team designed and built the new campaign experience. The decision determines whether they move forward with a full launch, roll it back to iterate further, or scratch it entirely.
- Marketing Team: Marketing team's the goal is to improve early engagement and conversion. Outcome directly impacts this team.
- Company's Leadership: Leadership rely on results to have higher revenue, retention, and growth targets.
The Maintenance Team: If a full rollout is approved, maintanance team will be responsible for develop, scaling, deploying, and maintaining the new experience for the entire user base.


3. What Metric Should Improve?

User Conversion Rate: The percentage of new users who take next step, like first purchase or signing up for a paid subscription is expected to increase.
Early Engagement Rate: The percentage of users who actively interact with the product within their first 5 days is expected to increase.
Onboarding Completion : The percentage of users who actually make it all the way through every step of your onboarding setup is expected to be increased.
Time to First Action by the user needs to be decreased.

4. What Risks Must Be Monitored?
It is important to monitor User drop-off, Revenue impact, Technical Stability, Retention risk to not drop. 

5. What evidence is required before making a recommendation
The following evidence must be gathered and validated before a launch decision is made:
- Primary metrics must show statistically significant improvement (p-value < 0.05).
- Increase in conversion rate and engagement rate must be meaningful enough to justify rollout cost.
- Experiment must have run long enough with enough users to avoid underpowered results.
- No significant degradation in retention, revenue, or support metrics.
- Results must hold across key user segments (region, device, plan type) — no harmful subgroup effects.


# Task 2: Define the North Star Metric:
*** North Star Metric: Conversion to Paid Rate ***
Why it's the North Star
Conversion to Paid is the only metric that directly measures whether the campaign achieved its core business objective — turning new sign-ups into paying customers. Every other metric (landing page visits, trial starts, onboarding completion) is just a step toward this outcome, not the outcome itself.

Why others are supporting metrics
Metrics like engagement score and onboarding completion measure activity and process quality, but a user can complete onboarding, stay highly engaged, and never pay. They indicate progress through the funnel but do not confirm business value.

How it connects to business growth
Every improvement in conversion rate directly increases paying subscribers, Monthly Recurring Revenue (MRR), and Customer Lifetime Value (LTV). In this experiment alone, the lift from 3.17% to 6.99% generated 28 additional paying customers from just 1,408 users.

What could go wrong if optimized blindly
Aggressive tactics could force conversions while increasing refunds, churn, and support tickets — all of which are already showing early warning signs in this experiment. A high conversion rate means nothing if users cancel within 30 days or require excessive support to stay.

#Task 4: Clean and Prepare Experiment Data#
1. 1. Missing Values
	
Row-Labels	 Control	Treatment	 Grand-Total
Desktop	      200	     214	      414
Mobile	      428	     436	      864
Tablet	      56	     56	          112
(blank)	      9	         9	          18
Grand-Total	 693	   715	          1408

2. Row-Labels	Count of user_id
   Control	        693
   Treatment	    715
   Grand-Total	   1408

3. Total duplicate user_ids found - 8
Unique user_ids duplicated - 5
Control group duplicates - 3
Treatment group duplicates - 5


MISSING_Engagement_Score -	14
MISSING_Days_To_Convert	- 1336
MISSING_Traffic_Source	- 24
MISSING_Device Type - 18

Top 10 Revenues:
Row Labels	Max of revenue_30d
USR-100106	8610.72
USR-100303	6788.95
USR-100103	3887.98
USR-101322	2660.21
USR-100336	2206.88
USR-100411	2144.82
USR-100889	2064.55
USR-101012	1938.31
USR-101025	1906.23
USR-101147	1858.85


		
Row-Labels	 Control	Treatment	Grand-Total
East	     158	       172	      330
North	     203	       180	      383
South	     184	       184	      368
West	     148	       179	      327
Grand-Total	 693	       715	      1408

Row-Labels	Control	Treatment	Grand-Total
Desktop     	200	    214	     414
Mobile	        428	    436	     864
Tablet	        56	    56	     112
(blank)	         9   	9	     18
Grand-Total	   693	   715	     1408

Row-Labels	Control	Treatment	Grand-Total
Basic	        223	  235	     458
Free	        361	  368	     729
Premium	        109	  112	     221
Grand-Total 	693	  715	    1408
            
	
Row-Labels	Control	Treatment	Grand-Total
Email	     74	     56	          130
Organic	     246	 241	      487
Paid Search 156	     176	      332
Referral	 81	      91	      172
Social	     130     133	      263
(blank)       6	     18	           24
Grand-Total	 693	715	         1408
