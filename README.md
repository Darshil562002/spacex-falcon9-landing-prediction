# SpaceX Falcon 9 First Stage Landing Prediction

A comprehensive data science project analyzing SpaceX Falcon 9 rocket launches to predict first stage landing success. This project covers the complete data science lifecycle from data collection to machine learning model deployment.

## Project Overview

This project analyzes SpaceX Falcon 9 rocket launch data to predict whether the first stage of the rocket will successfully land. The analysis includes data collection via API and web scraping, data wrangling, exploratory data analysis, visualization, and machine learning model development.

## Table of Contents

- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Project Phases](#project-phases)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```
IBM DATA SCIENCE CAPSTONE PROJECT copy/
│
├── api collection/
│   ├── spacex-data-collection-api.ipynb
│   └── dataset_part_1.csv
│
├── webscraping/
│   ├── jupyter-labs-webscraping.ipynb
│   └── spacex_web_scraped.csv
│
├── Data Wrangling/
│   ├── labs-jupyter-spacex-Data wrangling-v2.ipynb
│   └── dataset_part_2.csv
│
├── EDA/
│   ├── jupyter-labs-eda-sql-coursera_sqllite.ipynb
│   ├── my_data1.db
│   └── Spacex (1).csv
│
├── EDA VISUALISATION/
│   ├── jupyter-labs-eda-dataviz-v2.ipynb
│   └── dataset_part_3.csv
│
├── Interactive Visual Analytics with Folium lab/
│   ├── lab-jupyter-launch-site-location-v2.ipynb
│   ├── Interactive Visual Analytics with Folium Lab.html
│   └── spacex_launch_geo*.csv
│
├── Machine Learning Prediction lab/
│   └── SpaceX-Machine-Learning-Prediction-Part-5-v1.ipynb
│
├── Interactive Dashboard with Plotly Dash/
│   ├── spacex-dash-app.py
│   ├── dashboard-overview-1.png
│   ├── dashboard-launch-site-analysis.png
│   ├── dashboard-payload-range.png
│   ├── dashboard-success-rate.png
│   └── dashboard-overview-2.png
│
└── README.md
```

## Technologies Used

- **Python 3.14**
- **Jupyter Notebooks**
- **Libraries:**
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computing
  - `matplotlib` - Data visualization
  - `seaborn` - Statistical data visualization
  - `plotly` - Interactive visualizations
  - `dash` - Interactive web applications
  - `folium` - Interactive maps
  - `scikit-learn` - Machine learning
  - `requests` - API calls
  - `beautifulsoup4` - Web scraping
  - `sqlite3` - Database operations

## Project Phases

### 1. Data Collection
- **API Collection** (`api collection/`): Collected SpaceX launch data using REST API
- **Web Scraping** (`webscraping/`): Scraped additional data from SpaceX Wikipedia page

### 2. Data Wrangling
- **Data Cleaning** (`Data Wrangling/`): Cleaned and transformed raw data
- Handled missing values, data type conversions, and feature engineering

### 3. Exploratory Data Analysis (EDA)
- **SQL Analysis** (`EDA/`): Performed SQL queries to analyze launch patterns
- **Data Visualization** (`EDA VISUALISATION/`): Created visualizations to understand data patterns
- Analyzed success rates, launch sites, payload masses, and orbital parameters

### 4. Interactive Visualizations
- **Folium Maps** (`Interactive Visual Analytics with Folium lab/`): Created interactive maps showing launch site locations
- **Plotly Dash Dashboard** (`Interactive Dashboard with Plotly Dash/`): Built an interactive web dashboard for launch analysis

### 5. Machine Learning
- **Model Development** (`Machine Learning Prediction lab/`): 
  - Trained multiple classification models:
    - Logistic Regression
    - Support Vector Machine (SVM)
    - Decision Tree Classifier
    - K-Nearest Neighbors (KNN)
  - Performed hyperparameter tuning using GridSearchCV
  - Evaluated model performance and selected the best model


## Usage

### Running the Interactive Dashboard

1. Navigate to the dashboard directory:
   ```bash
   cd "Interactive Dashboard with Plotly Dash"
   ```

2. Ensure you have the required CSV file (`spacex_launch_dash.csv`)

3. Run the Dash application:
   ```bash
   python spacex-dash-app.py
   ```

4. Open your browser and navigate to `http://127.0.0.1:8050`

### Running Machine Learning Models

1. Open the machine learning notebook:
   ```bash
   jupyter notebook "Machine Learning Prediction lab/SpaceX-Machine-Learning-Prediction-Part-5-v1.ipynb"
   ```

2. Run all cells sequentially to:
   - Load and preprocess data
   - Train multiple models
   - Evaluate and compare model performance
   - Generate predictions

### Viewing the Interactive Folium Map

The project includes an interactive HTML version of the Folium map visualization. To view it:

1. **Option 1: View directly on GitHub**
   - Navigate to the file: `Interactive Visual Analytics with Folium lab/Interactive Visual Analytics with Folium Lab.html`
   - Click on the file in GitHub
   - Click "Download" or "View Raw" to open it in your browser

2. **Option 2: View locally**
   - Clone the repository or download the HTML file
   - Open the file `Interactive Visual Analytics with Folium lab/Interactive Visual Analytics with Folium Lab.html` in any web browser
   - The interactive map will load with all markers and popups functional

3. **Option 3: Generate from notebook**
   - Open the notebook: `Interactive Visual Analytics with Folium lab/lab-jupyter-launch-site-location-v2.ipynb`
   - Run all cells to generate the interactive map
   - Or convert to HTML using:
     ```bash
     python3 -m nbconvert --to html "Interactive Visual Analytics with Folium lab/lab-jupyter-launch-site-location-v2.ipynb" --output "Interactive Visual Analytics with Folium Lab.html"
     ```

## Results

### Model Performance

The project evaluated four machine learning models:

| Model | Validation Accuracy | Test Accuracy |
|-------|-------------------|---------------|
| Logistic Regression | 84.64% | 83.33% |
| Support Vector Machine | 84.82% | 83.33% |
| Decision Tree | 87.68% | 66.67% |
| K-Nearest Neighbors | 84.82% | 83.33% |

**Best Model:** Logistic Regression (selected based on consistent performance)

### Key Findings

- **Launch Site Analysis:** Different launch sites show varying success rates
- **Payload Mass Impact:** Heavier payloads may affect landing success
- **Orbital Parameters:** Specific orbits correlate with landing success
- **Temporal Trends:** Success rates have improved over time

## Screenshots

The project includes several screenshots of the interactive dashboard:

- `dashboard-overview-1.png` - Dashboard overview
- `dashboard-launch-site-analysis.png` - Launch site analysis
- `dashboard-payload-range.png` - Payload range visualization
- `dashboard-success-rate.png` - Success rate analysis
- `dashboard-overview-2.png` - Additional dashboard view

## Key Features

- Complete data science pipeline implementation
- Multiple data collection methods (API + Web Scraping)
- Comprehensive data cleaning and preprocessing
- Interactive visualizations and dashboards
- Multiple machine learning models with hyperparameter tuning
- Model evaluation and comparison
- Production-ready dashboard application

## Notebooks Description

1. **spacex-data-collection-api.ipynb**: Collects SpaceX launch data via REST API
2. **jupyter-labs-webscraping.ipynb**: Web scraping SpaceX Wikipedia page
3. **labs-jupyter-spacex-Data wrangling-v2.ipynb**: Data cleaning and transformation
4. **jupyter-labs-eda-sql-coursera_sqllite.ipynb**: SQL-based exploratory data analysis
5. **jupyter-labs-eda-dataviz-v2.ipynb**: Data visualization and analysis
6. **lab-jupyter-launch-site-location-v2.ipynb**: Interactive map visualizations
7. **SpaceX-Machine-Learning-Prediction-Part-5-v1.ipynb**: Machine learning model development


## License

This project is part of the IBM Data Science Professional Certificate Capstone Project.

## Author

**Darshil Shethia**

- Project completed as part of IBM Data Science Professional Certificate
- Capstone Project: SpaceX Falcon 9 First Stage Landing Prediction

## Acknowledgments

- IBM for providing the course materials and datasets
- SpaceX for making launch data publicly available
- The open-source community for excellent data science tools

---

**Note:** This project is for educational purposes as part of the IBM Data Science Professional Certificate program. This project gave me a chance to show off all I learnt during the IBM Data Science professional certifiate.
