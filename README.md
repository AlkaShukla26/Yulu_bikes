# Yulu Bike Sharing – Data Science Case Study

## 📌 Project Overview
This project analyzes **Yulu bike rental demand** (10,886 records, 12 features) to understand how **time, weather, seasonality, and working patterns** influence user behavior. Using **EDA, hypothesis testing, and statistical modeling**, the goal was to extract insights and provide actionable recommendations for business decisions.

---

## 🔍 Key Insights

### Data Profiling & EDA
- Dataset was **clean (no missing/duplicate values)**, ready for analysis.  
- **Temp vs. Atemp** showed near-perfect correlation → dropped *atemp* to avoid multicollinearity.  
- **Count = Casual + Registered** → retained only *count* as target to prevent redundancy.  
- **Outliers** in rental counts reflect **real-world demand surges** (e.g., festivals/events), so were retained.  

### Statistical Findings
- **Weekday vs. Weekend Demand**:  
  - Welch’s t-test (p = 0.0085) and Mann-Whitney U test (p = 0.0423) both confirm **weekend rentals > weekday rentals**.  
- **Holiday vs. Regular Days**:  
  - No significant difference (Levene’s p = 0.0604, variances equal).  
- **Weather Impact**:  
  - ANOVA/Kruskal-Wallis show demand drops in bad weather (rain, mist).  
- **Seasonal Variation**:  
  - Rentals fluctuate significantly with seasons (higher in summer/autumn, lower in winter/monsoon).  
- **Chi-Square Test**: Weather types are **dependent on season**, reinforcing seasonal-weather interplay.

---

## 🎯 Recommendations
- **Weekday Commuters**: Increase bike availability during office commute hours; launch commuter-focused passes.  
- **Seasonal Inventory Management**: Reallocate bikes using **seasonal demand forecasting** (more in summer/spring, fewer in monsoon/winter).  
- **Weather-Aware Operations**: Integrate weather forecasts into planning; notify users about availability & safety during rain/mist.  
- **Data Modeling Best Practices**: Drop redundant features (atemp, casual, registered) for cleaner predictive models.  
- **Event-Driven Demand Spikes**: Treat outliers as opportunities — deploy temporary surges near **festivals, marathons, and rallies**.  

---

## 🛠️ Tools & Techniques
- **Python (Pandas, NumPy, Matplotlib, Seaborn)** – Data cleaning, visualization, statistical analysis.  
- **Hypothesis Testing** – Levene’s Test, Shapiro-Wilk, Welch’s t-test, Mann-Whitney U, ANOVA, Chi-Square.  
- **EDA Methods** – Scatter plots, correlation analysis, boxplots, group statistics.  

---

