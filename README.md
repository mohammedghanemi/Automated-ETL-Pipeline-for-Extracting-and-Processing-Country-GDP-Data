# Global-Country-Intelligence-Dashboard

This project aims to collect and process global country information using a public API, followed by cleaning and transforming the data to prepare it for further use. The primary goal is to gather data on various aspects of countries such as population, languages, currencies, and more, then clean and transform this data to make it usable for analytical or database purposes.

## Overview

### 1. **Data Collection**

The data is collected using the **RESTCountries API**, a free API that provides comprehensive information about all countries. This API includes details such as:

- Country name
- Population
- Languages
- Currencies
- Region and subregion
- Flag images

No authentication or API keys are required to access the RESTCountries API, making it easy to collect data from all countries worldwide.

### 2. **Data Cleaning & Transformation**

Once the data is collected, it's processed using **Python** and the **Pandas** library. This step involves:

- **Cleaning the Data**:
  - Removing or handling missing values.
  - Ensuring consistency and correcting any anomalies in the data.

- **Data Transformation**:
  - Converting categorical data into a usable format.
  - Ensuring that all values are in the correct units or formats (e.g., transforming population data to integers, fixing date formats).

- **Preparation for Database Insertion**:
  - The transformed data is saved as a `.csv` file and prepared for storage in a relational database, making it ready for use in further analysis.

### Final Output

After the cleaning and transformation steps, the final dataset is saved as `countries_cleaned.csv`.

## Files Included:

- **countries_raw.csv**: Contains the initial data collected from the RESTCountries API.
- **countries_cleaned.csv**: The cleaned and transformed data ready for storage or further analysis.
- **data_colle_clean_transfo.ipynb**: Jupyter notebook that includes the code for data collection, cleaning, and transformation.
