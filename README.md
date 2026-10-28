# ECB-Exchange-Rate-Against-EURO-
# FX Treasury & Risk Analytics Toolkit


# FX Data Analysis & Automated Monitoring with Python

## Project Overview

This project uses Python to analyse historical foreign exchange (FX) rates, calculate currency movements, evaluate exchange-rate volatility, and identify significant rate changes through automated threshold-based alerts.

The project demonstrates how Python can be used to transform raw financial data into meaningful insights for financial analysis, reporting, and monitoring.

## Business Problem

Exchange rates fluctuate continuously and can affect international payments, invoices, and business costs. Manually monitoring these changes can be time-consuming and may make it difficult to identify important movements quickly.

This project addresses that problem by building a reusable workflow to:

- Retrieve and process historical exchange-rate data.
- Analyse GBP, USD, and INR exchange rates.
- Calculate currency conversions.
- Evaluate potential foreign-exchange gains and losses on invoices.
- Measure exchange-rate volatility.
- Flag significant rate movements using configurable thresholds.
- Log alerts and track previously triggered alerts to reduce duplicate notifications.

## Key Features

### 1. Data Collection

- Uses historical exchange-rate data from the European Central Bank (ECB).
- Downloads and extracts exchange-rate data from a ZIP archive.
- Loads the data into pandas DataFrames for further analysis.

### 2. Data Cleaning and Quality Checks

- Inspects the structure and quality of the source data.
- Handles dates and numeric exchange-rate values.
- Prepares the data for time-series analysis.
- Selects month-end exchange rates for reporting.

### 3. Currency Conversion

- Analyses exchange rates involving GBP, USD, and INR.
- Calculates currency conversions using historical rates.
- Supports financial analysis involving different currencies.

### 4. Invoice FX Gain/Loss Analysis

- Loads invoice data from an Excel file.
- Analyses the potential foreign-exchange impact on invoices.
- Demonstrates how exchange-rate changes can affect financial values.

### 5. Exchange-Rate Volatility Analysis

- Calculates currency returns using percentage and logarithmic changes.
- Uses rolling-window calculations to examine exchange-rate movements.
- Estimates annualised volatility to understand the variability of exchange rates over time.
- Uses Matplotlib to visualise trends and volatility.

### 6. Automated Threshold-Based Alerts

- Compares the latest exchange rate against a rolling historical average.
- Calculates the percentage deviation from the reference rate.
- Flags movements that exceed a configurable threshold.
- Uses configuration settings to control alert parameters.
- Records alerts in a log file.
- Stores alert state in JSON to help prevent duplicate alerts.

**Note:** The current implementation generates file-based alerts. It does not currently send email notifications or run on a scheduled background service.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and time-series analysis |
| NumPy | Numerical calculations |
| Matplotlib | Data visualisation |
| ConfigParser | Configurable monitoring parameters |
| Logging | Recording application activity and alerts |
| JSON | Persisting alert state |
| Excel | Reading invoice data |
| Jupyter Notebook | Interactive analysis and development |

## Methodology

The project follows a data-processing and analysis workflow:

1. **Data ingestion:** Obtain historical exchange-rate data from the ECB.
2. **Data preparation:** Inspect, clean, and transform the data into a usable format.
3. **Time-series analysis:** Extract monthly observations and analyse currency movements.
4. **Financial calculations:** Perform currency conversions and invoice FX gain/loss analysis.
5. **Volatility estimation:** Calculate returns and rolling volatility.
6. **Monitoring:** Compare the latest rate with a historical reference value.
7. **Alert generation:** Flag deviations that exceed the configured threshold.
8. **Logging and state management:** Record alert events and track previously triggered alerts.

## Example Applications

This project demonstrates techniques that can be applied to:

- Monitoring exchange rates for international transactions.
- Analysing historical currency movements.
- Assessing potential foreign-exchange exposure.
- Producing monthly financial reports.
- Identifying unusual exchange-rate movements.
- Building simple rule-based financial monitoring systems.

## Skills Demonstrated

### Data Analysis
- Data ingestion and preprocessing
- Data quality inspection
- Time-series analysis
- Rolling-window calculations
- Statistical analysis and volatility estimation
- Data visualisation

### Python Programming
- Working with functions and reusable code
- Using Python libraries for data analysis
- Configuration management
- Logging and error investigation
- JSON-based state persistence
- Basic automation and rule-based monitoring

### Financial Analysis
- Foreign-exchange rate analysis
- Currency conversion
- Invoice FX gain/loss analysis
- Exchange-rate volatility
- Threshold-based anomaly flagging

## Project Structure

A suggested repository structure is:

```text
fx-data-analysis/
├── data/
│   └── .gitkeep
├── notebooks/
│   └── Practice_automation_project.ipynb
├── outputs/
│   └── .gitkeep
├── config.ini
├── requirements.txt
├── .gitignore
└── README.md
```

The structure can be adapted as the project develops. For a more maintainable version, data-processing and alerting functions could later be moved into separate Python modules.

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/fx-data-analysis.git
cd fx-data-analysis
```

Replace `YOUR_USERNAME` with your GitHub username and update the repository name if necessary.

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Or on macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib openpyxl
```

Add any other dependencies required by the notebook to `requirements.txt`.

### 4. Configure file paths

Update the notebook's file paths so they work on your machine. Avoid hard-coded paths specific to a personal computer.

### 5. Run the notebook

Open Jupyter Notebook or JupyterLab and run the notebook cells in sequence.

## Limitations and Future Improvements

Potential improvements include:

- Replace machine-specific file paths with configurable, relative paths.
- Add automated tests for currency conversions and financial calculations.
- Validate invoice FX gain/loss calculations against clearly defined exchange-rate conventions.
- Preserve the exact observation date used for each month-end rate.
- Exclude the latest observation from the historical baseline when appropriate, so the comparison is not diluted by the value being monitored.
- Improve handling of missing observations and unusual data.
- Add email or messaging notifications.
- Schedule monitoring to run automatically.
- Add a dashboard for exchange-rate trends, volatility, and alerts.
- Separate reusable functions from the notebook into Python modules.
- Add a reproducible environment using a complete `requirements.txt`.

## Disclaimer

This project is intended for educational and analytical purposes. Its outputs should not be treated as financial advice or as a substitute for independent verification of exchange rates and accounting calculations.

## Author

**Somil**

MSc Astrophysics | Python | Data Analysis | Time-Series Analysis

[GitHub Profile](https://github.com/YOUR_USERNAME)
