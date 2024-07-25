# Mars News and Weather Data Scraping Challenge

This project involves two main tasks: scraping titles and preview text from the Mars News website and scraping and analyzing Mars weather data. Below are the detailed steps for each part of the project. For the complete code and notebooks, please refer to the following links:

- [Part 1: Scrape Titles and Preview Text from Mars News](https://github.com/steve-yuan-8276/mars_news_challenge/blob/main/part_1_mars_news_solution.ipynb)
- [Part 2: Scrape and Analyze Mars Weather Data](https://github.com/steve-yuan-8276/mars_news_challenge/blob/main/part_2_mars_weather_solution.ipynb)

## Project Directory Structure

The repository is structured as follows:
    
    

    
    mars_news_challenge/
    ├── part_1_mars_news_solution.ipynb
    ├── part_2_mars_weather_solution.ipynb
    ├── README.md
    ├── Outputs_data/
    │   ├── mars_news.json
    │   └── mars_weather.csv
    └── Outputs_images/
        ├── aavg_low_temp(unsorted_version).png
        ├── avg_low_temp(sorted_version)
        ├── avg_pressure_mars.png
        └── number_of_terrestrial_days.png
    

## Python Libraries Used

The following Python libraries are used in this project:

- **BeautifulSoup**: For parsing HTML and extracting data from web pages.
- **Splinter**: For automated browser actions and web scraping.
- **Pandas**: For data manipulation and analysis.
- **Matplotlib**: For creating visualizations such as bar charts and line plots.
- **Selenium**: For controlling web browsers through programs and performing browser automation tasks (used indirectly through Splinter).

## Part 1: Scrape Titles and Preview Text from Mars News

Open the Jupyter Notebook `part_1_mars_news_solution.ipynb` to perform the following steps to scrape the Mars News website.

1. **Visit the Mars News Site**

    - Use automated browsing to visit the [Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html).
    - Inspect the page to identify which elements to scrape.
2. **Create a Beautiful Soup Object**

    - Use Beautiful Soup to parse the HTML content of the website and extract text elements.
3. **Extract Titles and Preview Text**

    - Extract the titles and preview text of the news articles.
    - Store the scraping results in Python data structures as follows:
        - Store each title-and-preview pair in a Python dictionary with keys `title` and `preview`.
        - Store all dictionaries in a Python list.
        - Print the list in the notebook.
4. **Optional: Export Data to JSON**

    - Optionally, export the scraped data to a JSON file for easier data sharing.

## Part 2: Scrape and Analyze Mars Weather Data

Open the Jupyter Notebook `part_2_mars_weather_solution.ipynb` to perform the following steps to scrape and analyze Mars weather data.

1. **Visit the Mars Temperature Data Site**

    - Use automated browsing to visit the [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html).
    - Inspect the page to identify which elements to scrape.
2. **Create a Beautiful Soup Object**

    - Use Beautiful Soup to scrape the data from the HTML table.
    - Alternatively, the Pandas `read_html` function can be used, but Beautiful Soup is recommended to enhance web scraping skills.
3. **Assemble Data into a DataFrame**

    - Assemble the scraped data into a Pandas DataFrame with columns matching the table on the website:
        - `id`: Identification number of a single transmission from the Curiosity rover
        - `terrestrial_date`: The date on Earth
        - `sol`: The number of elapsed sols (Martian days) since Curiosity landed on Mars
        - `ls`: The solar longitude
        - `month`: The Martian month
        - `min_temp`: The minimum temperature in Celsius of a single Martian day (sol)
        - `pressure`: The atmospheric pressure at Curiosity's location
4. **Examine and Cast Data Types**

    - Examine and, if necessary, cast the data to appropriate `datetime`, `int`, or `float` data types.
5. **Analyze the Dataset**

    - Use Pandas functions to answer the following questions:
        - How many months exist on Mars?
        - How many Martian days' worth of data exist in the dataset?
        - What are the coldest and warmest months on Mars (at Curiosity's location)?
            - Find the average minimum daily temperature for all months.
            - Plot the results as a bar chart.
        - Which months have the lowest and highest atmospheric pressure on Mars?
            - Find the average daily atmospheric pressure for all months.
            - Plot the results as a bar chart.
        - How many terrestrial days are in a Martian year?
            - Consider how many days elapse on Earth during a Martian year.
            - Visually estimate the result by plotting the daily minimum temperature.
6. **Export Data to CSV**

    - Export the DataFrame to a CSV file for further analysis or sharing.

This README provides an overview of the tasks involved in the Mars News and Weather Data Scraping Challenge. For detailed implementation, please refer to the linked Jupyter notebooks.