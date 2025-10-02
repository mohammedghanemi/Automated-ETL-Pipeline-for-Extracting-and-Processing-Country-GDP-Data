# ETL Project: Countries by GDP Extraction and Database Loading

## Project Overview
This project implements a **complete ETL (Extract, Transform, Load) pipeline** to automatically extract, process, and store GDP data of countries from the International Monetary Fund (IMF) website. The pipeline is designed for automation, enabling the organization to update GDP data twice a year as published by IMF.

The project is developed as part of a junior Data Engineer assignment, using **Python** and relevant data processing libraries.

---

## Project Objectives
- Extract country-wise GDP data from IMF website.
- Transform the data to clean it and round GDP values to **2 decimal places**.
- Load the transformed data into:
  - A **JSON file** (`Countries_by_GDP.json`)
  - A **SQLite database** table (`Countries_by_GDP`) in `World_Economies.db`
- Log the entire ETL process in `etl_project_log.txt`.
- Demonstrate querying the database for countries with **GDP greater than 100 billion USD**.

---

## Features
- Web scraping using `requests` and `BeautifulSoup`.
- Data cleaning and transformation using Python built-in functions.
- JSON and SQLite database integration.
- Logging of ETL steps with timestamps.
- Ability to automate updates when IMF releases new data.
- Demonstration query to filter high GDP countries.

---

## How It Works

### 1. Extraction
- The script fetches the GDP table from the IMF website.
- Parses HTML using **BeautifulSoup**.
- Extracts country names and GDP values into a Python list of dictionaries.

### 2. Transformation
- GDP values are converted to floats and **rounded to 2 decimal places**.
- Country names are cleaned for consistent formatting.
- Data is optionally sorted by GDP.

### 3. Loading
- The transformed data is saved in two formats:
  - **JSON file:** `Countries_by_GDP.json`
  - **SQLite table:** `Countries_by_GDP` in `World_Economies.db`
- SQL table has columns:
  - `Country` (TEXT)
  - `GDP_USD_billion` (REAL)

### 4. Logging
- All ETL steps are logged in `etl_project_log.txt` with **timestamped messages**.

---
## Tools and Libraries Used

- Python 3.11 – programming language.
- requests – fetch data from web.
- BeautifulSoup4 – parse HTML content.
- pandas – optional, for tabular data handling.
- sqlite3 – database management.
- json – save data as JSON.
- datetime – timestamp logging.
