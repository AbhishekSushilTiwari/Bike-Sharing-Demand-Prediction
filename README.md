**Bike_Sharing_Demand_Prediction**

I worked with the Seoul Bike Sharing dataset, covering the period from December 2017 to November 2018. The dataset includes details on various environmental factors such as temperature, dew point temperature, humidity, visibility, solar radiation, rainfall, and snowfall. It also contains information about the type of day, including whether it was a functional day or a public holiday.

My work focused on three key areas:

1. I conducted exploratory data analysis (EDA) to extract meaningful insights from the dataset.
2. I explored the relationships between bike demand and environmental variables.
3. Most importantly, I developed a machine learning model to predict bike demand at specific hours, using the day’s attributes as input.

**Problem Statement**

The dataset is of Seoul's public bike rental service called "Ttareungi," also known as Seoul Bike. It has become one of the capital city's most popular public transport systems by being used more than 100 million times since the service was launched in December 2015, as reported in early 2022. The popularity however has posed the challenge of keeping the bikes available as and when the demand for them rises.

So our goal is to identify the variables that have a say in the demand of the bikes and then build a model that helps predict the demands as and when the climatic conditions change.

**Dataset**
Date : Date of the rental agreement

Rented Bike Count : Number of bikes rented

Hour : Hour of the day

Temperature(°C) : Temperature

Humidity(%) : Humidity measure

Wind speed(m/s) : Wind speed

Visibility (10m) : Visibility measure

Dew point temperature(°C) : Dew point temperature measure

Solar Radiation (MJ/m2) : Solar Radiation measure

Rainfall(mm) : Rainfall in mm

Snowfall(cm) : Snowfall measure

Seasons : Season

Holiday : Whether a holiday or not

Functioning Day : Whether a functional day or not

**Data Cleaning and Wrangling**

At first glance, the dataset appears much cleaner than most datasets I typically work with. It has no missing or duplicate values.

The dataset contains 8,760 data points, with 13 independent variables and one dependent variable, which is the "Rented Bike Count."

Most of the variables are numerical, with only four of the 14 being of object datatype.

I converted the "Date" column from an object datatype to a Datetime datatype. Additionally, I added new columns for the "Month" and "Day" to represent the month and the day of the week, as they could be helpful during the exploratory data analysis (EDA) process.

**EDA Process**

I conducted a thorough analysis of the dataset using various visualizations such as heatmaps, bar plots, scatter plots, line plots, and pie charts. These were employed to perform univariate, bivariate, and multivariate analyses. For the detailed insights and findings, please refer to the presentation.

**Predictive Model**

I developed a predictive model that achieved an R² score of 0.94. The model is CatBoost Regression algorithm, with hyperparameters optimized through the GridSearchCV cross-validation technique.

For a detailed explanation of the process and results, I recommend reviewing the project notebook or the final presentation.


**Deployment**

I deployed the project using Gradio, creating an interactive web interface where users can input environmental attributes and receive predicted bike demand for a specific hour. This allows for easy testing and visualization of the model’s predictions in real-time. For more details, refer to the deployed app or the project documentation.
