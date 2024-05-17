# GEOG5990
# My title is How does the level of education in different parts of London affect house prices.

1. Loading data
First, two CSV files are loaded from the specified path, containing data on the highest level of education and median house price data for 2014-2015.The median house price data for each MSOA area in London is data I obtained from the CDRC website at the following link (see: https://data.cdrc.ac.uk/dataset/cdrc-median-house-prices-geodata-pack-1995-2015-city-of- london-e09000001). Then the level of educational attainment of the population in each MSOA borough in London I got from the 2011 UK Census.

2. Merging data sets
The education attainment data and house price data were first merged together via the London MSOA codes.The merged dataset contains information on educational attainment and median house prices for each MSOA in London, which facilitates further analysis and visualisation.



3. Calculation of the percentage of the population with a high level of education and with a low level of education
Calculation of the proportion of the population with high and low levels of qualifications in each MSOA in London. Higher education levels include Highest_level_of_qualification_Level_3_qualifications_and_Highest_level_of_qualification_Level_4_qualifications_and_above, low education levels include Highest_level_of_qualification_Level_1_Level_2_or_Apprenticeship.

4. Data standardisation
StandardScaler is the standardisation of data. StandardScaler allows K-mean clustering to be performed in such a way that differences in the proportions of different features do not affect the clustering results.

5. K-means clustering
The data obtained after standardisation was subjected to cluster analysis using K-means. The data was divided into 3 clusters, which were used to show the relationship between high education levels and the distribution of house prices, in preparation for the subsequent scatterplot.The main process of K-means clustering is to classify points and then minimise their distance from their centre of mass.

# Non-spatial data visualisation

6. Non-spatial data visualisation of the resulting clustering results for high education levels
The Seaborn library was borrowed to create a scatterplot to show the relationship between the percentage of highly educated people and the median house price, and then the different clusters were represented in purple, green and yellow respectively. Its main purpose is to better distinguish.

# Spatial data processing and visualisation

7. Loading GeoJSON files
Load a GeoJSON file containing the geographic boundaries of London from the specified path. This file contains geographic boundary information for each MSOA and is used for spatial data visualisation.

8. Merging the GeoDataFrame with the clustering results
Merge the geographic boundary data with the clustering results calculated earlier. This allows the clustering results for each MSOA to be displayed on a map for spatial data analysis and visualisation.

9. Spatial data visualisation of the percentage of people with high levels of educational attainment
GeoPandas was used to create a map showing the distribution of the percentage of people with high levels of education in each region. Different colours represent different percentages of people with high levels of education, which allows us to visualise the distribution of education levels in each region of London.

10. Classification and visualisation of median house prices
Based on the median house price quartile, house prices are categorised into five classes and maps are created to show the spatial distribution of different house price ranges. This provides a clearer picture of the distribution of house prices by region.
