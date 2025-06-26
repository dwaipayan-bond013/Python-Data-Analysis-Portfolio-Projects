# 🚲 GoBike Rental Analysis



This project performs an in-depth analysis of GoBike rental data to uncover usage patterns, trends, and insights based on time, user type, and environmental conditions. The analysis includes visualizations and statistical tests to understand rental behavior better.

---

## 🧭 Project Overview

**GoBike Rental Analysis** is a data-driven project aimed at understanding how different factors influence the usage of a bike-sharing system over time. Using real-world rental data collected on an hourly basis, this analysis helps identify usage patterns that can inform **business strategies, operational improvements**, and **customer engagement efforts**.

### 🔍 Why This Analysis Matters

Bike-sharing systems have become a key component of urban mobility. Operators need to understand:
- When and why people use shared bikes
- How usage differs between casual users and subscribers
- The impact of weather, time, and holidays on demand
- How to optimize availability and staffing for peak usage

This project addresses these needs through **data exploration**, **visual storytelling**, and **statistical hypothesis testing**.

### 📦 What This Project Includes

- **Exploratory Data Analysis (EDA)** to examine rental trends over time (hour, day, season)
- **Segmented analysis** of two user types: **casual** (non-subscribers) and **registered** (subscribers)
- **Visualization of seasonal, monthly, and hourly usage** to identify high-demand periods
- **Correlation analysis** between rental volume and weather-related variables (temperature, humidity, etc.)
- **Statistical testing** (Shapiro-Wilk, t-tests, ANOVA) to validate key assumptions

### 📈 Key Questions Answered

| Question                                                                 | Insight Provided                                                  |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| Do people rent more on working days or holidays?                        | Working days see significantly higher usage (confirmed via t-test) |
| Which seasons or months are most popular for bike rentals?              | Summer and spring months peak in usage                             |
| How does weather influence rental volume?                               | Poor weather (rain, wind, cold) decreases rentals                  |
| How do registered users behave differently from casual users?           | Registered users show commuting patterns; casuals rent more on weekends |
| What time of day sees the most traffic?                                 | Morning and evening rush hours, mainly by registered users         |

### 🎯 Use Cases

- **Operations**: Improve bike availability during high-demand periods
- **Marketing**: Target promotions to casual users during weekends or good weather
- **Infrastructure**: Plan station placement based on peak usage times and user type
- **Expansion Planning**: Understand seasonal dips and surges for fleet scaling

---

## 📁 Files

- `GoBike_Rent_Analysis.ipynb`: Main Jupyter notebook with code, plots, and statistical analysis.
- `GoBike_sharing_dataset.csv`: Dataset containing hourly bike rental information.
- Output plots (generated upon execution):
  - `rentals_by_season.png`
  - `monthly_avg_rentals.png`
  - `hourly_trend_users.png`
  - `correlation_heatmap.png`

---

## 📊 Dataset Overview

| Column       | Description                                             |
|--------------|---------------------------------------------------------|
| `datetime`   | Timestamp of the observation                            |
| `season`     | 1: Winter, 2: Spring, 3: Summer, 4: Fall                 |
| `holiday`    | 1 if the day is a holiday, otherwise 0                  |
| `workingday` | 1 if the day is a working day, otherwise 0              |
| `weather`    | 1 to 4, from clear to heavy rain/storm                  |
| `temp`       | Normalized temperature in Celsius                       |
| `atemp`      | "Feels like" temperature                                |
| `humidity`   | Relative humidity (%)                                   |
| `windspeed`  | Wind speed                                              |
| `casual`     | Number of non-registered user rentals                   |
| `registered` | Number of registered user rentals                       |
| `count`      | Total rentals (casual + registered)                     |

---

## 🧪 Methodology

### 🧹 Data Preprocessing
- Converted `datetime` into `hour`, `month`, `weekday`, and `year` features
- Checked for nulls and data types

### 📈 Visualizations
- **Boxplots** for seasonal variation
- **Line plots** for monthly and hourly trends
- **Heatmaps** for correlation analysis

### 🔬 Statistical Analysis
- **Shapiro-Wilk test** for normality
- **T-test**: Compared rental counts on working vs. non-working days
- **ANOVA**: Analyzed rental variation across seasons

---

## 🔍 Key Insights

| Factor         | Insight                                                                 |
|----------------|-------------------------------------------------------------------------|
| **Season**     | Summer (season 3) has the highest rentals; winter (season 1) the lowest |
| **Working Days** | Rentals significantly higher on working days (via t-test)              |
| **User Types** | Registered users dominate weekdays; casuals peak on weekends            |
| **Hourly Use** | Morning (7–9 AM) and evening (4–7 PM) peaks for commuters               |
| **Weather**    | Rentals drop in bad weather, high humidity, and low temperature         |
| **Temperature**| Positively correlated with rentals                                       |

---

## 📦 How to Run

1. Open `GoBike_Rent_Analysis.ipynb` in Jupyter Notebook
2. Ensure `GoBike_sharing_dataset.csv` is in the same directory
3. Run all cells to generate plots and perform analysis

---

## 📚 Dependencies

Install via pip:
```bash
pip install pandas matplotlib seaborn scipy

