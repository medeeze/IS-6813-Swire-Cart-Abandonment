# IS 6813 Swire Cart Abandonment
As part of my MSBA Capstone, I worked in a team of 3 (including me) to work through the issue of cart abandonments on Swire's online platform. Our task was to analyze customer behavior to determine the causes of abandonment and recommendations to reduce it.

## Business Problem
MyCoke360 experiences a high rate of cart abandonment where customers add products but fail to complete the purchase before their order window closes. The objective of this project is to analyze user behavior within each order window to understand what actions or patterns lead to abandonment and why customers fail to convert. By identifying the behavioral patterns most associated with the drop off, we can deliver actionable insights that can help Swire reduce lost orders and improve the platform’s overall conversion performance. As a result of lowering abandonment rate, Swire captures more of the potential revenue that would otherwise be lost.

## Solution
Our group’s solution was to model cart abandonment using behavioral sequences that consist of a sequence of actions, rather than single events. Raw event level models performed poorly, so we engineered features that reflected how customers actually move through an order window. This includes how much they browse, whether they start checkout, and whether they remove items after adding them. Once we modeled these behaviors, predictive performance improved dramatically. The strongest drivers of abandonment became clear which we found were heavy browsing without checkout, removing items after adding them, and a lack of checkout progress. These patterns give Swire clear points of intervention to reduce abandonment and recover lost orders.

## Project Contribution
My contributions to this project focused on both the exploratory analysis and the modeling foundation used in our group solution. I completed the missing data and results sections of the EDA and built an individual notebook using a random sample due to the large scale of the dataset. I analyzed the relationship between device type and abandonment, identified events with positive lift that commonly appeared in abandoned sessions, and completed the logistic regression and random forest models that was finalized in the group modeling. I also engineered the behavioral action sequence features allowing us to move from single events to order window level behaviors. Finally, I wrote the Modeling process and Results sections for the final report, summarizing how our models worked and what insights they produced. To summarize, I:

- Completed the Missing Data and Results portions of the EDA.
- Conducted individual EDA using a random sample to explore device effects and lift based patterns.
- Built the logistic regression and random forest models used as references for the group modeling code.
- Created behavioral action sequence features, shifting the analysis from raw events to meaningful user behavior patterns.
- Wrote the Modeling Process and Results sections for the final submission.

## Business Value
Our solution provides Swire with a clear understanding of why customers abandon their carts and which behaviors signal risk in the order window. Instead of reacting after an order is lost, Swire can now identify high-risk sessions and add targeted actions to the platform such as reminders, simplified checkout steps, or personalized discounts/offers. By using behavioral sequences we can pinpoint the moments where customers hesitate or backtrack. Reducing abandonment even slightly would translate into meaningful gains because a large portion of potential revenue currently falls out between adding items and completing the purchase. The insights developed here give Swire an opportunity for capturing more of that value.

## Challenges
One of our biggest challenges was managing missing and inconsistent data in multiple datasets containing millions of rows. Building the order window structure was also difficult since it required accurately rebuilding customer sessions without introducing leakage. On the modeling side, we faced overfitting, especially with more complex models like the random forest. Our group invested a lot of time into solutions for these issues and challenges. 

## What I Learned
This project really showed me how much the quality of your data impacts any analysis. Once we cleaned and reorganized the data into clearer behavioral segments, the models suddenly improved dramatically. The majority of the time spent in this project was in the data cleaning and order window creation. Spending that effort I also learned how to build features that capture real user behavior instead of just counting events, which helped us understand what customers were actually doing in each order window. 
