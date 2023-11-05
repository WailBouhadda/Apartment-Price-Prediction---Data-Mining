# Apartment-Price-Prediction-and-Valuation-Using-Data-Mining


#### Author:  - <a href="https://github.com/WailBouhadda">Wail Bouhadda</a>

## Table of Contents

- [Project Overview](#project-overview)
- [Data Collection](#data-collection)
- [Data Preprocessing](#data-preprocessing)
- [Data Visualization](#data-visualization) ![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)
- [Feature Extraction](#feature-extraction) ![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)
- [Model Training](#model-training) ![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)
- [Model Evaluation](#model-evaluation) ![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)
- [Testing on Real Data](#testing-on-real-data) ![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)

## Project Overview

Welcome to the Apartment Price Prediction project, where we employ data mining techniques to predict apartment prices. Our goal is to build a robust machine learning model that can accurately predict apartment prices based on various features.

#### Project Goals

- Collect a comprehensive dataset of apartment listings, including essential attributes such as location, type, price, and more.
- Utilize data mining techniques to preprocess and clean the dataset for analysis.
- Develop and train a machine learning model to predict apartment prices.
- Evaluate the model's performance and provide insights into feature importance.
- Create a practical tool for individuals interested in estimating apartment prices in the target area.

## Data Collection

In this project, we undertook a comprehensive data collection process to gather information about apartments available for sale in morocco. Our dataset consists of approximately 33,000 apartment listings obtained from the Avito website, spanning across 960 web pages by utilizing Selenium to navigate and scrape information. The raw data was saved in a CSV file, which is available in the `data/` directory of this repository.

#### Data Sources

- **Website**: We collected data from the Avito website, a well-known platform for apartment listings. The website provided detailed information about various apartments, including their attributes and prices.

- **Selenium**: We used Selenium, a web automation tool, to navigate through the website, access individual listing pages, and extract data. Selenium allowed us to interact with the website's elements, such as clicking through multiple pages and scraping information efficiently.


## Data Preprocessing

Before using the collected data for analysis and model development, we conducted a series of preprocessing steps to ensure the dataset's quality and suitability for our goals. The preprocessing phase involved addressing missing values, removing unnecessary columns, and making the data ready for modeling.

#### Handling Missing Values

1. **Columns with High Missing Values**: We identified columns with a significant number of missing values and decided to remove them from the dataset. Columns with excessive missing data may not contribute significantly to our model and can potentially introduce noise.

2. **Rows Missing the Target (Price)**: Rows that were missing the target variable, which is the price of the apartment, were removed from the dataset. Since our primary goal is price prediction, these rows would not provide useful information.

3. **Categorical Values**: For categorical columns with missing values, we filled them with the mode (most frequent value) of the respective column. This approach helps maintain data distribution while addressing missing categorical data.

4. **Numerical Values**: Numerical columns with missing values were imputed using the mean or median, depending on the data distribution. Mean imputation was used for columns with a relatively normal distribution, while median imputation was applied when data exhibited significant skewness.

#### Data Cleaning

In addition to missing value handling, we performed other cleaning tasks, including:

- **Duplicates**: We checked for and removed duplicate rows to maintain data integrity.

- **Outliers**: We assessed the presence of outliers in numerical columns and implemented strategies to either remove or transform these values to ensure they didn't adversely affect our model.

- **Data Types**: We ensured that data types were appropriately set for each column, making sure categorical variables were encoded as such.

The preprocessed data was saved as a CSV file named `preprocessed_data.csv`, which is located in the `data/` directory of this repository. This cleaned and refined dataset served as the basis for building and training our apartment price prediction model.


## Data Visualization

![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)

## Feature Extraction

![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)

## Model Training

![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)

## Model Evaluation

![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)

## Testing on Real Data

![In Progress](https://img.shields.io/badge/Status-In%20Progress-yellow)

