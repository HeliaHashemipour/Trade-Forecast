This Python script is designed to scrape population data for population and GDP for different countries (we have two file for that which is for different continents)from the website "https://www.macrotrends.net/countries/". The script uses Selenium WebDriver to navigate the website, extract the data, and store it in a CSV file named "{country_name}_pop_data.csv".
Requirements:
Python 3.x
Selenium library: 
- pip install selenium
WebDriver Manager library: 
- pip install webdriver_manager
Chrome WebDriver: The script uses Chrome WebDriver to interact with the website. It will be automatically downloaded and managed by the ChromeDriverManager class from webdriver_manager.chrome.
Instructions:
Install the required Python libraries using the commands mentioned above.
Copy the script into a Python file (e.g., population_scraper.py).
Run the Python script with the command: python population_scraper.py.
Script Overview:
The script uses Selenium to automate the web browsing process. It first installs the Chrome WebDriver using ChromeDriverManager().install() and then initializes the Chrome WebDriver to open the website URL.
Once the website is loaded, the script locates the table containing the population data for Iceland. It then iterates through the rows of the table (excluding header rows) to extract the year and population data. The data is then stored in a pandas DataFrame and saved to a CSV file named "{country_name}_pop_data.csv" in the same directory as the script.
Note: The script contains commented-out code that demonstrates how to extend the scraping process to collect data for other countries listed on the website. If needed, uncomment and modify this section to scrape data for other countries. Remember this site needs VPN for crawling ((((: