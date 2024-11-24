# James-Mwaura-Data-Science-Project1-Repo
Aviation Data Analysis Repository
James Kimani Mwaura 
Data Science(Phase1 Project)
Submitted: 24th November 2024
Project Title: Aviation Data Analysis( Insights into Safety and Risk Management)
Overview/Goal
This project aims to analyze aviation accident data to uncover patterns, assess risks, and provide actionable recommendations to enhance flight safety. The focus includes understanding the impact of weather, aircraft type, and operational conditions on accident outcomes.
Source of the Data
The dataset used for this analysis is the AviationData.csv, which contains detailed records of aviation accidents, including factors such as aircraft make, flight phase, weather conditions, and injury severity. The data has been filtered to include only accidents in the United States to ensure consistency and relevance.
________________________________________
1. Introduction
This project analyzes aviation accident data to identify patterns related to aircraft safety, focusing on injury severity, aircraft make/model, weather conditions, and engine configuration. The goal is to identify factors that contribute to accidents and determine which aircraft are associated with lower-risk profiles.
________________________________________
2. Setting Up the Environment
To begin the analysis, the following Python libraries were imported:
python
Copy code
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
These libraries support data manipulation, numerical operations, and visualization in Jupyter Notebook.
________________________________________

3. Loading and Exploring the Dataset
The aviation accident dataset was loaded into a pandas DataFrame using:
python
Copy code
df = pd.read_csv('AviationData.csv', encoding='ISO-8859-1', low_memory=False)
Dataset Overview:
•	Total Records: 88,889
•	Columns: 31 (including event details, aircraft characteristics, injury severity, etc.)
Key dataset characteristics include:
•	Missing Values: Some columns like Latitude, Longitude, Aircraft Category, etc., have missing values, and these were addressed in data cleaning.
________________________________________
4. Data Cleaning
I. Missing Values
The dataset contains several missing values, such as:
•	52 missing values in Location
•	22,641 missing values in Country
•	54,507 missing values in Latitude
To handle these:
1.	Categorical Fields: Replaced missing values with "Unknown" (e.g., Location, Country, Weather Condition).
2.	Numeric Fields: Filled missing values with 0 or appropriate imputation, like the mode for Engine Type.
3.	Dropped Irrelevant Columns: Columns with excessive missing data, such as FAR.Description and Schedule, were dropped.
The cleaned dataset now has 79,906 entries and 26 columns.
________________________________________
5. Data Analysis
Key Risk-Related Variables:
1.	Aircraft Damage Distribution:
o	Substantial damage: 61,666 incidents
o	Destroyed: 16,419 incidents
2.	Injury Severity:
o	Non-Fatal: 64,458 incidents
o	Fatal: 5,852 incidents
3.	Injury Counts:
o	Fatal Injuries: Mean of 0.38 (max: 265)
o	Serious Injuries: Mean of 0.23 (max: 137)
o	Minor Injuries: Mean of 0.29 (max: 125)
________________________________________
6. Low-Risk Aircraft Analysis
We performed a grouped analysis by aircraft make and model to identify aircraft with low accident severity (low fatalities, serious injuries, and damage).
Top 10 Low-Risk Aircraft:
Make	Model	Total Incidents	Avg Fatal Injuries	Avg Serious Injuries	Avg Damage Severity
BOEING	737-800	20	0	0	0.05
Boeing	717-200	16	0	0.06	0.25
De Havilland	DHC-8-102	10	0	0.1	0.2
Airbus	A300	9	0	0	0									
Recommendation:
•	Boeing 737-800 and Airbus A300 show particularly strong safety records with no fatalities, low damage rates, and moderate incident numbers.
________________________________________
7. Conclusion
Through this analysis, we have identified key risk factors in aviation accidents, including aircraft make/model, weather conditions, and engine configurations. Recommendations based on low-risk aircraft, along with insights into accident trends, can help inform safety improvements in the aviation industry.
Key Insights:
•	Boeing 737-800 stands out for its low accident severity.
•	Weather conditions and aircraft configurations play critical roles in accident rates.
•	Larger engines do not necessarily lead to lower fatality rates.
This project provides actionable insights that could enhance aviation safety measures.


