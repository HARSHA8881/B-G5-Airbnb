🏙️ NYC Airbnb Analytics Engine
End-to-End Data Pipeline • EDA • Statistical Insights • Tableau Intelligence
🚀 Project Overview

This project delivers a full-stack data analytics pipeline for the NYC Airbnb ecosystem — transforming raw listing data into actionable business intelligence.

It combines:

⚙️ Robust ETL pipeline (Python)
📊 Deep Exploratory Data Analysis
📈 Statistical inference
📉 Interactive Tableau dashboards

The goal: enable data-driven decisions for hosts, investors, and platform strategists.

🧠 Problem Context

The NYC Airbnb market is:

Highly fragmented
Over-saturated in prime locations
Lacking structured insights

This leads to:

Suboptimal pricing
Poor location decisions
Missed revenue opportunities
🎯 Key Objectives
Identify high-demand vs oversupplied neighborhoods
Analyze pricing dynamics & revenue drivers
Evaluate guest satisfaction patterns
Provide strategic recommendations
🏗️ Project Architecture
├── data/           # Raw & processed datasets
├── docs/           # Project documentation & references
├── notebooks/      # Jupyter notebooks (EDA, cleaning, analysis)
├── reports/        # Final reports & insights
├── scripts/        # ETL pipelines & reusable Python scripts
├── tableau/        # Tableau dashboards & exports
├── .gitignore
├── README.md
⚙️ Tech Stack
Layer	Tools Used
Data Processing	Python, Pandas, NumPy
Visualization	Matplotlib, Seaborn, Tableau
Analysis	Statistical Testing, Regression
Environment	Jupyter Notebook
Data Source	Inside Airbnb
🔄 Data Pipeline (ETL)
🧹 Data Cleaning
Standardized column naming conventions
Missing value imputation (median-based)
Outlier capping (99th percentile)
Duplicate removal
Data type corrections
⚡ Feature Engineering
price_tier → segmentation (Budget → Luxury)
estimated_revenue → revenue proxy
occupancy_rate → demand indicator
total_price → real guest cost
📊 Exploratory Data Analysis (EDA)
🏙️ Market Insights
Manhattan + Brooklyn = ~85% supply
Queens = high-growth opportunity zone
💰 Pricing Insights
Avg listing price: $626
Avg total cost: $751+
Service fees ≈ 20% of price
🛏️ Property Trends
Entire homes dominate (>50%)
Private rooms → better value segment
⭐ Review Dynamics
Bimodal ratings (~2.6 vs ~1.7)
Indicates quality divide in hosts
📈 Statistical Analysis
🔬 Hypothesis Testing
Instant Booking vs Review Rate
Result: No significant difference
👉 Convenience ≠ lower quality
📉 Regression Analysis
Positive price trend post-pandemic
👉 Demand recovery confirmed
📊 Tableau Dashboards
1️⃣ Market Overview
Borough distribution
Neighborhood demand
Listing density
2️⃣ Pricing Intelligence
Revenue trends
Price tier segmentation
Heatmaps
3️⃣ Guest Experience
Review distribution
Cancellation policies
Host behavior
💡 Strategic Insights
🏆 Queens = Best investment opportunity
⚠️ Brooklyn hotspots = Highly saturated
📈 Post-pandemic = Price surge
⚡ Instant booking = Safe to enable
🔄 Flexible policies = Higher conversions
🧭 Recommendations
Priority	Action	Impact
High	Enable Instant Booking incentives	+10–15% conversions
High	Expand supply in Queens	Market growth
Medium	Promote flexible cancellation	Lower vacancy
Medium	Target budget segment	More bookings
Medium	Improve low-rated hosts	Better platform quality
⚠️ Limitations
Static dataset (no real-time updates)
No actual booking transactions
Review bias possible
Regulatory changes not fully captured
🔮 Future Enhancements
🤖 ML-based price prediction (XGBoost)
📡 Real-time dashboard integration
🧠 NLP sentiment analysis on reviews
📊 Regulatory impact modeling
📂 Key Files & Workflow
File/Folder	Purpose
notebooks/02_cleaning.ipynb	Data preprocessing
notebooks/03_eda.ipynb	Exploratory analysis
notebooks/04_statistical_analysis.ipynb	Hypothesis testing
scripts/etl_pipeline.py	Automated pipeline
tableau/	Dashboard files
reports/	Final insights
📌 Business Impact

This project enables:

📈 Better pricing strategies
📍 Smarter location targeting
💰 Increased host revenue
⭐ Improved guest experience
🏁 Conclusion

The NYC Airbnb market is:

Highly concentrated
Price-sensitive
Quality-divided

This project transforms raw data into clear, strategic decisions, helping stakeholders maximize ROI in a competitive environment.

📎 Reference

Project content derived from full analytical report:
https://docs.google.com/document/d/1KZJvpFIPW3gtA3Q9yimsABRNF6iLnz477pQkHIO0VfI/edit?usp=sharing
