# 🚗 US Traffic Accident Analysis Dashboard
## A Data Science Capstone Project for Data-Driven Road Safety Insights

### 🧭 Project Overview

- This project explores U.S. traffic accident data to identify key factors influencing accident severity and frequency across different states, weather conditions, times, and weekdays.
- The analysis culminates in an interactive Streamlit dashboard designed for non-technical stakeholders such as transportation officials and policy makers, helping them explore trends and make informed safety decisions.

### 🎯 Objectives
- Analyze accident trends and relationships between severity and categorical variables (Weather, State, Hour, Weekday).
- Perform statistical testing to validate observed patterns.
- Identify actionable recommendations to reduce accident frequency and severity.
- Build an interactive dashboard to visualize findings and support decision-making.

### 🧩 Dataset
- Source: US Accidents Dataset (2016–2023) – Kaggle
- Size: ~7 million accident records
- Key Features:
     - Severity: Accident impact level (1–4)
     - Weather_Condition, State, Hour, Weekday, Visibility(mi), Temperature(F), etc.
     - Start_Lat, Start_Lng: Coordinates for mapping


### Data Preparation
- Data Cleaning
        - Removed null values, duplicates, and irrelevant columns.
        - Handled missing Weather_Condition and Visibility using median imputation.
        - Extracted Hour, Weekday, and Month from timestamps.

- Feature Engineering
       - Created categorical groupings for weather and time-based patterns.
       - Normalized continuous variables where required.

- Data Export
 - df.to_csv('US_Accidents_Cleaned.csv', index=False)

### 📊 Exploratory Data Analysis (EDA)
- Comprehensive analysis performed using Pandas, Matplotlib, Seaborn, and ydata-profiling.
- Key insights include:
       - Accident severity is significantly correlated with weather conditions (Chi² = 368,728; p < 0.001).
       - Severity varies significantly across states (Chi² = 483,781; p < 0.001).
       - Peak accident hours: 7–9 AM and 4–7 PM (commute times).
       - Weekday trend: Friday shows the highest frequency of accidents.


### 🧠 Statistical Analysis

| Test        | Variables Tested                  | Result        | Interpretation                             |
| ----------- | --------------------------------- | ------------- | ------------------------------------------ |
| Chi-Square  | Weather × Severity                | p < 0.001     | Weather significantly affects severity     |
| Chi-Square  | State × Severity                  | p < 0.001     | Severity differs by state                  |
| ANOVA       | Hour × Severity                   | p < 0.001     | Accident severity varies by hour           |
| Correlation | Visibility, Temperature, Severity | Weak negative | Low visibility slightly increases severity |

### 💡 Data-Driven Recommendations
- 1️⃣ Implement Real-Time Weather Alerts
       - Insight: Severe weather conditions (fog, heavy rain, snow) correlate with higher accident severity.
       - Action: Deploy weather-integrated driver alerts and adaptive speed limit systems.
       - Metric: Reduction in weather-related severe crashes (% change YoY).

- 2️⃣ Enhance Traffic Enforcement During Peak Hours
       - Insight: Most accidents occur during 7–9 AM and 4–7 PM.
       - Action: Increase patrol and monitoring during peak commute hours.
       - Metric: Decrease in accident frequency per hour.

- 3️⃣ Target High-Risk States with Road Safety Campaigns
      - Insight: States like CA, TX, and FL show consistently high accident counts.
      - Action: Conduct targeted road safety awareness and infrastructure audits.
      - Metric: Reduction in accident severity index by state.


### 💻 Interactive Dashboard
- Built With:
    - 🧱 Streamlit – Interactive web framework
- Features:
      - ✅ Filter by State, Weather, Severity
      - ✅ Explore patterns by Hour, Weekday, and Location
      - ✅ Interactive charts & pie plots
      - ✅ Live map of accident density
  
### 🧩 Technologies Used

| Category          | Tools                       |
| ----------------- | --------------------------- |
| Programming       | Python (Pandas, NumPy)      |
| Visualization     | Matplotlib, Seaborn, Plotly |
| Dashboard         | Streamlit                   |
| Statistical Tests | Scipy, Statsmodels          |
| Profiling         | ydata-profiling             |
| Dataset Source    | Kaggle                      |

### 🔍 Reflection
- 🏆 Accomplishments:
      - Successfully identified significant relationships using Chi-Square and ANOVA tests.
      - Built a fully functional interactive dashboard.
      - Derived clear, actionable insights with measurable impact.

- ⚙️ Challenges:
      - Handling large dataset memory constraints.
      - Cleaning and standardizing inconsistent weather and state entries.
      - Ensuring visualizations remained interpretable for non-technical users.

- 🚀 Future Improvements:
     - Incorporate real-time accident feeds and weather APIs.
     - Integrate machine learning models for severity prediction.
     - Enhance the dashboard with trend forecasting and KPI tracking.


### 📈 Metrics for Success 
| Objective                 | KPI                         | Measurement                            |
| ------------------------- | --------------------------- | -------------------------------------- |
| Reduce severe accidents   | Severity Index              | Average severity over time             |
| Improve weather safety    | Weather-related crash ratio | % of crashes during adverse conditions |
| Optimize peak-hour safety | Hourly accident rate        | Crashes per 100k vehicles per hour     |



### 🧑‍💻 Author
- Faheemunnisa Syeda
- Data Science Capstone Project – US Traffic Accident Analysis
- 📧 Contact: [syedafaheem56@gmail.com]
- 🔗 GitHub: [https://github.com/syedafaheem7/]
