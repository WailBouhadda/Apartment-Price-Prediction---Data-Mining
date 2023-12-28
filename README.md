# Apartment-Price-Prediction---Data-Mining


#### Author:  - <a href="https://github.com/WailBouhadda">Wail Bouhadda</a>

## Table of Contents

- [Project Overview](#project-overview)
- [Data Collection](#data-collection)
- [Data Preprocessing](#data-preprocessing)
- [Data Visualization](#data-visualization)
- [Feature Extraction](#feature-extraction)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)

## Project Overview

Welcome to the Apartment Price Prediction project, where we employ data mining techniques to predict apartment prices. Our goal is to build a robust machine learning model that can accurately predict apartment prices based on various features.

#### Project Goals

- Collect a comprehensive dataset of apartment listings, including essential attributes such as location, type, price, and more.
- Utilize data mining techniques to preprocess and clean the dataset for analysis.
- Develop and train a machine learning model to predict apartment prices.
- Evaluate the model's performance and provide insights into feature importance.
- Create a practical tool for individuals interested in estimating apartment prices in the target area.

## Data Collection

In this project, we undertook a comprehensive data collection process to gather information about apartments available for sale in morocco. Our dataset consists of approximately 33,000 apartment listings obtained from the Avito website, spanning across 960 web pages by utilizing Selenium to navigate and scrape information. The raw data was saved in a CSV file named `Apartment.csv`, which is available in the `data/` directory of this repository.


![originale dataset](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/3bdbe02b-167d-4cc0-9e18-ff5d998d3339)


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

![missingvalues](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/2a89a3b6-0ee1-485f-9bd4-4aca05b3ec83)

#### Data Cleaning

In addition to missing value handling, we performed other cleaning tasks, including:

- **Duplicates**: We checked for and removed duplicate rows to maintain data integrity.

- **Outliers**: We assessed the presence of outliers in numerical columns and implemented strategies to either remove or transform these values to ensure they didn't adversely affect our model.

- **Data Types**: We ensured that data types were appropriately set for each column, making sure categorical variables were encoded as such.

The preprocessed data was saved as a CSV file named `data.csv`, which is located in the `data/` directory of this repository. This cleaned and refined dataset served as the basis for building and training our apartment price prediction model.

![data](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/25c1bbed-3c85-49df-977d-d8188ef0f682)

## Data Visualization

In this section, we explore the dataset through visualizations to gain insights into the relationships between variables and the distribution of apartment prices.

### Scatter Plot - Price vs. Surface Habitable

We visualize the distribution of apartment prices based on the surface habitable to identify any trends or patterns.

![prixXsurface](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/2774ff30-2ec2-4cac-a818-179fd2b99309)

### Average Price and Surface Habitable by City

To understand the average price and surface habitable in different cities, we create a visualization that provides insights into regional variations.

![Average_Price_And_Surface_By_City](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/bf128e9c-9265-4482-9d04-febd069c64ae)

### Boxplot - Price Distribution

A boxplot is used to visualize the distribution of apartment prices, allowing us to identify outliers and assess the spread of the data.

![prix](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/54c41867-247f-4542-a659-9bb63cf46618)

### Boxplot - Surface Distribution

A boxplot is used to visualize the distribution of apartment Surface, allowing us to identify outliers and assess the spread of the data.

![surface](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/4d55c8b7-996e-4c4b-b252-956a2ebb5148)

### KDE Plot - Price Density

Kernel Density Estimation (KDE) plot helps visualize the density of apartment prices, providing insights into the distribution characteristics.

![density prix](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/352916bd-b1ba-444f-b4c1-26abdc8b990a)

The visualizations above offer valuable insights into the dataset, guiding our feature extraction and modeling decisions.


## Feature Extraction

In this section, we focus on feature extraction, aiming to identify and select the most relevant features for our predictive model.

### Selected Features

We carefully choose features that contribute significantly to predicting apartment prices. This process involves analyzing correlations, feature importance from models, and domain knowledge.

- Etage
- Surface habitable
- NB Salons
- NB Chambres
- NB Salles de Bain
- Ville
- **Longitude and Latitude:** We transformed the 'ville' (city) feature into two separate features representing the longitude and latitude. This allows the model to capture geographical information that may influence apartment prices.

### Feature Engineering

We explore opportunities for feature engineering, including transformations, scaling, or creating new features that enhance the model's predictive power.

![dataafter](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/a47cd9af-3caa-42fe-bb4e-07f0a7f91235)

## Model Training

In this section, we embark on the process of training machine learning models for predicting apartment prices. The goal is to explore and compare the performance of different regression models, each with its unique strengths and characteristics.

### Linear Regression Model

We begin with the linear regression model, a fundamental approach that assumes a linear relationship between the input features and the target variable. This model is well-suited for capturing straightforward dependencies and providing a baseline for comparison.

### Decision Tree Regressor

Moving beyond linear relationships, we delve into the decision tree regressor. This model is capable of capturing non-linear patterns and interactions within the data. Decision trees are intuitive, and their ability to create complex decision boundaries makes them a valuable tool for regression tasks.

### Random Forest Regressor

To enhance predictive accuracy and robustness, we introduce the random forest regressor. This ensemble learning method combines multiple decision trees to achieve improved generalization and performance. Random forests can handle a variety of data complexities and are particularly useful for capturing intricate relationships in the dataset.

The choice of these models allows us to explore different aspects of the data, from linear trends to complex non-linear patterns. Each model will be trained on the prepared dataset, and their performance will be evaluated using appropriate metrics in the subsequent "Model Evaluation" section.

## Model Evaluation

In this section, we thoroughly assess the performance of our trained regression models using a variety of evaluation metrics. These metrics provide insights into the models' predictive accuracy and their ability to generalize to unseen data.

### Evaluation Metrics

We employ a set of key regression metrics to rigorously evaluate the performance of each model:

- **Mean Squared Error (MSE):** Measures the average squared difference between predicted and actual values.
- **Root Mean Squared Error (RMSE):** The square root of the MSE, providing a measure in the original units of the target variable.
- **Mean Absolute Error (MAE):** Represents the average absolute difference between predicted and actual values.
- **R-squared (\(R^2\)):** Measures the proportion of the variance in the target variable explained by the model.

### Results

We present the evaluation results for each model, offering a comprehensive overview of their strengths and limitations. A tabular format is utilized to showcase the quantitative performance metrics, including MSE, RMSE, MAE, and \(R^2\), allowing for easy comparison between models.

| Model                 | MSE         | RMSE        | MAE         | \(R^2\)      |
|-----------------------|-------------|-------------|-------------|-------------|
| Linear Regression     | 60496006281.157875 | 245959.35900298218 | 186331.35502839476 | 0.4932979852838194 |
| Decision Tree         | 63876268662.44258 | 252737.54897609216 | 171665.33411296006 | 0.4649856079195017 |
| Random Forest         | 43151803581.3871 |  207730.12198857224 | 146485.15010682642 | 0.6385694336299377  |

### Scatter Plots

In addition to numerical metrics, we provide scatter plots for each model to visually represent the differences between predicted and actual values. Each plot highlights the model's performance in capturing the underlying patterns in the data.


- **Linear Regression Scatter Plot**

![LinearRegression](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/65392dcd-32d4-4c66-ba92-e70f501b7fd0)

- **Decision Tree Scatter Plot**

![decision Tree](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/23951af1-295d-4e42-8ca5-76817dda785d)

- **Random Forest Scatter Plot**

![RF](https://github.com/WailBouhadda/Apartment-Price-Prediction-and-Valuation-Using-Data-Mining/assets/47559086/08cec68f-4427-40ab-ad12-8fdbff744920)

These scatter plots offer a visual understanding of how well the models align with the true values, providing valuable insights into the strengths and weaknesses of each regression approach.
