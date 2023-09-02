# Phase4_project
# Overview
This project involves building a time series model using Zillow data to aid real estate investors in making informed investment decisions.
The dataset comprises property information, and the project encompasses:
* Data preprocessing,
* Time series transformation,
* Exploratory data analysis,
* Model selection,
* Training
* Evaluation.

Recommendations on where to invest will be provided based on these predictions and supplemented with additional insights from EDA.
The project also includes documentation, deployment, maintenance, and a feedback loop to continuously enhance the model's accuracy and relevance to real estate investment needs.

![download](https://github.com/WatiriVivian/Phase4_project/assets/118829983/dbad7ca6-54ad-42c8-a62b-1c8e8026fda5)


# Business Understanding
This project aims to significantly enhance business understanding for real estate investors by leveraging time series analysis of *Zillow data*. 
It will provide investors with historical property *price trends, helping them make data-driven investment decisions, manage risks, identify promising locations, and access forecasts through a user-friendly interface*. 

The project's continuous improvement approach, including a feedback loop and regular updates, ensures that investors stay well-informed in a dynamic real estate market, ultimately empowering them to optimize their investments and improve their overall understanding of the industry.

# Project Objective
The project's main objective is to develop a time series forecasting model using **Zillow data** to assist real estate investors in making informed decisions about where to invest their capital. 
This model will provide predictions and insights into property price trends, helping investors identify regions and cities with potential for price appreciation. Ultimately, the project aims to empower investors with data-driven tools that enhance their understanding of real estate market dynamics, enabling them to make more strategic and profitable investment choices.
**The key question is: What are the top 5 best zip codes for us to invest in**

# Data Understanding and Preparation
### For data understanding:
This dataset contains information about median housing sales values for various zip codes over a span of *22 years, from April 1996 to April 2018*.

* There are 272 columns
* 14723 rows indexed from 0 to 14722.
* RegionID: Is a unique index for each region (zip code) ranging from 58196 to 753844
* RegionName: Is a unique zip code for each region, ranging from 1001 to 99901

219 columns are float data type
49 columns are integer data types.
4 columns are object data types.
There are 220 columns with missing values. 

### preparation:
1. We began by thoroughly exploring the Zillow dataset
2. Checking for missing values, and addressing outliers
3. Transforming the dataset into a time series format, with 'RegionName' representing unique properties or regions and 'Date' as the time dimension.
4. Filtering for the top 5 zip codes using ROI that is calculated using ROI
   *Net income / Cost of investment x 100.*
5. Also transforming the data from *wide-form* to *long-form*
6.  Calculate relevant time-based features, such as moving averages or seasonality patterns, to capture temporal trends.
7.   Additionally, splitting the data into training and testing sets, and reserving the most recent data for validation. This will create a clean, structured dataset for time series modeling and forecasting.

# EDA
The median (50th percentile) size rank is approximately 46106, indicating the middle-sized zip code in the dataset.
**The median housing sales value across all zip codes ranges from around USD11,300 to USD 3,849,600.**
The mean (average) housing sales value across all zip codes ranges from approximately *USD 118,299 to USD 288,039*.
![download](https://github.com/WatiriVivian/Phase4_project/assets/118829983/1da11bcd-eb9b-4ae0-8f49-e47c76b62dc3)
The District of Columbia (DC) leads with the highest average of Annualized ROI. There is a noticeable variance in average ROI across states, with some states having ROIs above 5% and others below 3%.

![download](https://github.com/WatiriVivian/Phase4_project/assets/118829983/0549dc3b-9788-46c7-8cc8-283b27d76148)

A visualisation of the 5 ROI that we chose

# Modelling, Forecasting, and Conclusion
The exploration of the Zillow dataset through time series modeling revealed valuable insights into housing price trends and seasonality. Utilizing SARIMA, the project effectively captured data patterns, generating accurate forecasts.

Key Takeaways:

* Decomposition: Data decomposition highlighted patterns in seasonality, trend, and residual components, forming the basis for robust forecasting models.

* Model Performance: Low Mean Squared Error (MSE) values, such as 1.5479, 1.7155, and 2.0511, demonstrated the SARIMA model's effectiveness in comparison to test data.

* Forecasting: The model's predictions and confidence intervals provided investors with future insights, facilitating an understanding of market dynamics.

In Conclusion, the SARIMA-driven exploration of the Zillow dataset empowered decision-making in the housing market. Insights, supported by performance metrics, highlight the potential of data-driven methodologies for strategic choices.


# Recommendations

Diversify Investments: To manage risk and capture market dynamics, diversify your portfolio across analyzed states like Oyster Bay, Freedom, Winfield, Cincinnatus, and Schaghticoke.

Explore Oyster Bay: With ample data, Oyster Bay offers stability, making it a viable investment option.

Prioritize ROI: Focus on cities with higher Return on Investment (ROI) figures for lucrative opportunities.

Evaluate Risk: Assess risk using the Coefficient of Variation (CV). Lower CV values, e.g., Winfield, indicate stable investments.

Consider Location: Factor in city attributes, growth potential, amenities, and demand when making investment choices.

In summary, diversification, ROI emphasis, risk evaluation, and location considerations are key in USA real estate investment decisions.

# Conclusion

Based on our model assumptions, the selected zipcode will continue to experience an
anualised ROI of about 14% which should lead in singnificant growth in their investments
• Therefore it will be prudent to consider investing in any these 5 zipcodes
1. 11211 – New York Kings
2. 11222 – New York Kings
3. 11216 – New York Kings
4. 7302 – Jersy City Hudson
5. 11215 – New York Kings