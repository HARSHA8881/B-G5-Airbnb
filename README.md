# 🏙️ NYC Airbnb Analytics Engine

> End-to-end data pipeline · Exploratory Data Analysis · Statistical Inference · Tableau Intelligence

## 📌 Overview

This project delivers a **data analytics pipeline** for the NYC Airbnb ecosystem — transforming raw listing data into actionable business intelligence for hosts, investors, and platform strategists.

**What's inside:**
- ⚙️ Robust ETL pipeline built in Python
- 📊 Deep Exploratory Data Analysis (EDA)
- 📈 Statistical inference & hypothesis testing
- 📉 Interactive Tableau dashboards

---

## 🧠 Problem Context

The NYC Airbnb market is highly fragmented, over-saturated in prime neighborhoods, and lacks structured analytical insights. This leads to suboptimal pricing decisions, poor location strategies, and missed revenue opportunities.

**This project addresses:**
- Identifying high-demand vs. oversupplied neighborhoods
- Analyzing pricing dynamics and revenue drivers
- Evaluating guest satisfaction patterns
- Delivering clear, data-backed strategic recommendations

---

## 🏗️ Project Structure

```
nyc-airbnb-analytics/
├── data/                        # Raw & processed datasets
├── docs/                        # Project documentation & references
├── notebooks/
│   ├── 02_cleaning.ipynb        # Data preprocessing
│   ├── 03_eda.ipynb             # Exploratory analysis
│   └── 04_statistical_analysis.ipynb  # Hypothesis testing & regression
├── reports/                     # Final insights & summaries
├── scripts/
│   └── etl_pipeline.py          # Automated ETL pipeline
├── tableau/                     # Tableau dashboards & exports
├── .gitignore
└── README.md
```

---

## ⚙️ Tech Stack

| Layer | Tools |
|-------|-------|
| Data Processing | Python, Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Tableau |
| Statistical Analysis | Hypothesis Testing, Regression |
| Environment | Jupyter Notebook |
| Data Source | [Inside Airbnb](http://insideairbnb.com/) |

---

## 🔄 ETL Pipeline

### 🧹 Data Cleaning
- Standardized column naming conventions
- Missing value imputation (median-based)
- Outlier capping at the 99th percentile
- Duplicate removal and data type corrections

### ⚡ Feature Engineering

| Feature | Description |
|---------|-------------|
| `price_tier` | Segmentation from Budget → Luxury |
| `estimated_revenue` | Proxy for host revenue potential |
| `occupancy_rate` | Demand indicator |
| `total_price` | Real guest cost (base + fees) |

---

##  Key Findings

###  Market
- Manhattan + Brooklyn account for **~85% of supply**
- Queens is an emerging **high-growth opportunity zone**

### Pricing
- Average listing price: **$626**
- Average total guest cost: **$751+** (service fees ≈ 20%)

### Property Types
- Entire homes dominate at **>50% of listings**
- Private rooms offer a **better value** segment

### Reviews
- Bimodal rating distribution (~2.6 vs ~1.7 peaks)
- Indicates a significant **host quality divide**

---

##  Statistical Analysis

### Hypothesis Testing
**Instant Booking vs. Review Rate** — Result: No significant difference detected.
> Enabling instant booking does not negatively impact review quality. Convenience ≠ lower quality.

### Regression Analysis
**Post-pandemic price trend** — Result: Statistically significant positive trend.
> Demand recovery is confirmed with prices rising year-over-year since 2021.

---

## Tableau Dashboards

Three dashboards provide layered business intelligence:

1. **Market Overview** — Borough distribution, neighborhood demand, listing density
2. **Pricing Intelligence** — Revenue trends, price tier segmentation, geographic heatmaps
3. **Guest Experience** — Review distribution, cancellation policy analysis, host behavior patterns

---

## Strategic Recommendations

| Priority | Action | Expected Impact |
|----------|--------|-----------------|
| 🔴 High | Enable Instant Booking incentives | +10–15% conversions |
| 🔴 High | Expand supply in Queens | Market growth opportunity |
| 🟡 Medium | Promote flexible cancellation policies | Lower vacancy rates |
| 🟡 Medium | Target the budget price segment | Volume-driven bookings |
| 🟡 Medium | Identify & improve low-rated hosts | Better platform quality |

---

## ⚠️ Limitations

- Static dataset — no real-time updates
- No actual booking transaction data
- Potential review bias from self-selection
- Regulatory changes not fully captured in the dataset

---

## 🔮 Future Enhancements

- 🤖 ML-based price prediction (XGBoost / LightGBM)
- 📡 Real-time dashboard integration via API
- 🧠 NLP sentiment analysis on guest reviews
- 📊 Regulatory impact modeling

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/your-username/nyc-airbnb-analytics.git
cd nyc-airbnb-analytics

# Install dependencies
pip install -r requirements.txt

# Run the ETL pipeline
python scripts/etl_pipeline.py

# Launch notebooks
jupyter notebook
```

---

## 📂 Data Source

Data sourced from [Inside Airbnb](http://insideairbnb.com/) — an independent, non-commercial project providing public Airbnb listing data.

---

## 📎 Full Report

The complete analytical report is available here:
[📄 View Full Report](https://docs.google.com/document/d/1KZJvpFIPW3gtA3Q9yimsABRNF6iLnz477pQkHIO0VfI/edit?usp=sharing)

---

## 📬 Contact

Have questions or want to collaborate? Feel free to open an issue or reach out via GitHub.

---

*Built with 🧡 using Python, Pandas, and Tableau — transforming raw data into strategic decisions.*
