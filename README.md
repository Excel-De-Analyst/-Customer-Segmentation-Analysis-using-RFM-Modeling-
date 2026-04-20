# -Customer-Segmentation-Analysis-using-RFM-Modeling-
RFM modeling segments 1,000 customers by Recency, Frequency, and Monetary scores. After cleaning messy data, each customer receives a 3-digit RFM code mapping them to segments like "Champions", "Loyal Customer" or "Big Spenders"enabling targeted marketing and smarter retention decisions.

 
**What is RFM Analysis?**
-RFM analysis is a data-driven marketing technique that ranks customers based on three behavioral dimensions:
**R** - Recency: How recently did the customer purchase?
Measured in days since last purchase
Smaller numbers = Better customers
Example: A customer who bought yesterday (1 day) is more valuable than one who bought six months ago (180 days)

**F** - Frequency: How often does the customer purchase?
Measured in total number of purchases (or transactions per time period)
Larger numbers = Better customers
Example: A customer with 50 purchases is more valuable than one with 5 purchases

**M** - Monetary: How much money does the customer spend?
Measured in total currency spent (₦, $, €, etc.)
Larger numbers = Better customers
Example: A customer who spent ₦500,000 is more valuable than one who spent ₦50,000

**The 1-5 Scoring System Explained**
Instead of working with raw numbers (e.g., 408 days, 12 purchases, ₦120,500), I convert everything to a simple 1-5 scale:

**Score	Meaning	Action Implication**
5-Excellent         	-     Priority treatment, rewards, VIP programs
4-Good	              -     Positive engagement, nurture relationships
3-Average             -	    Standard communication, monitor trends
2-Below Average	      -     Investigate, consider re-engagement offers
1-Poor	              -     Low priority, possible win-back campaigns

**Why use a 1-5 scale instead of raw numbers?**

**Benefit**         **Explanation**
Simplicity	          Marketing teams easily understand "5 = best" without technical training
Normalization       	Works for companies of any size (10 customers or 10 million)
Consistency         	Scores are comparable across different time periods and product categories
Actionability	        Clear thresholds (e.g., "contact all customers with R score 1-2")

**The Recency Reversal Explained (Critical Concept!)**
This is the most confusing part of RFM analysis. Let me explain clearly:
**The Problem:**

For Recency: Smaller number of days = Better customer (3 days is better than 45 days)
For scoring: We want 5 = Best, 1 = Worst

**The Conflict:**
When we rank customers by Recency (ascending order):
Customer with 3 days gets Rank 1 (smallest)
Customer with 45 days gets Rank 5 (largest)

**If I use Rank directly as a score:**
Best customer (3 days) gets score 1 (WRONG!)
Worst customer (45 days) gets score 5 (WRONG!)
The Solution: Reverse the scale

**Formula:** Final Score = 6 - Scaled Score

This flips 1→5, 2→4, 3→3, 4→2, 5→1

                                           
   **Methodology**                                        
                                            
Step 1: Data Cleaning

        ↓
Step 2: Calculate Days Since Last Purchase

        ↓
Step 3: Calculate Raw Ranks (R, F, M)

        ↓
Step 4: Scale Ranks to 1-5 and Reverse Recency

        ↓
Step 5: Generate RFM Codes and Assign Segments
