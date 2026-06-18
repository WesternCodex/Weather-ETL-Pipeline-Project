# Weather-ETL-Pipeline-Project
# 🌦️ Weather Data ETL Pipeline

## Project Overview

This project demonstrates an **Extract, Transform, and Load (ETL)** pipeline developed in Python to collect, process, and analyze real-time weather data for major cities in Nigeria using the OpenWeatherMap API.

The project automates the retrieval of weather information, cleans and enriches the dataset with additional descriptive features, and prepares the data for analysis. The final dataset provides meaningful insights into weather conditions across different Nigerian cities and can serve as a foundation for dashboards, reporting, or predictive analytics.

---

## Data Source

The weather data was obtained from the **OpenWeatherMap API**, which provides real-time meteorological information.

The API returns weather information in JSON format, including:

* Country
* City
* Temperature
* Humidity
* Wind Speed
* Weather Category
* Weather Description
* Date and Time

The API data was accessed using Python requests and converted into a structured tabular format.

---

## ETL Process

### 1. Extract

The extraction stage involved:

* Connecting to the OpenWeatherMap API.
* Sending HTTP requests for multiple Nigerian cities.
* Receiving weather data in JSON format.
* Collecting the responses into a Python list.

---

### 2. Transform

The transformation stage included several data cleaning and enhancement tasks:

* Converted country codes (e.g., **NG**) into full country names (**Nigeria**).
* Standardized column names for readability.
* Converted timestamps into Python datetime format.
* Added a **Weather Description** column.
* Created a **Weather Meaning** column using a custom dictionary that translates weather descriptions into human-readable explanations.
* Handled missing values by assigning default descriptions when necessary.
* Organized the dataset into a structured pandas DataFrame.

---

### 3. Load

The transformed dataset was exported into a CSV file for further analysis and visualization.

The cleaned dataset can easily be imported into:

* Power BI
* Tableau
* Excel
* SQL databases
* Python notebooks

---

## Tools Used

| Tool               | Purpose                                     |
| ------------------ | ------------------------------------------- |
| Python             | ETL development                             |
| Requests           | API communication                           |
| Pandas             | Data cleaning and transformation            |
| OpenWeatherMap API | Weather data source                         |
| PyCountry          | Convert country codes to full country names |
| Jupyter Notebook   | Development environment                     |
| CSV                | Data storage format                         |
| GitHub             | Version control and project hosting         |

---

## Steps Taken

1. Generated an API key from OpenWeatherMap.
2. Created a list of major Nigerian cities.
3. Sent API requests for each city.
4. Retrieved weather information in JSON format.
5. Extracted relevant weather attributes.
6. Combined the responses into a single dataset.
7. Converted country abbreviations to full names.
8. Added weather descriptions and their meanings.
9. Formatted timestamps into readable datetime values.
10. Saved the cleaned dataset as a CSV file.
11. Performed exploratory data analysis on the transformed dataset.

---

## Key Findings

The exploratory analysis revealed several insights into the weather patterns across Nigerian cities:

* Most sampled cities experienced **cloudy weather**, particularly **overcast clouds**.
* Northern cities generally recorded **higher temperatures** than southern cities.
* Humidity levels were significantly higher in coastal cities such as Lagos, Port Harcourt, and Calabar.
* Wind speeds varied across locations but were generally low to moderate.
* Enriching the dataset with descriptive weather meanings improved interpretability for non-technical users.
* The ETL pipeline successfully automated the collection and preparation of weather data, reducing manual processing and ensuring consistency.

---

## Future Improvements

Potential enhancements to this project include:

* Automating data collection using scheduled jobs (Cron or Task Scheduler).
* Loading the data directly into a SQL database.
* Building an interactive Power BI or Tableau dashboard.
* Incorporating historical weather data for trend analysis.
* Implementing logging and exception handling for improved reliability.
* Deploying the pipeline to a cloud platform for continuous data updates.

---

## Project Structure

```text
Weather-ETL/
│
├── data/
│   ├── raw_weather.csv
│   └── transformed_weather.csv
│
├── notebooks/
│   └── Weather_ETL.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Author

**Chukwudi Onwusa**

Data Analyst | Python | SQL | Power BI | ETL | Data Visualization

---

## License

This project is available under the MIT License.
