# GEOG5990 Fianl Project
# My title is How does the level of education in different parts of London affect house prices.

# Hypothesis
The higher the house price, the higher the level of education of the population living in the area.

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

11. Calculation and visualisation of the correlation index

Normalise the percentage of highly educated people and the house price classification and calculate the sum of the two as a correlation index. This correlation index provides a comprehensive view of the spatial distribution of education levels and house prices and displays the distribution on a map.

# Reach a verdict

# (i) High correlation areas are concentrated in Central and West London:

As can be seen from the correlation index graphs, the correlation index is higher in Central and West London, with a yellowish-green colour, indicating that there is a stronger positive correlation between the proportion of highly educated people and median house prices in these areas. This means that as the proportion of highly educated people increases in these areas, house prices are correspondingly higher.

# (ii) Weaker correlation in peripheral areas:

In outer London areas, the correlation index is lower and coloured purple, indicating a weaker correlation between the proportion of the population with higher education and median house prices in these areas. The correlation between the proportion of the population with higher education and median house prices is weaker in these areas. This reflects that there is no obvious link between house prices and educational attainment in these districts, or that they are more affected by other factors.

# (iii) There is a clear divide between central and outer boroughs:

Overall, Central and West London not only have higher house prices and a higher proportion of the population with higher education, but also a stronger correlation between the two. The peripheral areas, on the other hand, have lower levels of all three. This centre-periphery divide reflects the uneven distribution of London's economic and educational resources.

# (iv) Policy and urban planning insights:

This concentration of high correlation areas suggests that policy makers and urban planners need to focus on the advantages of central and west London in terms of house prices and educational resources, and also consider how to upgrade the educational level and economic conditions of peripheral areas to narrow the inter-regional gap. For example, by increasing investment in education and improving infrastructure in peripheral areas, it may be possible to help increase the attractiveness of these areas and boost their house prices and education levels.
