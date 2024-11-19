**Data Transformation Assignment: KNMI Weather Data Analysis**

**Objective**  
In this assignment, we’ll analyze KNMI weather data (average temperatures from 1901–2016) to investigate if there is visually compelling evidence of climate change in the form of increasing temperatures in the Netherlands.

**Instructions**

### 1. Setup
- **Download the Data**: Obtain the KNMI data here.
- **Jupyter Notebook**: Create a Jupyter Notebook named `transformation_KNMI.ipynb`.

### 2. Loading the Data
- **Read the Files**: Load each data file using `pandas.read_csv()`.
- **Merge DataFrames**: Use `pd.concat()` to merge all data into a single DataFrame.
- **Initial Inspection**: Print the combined DataFrame and ensure that it appears correct.
- **Identify Formatting Issues**: Try accessing individual columns to check for errors. Open one of the files in a text editor to identify formatting inconsistencies. Adjust `read_csv` optional arguments as needed to resolve any formatting issues.

### 3. Basic Plotting and Trend Analysis
- **Plotting**: Use `matplotlib.pyplot` to plot the years on the x-axis and temperatures on the y-axis.
- **Trendline Fitting**: 
  - Import the Linear Regression model: `from sklearn.linear_model import LinearRegression`.
  - Create an instance of the model: `model = LinearRegression()`.
  - Fit the model using `model.fit(X, y)`, where `X` represents the years and `y` represents the temperatures. Note that `X` will need to be reshaped to a 2D array using `.to_numpy().reshape(-1, 1)`.
  - Predict the trend using `model.predict(X)` and add the trendline to the DataFrame as a new column.
- **Plot Trendline**: Modify the original plot to include this fitted trendline, labeling both lines accordingly.

### 4. Seasonal Analysis: Plotting Monthly Trends
- **Select Specific Months**: Use Boolean indexing to filter data for June, July, and August.
- **Separate Plots for Each Month**: For each month:
  - Plot both the temperature data and its respective fitted trendline.
  - Refactor your code into reusable functions to avoid repetitive code.
- **Handling SettingWithCopyWarning**: You may encounter a `SettingWithCopyWarning`. Refer to [this blog post](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#why-does-assignment-fail-when-using-chained-indexing) for insights on why this occurs and how to handle it.

### 5. Smoothing by Averaging Across Time Periods
- **Annual Averages**: Use `groupby()` to calculate average temperatures for each year, then plot these averages along with the fitted trendline.

- **Decadal Averages**: Further smooth the trend by calculating decadal averages using `groupby()`, and plot the resulting data with the trendline. This will help in identifying long-term patterns more clearly.
