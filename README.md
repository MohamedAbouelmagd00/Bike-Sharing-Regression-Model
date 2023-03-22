# Bike Sharing Regression Model

## Project Outline

This notebook explains how we can go about explore and prepare data for model building.The notebook is structured in the following way

- About Dataset
- Data Summary
- Feature Engineering
- Missing Value Analysis
- Outlier Analysis
- Correlation Analysis
- Visualizing Distribution Of Data
- Visualizing Count Vs (Month,Season,Hour,Weekday,Usertype)
- Filling 0's In Windspeed Using Random Forest
- Linear Regression Model
- Regularization Models
- Ensemble Models

## About Data Set

### Link On Kaggle

[Bike Sharing Demand](https://www.kaggle.com/competitions/bike-sharing-demand/overview)

### **Overview**

Bike sharing systems are a means of renting bicycles where the process of obtaining membership, rental, and bike return is automated via a network of kiosk locations throughout a city. Using these systems, people are able rent a bike from a one location and return it to a different place on an as-needed basis. Currently, there are over 500 bike-sharing programs around the world.

### **Data Fields**

- datetime - hourly date + timestamp
- season - 1 = spring, 2 = summer, 3 = fall, 4 = winter
- holiday - whether the day is considered a holiday
- workingday - whether the day is neither a weekend nor holiday
- weather -
    - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
    - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp - temperature in Celsius
- atemp - "feels like" temperature in Celsius
- humidity - relative humidity
- windspeed - wind speed
- casual - number of non-registered user rentals initiated
- registered - number of registered user rentals initiated
- count - number of total rentals (Dependent Variable)

## Project Steps

### Libraries Used

1. **NumPy**
    - NumPy is used for numerical computing and is widely used in machine learning projects for numerical operations and data manipulation.
2. **Pandas** 
    - Pandas is used for data manipulation and analysis. It is widely used in machine learning projects for data preprocessing, cleaning, and transformation.
3. **Matplotlib**
    - Matplotlib is a plotting library used for data visualization. It is widely used in machine learning projects for visualizing data.
4. **Seaborn**
    - Seaborn is a data visualization library based on Matplotlib. It is used for creating more complex visualizations and is widely used in machine learning projects.
5. **PyLab**
    - PyLab is a module in Matplotlib that provides a more convenient interface for Matplotlib.
6. **Calendar**
    - Calendar is a module in Python that provides functions to work with calendars.
7. **SciPy**
    - SciPy is a library used for scientific computing and technical computing. It is widely used in machine learning projects for statistical analysis and optimization.
8. **Missingno**
    - Missingno is a library used for visualizing missing data. It is widely used in machine learning projects for data cleaning.
9. **Datetime**
    - Datetime is a module in Python that provides classes for working with dates and times.

### Importing the Data Set

1. Importing the ‘train.csv’ data using pandas function read_csv()
2. copy the data into new DataFrame to work on using .copy()

### Data Exploration

1. Getting the size of the dataset.
2. Getting summary statistics of the data.
3. Getting the data info to know the datatype, the non-null counts for each feature.
4. Counting Unique values for each column.
5. Checking for nulls and visualizing missing values using matrix.
6. visualizing the Features distribution.
7. Checking for outliers using ******histograms and box plots******
8. Getting the correlation between variables and visualizing it using heatmap to make feature selection.
9. Exploring features with time to get trends.

### Data Preprocessing

1. Feature Engineering of the [‘datetime’] column into [ ‘date’, ‘hour’, ‘weekday’, ‘month’, ‘season’, ‘weather’ ]
2. Changing the datatype of "season", "weather", "holiday", "workingday" into "category" datatype
3. Handling outliers by removing 3 standard deviations above and below.
4. **RandomForestRegressor** Algorithm to predict the missing values in the ‘windspeed’ column.

### Machine learning Model

1. Loading the test data using the same way we loaded the train data before.
2. Perform the same preprocessing on the test data.
3. Splitting data into train and test data
4. The Feature we want to predict is the **[‘count’]**
5. The features are used to predict with are [‘**season’, ‘holiday’, ‘workingday’, ‘weather’, ‘temp’, ‘atemp’, ‘humidity’, ‘windspeed’, ‘hour’, ‘year’, ‘weekday’, ‘month’]**
6. building RMSLE Scorer
7. Building Linear Regression Model
8. Regression Model Using Lasso
9. Buiding RandomForestRegressor Model

### Models Results

- `RMSLE Value For Linear Regression:  0.9779716848523355`
- `RMSLE Value For Ridge Regression:  0.977971669783334`
    - `{'alpha': 0.1, 'max_iter': 3000}`
- `RMSLE Value For Lasso Regression:  0.9781087413435852`
    - `{'alpha': 0.005, 'max_iter': 3000}`
- `RMSLE Value For Random Forest:  0.10126804895110852`
    - `relation_square :  0.9941188130079771`

# Contact Info

mohamedabouelmagd00@gmail.com

[](https://www.linkedin.com/in/mohamed-abouelmagd/)

[Mohamed Abou-Elmagd | LinkedIn](https://www.linkedin.com/in/mohamed-abouelmagd/)