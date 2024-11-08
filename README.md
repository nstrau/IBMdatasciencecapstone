# IBM Data Science Capstone Project: Predicting Falcon 9 First Stage Landing Success
Project Overview
This project aims to predict the success of Falcon 9 first-stage landings, which allows SpaceX to reduce launch costs by reusing rockets from successful landings. Predicting whether the first stage will land successfully can help other companies assess competitive bids for launches.


# Project Files and Notebooks
The project is organized into the following steps:

1. Data Collection
data_collection.ipynb: Collected Falcon 9 launch data using the SpaceX API and transformed it into a usable format by cleaning and structuring the response data.
webscraping.ipynb: Extracted additional launch records from Wikipedia using BeautifulSoup. The HTML table data was parsed and converted into a Pandas DataFrame for further analysis.
2. Data Wrangling
data_wrangling.ipynb: Performed exploratory data analysis to understand the dataset and identify training labels. This stage involved handling missing values, formatting data, and preparing the initial features.
3. Exploratory Data Analysis (EDA) with SQL
EDA_exploratory_data_analysis.ipynb: Loaded the dataset into a Db2 database and conducted SQL queries to gain insights into the Falcon 9 data.
4. EDA with Data Visualization
eda_data_visualiz.ipynb: Explored and visualized key features of the data using Matplotlib. This step focused on understanding trends, correlations, and distributions for feature engineering.
5. Interactive Data Visualization with Folium
visual_analytics_folium.ipynb: Created an interactive map with Folium, marking each launch site with labels indicating success or failure. This map includes distances from the launch sites to various proximities to visualize launch conditions and success factors.
6. Interactive Dashboard with Plotly Dash
spacex_dash.py: Built an interactive dashboard using Plotly Dash to allow users to analyze and visualize SpaceX launch success rates across the launch sites. The app includes a dropdown to filter launch sites, a pie chart to view launch success distribution per site, a payload range slider, and a scatter plot to explore how the payload mass correlates with the success rate.
7. Machine Learning Modeling
spacex_ML_pred.ipynb: Conducted machine learning analysis, including feature engineering, data standardization, and model evaluation. SVM, Classification Trees, and Logistic Regression models were trained, and hyperparameters were optimized to identify the best-performing model for predicting the first stage’s landing success.

# Data Files
spacex_web_scraped.csv: A CSV file containing data scraped from Wikipedia, including information on Falcon 9 launches, to supplement the SpaceX API data.
dataset_part_1, dataset_part_2, and dataset_part_3: Intermediate datasets generated during the data collection and wrangling processes.

# Installation and Setup
To run this project, you need the following libraries:

Pandas, Matplotlib, Seaborn for data manipulation and visualization
Folium for mapping and geographical data visualization
Plotly Dash for building the interactive dashboard
BeautifulSoup for web scraping
Scikit-learn for machine learning modeling

Usage
Data Collection: Start with data_collection.ipynb and webscraping.ipynb to retrieve and clean data from SpaceX API and Wikipedia.
Data Wrangling: Run data_wrangling.ipynb to prepare the dataset for EDA.
Exploratory Data Analysis: Use EDA_exploratory_data_analysis.ipynb and eda_data_visualiz.ipynb to explore the data with SQL queries and visualizations.
Interactive Visualizations: View the visual_analytics_folium.ipynb and spacex_dash.py files to interact with the visualized data through maps and dashboards.
Machine Learning: Open spacex_ML_pred.ipynb to run the models, optimize hyperparameters, and determine the best prediction model.

# Results
After exploring, visualizing, and modeling the data, the project yielded the following insights:

Key factors influencing landing success include launch location, payload, and booster version.
Logistic Regression performed best among the models tested, providing a reliable method to predict the first-stage landing outcome.
Future Work
Further analysis could include:

Analyzing additional external factors like weather conditions or wind speeds at launch.
Incorporating real-time tracking data and expanding the model to more complex deep learning architectures.
Acknowledgments
Special thanks to IBM and Coursera for providing the dataset and project guidance. This project is part of the IBM Data Science Professional Certificate Capstone course.

