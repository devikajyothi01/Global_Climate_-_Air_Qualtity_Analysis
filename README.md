# Global_Climate_&_Air_Qualtity_Analysis
## 📊Project Overview

This project presents a comprehensive analysis of global climate conditions and air quality using Python for data preprocessing and Power BI for interactive visualization.

The dashboard helps in understanding:

Air pollution levels (PM10)
Climate patterns (temperature, humidity, wind speed)
Global environmental trends

## 🎯Objectives
Analyze PM10 pollution levels across countries
Identify most polluted regions
Study climate variables (temperature, humidity, wind speed)
Visualize trends over time
Explore relationships between environmental factors

## 🛠️Tools & Technologies
Python (Pandas, Matplotlib)
Power BI
DAX (Data Analysis Expressions)
Kaggle Dataset

## 🐍Data Preprocessing (Python)

Initial data exploration and cleaning were performed using Python:

Checked dataset structure using info()
Generated statistical summary using describe()
Handled missing values
Removed duplicate records
Dropped unnecessary columns
Performed basic exploratory analysis

## 🧠Data Modeling
Created a Country Dimension Table
Established One-to-Many relationship
Ensured consistent aggregation across visuals

## 🧮Key DAX Measures
### Average PM10
Avg PM10 = AVERAGE('cleaned_weather_data'[PM10])

### Pollution Level Classification
Pollution Level =
SWITCH(
TRUE(),
[Avg PM10] <= 50, "Low",
[Avg PM10] <= 100, "Moderate",
[Avg PM10] <= 200, "High",
"Severe"
)

## 📊Dashboard Features
### 🔹 KPI Cards

Average Temperature\n
Average Humidity

Average Wind Speed

Average PM10

### 🔹 Visualizations
🗺️ Filled Map – Global Pollution Distribution
📊 Bar Chart – Top Polluted Countries
🍩 Donut Chart – Weather Condition Distribution
📈 Line Charts – Pollution & Temperature Trends
🔵 Scatter Plot – Temperature vs Humidity

### 🔹 Slicers
Country
Weather Condition
Date

### 🎨 Design Highlights
Clean and minimal layout
Consistent color coding:
🟢 Low
🟡 Moderate
🟠 High
🔴 Severe
Interactive dashboard

## 🔍 Key Insights
Chile is the most polluted country (highest PM10)
Air pollution shows a decreasing trend over time
Weak correlation between temperature and humidity
Clear weather is the most common condition globally

## ⚠️ Challenges & Solutions
Challenges
Aggregation mismatch (SUM vs AVG)
Inconsistent results across visuals
Map coloring limitations
Solutions
Used Average PM10 consistently
Created Pollution Level classification
Fixed data model using Country table relationship

## 🚀 Future Improvements
Add PM2.5 / AQI index
Real-time data integration
Forecasting and predictive analysis
Advanced interactivity
