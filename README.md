# NYC Property Sales EDA 
Exploratory Data Analysis and Visualisation of rolling property sales data in NYC from 2023 to 2024.

## About 
The New York City Department of Finance maintains detailed public records of sales information for properties sold within NYC on an annualized basis since 2003, where detailed transaction metrices such as location, sale price, building class types and floor area are listed. 

[NYC Rolling Sales Data](https://www.nyc.gov/site/finance/property/property-rolling-sales-data.page)

The objective of this project is to analyze and answer the following questions: 

- What are the most popular neighborhoods for homebuyers in terms of transactions?
- What are the trends in transacted property types and their median price?
- What are the most and least expensive neighborhoods for property buying in NYC?

For the purposes of this repository data from a 24-month period of (2023-2024) will be used with findings published within a Jupyter notebook.  

## Steps and Deployment 
- Data importation and cleaning (Jupyter Notebook in VS Code, [Data Wrangler](https://code.visualstudio.com/docs/datascience/data-wrangler))
- Analysis and Data Visualisation (Plotly Express)

### Data importation and cleaning (Jupyter Notebook)
*This section provides an overview on the key steps undertaken to clean and import the data. For detailed steps, refer to 'NYC_Property_Notebook.ipynb'*

The workflow diagram the key criteria and processes undertaken to allow for initial key findings for the provided data. As the DOF provides the yearly data seperated by boroughs, a data processing function was created to allow for data preparation at scale for past years. 

![NYC_Property drawio](https://github.com/user-attachments/assets/7f207283-ef0d-4196-8b16-ce68871585a1)

An aspect of the data provided also necessicated the record removal of what is known as a '$0 sale price', or nominal/token sale prices - indicating transfer of property ownership with no cash consideration. Datapoints with very high sale prices known to be outlier (determined to be in excess of USD $2million) were left as-is, owing to the existence of such properties, typically within Manhatten. The final dataset for the period of 2 years contains approximately 92,400 records.

![scatter](https://github.com/user-attachments/assets/16e503fe-bfeb-4381-8e5c-4a2e76e5dab6)

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

- The percentage distribution of transactions between boroughs has remained relatively consistent between 2023 and 2024, with Queens, Brooklyn and Manhattan typically taking up about 80% of transaction volume.

![trans_vol_23](https://github.com/user-attachments/assets/efd07809-8348-449b-9dd3-2133c1ebbd3f)
![trans_vol_24](https://github.com/user-attachments/assets/11171ccc-e2d3-467b-badc-101f3124c77d)

- Overall transactions seem to trend upwards during the summer months (from May to September) between both years with fewer transactions in winter (to December to March); although this will need to be verified with another year as there were no recorded transactions from Jan-Feb 2024 in the provided dataset
![stacked_trans_23](https://github.com/user-attachments/assets/bb295c62-c462-46c5-81a6-f800241107eb)
![stacked_trans_24](https://github.com/user-attachments/assets/fe378ea3-0904-41c6-bebc-e11d8b0138c3)

- The most popular neighborhoods for residential transactions are that of Flushing-North (Queens), Upper East Side (Manhattan) and Upper West Side (Manhattan), remaining consistent throughout both years. Overall, the boroughs of Manhattan and Queens were the most popular.
![top_10_23](https://github.com/user-attachments/assets/244bfcda-a8d1-4de4-88c4-02265452744d)
![top_10_24](https://github.com/user-attachments/assets/ceb065af-0109-4c01-b61a-15441b0f5e1e)

In terms of building types, Elevator Apartments (Coop and Condos), as well as One and Two Family dwellings were the most commonly transacted type of properties. Owing to the range of properties and sale prices within NYC, only transactions below USD $5 were considered. 

![building_23](https://github.com/user-attachments/assets/260e547d-b1ae-444c-b82a-f6df402e1347)
![building_24](https://github.com/user-attachments/assets/18c8c66d-6868-4f78-9b24-7448d02d7b66)

## Further Actions 
The EDA steps above allowed for an initial exploration and analysis of the dataset to provide transactional trends that can be further explored in detail, particularly in residential dwellings and apartments. 

It also showed via scatterplot a detection of transaction outliers not captured in the data preparation phase. For more detailed analysis towards potential use in Machine Learning models outlier treatment will have to be determined. 

The dataset also contains records containing detailed location elements (Neighborhood, Address, ZIP code), which is in line with the Neighborhood Tabulation Areas (NTAs) as defined by the [NYC Department of City Planning](https://www.nyc.gov/content/planning/pages/resources/datasets/neighborhood-tabulation). Data tranformation to incoprate this the NTA will also allow for deatiled analysis in terms of dimensionality, particularly in the geospatial aspect. 

![NYC_NTA](https://github.com/user-attachments/assets/ecd17000-5d48-4f49-9f82-4f9d84e5066b)

*2020 NTA, Geopandas/GeoJSON*


