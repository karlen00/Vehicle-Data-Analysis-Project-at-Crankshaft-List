# README

## Vehicle Data Analysis Project at Crankshaft List

### Project Description

This project aims to analyze vehicle advertisement data displayed on the Crankshaft List website. We will study the factors that affect vehicle prices based on data collected over several years. This analysis will include data inspection, preprocessing, feature calculation, and data exploration.

### Project Steps

#### Step 1: Load and Understand the Data
1. Read the data file from the path: `/datasets/vehicles_us.csv`.
2. Examine the general information of the dataset, including size and initial description of the data.

#### Step 2: Data Preprocessing
1. **Check and Fill Missing Values:**
   - Identify columns with missing values.
   - Fill in missing values based on logical assumptions (e.g., if the Boolean column `is_4wd` only contains `True` values, assume missing values are `False`).
   - Explain potential causes of missing values.

2. **Change Data Types:**
   - Identify columns that need their data types changed (e.g., `date_posted` to datetime).
   - Change data types as needed and explain the reasons behind these changes.

#### Step 3: Calculate Additional Features
1. Add new columns to the table:
   - Day of the week, month, and year the ad was posted (`day_of_week`, `month`, `year`).
   - Vehicle age when the ad was posted (`vehicle_age`).
   - Average vehicle mileage per year (`mileage_per_year`).

2. Convert the `condition` column to a numerical scale:
   - new = 5
   - like new = 4
   - excellent = 3
   - good = 2
   - fair = 1
   - salvage = 0

#### Step 4: Exploratory Data Analysis
1. **Study Parameters:**
   - Price (`price`), vehicle age (`vehicle_age`), mileage (`odometer`), number of cylinders (`cylinders`), and condition (`condition`).
   - Create histograms for each parameter and analyze how outliers affect the histogram shapes.

2. **Handle Outliers:**
   - Determine the upper limit of outliers and remove them from the data.
   - Save outliers in a separate DataFrame.
   - Create new histograms without outliers and compare them with the previous histograms.

3. **Analyze Ad Duration:**
   - Create a histogram for `days_listed`.
   - Calculate the mean and median duration of ads being listed.
   - Determine when ads are removed quickly and when they are listed for a very long time.

4. **Vehicle Type Analysis:**
   - Calculate the number of ads and average price for each vehicle type.
   - Create a graph showing the dependency of ad numbers on vehicle types.
   - Select the two vehicle types with the highest number of ads.

5. **Factors Affecting Vehicle Price:**
   - Study the relationship between price and age, mileage, condition, transmission type, and color for popular vehicle types.
   - Create boxplots for categorical variables (transmission type and color).
   - Create scatterplots for other variables.

#### Step 5: Conclusion
1. Write a comprehensive conclusion based on the analysis conducted.
2. Format the conclusion clearly and structured in the Jupyter Notebook.

### Data Description

The dataset used in this project contains the following columns:
- `price`: Vehicle price.
- `model_year`: Vehicle model year.
- `model`: Vehicle model.
- `condition`: Vehicle condition (new, like new, excellent, good, fair, salvage).
- `cylinders`: Number of engine cylinders.
- `fuel`: Type of fuel (gas, diesel, etc.).
- `odometer`: Vehicle mileage when the ad was posted.
- `transmission`: Type of vehicle transmission.
- `paint_color`: Vehicle paint color.
- `is_4wd`: Whether the vehicle has 4-wheel drive (Boolean).
- `date_posted`: Date the ad was posted.
- `days_listed`: Number of days the ad was listed until removed.

### Closing

This project is organized in a Jupyter Notebook with code placed in code cells and explanations in markdown cells. Each step is explained in detail to ensure thorough and structured analysis.
