# NYC Property Sales EDA 
Exploratory Data Analysis of rolling property sales data in NYC from March 2024-2025

## About 
The New York City Department of Finance maintains detailed public records of sales information for properties sold within NYC on an annualized basis since 2003, where detailed transaction metrices such as location, sale price, building class types and floor area are listed. 

[NYC Rolling Sales Data](https://www.nyc.gov/site/finance/property/property-rolling-sales-data.page)

The objective of this project is to analyze and answer the following questions: 

- What are the most popular neighborhoods for homebuyers in terms of transactions?
- What are the trends in transacted property types and their median price?
- What are the most and least expensive neighborhoods for property buying in NYC?

For the purposes of data exploration, only data from a 24-month period of March 2023 to March 2025 will be used, with findings deployed on a Streamlit app. 

## Steps and Deployment 
- Data importation and cleaning (Jupyter Notebook)
- Univariate Analysis and Data Visualisation
- Geocoding of neighborhoods for geospatial analysis (Using NYCOpenData Neighborhood Tabulation Areas)
- Deployment on Streamlit (Python Script)

### Data importation and cleaning (Jupyter Notebook)
*This section provides an overview on the key steps undertaken to clean and import the data. For detailed steps, refer to 'NYC_Property_Notebook.ipynb'*

## Key Findings 
- The percentage distribution of transactions between boroughs has remained relatively consistent between 2023 and 2024, with Queens, Brooklyn and Manhattan typically taking up about 80% of transactions. 
![pie_chart_2](https://github.com/user-attachments/assets/e9279e55-3aa5-44a7-8bc4-3a4ec306c50b)
![pie_chart_1](https://github.com/user-attachments/assets/f62291b3-0155-411b-ad34-7c4c65b22496)

- Overall transactions seem to trend upwards during the summer months (from May to September) between both years with fewer transactions in winter (to December to March); as there are no recorded transactions from Jan-Feb 2024 previous years will need to be implemented to verify this trend.
![stacked_1](https://github.com/user-attachments/assets/c34cf48c-d3cc-4784-aed7-16d56fa45e61)
![stacked_2](https://github.com/user-attachments/assets/0be90e17-cbca-4c4a-95f8-1dd79f853599)

- The most popular neighborhoods for residential transactions are that of Flushing-North (Queens), Upper East Side (Manhattan) and Upper West Side (Manhattan). Overall, the boroughs of Manhattan and Queens were the most popular 
![neighborhood_1](https://github.com/user-attachments/assets/bb0b0136-54e6-4e16-a904-af4dd6c22178)
![neighborood_2](https://github.com/user-attachments/assets/fcac198c-8ea8-47f7-9ff4-761fe1def57f)

## Further Actions 
