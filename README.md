# E-Commerce Growth Funnel Analysis

A end-to-end growth analytics project analyzing customer conversion behavior 
across 400K+ transactions — built to mirror the type of funnel analysis done 
by growth teams at companies like Meta, Google, and Amazon.

---

## Problem Statement

E-commerce businesses lose a significant portion of customers between their 
first purchase and becoming loyal, repeat buyers. Without understanding *where* 
and *why* customers drop out of the purchase journey, product and marketing 
teams make decisions based on intuition rather than data.

---

## Objective

- Build a 4-stage customer growth funnel from raw transaction data
- Identify the biggest drop-off stage and quantify its business impact
- Segment the drop-off by country, order value, and acquisition cohort
- Propose data-backed product recommendations to recover lost conversions

---

## Dataset

- **Source:** Online Retail II — UCI Machine Learning Repository
- **Size:** 397,885 transactions | 4,338 unique customers
- **Period:** December 2010 – December 2011
- **Link:** https://archive.ics.uci.edu/dataset/502/online+retail+ii

---

## Tools & Tech

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data cleaning, funnel engineering, segmentation |
| Matplotlib | Visualization — funnel chart, cohort trend, segment bars |
| Google Colab | Development environment |
| GitHub | Version control and portfolio hosting |

---

## Funnel Definition

| Stage | Definition | Customers | Conversion % |
|-------|-----------|-----------|-------------|
| 1. Acquired | Made at least 1 purchase | 4,338 | 100% |
| 2. Engaged | Bought more than 1 product type | 4,247 | 97.9% |
| 3. Converted | Placed 3+ orders | 2,010 | 46.3% |
| 4. Retained | Active across 3+ months | 1,787 | 41.2% |

---

## Key Findings

### Finding 1 — Critical drop-off at Engaged → Converted (52.7%)
Over half of engaged customers never placed a 3rd order. This is the primary 
growth leak and the focus of all downstream recommendations.

### Finding 2 — Late-2011 cohorts converting at 2x lower rates
Customers acquired in Aug–Nov 2011 converted at 17–34% vs 74.7% for the 
Dec 2010 cohort — suggesting an onboarding or re-engagement gap for newly 
acquired users.

### Finding 3 — Low-AOV customers churn at alarming rates
Customers with avg order value under £50 converted at only 22% vs 50%+ for 
customers spending over £150 per order — pointing to an acquisition 
targeting problem.

### Finding 4 — UK underperforms vs smaller markets
UK (87% of customers) converts at 46.5% while France (52.9%) and Germany 
(53.2%) outperform despite far smaller customer bases.

---

## Visualizations

<img width="1589" height="1217" alt="download" src="https://github.com/user-attachments/assets/0c884368-9e59-401c-88b2-e94268c8d0f1" />


---

## Recommendations

| Priority | Recommendation | Projected Impact |
|----------|---------------|-----------------|
| High | Launch 30-day re-engagement email/push sequence for new users at day 7, 14, 30 | +600 converted customers |
| High | Introduce loyalty incentive triggered after 2nd order to pull users across conversion line | +5pp conversion lift |
| Medium | Audit and tighten UK paid acquisition targeting toward higher-intent signals | UK rate 46.5% → 50%+ |

---

## Resume Bullet Points

> Analyzed 400K+ e-commerce transactions across 4,338 customers in Python; 
> engineered a 4-stage growth funnel uncovering a critical 52.7% drop-off 
> at the conversion stage across 12 months of behavioral data.

> Segmented conversion drop-off by country, order value, and acquisition 
> cohort; identified late-2011 cohort decay and low-AOV churn as primary 
> levers; recommended 3 targeted product interventions projected to improve 
> overall conversion rate by 8–10pp.

---

## Project Structure
```
ecommerce-growth-funnel-analysis/
│
├── funnel_analysis.ipynb       # Main analysis notebook
├── funnel_analysis.png         # 4-chart visualization output
├── README.md                   # Project documentation
└── data/                       # Download dataset from UCI link above
```

---

## How to Run

1. Download the dataset from the UCI link above
2. Open `funnel_analysis.ipynb` in Google Colab or Jupyter
3. Upload `online_retail_II.xlsx` when prompted
4. Run all cells in order

---

## Author

**Aakash Malhan**  
