# TravelTide — Customer Segmentation for Personalized Rewards

## 📌 Project Overview
This project delivers a data-driven customer segmentation for **TravelTide**, an AI-powered travel itinerary platform.  
Using SQL, Python, and machine learning (**K-Means clustering**), we identified six distinct traveler segments and mapped each to a personalized perk aimed at increasing retention, engagement, and revenue.

### Key Highlights:
- 6 behavior-based customer segments
- 21 engineered features covering engagement, conversion, spend, loyalty, and cancellations
- SQL-based feature engineering from raw relational database tables
- Best-performing clustering model: **K-Means (k=6, silhouette score ≈ 0.474)**
- Professional reports and deliverables ready for stakeholders

---

## 🏢 Business Context
TravelTide’s marketing team needed a personalized rewards program tailored to actual customer behavior.  
Instead of assuming perk preferences, this approach:
- Uses unsupervised learning to find natural segments  
- Matches perks to behavioral profiles  
- Prepares A/B testing metrics for marketing rollout  

---

## 📊 Data Pipeline

**1. Data Source**  
Relational PostgreSQL database with 4 key tables:  
- **users** — demographics & home location  
- **sessions** — browsing sessions & interactions  
- **flights** — purchased flights & itinerary details  
- **hotels** — purchased hotel stays  

**2. SQL Feature Engineering**  
- Filter: users with > 7 sessions after `2023-01-04`  
- Engineered 21 user-level features (conversion rate, spend, distance, loyalty score, cancellation rate, etc.)  
- Output: `traveltide_final.csv` (**5,998 users**)  

**3. Python Analysis (Jupyter/Colab)**  
- Data preprocessing & scaling  
- **K-Means clustering** (k=6)  
- PCA for visualization  
- Cluster profiling & perk assignment  

**4. Deliverables**  
- Executive summary & detailed report  
- Feature dictionary  
- SQL query (PDF + TXT)  
- Final user-perk mapping (`traveltide_user_perk.csv`)  

---

## 📂 Repository Structure

TravelTideProject/
│
├── data/
│ ├── raw/
│ │ └── traveltide_filtered_session_lvl.csv
│ └── processed/
│ ├── traveltide_final.csv
│ ├── traveltide_final_completed.csv
│ ├── traveltide_log_cols.csv
│ ├── traveltide_reduced_scaled.csv
│ └── traveltide_scaled.csv
│
├── notebooks/
│ └── traveltide_final.ipynb
│
├── output/
│ ├── traveltide_user_perk.csv
│ ├── traveltide_final_query.pdf
│ └── traveltide_final_query.txt
│
├── reports/
│ ├── traveltide_executive_summary.pdf
│ ├── traveltide_detailed_report.pdf
│ ├── traveltide_feature_dictionary.pdf
│ ├── traveltide_database_link_raw.pdf
│ └── traveltide_presentation_slides.pdf
│
└── README.md

---

## 📑 Reports
- **Executive Summary**: High-level business-focused overview  
- **Detailed Report**: Expanded methodology and findings  
- **Feature Dictionary**: Documentation of each engineered feature  
- **Database Link Raw**: Table schema and database connection info  
- **Presentation Slides**: Stakeholder-ready visuals  