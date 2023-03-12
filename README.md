<h2 align="center">Starbucks Reward Offer Marketing Attribution – 


Customer Segmentation & Offer Type Variant Strategy
</h2>

Imagine waking up in the morning to go to your local Starbucks. You order your favorite drink, the baristas say “hi”, and then you lounge in their seating area to take a beat before starting your day. Whether at home or on vacation, from the remote islands in Hawaii, to the closest Target store, to the hotel you are staying in, Starbucks is there. It’s ubiquitous! The song that pops into my head is the Rembrandt’s, “I’ll be there for you”. This is not a coincidence; this is by design. Starbuck’s seamless, convenient, and standardized vibe across its global stores makes the customer experience unique.


For those unfamiliar, Starbucks is a Business to Consumer Company that is the largest coffeehouse chain in the world. It offers specialty coffee, food items, handcrafted beverages, and merchandise. Howard Schulz, the CEO of Starbucks, designed it to be the ultimate “Third Place” experience: a place other than Home and Work where people go for connection and belonging.


The key to Starbuck’s success in scaling its business is the Starbucks Reward Program integration with their mobile app. This enables Starbucks to showcase their current marketing offers that reward customers for purchasing a product by awarding them stars to redeem free items in future purchases. 


Starbucks is distinct from other loyalty programs in that it is more gamified. The Mobile Pay as you Go feature released in 2011 is also a seamless digital experience. Just find your closest Starbucks, make your purchase, and pick up your food without transacting any physical cash. Starbucks has minimized friction points so you can buy with just a click of a button, which drives sales and increases Starbuck’s operational efficiency. It’s no surprise then that Starbucks stock has outperformed the market by 7.33% on an annualized basis over the past 15 years. As a result of their keen strategic business decisions and investments and now with commitment to sustainability, I can only see the business continuing to grow. 


This analysis will explore how Starbucks can use marketing attribution to optimize their rewards offer marketing strategy.  By doing so, Starbucks will drive user engagement and increase transactions and revenue, positively impacting the bottom line. Marketing attribution is how we determine how marketing tactics and user interactions contribute to sales. This information will be used to analyze which channels and marketing offers inspire consumers to act. This will be used to answer the two central business questions for business leaders to inform future marketing strategy of (a) who to target and (b) which types of marketing offer will incentivize the most purchases?


To answer this question, I utilized a Starbucks reward offers dataset bundle from Kaggle which simulates the Starbucks Reward Program. It represents 76,277 marketing offers sent to 17,000 users, by offer type variant and channel, during a 30-day test period.


There are three tables:
1.	An event log of user actions such as marketing offers received, viewed, completed, and transactions.
2.	The user profiles of Starbucks members by age, gender, income, and the date they became a member. 
3.	The types of reward variants that were sent to users through what channels.


### Let’s understand our customers in this dataset through descriptive statistics first.


### 1.	Starbucks member user growth in this sample is exponential. 

<p align="center">
<img src="images/1 User Growth.png" width=400>
</p>

The growth rate of Starbucks member user sign ups in our sample was exponential from 2013-2017, which demonstrates the popularity of this loyalty program. Note: the exponential trend does not appear to hold in 2018, possibly because it is a partial year of data. 

### 2.	Starbucks members are high value.

<p align="center">
<img src="images/2 Cohort Analysis.png" width=800>
</p>

Through cohort analysis, if we analyze transaction data by customer cohort sign up year, we find these customers represent $1.8M in Starbucks gross revenue over the course of a month. Calculating the average spend over one month shows that customers spend $3.5 per day at Starbucks, which is almost the price of a coffee or tea per day. While there were sharp increases in user sign ups between 2013 and 2017, the 2016 cohort spent the most on average per person.

### 3. Starbucks average spend increases with customer age. 

<p align="center">
<img src="images/3 Avg Spend by Age Group.png" width=700>
</p>

I wanted to use a more statistical approach to binning. Using Sturges rule from Statistics to determine the optimal number of bins (log2N + 1), 15 bins were prescribed. After comparing their average transactions over time, I was comfortable grouping the higher transaction age groups into four groups. 
Starbucks average spend increases with customer age. Customers aged 51-67 spend 50% more than those between 18-34, on average.  As age is correlated with income (r = 0.32), it is no surprise that the average spend increases with age. Based on this pattern, Starbucks should send offers that appeal to customers based on their age group. This could take the form of discount offers aimed at young, cost-conscious customers (age 18-34) and rewards to older customers that incentivize more frequent or higher average order values (ages 35 and up).

### 4. Starbucks members who are female between spend more than males on average across age groups.

<p align="center">
<img src="images/4 Avg Spend by Age Group & Gender.png" width=550>
</p>

### 5. There is opportunity to activate 2.5% of inactive members.

<p align="center">
<img src="images/5 Active vs Inactive Members.png" width=500>
</p>

Active members are defined by spending > $0 in the time range of this dataset. Inactive members are defined as spending $0 in the time range of this dataset.
A short-term tactic is to offer a free good or pair a free good with a conditional action to inactive members, similar to the free bakery item members can get on their birthday. A long-term tactic would apply that to  loyalty discount offers for members who are consistently active so inactive members are incentivized to participate.

### 6. The average user tenure is 6 years, ranging between 4.5 and 9.5 years.

<p align="center">
<img src="images/6 User Tenure.png" width=400>
</p>

The user tenure is defined as when they signed up to the Starbucks rewards program, which is how they can digitally receive rewards offers. This may be a useful feature in customer segmentation.

### Now that we understand our customers better, let’s examine the influence of reward offers on user behavior.

### 1.	While reward offers influences user behavior, some members purchase independent of offers.

<p align="center">
<img src="images/2 1 Funnel Analysis.png" width=800>
</p>

Typical marketing funnels narrow to form an inverted triangle the further you travel through the funnel. This shows that transactions are made independent of offers. Some users make transactions independent of using rewards they have seen, probably because they were unaware, forgot, were in a hurry, or intended to redeem later.

### 2. The likelihood of completing an offer after receiving an offer increases with age and income. 

<p align="center">
<img src="images/2 2 Age & Income Group Segment.png" width=800>
</p>

### 3. Females respond more than males to reward offers.

<p align="center">
<img src="images/2 2 Gender Segment.png" width=400>
</p>

### 4.	A majority of the top 5 performing offer variants are discount reward offers. The best performing BOGO offers are $5 difficulty and $5 reward. The bottom 3 performing offer variants are $20 difficulty discount and $10 BOGO offers.

<p align="center">
<img src="images/2 3 Response Rate of Offer Type Variant.png" width=800>
</p>

### 5.	Offers with the same difficulty and reward perform better with a longer offer duration.

<p align="center">
<img src="images/2 4 Same Difficulty & Reward.png" width=800>
</p>

Difficulty in this context is how much you need to spend to get the reward.

The longer the offer is available, the likelier it is that the user will get the opportunity to act on it and complete the rewards offer.

### 6.	The top 10 performing rewards offers are typically completed by females and are discount offers that have a 7-10 duration to complete.

<p align="center">
<img src="images/2 5 Response Rate of Offer Type Variant.png" width=800>
</p>

The best performing BOGO offer by gender is valued at $5.
The bottom performing offers by gender are $20 difficulty discount & $10 BOGO offers.
The same trend by gender is also what is observed at the aggregate level.

Note: I wanted to create a leaderboard ranking from highest to lowest to measure the relative performance of reward offers based on offers completed/offers received. This is a a proof of concept for my future dashboard that is most intuitive and interpretable to users. 

### 7.	Emails were used most frequently to complete offers, followed by mobile & web, and then social. However, it’s essentially a tie in channel effectiveness.

<p align="center">
<img src="images/2 6 Channel Effectiveness.png" width=800>
</p>

### 8.	Discount offers have a higher response rate and a higher likelihood of completion conditional on being viewed.

<p align="center">
<img src="images/2 7 Response Rate Metrics.png" width=900>
</p>

Response rates are higher if the user views the offer. This is true for both Discount and BOGO offers.

Direct Response Rate = Number of Offers Completed / Number of Offers Received

Conversion Rate = Number of Offers Completed / Number of Offers Viewed

If you can get users to view the discount offers, the response rate jumps from 60% to 85%, which is a 25% difference. For BOGO offers, the response rate jumps from 50% to 60%, a 10% difference. Bottom line: it is strategic to get users to be positively engaged in the long run. However, be cognizant of spam / messaging fatigue that can also detract from user engagement.

### Takeaways

1.	Starbucks average spend increases with customer age and with customer income.

2.	 Female customers spend more than male customers, on average.

3.	2.5% of members are inactive. A short-term tactic to activate them is offering a complimentary item that can be contingent on an action. A long-term tactic is offering loyalty discount offers for members who are consistently active so inactive members are incentivized to participate.

4.	Offers with the same difficulty & reward performed better with a longer offer duration.

5.	While email is the most frequently used channel, all channels (email, mobile, web, social) exhibit similar response rates from the user of 55-57%. Continue with current channel strategy as it is.

6.	Discount offers perform relatively better than BOGO rewards offers. 

7.	If you can motivate users to view the offer, the response rate improves by 25% for discount & 10% for BOGO offers.

Actionable recommendations to answer the original business question:

### Who should I target and what kind of marketing reward type offer should I use? 

1.	To improve the reward offer promotional strategy, target age groups 35-50, 51-67, 68-83, 84-101 because they tend to spend more at Starbucks than younger age groups. I recommend sending offers that resonate best to customers based on their age group.		

2.	Provide more or create new discount rewards offers to female consumers, with a duration of 7 to 10 days to complete them.								

3.	Continue to promote the best performing BOGO offer, which has a $5 difficulty and $5 reward.

4.	Consider reducing $20 difficulty discount offers and $10 BOGO offers, which do not as well relative to existing reward offers because of their difficulty to complete. $20 appears to be too much to spend for the average consumer to be worth the reward. Another option is to consider pivoting these higher spend offers toward older/higher income customers. However, more analysis needs to be done to validate this is true.



### Next Steps to Improve Marketing Strategy via ML

1.	Segment customers (via clustering) based on key features.
2.	Create attribution rules for direct and indirect attribution to display as key metrics.
3.	Create an R Shiny dashboard to display key metrics.
4.	Feature engineer to enhance dashboard metrics, such as average time to complete an offer.
5.	Create and evaluate a marketing attribution model. Productionize model.

### Conclusion

In summary, this is just Part I of the Starbucks Rewards Offer Marketing Attribution Data Science Project.

This project will follow CRISP-DM, which stands for Cross-Industry Standard Process for Data Mining. It is a cross industry standard framework that serves as a guide for a data science process.

Part I encompasses the Business Understanding, Data Understanding, and Data Preparation phases of the CRISP-DM model.

Part II will be created a dashboard to display key metrics to help stakeholders focus on the business outcome, using some proof-of-concept visualizations in Phase I. I will be adding other relevant visualization like a map of stores in the country because according to the Starbucks 2022 SEC 10-K, Starbucks financial results and long-term growth will be driven by new store openings, store sales, and cost management, so mapping store expansion geographically seems important. 

Part III will be the modeling/evaluation/deployment phase in the data science process. Stay tuned!

### Python Libraries Used 
- Pandas 
- Numpy 
- Matplotlib 
- Seaborn 
- Plotly 
- Sklearn 
- Datetime 
- Json


### Methods
- Data Visualization
