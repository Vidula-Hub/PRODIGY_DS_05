# Traffic Accident Analysis: Patterns and Hotspots in the US

## Overview
This project analyzes a sampled subset of the **US Accidents** dataset to identify patterns and hotspots in US traffic accidents. Using Python, we explore relationships between accidents and factors like time of day, weather, road conditions, lighting, and geographic locations, visualized through plots and interactive maps.

## Dataset
- **Source**: [US Accidents](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents)
- **Size**: ~10,000 records (sampled from original 7.7M rows using chunking), cleaned to ~9,995 rows after preprocessing
- **Key Columns**: `Start_Time`, `Start_Lat`, `Start_Lng`, `Weather_Condition`, `Road_Condition` (inferred from `Weather_Condition` and `Precipitation(in)`), `Sunrise_Sunset`, `Severity`, `City`, `State`

## Project Structure
Traffic-Accident-Analysis/
├── data/
│   ├── US_Accidents_March23.csv         # Original dataset (not committed)
│   ├── usa_traffic_accidents_sampled.csv  # Sampled dataset (10,000 rows)
│   ├── usa_traffic_accidents_cleaned.csv  # Cleaned dataset (~9,995 rows)
├── images/
│   ├── accidents_by_hour.png           # Accidents by hour
│   ├── accidents_by_day.png            # Accidents by day
│   ├── accidents_by_month.png          # Accidents by month
│   ├── accidents_by_weather.png        # Accidents by weather
│   ├── accidents_by_road.png           # Accidents by road (inferred)
│   ├── accidents_by_lighting.png       # Accidents by lighting
│   ├── accident_hotspots_folium.html   # Folium heatmap
│   ├── accident_hotspots_plotly.html   # Plotly scatter map
├── notebooks/
│   ├── preprocessing.ipynb             # Data loading, sampling, and cleaning
│   ├── eda.ipynb                       # Exploratory data analysis
│   ├── visualization.ipynb             # Visualizations
│   ├── insights.ipynb                  # Summary of findings
├── scripts/                            # Empty
├── .gitignore                         # Ignores venv/, pycache/
├── README.md                          # Documentation
├── requirements.txt                   # Dependencies

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Vidula-Hub/PRODIGY_DS_05.git
   cd Traffic-Accident-Analysis
Create and Activate Virtual Environment:
bash

Copy
python -m venv venv
.\venv\Scripts\activate  # Windows
Install Dependencies:
bash

Copy
pip install -r requirements.txt
Download the Dataset:
Download US_Accidents_March23.csv from Kaggle.
Place in data/.
Run preprocessing.ipynb to sample and clean the dataset (includes inferring Road_Condition).
Run the Notebooks:
Open VS Code and navigate to notebooks/.
Run preprocessing.ipynb, eda.ipynb, visualization.ipynb, and insights.ipynb in order.
Key Findings
Time Patterns:
Accidents peak during rush hours (7–9 AM, 4–6 PM).
Weekdays (e.g., Friday) have more accidents; weekends may show higher severity.
Weather:
Clear weather dominates; rain/snow increases severity.
Road Conditions:
Inferred dry roads (from clear/cloudy weather) have more accidents; wet roads (from rain/snow) correlate with severe outcomes.
Lighting:
Daylight has more accidents; darkness increases severity.
Hotspots:
Clusters in urban areas (visible in maps), likely near intersections.
Recommendations:
Enhance safety during rush hours with traffic calming measures.
Improve road conditions in adverse weather (e.g., better drainage for wet roads).
Increase lighting in high-risk areas at night.
Target patrols in hotspot areas identified in maps.
Visualizations
Bar plots for time, weather, road conditions (inferred), and lighting conditions (images/).
Interactive hotspot maps (images/accident_hotspots_folium.html, images/accident_hotspots_plotly.html).
Dependencies
See requirements.txt (e.g., pandas, matplotlib, seaborn, folium, plotly).

Author
Vidula Sri
GitHub: Vidula-Hub
License
MIT License

This README reflects the inferred Road_Condition column and the final dataset size (~9,995 rows).
It provides clear setup instructions and summarizes your findings.