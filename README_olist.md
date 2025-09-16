E-Commerce Sales & Delivery Analytics — Olist (Brazil)


Analyze order volume, revenue, delivery performance, reviews, and category trends using the Brazilian E-Commerce Public Dataset by Olist. 
This project shows a clean, reproducible workflow—from raw CSVs to KPIs, visuals, and simple models—ready for hiring managers and clients to review.

Highlights (tl;dr)


Built an order-level analytics table by joining orders, items, payments, reviews, customers, and products.


Clear monthly KPIs: Orders, Revenue (price + freight), and AOV, with publication-ready charts.


Delivery performance: on-time rate and a full delay distribution (early vs. late).


Customer feedback: review score distribution + a simple model to predict satisfied reviews (score ≥ 4).


Forecasts: baseline SARIMAX for next-6-months orders and revenue.


Model metrics (review satisfaction): Accuracy = 0.804, ROC-AUC = 0.655.

Business Questions


How are orders, revenue, and AOV trending month over month?


What is the delivery performance (on-time rate, typical late/early days)?


Which product categories drive the most revenue?


Can we estimate the likelihood of a satisfied review based on delivery and order features?


What might the next 6 months look like for orders and revenue?


Dataset

Brazilian E-Commerce Public Dataset by Olist (CSV files). 
Place the following into data/ locally (or attach the dataset in Kaggle):


olist_orders_dataset.csv


olist_order_items_dataset.csv


olist_order_payments_dataset.csv


olist_order_reviews_dataset.csv
olist_customers_dataset.csv


olist_products_dataset.csv


product_category_name_translation.csv

(optional) 
olist_sellers_dataset.csv, o
list_geolocation_dataset.csv


Note: To keep the repo lightweight, the data/ folder is git-ignored. The README explains exactly which

Tech Stack


Python, Pandas, NumPy, Matplotlib, Statsmodels, scikit-learn, Jupyter Notebook

EDA Outputs


Monthly Orders & Revenue → visuals/monthly_orders_revenue.png


Average Order Value (AOV) → visuals/monthly_aov.png


Delivery Delay (days) → visuals/delivery_delay_hist.png


Top Categories by Revenue → visuals/top_categories_revenue.png


(Optional) Retention Cohorts → visuals/cohort_retention_heatmap.png


These plots are designed to be pasted into README, Kaggle, and Upwork as portfolio visuals.

Modeling

1) Forecasts (Orders & Revenue)


Built monthly KPIs and ensured a continuous monthly index (missing months filled).


Baseline SARIMAX models with seasonal monthly structure.


Charts include train, test, and 6-month future horizon.


Outputs: visuals/forecast_orders.png, visuals/forecast_revenue.png


2) Review Satisfaction (Classification)

Target: 
satisfied review = (score ≥ 4).


Features: delivery delay (days), number of items, total value (price + freight), freight share, payment total.


Model: Logistic Regression (with scaling) on a 80/20 holdout split.


Results: Accuracy = 0.804, ROC-AUC = 0.655.


Additional visuals: ROC curve, confusion matrix, and coefficient bar chart.


Outputs: visuals/roc_review_satisfaction.png, visuals/cm_review_satisfaction.png, visuals/coef_review_satisfaction.png



The classification baseline is deliberately simple and fast to reproduce. It’s intended as a starting point for feature and model improvements.

Contact


If you have questions or would like to discuss a similar analysis for your business, feel free to reach out via GitHub.
You can also contact at : +92-336-5901990, nafeesayub@gmail.com
