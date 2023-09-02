# Unicorn-data-analysis
## Project Description
This project focuses on analyzing unicorn companies with a valuation over $1 billion as of March 2022. The analysis aims to guide companies and investors toward better decision-making by focusing on high-growth potential, investment diversification, and strategic partnerships.

## Project Steps
1. Data Cleaning: Removed duplicates, handled missing values, and converted data types where necessary.
2. Exploratory Data Analysis: Conducted univariate, bivariate, and multivariate analyses to derive insights from the data.
3. Data Visualization: Utilized Python libraries like Matplotlib and Seaborn to visualize key trends and insights.
4. Recommendations: Provided strategic recommendations based on the analysis.
5. observation: provided observations that explains the trends and insights gotten from the analysis
## Challenges and Solutions
- **Challenge 1**:Data Type Conversion for 'Valuation' 'Funding 'and 'date joined' Column:
  Initially, I attempted to convert the 'Valuation' and 'Funding' column to a numerical data type for calculations. However, this process was complicated by the presence of dollar signs in the column, making the standard string-to-float conversion methods unworkable.
-** Solutions:To enable calculations, I converted the 'M' and 'B' to their numerical equivalents (multiplying by 1,000,000 for 'm' and 1,000,000,000 for 'b'), and replaced the dollar signs with an empty space" ", then finally converting the entire column from an integer to a float type to enable me perform further analysis.
 .Converted the 'Date' column from object data type to datetime to better work with time-series data.


- **Challenge 2**: Dealing with Missing Values
  - **Description**: One of the significant challenges I faced while cleaning the dataset was handling missing values in certain columns like 'city'.
  
- **Solution 2 **: Assign a Unique Category
  - **Description**: To tackle this issue, I  decided to leave the missing rows in the city column because i 
have a fairly large dataset (1073 rows) and only 16 rows have missing 'city' values, the impact of leaving them as it is  will likely be minimal in the grand scope of things and 
the 'city' column is not that crucial for this analysis and  the other columns in those 16 rows hold valuable information that i  don't want to lose, then leaving them as they are , is a reasonable approach.


- **Challenge 3**: ROI Calculation with Zero 'Funding' Values
  - **Problem**: The 'Funding' column had some rows containing zero values, making the ROI (Return on Investment) calculation problematic because division by zero resulted in infinite (`inf`) values.
  - **Solution**: I used conditional logic to replace ROI values with `NaN` (Not a Number) where the 'Funding' was zero. This way, the ROI could be computed accurately for the rows where 'Funding' was non-zero.

## ...

  
