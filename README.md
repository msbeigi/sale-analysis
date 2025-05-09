### Report:

**Data Overview:**
- bakery sale data is between ‘01-01-2021’ and ‘09-30-2022’.
-	weather dataset is between 01-01-2021and 10-31-2022.


**Data Cleaning:**

**Handling Missing Values:**
- In the weather dataset removed columns that were almost empty and with no data ('tsun' and 'snow').
-	Imputed missing values using iterative imputation with a RandomForestRegressor for wind direction, speed, gust, and pressure.

**Anomaly Removal:**
- From the bakery dataset rows with non-informative entries ('.') in the Article column were removed.
-	Rows with zero or negative quantities and unit prices were also filtered out.

**Feature Engineering:**
- Added features in the weather dataset such as 'is_rainy’, ‘temp_range', 'is_hot_day', 'is_heavy_wind', 'is_high_pressure', 'day_of_week', and 'day_name'.
-	Feature selection based on correlation analysis (Pearson) and feature importance from two models helped identify key features for forecasting.
.

**Modeling:**
- Achieved Mean Absolute Error (MAE) of approximately 97 units.
- Recommendations for enhancing predictions include integrating more features, optimizing model hyperparameters, and exploring advanced ensemble techniques.

**Visualization:**

- **Top Sales Days:** Weekends or holidays hosted the top 10 highest sales days, mainly on Sundays. Notably, on August 14, 2022, despite moderate rain (7.6 mm) and wind (12.4 km/h), the bakery sold 1970.0 items. Following a holiday, weather had minimal impact on sales, with moderate wind speeds being typical on high sales days, e.g., July 16, 2022, recording €1,535 in sales and 30.0°C.
  <img src="https://github.com/msbeigi/sale-analysis/blob/main/img/Total%20Quantity%20sold.jpg" alt="Image Alt Text" width="700"/>
  
- **Product Preferences:** Key products like TRADITIONAL BAGUETTE, with 118,093 units sold, underscored customer preferences. Specialized items such as CEREAL BAGUETTE and SPECIAL BREAD also featured in the top 10, suggesting a niche market.

<img src="https://github.com/msbeigi/sale-analysis/raw/main/img/Best%20Seller%20Items.jpg" alt="Image Alt Text" width="500"/>

- **Weekly Sales Trends:** Sundays stood out with an average sale of 919.71 units, contrasting with weekdays (480.89 units on Tuesday to 545.55 units on Monday). Holidays, particularly Mondays like August 15, 2022, showed deviations from typical weekday trends.
<img src="https://github.com/msbeigi/sale-analysis/raw/main/img/Total%20Quantity%20sold%20by%20day%20week.jpg" alt="Image Alt Text" width="400"/>

