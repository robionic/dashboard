# Pinfield Inspection Dashboard

## 🏭 Overview

A browser-based inspection dashboard for reviewing PCB pin data, comparing measured values against nominal targets, and spotting outliers across a connector layout. The app is designed for fast quality checks from CSV data and helps operators understand where a board may be drifting outside acceptable limits.

## 🚀 Key Features

### Inspection Workflow
- **CSV Data Loading**: Import board inspection datasets from a local CSV file.
- **PCB Pin Mapping**: Visualize the connector layout as a clickable pin grid.
- **Pin-by-Pin Drilldown**: Inspect a selected pin's nominal value, measured variation, and quality status.
- **Multi-View Analytics**: Switch across scatter, distribution, and control-chart views for the same dataset.

### Quality Analysis
- **Tolerance Filtering**: Narrow the dataset by measurement bounds or inspection ranges.
- **Outlier Identification**: Highlight values that deviate from expected behavior.
- **Statistical Summaries**: Track representative measurement characteristics for each selected pin.
- **Production-Friendly Layout**: Quick visual review for QA and process engineers.

## 🛠️ Technology Stack

### Frontend
- **HTML5 & CSS3**: Layout and styling for the inspection UI
- **JavaScript**: Data handling, filtering, and chart interaction
- **Plotly.js**: Interactive charts for trend and distribution views

### Data Model
- **CSV-based Dataset**: Local inspection data loaded directly in the browser
- **Browser-side Filtering**: Fast analytical exploration without a database

## 📋 Installation & Setup

### Prerequisites
- A modern web browser
- Python 3 (optional for serving the page locally)

### Run Locally

1. Open the project folder in a terminal.
2. Start a simple web server:
   ```powershell
   python -m http.server 8000
   ```
3. Open the dashboard in your browser:
   ```text
   http://localhost:8000/pin_visualizer.html
   ```

You can also open `pin_visualizer.html` directly in the browser if you only need static viewing.

## 🎯 Usage Guide

### 1. Load the Dataset
- Click the load button or open the CSV file from your local machine.
- Confirm that the dataset is recognized and the connector is populated.

### 2. Inspect Connector Pins
- Click a pin on the PCB layout panel.
- Review the selected pin's summary metrics and measurement values.

### 3. Refine the View
- Apply filters such as value range or inspection window.
- Use the tabs to move between scatter, distribution, and control-based analyses.

### 4. Interpret Results
- Watch for pins with repeated irregular values or drift from the nominal target.
- Use the statistics panel to understand the pin's operating range and variance profile.

## 📁 Project Structure

```text
Dashboard/
├── README.md
├── pin_visualizer.html
├── TE_10Pin_PCBSide_Dataset.csv
└── ...
```

The HTML dashboard reads the dataset in the same folder and renders the interactive inspection views in the browser.

## 🔎 Typical Use Cases

- PCB assembly validation
- Connector quality review
- Outlier detection in production measurements
- Fast visual QA inspection for engineering teams
