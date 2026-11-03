# DataScienceCapstoneProject

# IBM SpaceX Data Science Capstone

## Overview

This project analyses SpaceX Falcon 9 launch data to identify factors associated with successful launches and booster landings. It covers data collection, cleaning, SQL analysis, visualization, interactive dashboards, geospatial mapping, and predictive modelling.

## Objectives

- Collect and prepare SpaceX launch data.
- Explore relationships between launch success, payload mass, orbit, launch site, and flight number.
- Create interactive dashboards and geographic visualizations.
- Build classification models that predict launch landing success.
- Compare model performance and identify the best-performing approach.

## Project Workflow

1. **Data collection:** Retrieve launch information through the SpaceX REST API and web scraping.
2. **Data wrangling:** Clean missing values, standardize fields, filter Falcon 9 missions, and create analysis-ready datasets.
3. **SQL analysis:** Query launch sites, payloads, mission outcomes, booster versions, and landing outcomes.
4. **Exploratory analysis:** Create charts showing relationships between launch features and success.
5. **Dashboard:** Explore launch outcomes interactively using Plotly Dash.
6. **Geospatial analysis:** Use Folium to visualize launch locations, outcomes, nearby infrastructure, and distances.
7. **Predictive analysis:** Train and evaluate classification models.

## Project Files

| File | Description |
|---|---|
| `1_jupyter_labs_spacex_data_collection_api_final.ipynb` | Collects and combines SpaceX API data. |
| `2_jupyter-labs-webscraping.ipynb` | Collects additional SpaceX launch data from web pages. |
| `3_labs-jupyter-spacex-Data wrangling-v2.ipynb` | Cleans and prepares the launch dataset. |
| `4_jupyter-labs-eda-sql-coursera_sqllite.ipynb` | Performs SQL exploratory data analysis. |
| `5_jupyter-labs-eda-dataviz-v2.ipynb` | Creates exploratory charts. |
| `6_lab-jupyter-launch-site-location-v2.ipynb` | Creates Folium geographic visualizations. |
| `7_spacex_dash_app.py` | Runs the interactive Plotly Dash dashboard. |
| `8_SpaceX-Machine-Learning-Prediction-Part-5-v1.ipynb` | Trains and evaluates classification models. |
| `spacex_launch_dash.csv` | Dashboard data. |
| `spacex_launch_geo.csv` | Geographic launch-site data. |
| `ds-capstone-template-coursera.pptx` | Project presentation template. |

## Machine-Learning Results

The following classifiers were trained using standardized features, an 80/20 train-test split, and 10-fold cross-validation:

- Logistic Regression
- Support Vector Machine
- Decision Tree
- K Nearest Neighbors

The Decision Tree achieved the highest mean cross-validation accuracy at **86.07%**. All four models achieved **83.33% accuracy** on the independent test set.

## Run the Dashboard

Install the required packages:

```bash
pip install pandas plotly dash
```

Run the application from the project directory:

```bash
python 7_spacex_dash_app.py
```

Then open the local address printed in the terminal, usually `http://127.0.0.1:8050`.

## Technologies

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Plotly and Dash
- Folium
- SQL
- Jupyter Notebook
- Scikit-learn

## Key Findings

- Launch success varies by launch site, orbit, payload mass, and flight number.
- Operational experience and booster reuse are associated with improved landing performance.
- The Decision Tree produced the highest tuning score, while test-set accuracy was equal across the four models.
