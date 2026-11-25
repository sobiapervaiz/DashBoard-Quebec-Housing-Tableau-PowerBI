# 📊 Quebec Real Estate Market Analysis (Tableau & Power BI)

[![Tableau](https://shields.io)](https://tableau.com)
[![Power BI](https://shields.io)](https://microsoft.com)
[![Kaggle](https://shields.io)](https://kaggle.com)
[![SQL / Python](https://shields.io)](https://python.org)

An interactive Business Intelligence project analyzing residential real estate trends, regional pricing disparities, and property valuation drivers across Quebec (Montreal, Quebec City, Laval, Gatineau, and surrounding regions). Built in both **Tableau** and **Microsoft Power BI** to compare dashboarding workflows and provide actionable market insights.

---

## 🔗 Live Dashboards & Links
- **Tableau Public Dashboard:** [View Interactive Workbook](#) *(Add your Tableau Public link)*
- **Power BI Report:** [View Live Report / Demo Video](#) *(Add your Power BI Service link or Loom/YouTube walkthrough)*
- **Dataset Source:** [Quebec Housing Dataset on Kaggle](#) *(Add Kaggle link)*

---

## 📸 Dashboard Previews

### Tableau Executive Overview
![Tableau Dashboard Preview](assets/tableau_dashboard.png)
*(Tip: Save high-res screenshots of your dashboards in an `assets/` folder in your repo)*

### Power BI Interactive Report
![Power BI Dashboard Preview](assets/powerbi_dashboard.png)

---

## 🎯 Business Questions Answered
This project was designed to help prospective homebuyers, real estate investors, and analysts answer key market questions:
1. **Regional Affordability:** How do median home prices and price-per-square-foot compare across major Quebec municipalities (e.g., Greater Montreal vs. Capitale-Nationale)?
2. **Property Type Breakdown:** What is the market share and pricing premium of Single-Family Homes vs. Condos vs. Multi-unit Plexes (Duplex/Triplex)?
3. **Age & Valuation:** How does construction year (`year_built`) impact property value, particularly for historic vs. modern builds?
4. **Feature Drivers:** Which structural attributes (bedrooms, bathrooms, lot size, living area) correlate most strongly with listing prices?

---

## 🛠️ Data Preparation & Modeling
Before connecting the dataset to Tableau and Power BI, the raw Kaggle CSV underwent cleaning and transformation:

- **Data Cleaning (Python / Power Query):**
  - Standardized municipality and neighborhood names (handled French accents/formatting inconsistencies).
  - Removed duplicate listings and handled extreme outliers (e.g., \$0 listings or ultra-luxury estates skewing averages).
  - Imputed missing `living_area` and `lot_size` values where appropriate or flagged them for filtering.
- **Feature Engineering & DAX / Calculated Fields:**
  - `Price per SqFt` = `Price / Living Area`
  - `Property Age` = `Current Year - Year Built`
  - `Price Tier` = Categorized properties into *Budget (<\$350K)*, *Mid-Market (\$350K–\$650K)*, *Upper-Mid (\$650K–\$1M)*, and *Luxury (\$1M+)*.
  - `Forward Sortation Area (FSA)` = Extracted first 3 characters of postal codes for geospatial heatmapping.

---

## 💡 Key Insights & Findings
*(Customize these bullet points with the exact numbers from your visuals)*
- **Geographic Premium:** Properties in the Greater Montreal Area command a **~35% higher median price** compared to the provincial average, driven heavily by proximity to transit hubs and downtown cores.
- **The "Plex" Factor:** Missing Middle housing (Duplexes and Triplexes) represents a major share of Montreal’s inventory, trading at higher total prices than single-family homes due to rental income potential.
- **Size vs. Location:** While square footage strongly correlates with price within the same city, location (FSA/municipality) accounts for the largest variance in `Price per SqFt`.

---

## 📁 Repository Structure
```text
quebec-housing-bi-analysis/
├── assets/
│   ├── tableau_dashboard.png      # Screenshot of Tableau dashboard
│   └── powerbi_dashboard.png      # Screenshot of Power BI report
├── data/
│   ├── raw/                       # Original Kaggle dataset (ignored if >100MB)
│   └── cleaned/                   # Cleaned dataset ready for BI ingestion
├── scripts/
│   └── data_cleaning.py           # Python / SQL data prep script
├── dashboards/
│   ├── Quebec_Housing_Analysis.twbx   # Packaged Tableau Workbook
│   └── Quebec_Housing_Report.pbix     # Power BI Desktop File
└── README.md
```

---

## 🚀 How to View Locally
1. **Clone the repository:**
   ```bash
   git clone https://github.com
   ```
2. **Tableau:** Open `dashboards/Quebec_Housing_Analysis.twbx` using **Tableau Desktop** or the free **Tableau Public** desktop app.
3. **Power BI:** Open `dashboards/Quebec_Housing_Report.pbix` using **Power BI Desktop** (Windows).

---

## 📬 Contact
Created by **[Your Name]** — [LinkedIn](#) | [Tableau Public](#) | [Portfolio Website](#)
