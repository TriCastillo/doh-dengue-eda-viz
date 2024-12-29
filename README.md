# DOH-EPI Dengue Data 2016-2021 EDA and Visualization
---

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Objective](#Objective)
4. [EDA Overview](#EDA-Overview)
5. [Visualizations](#Visualizations)
6. [Technologies Used](#Technologies-Used)
7. [Project Structure](#Project-Structure)
8. [Setup Instructions](#Setup-Instructions)
9. [Results and Insights](#Results-and-Insights)
10. [Future Work](#Future-Work)
11. [Contact Information](#Contact-Information)
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
 ### Dengue cases and deaths over time: Examined using line charts
 ![Dengue Cases by Year Line Chart](https://github.com/user-attachments/assets/7d82eda0-76f5-4c02-9f2f-d83596a58d5d)

 According to the line chart, **cases peaked** in the year **2019**, during the COVID-19 outbreak. But turns out to be a **misdiagnosis between COVID-19 and dengue (Khairunisa et al., 2021).

 ![Dengue Deaths by Year Line Chart](https://github.com/user-attachments/assets/a8d31434-5314-4f5c-8315-dc58303e6438)

**Deaths peaked** in the year **2016**, during the **Dengvaxia Controversy** as it was discovered that it may lead to more severe symptoms of dengue, with some resulting in death (Santos, 2019).

There has been a **decline** (2016-2018) in deaths ever since Dengvaxia had been discontinued.
 
 ### Relationship of Cases-Deaths: Visualized using scatterplot
 ![Cases-Deaths Relationship visualized with Scatterplot](https://github.com/user-attachments/assets/0f559966-622f-4cdb-ad12-e080cb020913)

 The scatterplot figure shows **NO RELATIONSHIP** between the two variables (Deaths, Cases). A higher count of cases doesn't mean more deaths, and vice versa.

 ### Correlation of each feature: Reviewed using a heatmap
 ![Feature Correlation Heatmap](https://github.com/user-attachments/assets/e35c1500-946f-4b38-ac0f-8168724db56b)

The correlation heatmap provides a visual representation of the relationship of each feature variable in the dataset with most values close to 0, indicating a **weak** or **non-linear relationship** among these features.

This may suggest that a **non-linear approach** to explore non-linear patterns would be appropriate going further.

 ### Total cases and deaths by region: Constructed with the use of pie charts
 ![Dengue Cases by Region Pie Chart](https://github.com/user-attachments/assets/4f678bbc-abd5-4a9b-9fd7-954e66b06ef6)

 Considering that the Philippines is a tropical country, making it **warm and humid**, after experiencing heavy rainfall throughout the year, an ideal breeding ground for mosquitoes (Ogliore, 2024).

 According to PhilAtlas, the top 3 regions in population are CALABARZON, NCR, and Central Luzon. Recent studies have proven that **populous areas** along with **poor sanitation**, including inadequate waste disposal and the presence of standing water, significantly contribute to more habitat for mosquitoes and dengue transmission (Agrupis et al., 2019 and Medina et al., 2023)

 ![Dengue Deaths by Region Pie Chart](https://github.com/user-attachments/assets/152310e5-fce2-4fc8-bb4b-686f48861d8a)

 Dengue deaths are mostly located around NCR, Visayas regions, and Central Mindanao. Calabarzon may be the top region with the most cases but isn't present in the top 5 regions by deaths.

 A recent study by De Vera et al. (2021) identified that **poor healthcare infrastructure** or even **substandard living conditions** contributes to the high incidence and mortality rates of dengue in the Philippines.

 ### Case-Death summary by location: Formed with stacked bar charts
 ![Dengue Cases and Deaths in CALABARZON Stacked Bar Chart](https://github.com/user-attachments/assets/5bbd90fb-867f-4716-bf07-e21fa5b3e7d0)

 In the CALABARZON region, various climate factors such as humidity and temperature, were associated (Magtibay et al., 2020)

 The region was not present in the top 5 regions in deaths due to the region actively spreading awareness (PNA, 2019)

 ![Dengue Cases and Deaths in NCR Stacked Bar Chart](https://github.com/user-attachments/assets/aa0a9275-8f4b-4e35-80a7-df5af8351835)

 According to GMA (2019), when it comes to the amount of trash in Quezon City, consider the geographic location of the area and number of squatters.

 The geographic and population factors may have contributed to its death count.
 ---
 
 ## Technologies Used
 - Languages: Python
 - Libraries: Pandas, NumPy, Matplotlib, Seaborn
 - Tools: Jupyter Notebook
 ---
 
 ## Project Structure
 - doh-epi-dengue-data-2016-2021.csv
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

  

