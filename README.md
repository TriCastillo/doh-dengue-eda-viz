# DOH-EPI Dengue Data 2016-2021 EDA and Visualization
---
## Table of Contents
1. [Introduction](##introduction)
2. [Dataset Description](##dataset-description)
3. [Objective](Objective)
4. [EDA Overview](EDA-Overview)
5. [Visualizations](Visualizations)
6. [Technologies Used](Technologies-Used)
7. [Project Structure](Project-Structure)
8. [Setup Instructions](Setup-Instructions)
9. [Results and Insights](Results-and-Insights)
10. [Future Work](Future-Work)
11. [Contact Information](Contact-Information)
---
## Introduction
Dengue is a mosquito-borne illness common in warm, tropical areas like our country, the Philippines. It can cause a nasty fever, headaches, muscle and joint aches, nausea, and a rash. 

The big concern is severe dengue, which can lead to bleeding, low blood pressure, and even death. 

With this dataset, we want to determine which factors may lead to more cases or deaths.
---
## Dataset Description
- Dataset Source: [Humanitarian Data Exchange DOH-Epi 2016-2021 Dengue Dataset](https://data.humdata.org/dataset/philippine-dengue-cases-and-deaths/resource/9e839677-3ff0-44b3-992c-1a99e68df515)
- Key Features:
  - ```loc```: City or province of entry
  - ```cases```: Number of dengue cases in a location and a given date
  - ```deaths```: Number of dengue deaths in a location and a given date
  - ```date```: Date when cases and death entries are recorded
  - ```Region```: Region where entry was recorded
 ---
 ## Objective
 - Identify factors contributing to dengue cases or deaths
 - Explore relationships between variables like cases-deaths, entry date, and region.
 - Visualize patterns and trends changing over time.
 ---
 ## EDA Overview
 - ```cases``` & ```deaths``` vs ```date```: Visualized using line charts and observed peaks in cases during the COVID-19 outbreak and deaths in 2016 during the Dengvaxia Controversy.
 - Examined the relationship between ```cases``` and ```deaths``` using a scatterplot and identified that both features have no relationship.
 - Observed weak correlation among all variables which may suggest that a non-linear approach would be appropriate going further.
 - Detected an irrelevant row in the dataset which was dropped as it may affect the results
 - Imputed missing data using the column median to retain data integrity.
 - No duplicates were detected in the dataset
 - A drop in the trend over time was observed due to insufficient entries
 
 ---
 ## Visualizations
 1. Dengue cases and deaths over time: Examined using line charts
 2. Relationship of Cases-Deaths: Visualized using scatterplot
 3. Correlation of each feature: Reviewed using a heatmap
 4. Total cases and deaths by region: Constructed with the use of pie charts
 5. Case-Death summary by location: Formed with stacked bar charts
 ---
 ## Technologies Used
 - Languages: Python
 - Libraries: Pandas, NumPy, Matplotlib, Seaborn
 - Tools: Jupyter Notebook
 ---
 ## Project Structure
 - data/
   - doh-epi-dengue-data-2016-2021.csv
 - notebooks/
   - doh-eda-viz.ipynb
 - README.md
 - requirements.txt
 ---
 ## Setup Instructions 
 1. git clone https://github.com/TriCastillo/doh-dengue-eda-viz.git
 2. Install dependencies:
    - ```pip install -r requirements.txt```
 3. Run the notebook
 --- 
 ## Results and Insights 
 - There is no direct connection between cases and deaths; the increase in cases does not affect the deaths and vice versa.
 - The nature of the country being warm and humid is an ideal breeding ground for mosquitos.
 - More people, more human footprints, more cases
 --- 
 ## Future Work 
 - Enhance visualizations with interactive dashboards
 - Non-linear predictive model implementation for further analysis
 --- 
 ## Contact Information
 You may reach out to me via:
 - LinkedIn: [Reynaldo III Castillo](https://www.linkedin.com/in/reynaldo-iii-castillo-975120303/)
 - Email: [Gmail](reynaldoiii.castillo@gmail.com)

  

