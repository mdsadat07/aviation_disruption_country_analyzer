# Global Aviation Disruption Analyzer

An interactive data analytics application that analyzes global aviation disruption impacts and estimates airline financial losses, cancelled flights, rerouted flights, and passenger impact by country.

The application automatically retrieves the latest dataset from Kaggle, processes the data using Python, and presents the results through an interactive Streamlit dashboard.

# Live Application

The application is deployed using Streamlit Community Cloud.

Access the live dashboard here:

Streamlit App: https://aviationdisruptioncountryanalyzer-fvej7yvotvd3rqjz49rh7r.streamlit.app/

# Project Overview

This project demonstrates how to build a real-time data analytics application using Python and Streamlit.

The system automatically retrieves aviation disruption data from Kaggle, processes it with Python (pandas), and presents an interactive dashboard where users can explore airline impacts by country.

Users can select a country from a dropdown menu to view:

* Airlines affected
* Estimated daily financial losses
* Cancelled flights
* Rerouted flights
* Passengers impacted
* Aggregated disruption statistics

# Data Source

Dataset provided by Kaggle:

Global Civil Aviation Disruption – Iran US War Scenario

Kaggle Dataset:
[https://www.kaggle.com/datasets/zkskhurram/global-civil-aviation-disruption2026-iranus-war](https://www.kaggle.com/datasets/zkskhurram/global-civil-aviation-disruption2026-iranus-war)

The application specifically uses:

`airline_losses_estimate.csv`

# Automatic Data Updates

The dataset is retrieved directly from Kaggle using the Kaggle API.

The application automatically:

1. Connects securely to Kaggle using API credentials stored in Streamlit Secrets.
2. Downloads the latest dataset file (`airline_losses_estimate.csv`).
3. Extracts and loads the data into a pandas DataFrame.
4. Caches the data for seven days to reduce API requests and improve performance.

After the cache expires, the dataset is automatically refreshed from Kaggle.

This ensures the dashboard always reflects the most recent available data.

# Technology Stack

Python
pandas – data processing and analysis
Streamlit – interactive web application framework
Kaggle API – automated dataset retrieval
GitHub – version control and project hosting
Streamlit Community Cloud – application deployment

# Application Architecture

Kaggle Dataset
↓
Kaggle API download
↓
Python data processing (pandas)
↓
Streamlit dashboard interface
↓
Streamlit Community Cloud deployment

The architecture allows the application to remain lightweight while keeping the dataset dynamically updated.

# Features

Interactive country selection using a dropdown menu

Airline disruption analysis including:

* Estimated daily financial losses
* Cancelled flights
* Rerouted flights
* Passenger impact

Real-time summary metrics including:

* Total financial loss
* Total cancelled flights
* Total rerouted flights
* Total passengers impacted

Automatic weekly dataset refresh from Kaggle

Interactive dashboard accessible from any web browser

# Example Dashboard Workflow

1. User opens the Streamlit application.
2. The system retrieves the latest dataset from Kaggle (if cache expired).
3. The user selects a country from the dropdown menu.
4. The dashboard displays airlines impacted in that country.
5. The system calculates aggregated disruption metrics.

# Installation (Local Development)

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/aviation-disruption-country-analyzer.git
cd aviation-disruption-country-analyzer
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
streamlit run app.py
```

The application will launch locally at:

```
http://localhost:8501
```

# Environment Configuration

The application requires Kaggle API credentials.

These are stored securely in Streamlit Secrets.

Example configuration:

```
[kaggle]
username = "YOUR_KAGGLE_USERNAME"
key = "YOUR_KAGGLE_API_KEY"
```

This prevents sensitive credentials from being stored in the repository.

---

# Project Structure

```
aviation-disruption-country-analyzer
│
├── app.py
├── requirements.txt
├── README.md
```

# Author

Sultan Munir Muhammad Sadat
