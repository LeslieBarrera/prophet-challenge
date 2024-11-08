# MercadoLibre Growth Analysis with Time Series Forecasting

## Project Overview
This project aims to analyze and forecast patterns in Google search traffic data for MercadoLibre, the most popular e-commerce site in Latin America. The analysis explores how search traffic correlates with stock prices and identifies trends that could be leveraged for strategic growth. Additionally, the project uses the Prophet model to forecast future search traffic trends.

## Project Steps

### 1. Data Preparation and Initial Analysis
- **Read and visualize the search traffic data**: The data for Google search trends was loaded, cleaned, and visualized to identify any unusual patterns or correlations with corporate financial events.
- **Key finding**: The search traffic in May 2020, when MercadoLibre released its quarterly financial results, was notably higher than the monthly median.

### 2. Mining Search Traffic for Seasonality
- **Hourly, daily, and weekly analysis**: The search data was grouped by hour, day of the week, and week of the year to identify patterns and peaks.
- **Insights**:
  - **Hourly**: Search traffic peaks in the afternoon and evening.
  - **Daily**: Higher search traffic is observed mid-week (e.g., Wednesday or Thursday).
  - **Weekly**: An increase in search traffic is noted during weeks leading up to holidays.

### 3. Correlation with Stock Price Patterns
- **Stock data analysis**: The stock price data was combined with search traffic data to investigate correlations between search traffic, stock volatility, and stock returns.
- **Key columns added**:
  - `Lagged Search Trends`: Shifts search trends data by one hour.
  - `Stock Volatility`: A four-hour rolling standard deviation of stock returns.
  - `Hourly Stock Return`: The percent change of the stock price on an hourly basis.
- **Finding**: The correlation between lagged search traffic and stock volatility or returns was weak, suggesting no strong predictive relationship.

### 4. Time Series Modeling with Prophet
- **Model setup and training**: The search traffic data was prepared and trained using the Prophet forecasting model.
- **Forecast analysis**:
  - The model predicted future trends over 2000 hours (approximately 80 days).
  - Visualizations included a forecast plot with confidence intervals and time series component plots.
- **Insights**:
  - **Daily seasonality**: Popular hours for search traffic were observed.
  - **Weekly seasonality**: The most active days of the week were identified.
  - **Yearly seasonality**: Seasonal dips in search traffic were noted during specific times of the year.

## Key Questions Answered
1. **What time of day exhibits the greatest popularity?**
   - Afternoon to early evening hours typically exhibit the greatest search traffic.

2. **Which day of the week gets the most search traffic?**
   - Mid-week days, such as Wednesday or Thursday, show the highest search traffic.

3. **What's the lowest point for search traffic in the calendar year?**
   - The lowest points often occur during major holidays or specific off-peak periods.

## Tools and Libraries Used
- **Python Libraries**:
  - `pandas` for data manipulation
  - `matplotlib` and `seaborn` for data visualization
  - `prophet` for time series forecasting
- **Environment**:
  - Jupyter Notebook or Google Colab for code execution

## Conclusion
This analysis provided insights into the seasonality and trends of MercadoLibre's search traffic, with forecasts that can inform strategic decision-making. While search traffic showed only a weak correlation with stock price volatility and returns, understanding peak times and seasonal dips can help optimize marketing efforts and anticipate changes in user behavior.

## How to Run the Code
1. Ensure you have Python and the required libraries installed (`pandas`, `matplotlib`, `prophet`).
2. Run the code cells step-by-step in a Jupyter Notebook or Google Colab.
3. View the plots and outputs for each section to understand the analysis and findings.

## Future Improvements
- Extend the analysis to include more data points or variables, such as economic indicators.
- Explore machine learning models for enhanced predictive capabilities beyond the Prophet model.
