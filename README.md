```markdown
# CensusDataEda: Unpacking U.S. Commuting Trends

## Project Overview

`CensusDataEda` is an exploratory data analysis (EDA) project focused on U.S. commuting patterns using data from the U.S. Census Bureau. This repository contains the Python scripts necessary to retrieve, clean, and preprocess raw American Community Survey (ACS) data, transforming it into clean, user-friendly CSV files. These prepared datasets will then be used for interactive data visualizations on Tableau Public, offering insights into how Americans commute across different states, income levels, and genders.

## Goals & Features

* **Automated Data Acquisition:** Programmatically fetch detailed commuting data from the U.S. Census Bureau API.

* **Robust Data Cleaning:** Utilize the `pandas` library in Python to clean raw Census data, convert cryptic column names into human-readable labels, and handle missing values.

* **Data Transformation:** Calculate derived metrics (e.g., percentages of commuters using various modes) to provide more actionable insights.

* **Export to CSV:** Output cleaned and transformed datasets into standardized CSV files, ready for external visualization tools.

* **Tableau Public Integration:** Serve as the data preparation backend for compelling data stories on Tableau Public, focusing on key commuting demographics.

## Technologies Used

* **Python:** The primary programming language for scripting and data processing.

* **Pandas:** A powerful Python library for data manipulation, cleaning, and analysis.

* **Requests:** For making HTTP requests to the Census Bureau API.

* **U.S. Census Bureau API:** The source of the raw American Community Survey (ACS) data.

* **Tableau Public:** The platform for creating interactive and shareable data visualizations.

## Data Sources

The project primarily utilizes data from the **2023 American Community Survey (ACS) 1-Year Estimates Detailed Tables**, specifically targeting tables related to commuting and demographic characteristics. Key tables include:

* **`B08007`**: POPULATION 16 YEARS AND OVER IN LABOR FORCE--COMMUTING TO WORK (Provides detailed commute modes and travel times).

* **`C08006`**: SEX OF WORKERS BY MEANS OF TRANSPORTATION TO WORK (Breaks down commute modes by gender).

* **`B19001` (or similar)**: HOUSEHOLD INCOME IN THE PAST 12 MONTHS (Will be used to categorize data by income brackets, often combined with commuting data).

## Setup and Usage

To run the data extraction and cleaning scripts:

1.  **Clone the Repository:**

    ```
    git clone [https://github.com/yourusername/CensusDataEda.git](https://github.com/yourusername/CensusDataEda.git)
    cd CensusDataEda

    ```

2.  **Install Dependencies:**

    ```
    pip install pandas requests

    ```

3.  **Obtain a Census API Key:**

    * You will need an API key from the U.S. Census Bureau. Register for one [here](https://www.census.gov/data/developers/community/api-registration.html).

    * Store your API key securely (e.g., in an environment variable or a configuration file that is not committed to Git). The Python scripts will need access to this key.

4.  **Run the Data Processing Script:**

    * Execute the main Python script (e.g., `process_census_data.py`, `main.py`, or similar name you choose for your script).

    * Ensure your API key is correctly configured within the script or environment.

    ```
    python your_main_script_name.py

    ```

    This will fetch the data, clean it, and save the resulting CSV files in a designated output directory (e.g., `data/cleaned_csvs/`).

## Cleaned Data Overview

The generated CSV files will feature human-readable column names and, where applicable, derived metrics (e.g., percentages). For instance, column names like `B08007_001E` will be transformed into descriptive labels such as `Total Commuters: Estimate` or `Percent Drove Alone`.

The output CSVs will typically include:

* **Geographic Identifiers and Names:** `GEO_ID` and `NAME` (renamed to `Geographic Identifier` and `Geographic Area`).

* **Commuting Modes:** Detailed counts and percentages for various transportation methods (driving alone, carpooling, public transit, walking, biking, working from home, etc.).

* **Commute Duration:** Distribution of travel times to work (e.g., less than 10 minutes, 10-14 minutes, etc.).

* **Gender Breakdown:** Commuting patterns specifically broken down by male and female workers.

* **Income Brackets:** Commuting data segmented by household income levels (requires combining with income-related tables).

## Visualizations (Tableau Public)

The cleaned CSVs will power interactive dashboards on Tableau Public, providing visual insights into:

1.  **Commute Duration by U.S. State:** A map or bar chart visualizing the average or typical commute times across different states.

2.  **Transportation Modes by Income Bracket:** Stacked bar charts or treemaps showing how different income groups utilize various transportation methods for commuting.

3.  **Transportation Modes by Gender:** Comparisons of commute mode preferences between male and female workers.

Links to the Tableau Public dashboards will be added here once they are published.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
