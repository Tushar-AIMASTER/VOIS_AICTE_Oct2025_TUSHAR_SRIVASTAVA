# VOIS Project1: Airbnb Data Analysis

## Author
Tushar Srivastava

## Project Overview
This project conducts an in-depth exploratory data analysis (EDA) on Airbnb open data to gain insights into the rental market dynamics in New York City. By analyzing various aspects such as property types, neighbourhood distributions, pricing trends, host performance, and review patterns, the project aims to uncover key trends and relationships within the Airbnb ecosystem. The analysis is performed using Python in a Jupyter notebook environment, leveraging libraries like Pandas, NumPy, Matplotlib, and Seaborn for data manipulation, statistical analysis, and visualization.

## Objectives
The primary objectives of this project are:
- To explore the distribution of different property types (room types) in the dataset.
- To identify neighbourhood groups with the highest number of listings and average prices.
- To investigate relationships between property attributes (e.g., construction year and price, price and service fee).
- To analyze host performance, including top hosts by listings count, impact of identity verification on reviews, and correlation between listings count and availability.
- To examine review rate variations across neighbourhood groups and room types.
- To provide visual insights through charts and plots for better understanding of the data.

## Dataset
- **Source**: Airbnb Open Data (Excel file: `1730285881-Airbnb_Open_Data.xlsx`)
- **Description**: The dataset contains information on Airbnb listings, including details like host information, property type, location, pricing, reviews, availability, and more.
- **Initial Shape**: [Rows: 102599, Columns: 26] (before cleaning)
- **Key Columns**: id, name, host_id, host_identity_verified, host_name, neighbourhood_group, neighbourhood, lat, long, country, country_code, instant_bookable, cancellation_policy, room_type, construction_year, price, service_fee, minimum_nights, number_of_reviews, last_review, reviews_per_month, review_rate_number, calculated_host_listings_count, availability_365.

## Methodology
1. **Data Loading**: Import the dataset using Pandas.
2. **Initial Exploration**: Examine dataset structure, shape, columns, and basic statistics.
3. **Data Cleaning**:
   - Remove duplicate entries.
   - Handle missing values: Drop columns with excessive nulls (e.g., 'license', 'house_rules'), and remove rows with remaining nulls.
   - Data type conversions: Convert price and service_fee to float, id and host_id to string, last_review to datetime, construction_year to int.
   - Fix data inconsistencies: Correct typos (e.g., 'Brookln' to 'Brooklyn').
   - Outlier removal: Drop listings with availability_365 > 500.
4. **Exploratory Data Analysis (EDA)**:
   - Generate descriptive statistics.
   - Perform groupby operations and aggregations.
   - Create visualizations: Bar plots, regression plots, box plots, etc.
   - Calculate correlations and means.
5. **Key Analyses**:
   - Property type distribution.
   - Neighbourhood group listings and average prices.
   - Construction year vs. average price.
   - Top 10 hosts by calculated host listings count.
   - Host verification vs. review rates.
   - Price vs. service fee correlation.
   - Average review rates by neighbourhood and room type.
   - Host listings count vs. availability.

## Key Findings
- **Property Types**: The dataset primarily consists of 'Entire home/apt' (around 50,000+ listings), followed by 'Private room' and 'Shared room'. 'Hotel room' is the least common.
- **Neighbourhood Groups**: Manhattan and Brooklyn have the highest number of listings (over 20,000 each), followed by Queens, Bronx, and Staten Island.
- **Average Prices**: Queens has the highest average price (~$170), while Bronx has the lowest (~$120). Manhattan and Brooklyn are around $150-160.
- **Construction Year vs. Price**: There is a general upward trend in average prices for newer properties, though not strictly linear.
- **Top Hosts**: The top hosts by listings count include names like [specific names from data, e.g., those with counts over 100,000], indicating professional hosts managing multiple properties.
- **Host Verification**: Verified hosts have a slightly higher average review rate (~3.5) compared to unverified (~3.4), suggesting a positive impact of verification.
- **Price and Service Fee**: Strong positive correlation (close to 1), indicating service fees are proportional to listing prices.
- **Review Rates**: Average review rates vary by neighbourhood (e.g., Staten Island highest at ~3.6) and room type (e.g., 'Entire home/apt' around 3.5). Visualized via bar plots and box plots.
- **Listings Count and Availability**: Positive correlation (~0.18), meaning hosts with more listings tend to have higher annual availability, possibly due to professional management.

## Visualizations
The project includes several visualizations saved as images (graph1.png, graph2.png, graph3.png) and generated in the notebook:
- Bar charts for property types, neighbourhood listings, average prices, top hosts, and review rates.
- Regression plots for construction year vs. price, price vs. service fee, and listings count vs. availability.
- Box plots for verification status vs. review rates.

## Tools and Libraries
- **Python**: Core language.
- **Jupyter Notebook**: For interactive analysis.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical operations.
- **Matplotlib**: Plotting and visualization.
- **Seaborn**: Statistical data visualization.

## Conclusion
This analysis provides valuable insights into the Airbnb market in NYC, highlighting trends in pricing, host behavior, and customer preferences. Neighbourhoods like Manhattan and Brooklyn dominate in listings, while Queens leads in average prices. Host verification and professional management appear to correlate with better reviews and higher availability. The strong link between price and service fee underscores the platform's fee structure. Future work could involve predictive modeling for pricing or sentiment analysis on reviews.

## How to Run
1. Ensure Python and required libraries are installed (use `pip install pandas numpy matplotlib seaborn`).
2. Open `TUSHAR_SRIVASTAVA.ipynb` in Jupyter Notebook.
3. Run cells sequentially to reproduce the analysis.

## Files in Project
- `TUSHAR_SRIVASTAVA.ipynb`: Main analysis notebook.
- `1730285881-Airbnb_Open_Data.xlsx`: Dataset.
- `graph1.png`, `graph2.png`, `graph3.png`: Sample visualizations.
- `README.md`: This project description.
