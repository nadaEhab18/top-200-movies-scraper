# 🎬 Top 200 Movies Web Scraper

A Python web scraping project that extracts the **top 200 highest-grossing movies** from Box Office Mojo using Selenium WebDriver automation.

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/)
[![Selenium](https://img.shields.io/badge/Selenium-4.15+-green.svg)](https://selenium-python.readthedocs.io/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5+-orange.svg)](https://pandas.pydata.org/)

## 📖 Project Overview

This project automatically scrapes movie data from [Box Office Mojo](https://www.boxofficemojo.com/chart/top_lifetime_gross/?area=XWW) to collect information about the top 200 highest-grossing movies of all time. The scraper extracts movie rankings, titles, lifetime gross earnings, and release years, then exports the data to a CSV file for further analysis.

## 🛠️ Required Software & Setup

### 1. Chrome WebDriver Installation

**⚠️ IMPORTANT**: You must download ChromeDriver to enable automated browser control.

ChromeDriver acts as a bridge between your Python script and the Chrome browser, allowing the automation software to:
- Open web pages automatically
- Navigate through website elements
- Extract data without manual intervention
- Handle dynamic content loading

**Download Steps:**
1. Check your Chrome browser version: `chrome://version/`
2. Visit [ChromeDriver Downloads](https://chromedriver.chromium.org/downloads)
3. Download the version matching your Chrome browser
4. Extract the file and add it to your system PATH, or place it in your project folder

### 2. Python Libraries Used

This project uses the following libraries with detailed descriptions:

#### **🔧 Selenium WebDriver**
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
```
- **Purpose**: Web browser automation and control
- **Function**: Opens Chrome browser, navigates to websites, finds HTML elements, and extracts text
- **Why needed**: Box Office Mojo uses dynamic content that requires JavaScript execution, which basic HTTP requests cannot handle

#### **🐼 Pandas**
```python
import pandas as pd
```
- **Purpose**: Data manipulation and analysis
- **Function**: Organizes scraped data into structured DataFrames, handles data cleaning, and exports to CSV format
- **Why needed**: Converts raw scraped text into organized tabular data for easy analysis

#### **📁 CSV Module**
```python
import csv
```
- **Purpose**: File handling for CSV export
- **Function**: Writes structured data to CSV files
- **Why needed**: Creates downloadable data files that can be opened in Excel or other analysis tools

#### **🖥️ IPython Display**
```python
from IPython.display import FileLink
```
- **Purpose**: Jupyter Notebook file interaction
- **Function**: Creates clickable download links for generated files
- **Why needed**: Provides easy access to scraped data files within the notebook environment

## 📋 Installation & Setup

### 1. Install Required Libraries
```bash
pip install selenium pandas jupyter
```

### 2. Download and Setup ChromeDriver
- Place chromedriver.exe in your project folder, or
- Add ChromeDriver to your system PATH environment variable

### 3. Verify Installation
```python
from selenium import webdriver
driver = webdriver.Chrome()  # This should open a Chrome window
driver.quit()
```

## 🚀 How the Scraping Process Works
### Step 1: Browser Initialization
### Step 2: Website Navigation
### Step 3: Data Location & Extraction
### Step 4: Data Processing
### Step 5: Data Organization & Export
### Step 6: Cleanup

## 📊 Output Data Structure

The scraper generates a CSV file (`topMovies.csv`) containing:

| Column | Description | Example |
|--------|-------------|---------|
| Rank | Movie ranking by lifetime gross | 1 |
| Title | Full movie title | Avatar |
| Lifetime Gross | Total worldwide earnings | $2,923,706,026 |
| Year | Movie release year | 2009 |

**🌟 Star this repository if it helped you learn web scraping!**
