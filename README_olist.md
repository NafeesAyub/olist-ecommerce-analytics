# E‑Commerce Sales & Delivery Analytics — Olist (Brazil)


Analyze order volume, revenue, delivery performance, reviews, and category trends using the 

**Brazilian E‑Commerce Public Dataset by Olist**. 
This project demonstrates a clean, reproducible analytics workflow: data loading, joins, KPIs, monthly trends, cohorts, and curated visuals suitable for portfolio use.



---

## Objectives
- Build an order‑level fact table from raw CSVs (orders, items, payments, reviews, products).

- Track core KPIs: monthly orders, revenue (price + freight), AOV, active customers, repeat rate.

- Evaluate delivery performance: on‑time rate and average delivery delay.

- Understand customer feedback: review score distribution and drivers.

- Surface category performance with a top‑categories view.

- (Optional) Customer retention cohorts (first‑order month vs subsequent activity).


---

## Data Source (exact files)
Kaggle dataset: 

**Brazilian E‑Commerce Public Dataset by Olist**  

Typical CSVs (expected filenames in `data/`):
- 
`olist_orders_dataset.csv`
- 
`olist_order_items_dataset.csv`
- 
`olist_order_payments_dataset.csv`
- 
`olist_order_reviews_dataset.csv`
- 
`olist_customers_dataset.csv`
- 
`olist_products_dataset.csv`
- 
`product_category_name_translation.csv`
- 
`olist_sellers_dataset.csv` (optional for seller analyses)
- 
`olist_geolocation_dataset.csv` 
(optional for geo)

> Place these files in `data/` locally. 
On Kaggle, use **Add data** and attach the Olist dataset.



---

## Tech Stack
Python · Pandas · NumPy · Matplotlib · Jupyter Notebook



---

## Repository Structure
```

olist-ecommerce-analytics/
├── data/                               
# raw CSVs (kept local; not pushed to git)

├── notebooks/
│   ├── 01_eda_olist.ipynb              
# EDA, KPIs, delivery, categories, cohorts
│   
└── 02_modeling_olist.ipynb         
# (optional) forecasting / retention models
├── visuals/                            
# exported PNGs
├── README.md
├── requirements.txt
└── .gitignore
```



---

## Environment & Setup
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate

pip install -r requirements.txt

```

**requirements.txt (suggested)**
```
pandas
numpy
matplotlib
```



---

## How to Run (local)
1) Put the Olist CSVs in `data/` (see list above).  
2) Launch Jupyter:
   
```bash
   jupyter notebook
   ```
3) Open and run: `notebooks/01_eda_olist.ipynb`  
   

Plots are saved to `visuals/` via a helper function inside the notebook.



---

## Notebook Path Pattern (works locally & on Kaggle)

Each notebook detects whether it runs on Kaggle and sets paths accordingly. 
On Kaggle, attach the dataset via **Add data**. Locally, files are read from `../data/`.



---

## Notebook Outputs (01_eda_olist.ipynb)

- Monthly KPIs (orders, revenue, AOV) — line charts

- Delivery performance (delay distribution, on‑time rate)

- Review score distribution
- Top categories by revenue (English names)

- (Optional) Customer retention cohort heatmap
- All figures saved to `visuals/


