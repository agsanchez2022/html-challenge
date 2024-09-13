# html-challenge
Deliverable 1: Scrape titles and preview text from Mars news articles.
Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

## Instructions

### Part 1: Scrape Titles and Preview Text from Mars News

1. Open the Jupyter Notebook in the starter code folder named `part_1_mars_news.ipynb`. Follow the steps below to scrape the Mars News website.
2. Use automated browsing to visit the [Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html). Inspect the page to identify which elements to scrape.
3. Create a Beautiful Soup object and use it to extract text elements from the website.
4. Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
   - Store each title-and-preview pair in a Python dictionary with two keys: `title` and `preview`. For example:
     ```python
     {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
      'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
     ```
   - Store all the dictionaries in a Python list.
   - Print the list in your notebook.

### Part 2: Scrape and Analyze Mars Weather Data

1. Open the Jupyter Notebook in the starter code folder named `part_2_mars_weather.ipynb`. Follow the steps below to scrape and analyze Mars weather data.
2. Use automated browsing to visit the [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html). Inspect the page to identify which elements to scrape.
3. Create a Beautiful Soup object and use it to scrape the data in the HTML table.
4. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
   - `id`: the identification number of a single transmission from the Curiosity rover
   - `terrestrial_date`: the date on Earth
   - `sol`: the number of elapsed sols (Martian days) since Curiosity landed on Mars
   - `ls`: the solar longitude
   - `month`: the Martian month
   - `min_temp`: the minimum temperature, in Celsius, of a single Martian day (sol)
   - `pressure`: the atmospheric pressure at Curiosity's location
5. Examine the data types associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
6. Analyze your dataset using Pandas functions to answer the following questions:
   - How many months exist on Mars?
   - How many Martian (and not Earth) days worth of data exist in the scraped dataset?
   - What are the coldest and the warmest months on Mars (at the location of Curiosity)?
     - Find the average minimum daily temperature for all months.
     - Plot the results as a bar chart.
   - Which months have the lowest and highest atmospheric pressure on Mars?
     - Find the average daily atmospheric pressure for all months.
     - Plot the results as a bar chart.
   - About how many terrestrial (Earth) days exist in a Martian year?
     - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
     - Visually estimate the result by plotting the daily minimum temperature of each observation.
7. Export the DataFrame to a CSV file.

