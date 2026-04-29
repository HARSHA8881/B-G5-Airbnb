# 🏙️ Airbnb NYC Market Insights and Visualization

> **New York City Short-Term Rental Market Analysis**  
> DVA Capstone 2 — Newton School of Technology | Team G-5 | April 2026

---

## 📋 Project Overview

| Field | Details |
|---|---|
| **Project Title** | Airbnb NYC Market Insights and Visualization |
| **Sector** | Travel & Hospitality / Short-Term Rental Market |
| **Team ID** | G-5 |
| **Institute** | Newton School of Technology |
| **Course** | DVA Capstone 2 |
| **Team Lead** | Hardik Shreyas |
| **GitHub** | [HardikShreays/B-G5-Airbnb](https://github.com/HardikShreays/B-G5-Airbnb) |
| **Tableau** | *(Add Tableau Public URL)* |
| **Submission Date** | April 2026 |

---

## 👥 Team Members & Roles

| Name | Student ID | Role |
|---|---|---|
| Harsha Gonela | 2401010181 | Presentation (PPT) & Report Writing Lead |
| Kanishka Dubey | 2401010208 | Dataset Sourcing & Report Writing |
| Sharma Piyush | 2401010437 | Dataset Sourcing & Tableau Dashboard Design |
| Hardik Shreyas | 2401010178 | EDA & Statistical Analysis |
| Vaibhav Singh | 2401020074 | Dataset Sourcing & Tableau Dashboard Design |
| Ankit | — | Dataset Sourcing, ETL & Data Cleaning |

---

## 🎯 Executive Summary

### Problem
New York City's Airbnb market is vast and fragmented, making it difficult for hosts, investors, and platform managers to identify high-performing neighbourhoods, optimal pricing strategies, and key drivers of guest satisfaction.

### Approach
We sourced a publicly available Airbnb NYC dataset (**102,599 listings**), cleaned it via a Python ETL pipeline, derived business metrics (price tiers, estimated revenue, occupancy), performed EDA and statistical analysis in Jupyter notebooks, and built **three interactive Tableau dashboards** to surface actionable insights.

### Key Findings

| # | Finding |
|---|---|
| 🏘️ | Bedford-Stuyvesant and Williamsburg dominate listing volume in Brooklyn |
| 🏠 | Entire home/apartment listings account for >50% market share |
| 💰 | Average listing price is **$626.20**, with service fees averaging **$125.20** |
| ⭐ | Instant Booking listings achieve comparable review rates (≈2.5) to non-instant listings |
| 📈 | Average total prices peaked near **$751–$944** in recent years (post-pandemic recovery) |

---

## 📊 Dataset

- **Source:** [Inside Airbnb — NYC Listings](http://insideairbnb.com/get-the-data/)
- **Time Period:** Multi-year data with review years from pre-2010 through 2024

| Metric | Value |
|---|---|
| Total Listings | 102,599 |
| Original Columns | 30+ |
| NYC Boroughs | 5 |
| Latest Review Year | 2024 |

### Key Columns

| Column | Description |
|---|---|
| `id` | Unique listing identifier |
| `neighbourhood` | Local neighbourhood name |
| `borough` | One of 5 NYC boroughs |
| `room_type` | Entire home/apt, Private room, Hotel room, Shared room |
| `price` | Nightly price in USD |
| `service_fee` | Platform service fee in USD |
| `review_rate_number` | Aggregate guest rating (1–5 scale) |
| `instant_bookable` | Whether instant booking is enabled |
| `cancellation_policy` | flexible / moderate / strict |
| `price_tier` | Derived: Budget / Economy / Mid-range / Premium / Luxury |
| `estimated_revenue` | Derived: `price × (365 - availability_365)` |

---

## 🛠️ ETL & Data Cleaning Pipeline

All cleaning steps were executed in Python (`notebooks/02_cleaning.ipynb` and `scripts/etl_pipeline.py`).

| Step | Action |
|---|---|
| Column standardisation | Lowercased, spaces → underscores |
| Missing values | `price`, `service_fee` nulls imputed with borough-level median |
| Outlier detection | Prices >$10,000/night capped at 99th percentile |
| Duplicate removal | Exact duplicate rows removed |
| Date parsing | `last_review` parsed to datetime; `review_year` extracted |
| Categorical fixing | Typos in `cancellation_policy` and `room_type` normalised |
| Type conversion | `price`, `service_fee` stripped of `$` and `,`; converted to float |

### Feature Engineering

| Derived Column | Logic |
|---|---|
| `price_tier` | Quantile binning: Budget (<$100), Economy ($100–$200), Mid-range ($200–$400), Premium ($400–$700), Luxury (>$700) |
| `estimated_revenue` | `price × (365 − availability_365)` |
| `occupancy_rate` | `(365 − availability_365) / 365` |
| `total_price` | `price + service_fee` |

---

## 📈 KPI Framework

| KPI | Formula | Business Relevance |
|---|---|---|
| Average Price | `mean(price)` | Benchmarks market pricing |
| Distinct Listing Count | `count(id)` | Measures market size |
| Average Review Rate | `mean(review_rate_number)` | Proxy for listing quality |
| Average Service Fee | `mean(service_fee)` | Measures guest cost burden |
| Average Total Price | `mean(price + service_fee)` | True cost to guest |
| Avg Reviews Per Month | `mean(reviews_per_month)` | Measures demand & occupancy |

---

## 🔍 Key EDA Insights

1. **Bedford-Stuyvesant** (~3,500 listings), **Williamsburg** (~3,400), and **Harlem** (~2,700) are the top three neighbourhoods — supply-saturated.
2. **Queens** is underserved (~6,000 listings) vs. Manhattan (~20,000) and Brooklyn (~19,000) — significant first-mover opportunity.
3. **Entire home/apt** listings dominate (>50%) but face highest regulatory risk under NYC Local Law 18.
4. **Price ↔ Service Fee** correlation: strong positive (~0.85).
5. **Review Rate** is bimodally distributed — listings cluster at ≈2.6 or ≈1.7, with little middle ground.
6. **Instant Booking** has no statistically significant impact on review rate (t-test: fail to reject H₀).
7. Post-pandemic average total prices spiked toward **$944** — recovery is accelerating.
8. **Building age** (2002–2022) shows no strong linear price trend — amenities matter more than construction year.

---

## 📊 Tableau Dashboards

### Dashboard 1 — Market Overview
- **KPIs:** Avg Price: $626.2 | Listings: 46,308 | Avg Review Rate: 2.505
- **Charts:** High-Growth Neighbourhoods, Room Type Market Share, Borough Count, NYC Map
- **Filters:** Borough, Neighbourhood, Room Type

### Dashboard 2 — Pricing & Revenue Intelligence
- **KPIs:** Avg Service Fee: $125.2 | Avg Total Price: $751.4
- **Charts:** Revenue Trend Over Years, Price Tier Distribution, Room Type × Price Heatmap, Construction Year vs Price

### Dashboard 3 — Guest Experience & Host Behaviour
- **KPIs:** Avg Review Rate: 2.505 | Avg Reviews Per Month: 1.184
- **Charts:** Review Rate Distribution, Instant Bookable vs Review Rate, Cancellation Policy Treemap, Host Verification Status
- **Filters:** Review Rate slider, Cancellation Policy, Borough

---

## 💡 Top Recommendations

| Priority | Recommendation | Expected Impact |
|---|---|---|
| 🔴 High | Enable Instant Booking platform-wide incentive | +10–15% booking conversion |
| 🔴 High | Target Queens for host acquisition campaigns | +2,000–3,000 new listings in 12 months |
| 🟡 Medium | Implement flexible cancellation policy nudges | -5–8% vacancy in off-peak months |
| 🟡 Medium | Introduce Budget Tier promotion | +8% bookings from price-sensitive segment |
| 🟡 Medium | Review Rate Improvement Programme for bottom-50% hosts | +0.5 pts average review rate |

---

## 🗂️ Project Structure

```
B-G5-Airbnb/
│
├── data/
│   ├── raw/                  # Original dataset
│   └── cleaned/              # Post-ETL cleaned dataset
│
├── notebooks/
│   ├── 02_cleaning.ipynb     # Data cleaning & ETL log
│   ├── 03_eda.ipynb          # Exploratory Data Analysis
│   └── 04_statistical_analysis.ipynb  # Hypothesis tests & regression
│
├── scripts/
│   └── etl_pipeline.py       # Standalone ETL pipeline script
│
├── tableau/                  # Tableau workbook files
│
├── reports/                  # Final report and presentation
│
└── README.md
```

---

## ⚠️ Limitations

- **Static Dataset:** Point-in-time snapshot; real-time changes not captured.
- **Self-Reported Reviews:** May be biased toward satisfied guests.
- **No Actual Bookings:** `availability_365` and `reviews_per_month` are demand proxies only.
- **NYC Regulatory Context:** Local Law 18 (2023) may have altered the landscape post-data collection.
- **Staten Island Underrepresented:** <1% of total listings.
- **No Host Expense Data:** Revenue estimates exclude operational costs.

---

## 🚀 Future Scope

- **Real-Time Dashboard:** Connect Tableau to a live Inside Airbnb API feed.
- **Predictive Pricing Model:** XGBoost / Random Forest for optimal nightly price prediction.
- **Sentiment Analysis:** NLP on guest review text for quality driver insights.
- **Regulatory Impact Study:** Quantify listing volume change pre/post NYC Local Law 18.
- **Competitive Benchmarking:** Add hotel pricing from Booking.com or Expedia.

---

## 📌 Contribution Matrix

| Team Member | Dataset | ETL & Cleaning | EDA | Statistics | Tableau | Report | PPT |
|---|---|---|---|---|---|---|---|
| Harsha Gonela | | | | | | ✓ | ✓ |
| Kanishka Dubey | ✓ | | | | | ✓ | |
| Hardik Shreyas | | | ✓ | ✓ | | | |
| Sharma Piyush | ✓ | | | | ✓ | | |
| Vaibhav Singh | ✓ | | | | ✓ | | |
| Ankit | ✓ | ✓ | | | | | |

> *We confirm that the above contribution details are accurate and verifiable through GitHub Insights, PR history, and submitted artifacts.*

---

## 📄 License

This project is submitted as part of the DVA Capstone 2 programme at Newton School of Technology. All data sourced from [Inside Airbnb](http://insideairbnb.com/) under its public data licence.
