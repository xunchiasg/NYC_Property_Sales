# NYC Property Sales EDA 
Exploratory Data Analysis of rolling property sales data in NYC from March 2024-2025

## About 
The New York City Department of Finance maintains detailed public records of sales information for properties sold within NYC on an annualized basis since 2003, where detailed transaction metrices such as location, sale price, building class types and floor area are listed. 

[NYC Rolling Sales Data](https://www.nyc.gov/site/finance/property/property-rolling-sales-data.page)

The objective of this project is to analyze and answer the following questions: 

- What are the most popular neighborhoods for homebuyers in terms of transactions?
- What are the trends in transacted property types and their median price?
- What are the most and least expensive neighborhoods for property buying in NYC?

For the purposes of data exploration, only data from a 24-month period of (2023-2024) will be used, with the final findings deployed via a streamlit app. 

## Steps and Deployment 
- Data importation and cleaning (Jupyter Notebook in VS Code, [Data Wrangler](https://code.visualstudio.com/docs/datascience/data-wrangler))
- Univariate Analysis and Data Visualisation (Plotly Express)
- Deployment on Streamlit (Python Script)

### Data importation and cleaning (Jupyter Notebook)
*This section provides an overview on the key steps undertaken to clean and import the data. For detailed steps, refer to 'NYC_Property_Notebook.ipynb'*

The workflow diagram the key criteria and processes undertaken to allow for initial key findings for the provided data. As the DOF provides the yearly data seperated by boroughs, a data processing function was created to allow for data preparation at scale for past years. 
![NYC_Property drawio (1)](https://github.com/user-attachments/assets/ad5f67c3-3872-4850-ba00-97f834ea778e)

## Key Findings 
- The percentage distribution of transactions between boroughs has remained relatively consistent between 2023 and 2024, with Queens, Brooklyn and Manhattan typically taking up about 80% of transactions. 
![pie_chart_1](https://github.com/user-attachments/assets/721f42fc-c762-48c6-aab3-92f2e6e3a598)
![pie_chart_2](https://github.com/user-attachments/assets/640130a1-a185-4ce5-9865-95e1c1a68b5b)

- Overall transactions seem to trend upwards during the summer months (from May to September) between both years with fewer transactions in winter (to December to March); although this will need to be verified with another year as there were no recorded transactions from Jan-Feb 2024 in the provided dataset
![stacked_1](https://github.com/user-attachments/assets/7ae21d03-9f15-46c7-8c46-ffb469994b43)
![stacked_2](https://github.com/user-attachments/assets/b034869c-badd-4e3b-b1d4-6b2f70e6a542)

- The most popular neighborhoods for residential transactions are that of Flushing-North (Queens), Upper East Side (Manhattan) and Upper West Side (Manhattan). Overall, the boroughs of Manhattan and Queens were the most popular 
![neighborhood_1](https://github.com/user-attachments/assets/35fca86b-e24c-49d8-98fe-6b75bfc47dbf)
![neighborood_2](https://github.com/user-attachments/assets/25e14a9c-cfb3-4857-9296-49b3398b6ea1)

## Further Actions 
The EDA steps above allowed for an initial statistical analysis of the provided data to detect categorical trends that can be further explored in detail, particularly in residential dwellings and apartments. 

It also showed via scatterplot a detection of transaction outliers not captured in the data preparation phase, which will have to be addressed before further analysis and feature engineering, potentially leading to linear regression to predict transaction prices for future years. 

The dataset also contains records containing detailed location elements (Neighborhood, Address, ZIP code), which is in line with the Neighborhood Tabulation Areas (NTAs) as defined by the [NYC Department of City Planning](https://www.nyc.gov/content/planning/pages/resources/datasets/neighborhood-tabulation). 

![NYC_NTA](https://github.com/user-attachments/assets/ecd17000-5d48-4f49-9f82-4f9d84e5066b)

*2020 NTA, Geopandas/GeoJSON*

Future processes for geocoding of transactions to spatial datasets provided may also help to add another dimensionality to the above analysis. 

