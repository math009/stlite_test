# Green Fuels & Energy Demand Dashboard
An interactive, **serverless** web application visualizing the transition to Power-to-X (PtX) and green energy demand across the EU27. This dashboard runs entirely in the browser using [stlite]((https://math009.github.io/stlite_test/)).

## Project Scope
This dashboard explores projected energy demand evolution (2025–2050) across two primary sectors:
* **Transport:** Evolution of road (heavy/light), aviation, rail, and shipping demand.
* **Industry:** Strategic outlook for energy-intensive materials (Iron, Steel, Chemicals) and the integration of Green fuels like Ammonia, Hydrogen, and Methanol.

## Architecture
* **Frontend:** Streamlit logic embedded directly into `index.html`.
* **Data Hosting:** CSV files are fetched dynamically from this GitHub repository.
* **Modules:**
    * `dashboard_final.py`: UI layout and user filters.
    * `mappings.py`: Color schemes and category translations.
    * `process.py`: Unit conversions (to EJ) and data cleaning.
    * `*_plots.py`: Specialized Plotly visualization functions.

## Repository Structure
* `index.html`: The main application entry point.
* `Results_REMIND_JRC.csv`: Transport demand source data.
* `2030_DK.csv`, `2030_EU27.csv`, etc.: Industry-specific demand files.
* `PtX_demand_*.csv`: Final combined output data.

## How to Run Locally
Because the app is a single HTML file, you can run it installing Python:
1. Clone the repo.
2. Install streamlit on your local computer
3. Open a terminal in the folder named Dashboard and run:
   streamlit run dashboard_final.py
