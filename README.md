FDE_LAB-1

USN Number: 1RVU23CSE180
Name: Hardik Goel

Stage 1 – Problem Definition & Requirements Gathering (Business Analyst)

Business Problem
The company wants to identify the top 5 products by total revenue and understand how customer sentiment varies for those products. This will help guide marketing, pricing, and quality improvement strategies.

Business Question
“What are the top 5 products by revenue, and how does customer sentiment vary for them?”

Rank	Product ID	Total Revenue	Avg. Sentiment Score
1	      P104	       55,149.00	       3.05
2     	P101	       52,072.50	       2.88
3	      P103	       46,830.00	       2.90
4	      P102	       45,945.00	       2.999
5	      P105	       34,161.00	       3.04

This means your top 5 products by revenue are P104, P101, P103, P102, P105, and their average sentiment scores range from about 2.88 to 3.05 (on a scale of 1–5).



Required Data Points

From sales_data_raw.csv:
product_id
sale_price
quantity_sold
customer_id
sale_date

From customer_feedback.json:
product_id
customer_id
sentiment_score
review_date


Key Metrics

Total Revenue per Product = sum of (sale_price × quantity_sold)
Average Sentiment Score per Product
Number of Reviews per Product

Desired Insights
Ranking of top 5 products by revenue
Average sentiment score for each of the top 5 products
Possible correlation between revenue and customer satisfaction


Stage 2 – Role-Based Collaboration Simulation

Data Engineer Responsibilities
Ingest CSV and JSON datasets from source systems

Clean data:
Normalize date formats (various date styles present in customer_feedback.json)
Remove duplicates and invalid entries
Ensure consistent product_id and customer_id formats
Join sales and feedback datasets using product_id and customer_id
Store cleaned data in the data warehouse (organized by date and product)


Data Scientist Responsibilities

Analyze cleaned data to:
Calculate total revenue per product
Identify top 5 products by revenue
Compute average sentiment score for each product
Check for correlation between revenue and sentiment
Build visualizations (bar charts, scatter plots)


Business Analyst Responsibilities

Interpret results:
Highlight top-performing products
Point out sentiment trends (e.g., high revenue but low satisfaction)
Suggest actions (product improvements, targeted marketing)
Create a presentation for stakeholders with actionable insights


Flow of Responsibilities & Dependencies
Business Analyst defines problem & required metrics → passes to Data Engineer
Data Engineer ingests & cleans data → provides to Data Scientist
Data Scientist analyzes & generates insights → sends to Business Analyst
Business Analyst prepares final report & recommendations
