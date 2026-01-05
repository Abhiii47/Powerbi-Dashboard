## 📖 Project Overview
This project is a high-fidelity **Marketing Analytics Dashboard** designed to help CMOs and Marketing Managers visualize cross-channel performance. It analyzes 5,000+ campaign records to identify high-ROI strategies across Facebook, Google Ads, LinkedIn, and more.

The dashboard transforms raw campaign data into actionable insights, answering key questions like:
*   *"Which channel delivers the lowest Cost Per Acquisition (CPA)?"*
*   *"Are we spending efficiently (ROAS) trended over time?"*
*   *"Which specific campaigns are underperforming?"*

## 💡 Key Features
*   **Dynamic Background Layout**: Uses a custom-designed background for a pixel-perfect "App-like" UI.
*   **Advanced DAX Measures**:
    *   `ROAS (Return on Ad Spend)` = Total Revenue / Total Spend
    *   `CPA (Cost Per Acquisition)` = Total Spend / Total Conversions
    *   `MoM Growth` logic for dynamic trend arrows (▲/▼).
*   **Interactive Visuals**:
    *   **KPI Cards** with custom SVG icons.
    *   **Channel Efficiency Matrix**: Comparing ROAS vs. Volume.
    *   **Drill-through Capability**: From high-level metrics to individual campaign details.

## 🛠️ Data Modeling
The data model consists of a **Star Schema**:
*   **Fact Table**: `MarketingData` (5,000 rows of campaign performance).
*   **Dimension Table**: `DateTable` (standard calendar table for time intelligence).
*   **Relationships**: One-to-Many relationship on `Date` columns.

## 📂 Project Structure
```bash
├── dashboard.pbix              # The main Power BI file
├── marketing_campaign_data.csv # Synthetic dataset generated for the project
├── modern_marketing_theme.json # Custom JSON theme for corporate color palette
├── dashboard_bg.png            # Custom UI background image
└── icons/                      # SVG assets for Revenue, Spend, etc.
```

## 🚀 How to Run
1.  **Data Source**: The report pulls from `marketing_campaign_data.csv`. Update the data source setting in Power BI if the path changes.
2.  **Theme**: The `modern_marketing_theme.json` is pre-applied.
3.  **Background**: Ensure `dashboard_bg.png` is set as the canvas background with 0% transparency.
