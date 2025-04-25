**Web Scraper: Bus & Train Data Extraction Tool**

**Overview**
This project is a web scraper application built using Streamlit and Selenium to extract bus and train travel details from websites like AbhiBus. It allows users to input URLs, scrape relevant travel data efficiently, and download the results as CSV files.

**Features**
Scrapes detailed bus information: bus name, type, departure/arrival times, route, duration, and price.

Supports expansion of government bus dropdowns for complete data extraction.

Scrapes train details (planned/extendable).

Data is presented cleanly in interactive tables on Streamlit.

Export scraped data as CSV files for offline use.

User-friendly interface with sidebar navigation.

Handles dynamic page loading using Selenium explicit waits.

Supports differentiation between government and private buses.

**Installation**
**Clone the repository**
git clone https://github.com/Vamsi-Vemulapati/Scrapper_tool.git

**Install required packages**
pip install -r req.txt
The main dependencies include:
streamlit
selenium
webdriver-manager
pandas

**Usage**
**Run the Streamlit app:**
 python -m streamlit run filename.py

 Use the sidebar navigation to choose:

  **Bus Scraper** 🚌

  **Train Scraper** 🚆 

Enter the target URL (e.g., a search page on AbhiBus).

Click Scrape to extract data.

View the scraped data in the table below.

Download CSV files for government and private buses separately.

**How it works**
The tool launches a Chrome browser controlled by Selenium.

It loads the given URL, waits for key page elements to appear.

It optionally expands dropdown sections for government buses to reveal hidden data.

Extracts textual data from specific HTML elements based on class names or CSS selectors.

Cleans and organizes the data into pandas DataFrames.

Displays data interactively and allows downloading as CSV files.
**Important Notes**
The scraper relies on the website's current HTML structure; if the site layout changes, selectors may need updating.

Running Selenium in headless mode is disabled by default but can be enabled in the code for faster scraping without opening a browser window.

Network speed and page load times affect scraping duration.

Avoid too frequent scraping to prevent being blocked by the target website.

**Troubleshooting**
**Timeouts / No Data Found:**
Ensure the URL is correct and publicly accessible.

**Driver Issues:**
Make sure you have Chrome installed and compatible with webdriver-manager.

**Permission / Security Warnings:**
Running Chrome with appropriate options (--no-sandbox, --disable-dev-shm-usage) helps stability.

