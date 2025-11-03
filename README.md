# Customer-Segmentation-Analysis-with-RFM-Metrics

<img width="1262" height="998" alt="pngimg com - mug_coffee_PNG16824" src="https://github.com/user-attachments/assets/fc2757b7-9ae6-4d7d-9ccc-a068ab82f0c2" />

### The modern coffee market is highly competitive, requiring businesses to make data-driven decisions to optimize their operations and maximize profit margins. The provided dataset, containing 730 entries of sales transactions over a period, represents a rich source of information on the company's performance.
### To sustain growth and maintain a competitive edge, the company needs to:

- Identify the Customer Segmentation and its solution for a best retention and business growth
- Evaluate Promotional Effectiveness: Assess whether the applied discount strategy is successfully driving increased sales volume and positive net revenue (Final Sales), or if discounts are eroding potential profits.
- Build the customer clustering for handling the customer retention in order to customer’s behaviours issue

### The coffee company currently lacks clear, granular insights into its sales performance dynamics and the efficacy of its pricing and discount strategies, leading to sub-optimal decisions in inventory management, marketing, and market expansion.
### Specifically, the primary problem to be addressed through data analysis is the absence of quantitative clarity regarding:

- Sales Concentration:  Customer Segmentation and Customer Behaviour
- Discount Impact: Is the current approach to offering a discount
- How to handle the customers that have an issue to leave and how to engage the loyal customer to be the lifetime customer and show the best business recomendation for a better business growth

### 📝 Dataset Specification

This dataset comprises 730 records across 11 columns. It is confirmed that the dataset is clean,
 featuring no missing values, no duplicate entries and the distribution of outliers seems normal.

Key Dimensions:

### 📍 City (Transaction Location): The dataset includes transactions conducted across 10 distinct cities:

  Hail,
Riyadh,
Jeddah,
Mecca,
Khobar,
Dammam,
Medina,
Buraidah,
Abha,
Tabuk.

### 🫘 Product (Coffee Bean Origin): The product column details the origin country of the coffee beans being sold:

  Costa Rica,
Colombian,
Brazilian,
Guatemala,
Ethiopian.

## ⏱️ Time Span:
The data covers a two-year period, spanning from 2023 through 2024.

## 🔻 Used Discount:
The data covers a twe values are False or True


<img width="913" height="373" alt="image" src="https://github.com/user-attachments/assets/172804fe-a65f-409e-8876-4de37b3225ac" />

## K-Means Clustering
 K-Means is sensitive to the scale of features. Since Recency, Frequency, and Monetary have different ranges, we must standardize them (transform them to have a mean of 0 and a standard deviation of 1).

-Determine the Optimal Number of Clusters (K):

The Elbow Method is commonly used to find the best value for $K$ (the number of clusters). We plot the Within-Cluster Sum of Squares (WCSS) for a range of $K$ values. The 'elbow' point on the plot suggests the optimal $K$.

The Silhouette Score quantifies how similar a data point is to its own cluster (cohesion) compared to other clusters (separation). It provides a measure of how well-defined and distinct the clusters are

<img width="690" height="667" alt="image" src="https://github.com/user-attachments/assets/bd362fd3-4e5d-4e7b-8f29-1f0b1935d5ba" />


## 📊 Insight of Segmentation

- Cluster 2 (Green):  This cluster represents highly engaged and frequent customers with good spending. They have relatively low Recency, high Frequency, and moderate to high Monetary values. They are your most valuable customers.

- Cluster 0 (Blue): This cluster represents less frequent or lower-value customers. They have moderate Recency, lower Frequency, and lower Monetary values compared to Cluster 2.

- Cluster 1 (Pink): This cluster includes customers who haven't purchased as recently but still show some level of activity and spending. They show higher Recency compared to Clusters 0 and 2, with moderate Frequency and Monetary values. This group might include 'About to Sleep' or 'Hibernating' customers.

## 〽️ Business Recomendation

- For Cluster 2 (Your Most Valuable Customers):
Recommendation: Nurture these relationships. Implement an exclusive loyalty program with tiered rewards, personalized offers based on their preferences, and early access to new products or promotions. Provide excellent customer service and seek their feedback.
Business Impact: Strengthens brand loyalty, encourages continued high-value purchases, and potentially turns them into brand advocates.

- For Cluster 0 (Less Frequent / Lower-Value Customers):
Recommendation: Consider low-cost strategies to encourage activity, such as general promotional emails or highlighting accessible entry-level products. Focus efforts more on acquiring and nurturing customers in higher-value segments.
 Business Impact: May yield some incremental sales, but the primary focus should be on higher-potential segments.

- For Cluster 1 (Potentially At-Risk / Hibernating Customers):
Recommendation: Develop targeted re-engagement campaigns. Send personalized emails with special discounts or promotions to entice them back. Consider reaching out through different channels. A win-back survey might help understand why they stopped purchasing.
Business Impact:  Potentially recovers lost revenue and reduces customer churn.

