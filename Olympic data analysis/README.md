# Olympics Data Analysis using Streamlit

## Overview

This project is an interactive data analysis application built using Streamlit.  
It analyzes historical Summer Olympics data and provides visual insights into medal trends, country performance, athlete statistics, and sport participation patterns.
The goal of this project is to explore data visualization, filtering, and dashboard development using Python and Streamlit.

### Dataset Link: https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results

## Features

### 1. Medal Tally
- View overall medal counts
- Filter medal tally by year
- Filter medal tally by country
- Country and year-based performance comparison

### 2. Overall Analysis
- Total number of editions
- Number of host cities
- Total sports, events, nations, and athletes
- Participating nations over time
- Events growth over the years
- Athlete participation trend
- Gold, Silver, and Bronze medal trend over time
- Top 5 sports participation trend
- Most successful athletes

### 3. Country-wise Analysis
- Year-wise medal tally of selected country
- Sport-wise medal heatmap
- Top 10 athletes of selected country

### 4. Athlete-wise Analysis
- Age distribution of medalists
- Age distribution by sport (Gold medalists)
- Height vs Weight comparison
- Male vs Female participation over time

## Tech Stack
- Python
- Streamlit
- Pandas
- NumPy
- Plotly
- Matplotlib
- Seaborn

## Installation and Setup
1. Clone the repository:
   git clone <repository_link>
2. Navigate to the project directory:
   cd <repository_name>
3. Install dependencies:
   pip install -r requirements.txt
4. Run the application:
   streamlit run app.py

## Deployment
The application can be deployed using Streamlit Community Cloud by connecting the GitHub repository and selecting `app.py` as the entry point.

## Dataset
The project uses two datasets:
- athlete_events.csv
- noc_regions.csv
These datasets contain historical records of Summer Olympic Games.

## Purpose
This project was developed as an experimental data analysis dashboard to practice:
- Data cleaning and preprocessing
- Exploratory data analysis
- Data visualization
- Interactive dashboard development
