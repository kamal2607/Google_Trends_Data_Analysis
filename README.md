📊 Google Trends Data Analysis
📌 Project Overview

This project performs Google Trends data analysis using the pytrends library to study public search interest patterns.
It analyzes how keywords trend across countries, over time, and in comparison with other keywords, using powerful data visualization libraries.

The project is useful for:

Job market trend analysis

Education & career research

Market research and social insights

Data visualization practice

🧠 Objectives

Fetch real-time and historical search trend data from Google Trends

Analyze country-wise search interest

Visualize time-wise trend patterns

Compare multiple keywords

Present insights using interactive and static plots

🛠️ Tech Stack & Libraries

Python

pytrends – Google Trends API wrapper

pandas – Data manipulation

matplotlib – Static visualizations

seaborn – Statistical plots

plotly – Interactive world maps

📦 Installation & Setup
1️⃣ Install Required Libraries
pip install pytrends pandas matplotlib seaborn plotly

2️⃣ Import Libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
from pytrends.request import TrendReq

⚙️ Project Workflow
🔹 Step 1: Initialize PyTrends
pytrends = TrendReq(hl='en-US', tz=360)
keyword = "jobs"

🔹 Step 2: Fetch Country-wise Search Interest
pytrends.build_payload([keyword], timeframe='today 12-m')
region_data = pytrends.interest_by_region()


✔ Visualized using:

Seaborn bar chart

Plotly interactive world map

🔹 Step 3: Time-wise Trend Analysis
time_df = pytrends.interest_over_time()


✔ Shows how interest in the keyword changes over time using line plots.

🔹 Step 4: Multiple Keyword Comparison
kw_list = ["jobs", "higher study", "unemployed"]
pytrends.build_payload(kw_list, timeframe='today 12-m')


✔ Compares trends of multiple keywords in a single plot.

📊 Visualizations Included

📈 Line chart for trend over time

📊 Bar chart for top searching countries

🌍 Interactive choropleth world map

🔍 Keyword comparison plots

📁 Project Structure
Google-Trends-Data-Analysis/
│
├── google_trends_analysis.py
├── README.md
└── requirements.txt (optional)

🚀 Use Cases

Job market demand analysis

Career & education planning

Social behavior research

Marketing & SEO analysis

Data visualization portfolio project

⚠️ Notes & Limitations

Google Trends data is relative (0–100), not absolute search volume

Results may vary based on location, timeframe, and Google’s sampling

Requires stable internet connection

📌 Future Enhancements

Add region/state-level analysis

Automate keyword input

Save plots and data as CSV

Deploy as a dashboard (Streamlit / Dash)

👨‍💻 Author

Kamal Kumar
B.Tech | Data Analytics & ML Enthusiast
📍 IIT Jodhpur
