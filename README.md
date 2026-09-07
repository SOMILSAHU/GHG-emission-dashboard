# Infosys GHG Audit Dashboard — Power BI

Interactive Power BI dashboard reconstructing and independently auditing Infosys Limited's Scope 1, 2, and 3 GHG footprint for FY 2023-24 through FY 2025-26, built from primary-source data in Infosys's own ESG Data Book.

# ⚠️ Note on viewing this on GitHub

GitHub does not render `.pbix` files inline — it's a proprietary binary format. To actually **view and interact** with the dashboard, you need one of:

1. **Power BI Desktop** (free) — download the `.pbix` from this repo and open it locally.
2. **Static preview** — see `screenshots/` folder in this repo for exported images of each tab, or `dashboard-preview.pdf` for a full-page export (File → Export → Export to PDF in Power BI Desktop).

# What's in this repo

| File | Description |
|---|---|
| `Infosys_GHG_Dashboard.pbix` | The Power BI report file. Open in Power BI Desktop. |
| `Infosys_GHG_PowerBI_Source.xlsx` | Underlying data tables (GHG_Trend, Scope3_Categories, Scope1_Refrigerants, Scope2_Reconciliation) — edit these and refresh in Power BI to update the dashboard. |
| `screenshots/` | PNG exports of each dashboard tab (Overview, Scope 1, Scope 2, Scope 3, Audit Findings), for anyone browsing on GitHub without Power BI installed. |


# Data source & methodology

All figures are sourced directly from Infosys Limited's own **ESG Data Book 2025-26** (Annexures 4–6), not third-party aggregators. This is an *independent bottom-up audit*, not a transcription:

- **Scope 1** — refrigerant fugitive emissions recalculated refrigerant-by-refrigerant from disclosed kilograms × disclosed GWP factors; fuel combustion estimated from disclosed fuel-GJ figures.
- **Scope 2** — location-based and market-based emissions independently recalculated using the CEA India grid factor, then reconciled against Infosys's own dual-reported figures.
- **Scope 3** — T&D losses independently recalculated; all other categories carry Infosys's published figures with explicit notes on which ones cannot be independently verified due to undisclosed underlying activity data (business travel pkm, employee commute survey data, etc.).

Every variance between the independent estimate and Infosys's published number is explained, not hidden — see the **Audit Findings** tab.

# Key figures (FY 2025-26)

| Metric | Value |
|---|---|
| Scope 1 | 11,483 tCO2e |
| Scope 2 (market-based) | 34,351 tCO2e |
| Scope 3 | 207,374 tCO2e |
| Total | 253,208 tCO2e |
| Intensity | 2.27 tCO2e / US$mn revenue |
| Decarbonization via green power | 76.4% |

# Limitations (disclosed, not hidden)

- SF6 and CO2 fire-extinguisher fugitive quantities are not publicly disclosed by Infosys — a small residual in Scope 1 is left unattributed rather than forced to zero.
- 5 of 8 Scope 3 categories cannot be independently recalculated because Infosys publishes only final figures and methodology, not underlying spend/distance/survey data.
- GHG Protocol Category 11 (use of sold products) is explicitly excluded by Infosys pending methodology development — the reported Scope 3 total understates the full downstream footprint for a software/IT services company.

# How to use

1. Clone or download this repo.
2. Open `Infosys_GHG_Dashboard.pbix` in Power BI Desktop.
3. Use the tab buttons (Overview / Scope 1 / Scope 2 / Scope 3 / Audit Findings) at the top of the report to navigate.
4. To update with new fiscal year data: edit `Infosys_GHG_PowerBI_Source.xlsx`, then in Power BI Desktop go to Home → Refresh.

# Disclaimer

This is an independent, unofficial analysis for portfolio/research purposes. It is not affiliated with, endorsed by, or reviewed by Infosys Limited. All source figures are publicly disclosed by Infosys in its ESG Data Book; all independent calculations, variance analysis, and audit commentary are the author's own.

# License

MIT — see `LICENSE` file. Underlying Infosys disclosure data remains the property of Infosys Limited and is used here under fair-use for independent analysis/commentary.


