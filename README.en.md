# 📈 Extracting and Visualizing Stock Data with Python

🌐 Language:
- 🇺🇸 English
- 🇧🇷 [Portuguese](README.pt-BR.md)

---

## Overview

This project demonstrates the process of extracting, cleaning, analyzing, and visualizing financial data using Python.

The analysis combines two different data collection methods:

- Financial market data extracted through the Yahoo Finance API (`yfinance`)
- Revenue data collected through web scraping (`BeautifulSoup`)

The project compares stock market performance and revenue information for two companies:

- Tesla (TSLA)
- GameStop (GME)

The final deliverable includes historical stock price analysis and revenue visualizations generated with Matplotlib.

---

## Source

**Source:** IBM Data Analyst Professional Certificate (Coursera)

**Note:** This project was developed as part of the course activities and enhanced with additional documentation and analysis.

---

## Objectives

The primary goals of this project are:

- Extract historical stock market data using APIs
- Perform web scraping to collect financial information
- Clean and prepare data for analysis
- Create visual representations of stock prices and revenue
- Compare business performance against stock market trends
- Practice real-world data analysis workflows

---

## Technologies Used

- Python
- Pandas
- yFinance
- Requests
- BeautifulSoup4
- Matplotlib
- Jupyter Notebook

---

## Project Workflow

### 1. Define the Visualization Function

A custom plotting function (`make_graph`) was provided to create visualizations comparing:

- Historical stock prices
- Historical company revenue

The graphs are generated using Matplotlib and display both metrics over time.

---

## Question 1: Tesla Stock Data Extraction

Historical stock market data was retrieved using the Yahoo Finance API.

### Ticker Used

```python
TSLA
```

### Tasks Performed

- Created a Tesla ticker object
- Downloaded the maximum available historical dataset
- Stored data in a DataFrame named `tesla_data`
- Reset the DataFrame index
- Displayed the first five rows

### Main Columns

- Date
- Open
- High
- Low
- Close
- Volume
- Dividends
- Stock Splits

---

## Question 2: Tesla Revenue Extraction with Web Scraping

Revenue data was extracted from an HTML page using:

```python
requests
BeautifulSoup
```

### Website Used

The revenue data was collected from a hosted HTML page provided by the IBM Skills Network lab.

### Tasks Performed

- Downloaded HTML content
- Parsed HTML using BeautifulSoup
- Located the **Tesla Quarterly Revenue** table
- Extracted:
  - Date
  - Revenue
- Created the DataFrame:

```python
tesla_revenue
```

### Data Cleaning

The following cleaning operations were applied:

- Removed dollar signs (`$`)
- Removed commas (`,`)
- Removed empty values
- Removed null values

Example:

```text
$21,454
```

became:

```text
21454
```

---

## Question 3: GameStop Stock Data Extraction

Historical GameStop stock data was extracted using Yahoo Finance.

### Ticker Used

```python
GME
```

### Tasks Performed

- Created a GameStop ticker object
- Downloaded maximum historical data
- Stored the data in:

```python
gme_data
```

- Reset the DataFrame index
- Displayed the first five rows

---

## Question 4: GameStop Revenue Extraction with Web Scraping

Quarterly GameStop revenue data was retrieved through web scraping.

### Tasks Performed

- Downloaded HTML data
- Parsed the webpage with BeautifulSoup
- Located the quarterly revenue table
- Extracted:
  - Date
  - Revenue

### Dataset Created

```python
gme_revenue
```

### Cleaning Operations

- Removed commas
- Removed currency symbols
- Removed null records
- Removed empty values

---

## Question 5: Tesla Visualization

The custom plotting function was used to visualize:

- Tesla historical stock prices
- Tesla quarterly revenue

### Graph Generated

```python
make_graph(tesla_data, tesla_revenue, "Tesla")
```

The chart provides a visual comparison between Tesla's stock performance and revenue evolution over time.

---

## Question 6: GameStop Visualization

The same methodology was applied to GameStop.

### Graph Generated

```python
make_graph(gme_data, gme_revenue, "GameStop")
```

This visualization highlights the relationship between GameStop's business performance and stock market behavior.

---

## Key Skills Demonstrated

### Data Collection

- API Consumption
- Financial Data Retrieval
- Web Scraping

### Data Processing

- Data Cleaning
- Data Transformation
- Missing Value Handling

### Data Analysis

- Financial Analysis
- Time Series Exploration
- Business Metrics Evaluation

### Data Visualization

- Matplotlib
- Multi-panel Charts
- Trend Analysis

---

## Key Findings

### Tesla

- Tesla demonstrates significant revenue growth over the analyzed period.
- Revenue expansion is accompanied by substantial long-term stock appreciation.
- Historical data highlights the company's rapid business growth and market expansion.

### GameStop

- GameStop presents periods of strong stock price volatility.
- Stock performance and revenue trends are not always directly correlated.
- The data provides an interesting example of how market sentiment can differ from business fundamentals.

---

## Project Structure

```text
.
├── Extracting_and_Visualizing_Stock_Data.ipynb
├── README.md
├── images
│   ├── tesla_stock_graph.png
│   └── gamestop_stock_graph.png
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/extracting-visualizing-stock-data.git
```

Access the project folder:

```bash
cd extracting-visualizing-stock-data
```

Install dependencies:

```bash
pip install pandas
pip install yfinance
pip install requests
pip install beautifulsoup4
pip install matplotlib
```

Or install everything at once:

```bash
pip install pandas yfinance requests beautifulsoup4 matplotlib
```

---

## Running the Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Run all notebook cells sequentially to:

1. Extract financial market data
2. Scrape revenue tables
3. Clean datasets
4. Generate visualizations

---

## Example Visualizations

The project generates two dashboards:

### Tesla

- Historical Share Price
- Historical Quarterly Revenue

### GameStop

- Historical Share Price
- Historical Quarterly Revenue

Example:

```markdown
images/tesla_stock_graph.png

images/gamestop_stock_graph.png
```

---

## Future Improvements

Potential enhancements for this project include:

- Interactive dashboards with Plotly
- Revenue forecasting models
- Additional company comparisons
- Financial ratio analysis
- Automated data pipelines
- Real-time market monitoring

---

## About the IBM Data Analyst Professional Certificate

This project was completed as part of the **IBM Data Analyst Professional Certificate** available through Coursera.

The certification covers:

- Python for Data Analysis
- Data Visualization
- Databases and SQL
- Data Wrangling
- Statistical Analysis
- Dashboards
- Data Analytics Projects

---

## Author

**Vanessa Batista Fabri**

Data Analytics Portfolio Project

📌 LinkedIn: [linkedin.com/in/vanessafabri](https://www.linkedin.com/in/vanessafabri/)

📌 GitHub: [vanessabfabri](https://github.com/vanessabfabri)

---

## Disclaimer

This repository contains educational work completed as part of the IBM Data Analyst Professional Certificate. The notebook has been documented and organized for portfolio purposes to demonstrate practical skills in data extraction, data cleaning, web scraping, exploratory analysis, and data visualization using Python.
