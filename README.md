# COVID19_Violations_Nashville

## Data Question 4: Nashville COVID-19 Violations
This project is a group project in collaboration with: https://github.com/jasonamyers and https://github.com/matttparker


Exploring COVID-19 violations reported to hubNashville, Metro Nashville government's comprehensive customer service system

### Part 1:
- Gathered data from hubNashville https://data.nashville.gov/Public-Services/hubNashville-311-Service-Requests/7qhx-rexh. 
- Looked at requests with Request Type of "COVID-19" and Subrequest Type of "COVID-19 Violations"
- Explored this dataset and looked at when and where these violations occurred
- Visualized Business Types by Google Place Tags
- Used Geocodio to match as many locations as possible to US addresses

<p float="left">
  <img src="https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/ClusterMap.PNG" width="380" />
  <img src="https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/zoomed.PNG" width="450" />
</p>


### Part 2:
- The file davidson_cases.csv contains the number of COVID cases in Davidson county per day from March 8 through October 29
- Used this dataset to compare the trend for the number of cases over time to the number of reported violations 
- Plotted the rolling average of violations and Covid cases in Nashville per week to look for patterns

<p float="left">
  <img src="https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/rolling_av1.png" width="550" />
</p>

<p float="left">
  <img src="https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/rolling_av2.png" width="550" />
</p>

### Part 3:
- The Metro Public Health Department tracks COVID-19 clusters
- The files `clusters.csv` and `clusters_by_type.csv` contain the tables of clusters as reported by [WSMV](https://www.wsmv.com/news/metro-health-releases-latest-covid-19-clusters/article_ef554e08-1558-11eb-b290-873345e174d7.html) along with the coordinates of the clusters
- Examined connections between the reported COVID violations and subsequent COVID clusters



<p float="left">
  <img src="https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/ClusterByNumRepViolations.PNG" width="500" />
  <img src="https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/NumByClusterLocation.PNG" width="500" />
</p>

### Part 4:
- The dataset from data.nashville.gov includes geospatial information, which allows you to see where violations occurred geographically, but it does not provide information in regard to the specific businesses that were reported. 
- Explored the businesses and types of businesses that have been reported using a heatmap

![](https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/heatmap.PNG)

- Took data from the [Google Places API](https://developers.google.com/places/web-service/overview). The values are as follows:
* `mapped_location`: The mapped location from the hubNashville dataset
* `address`: The address from the hubNashville dataset
* `results`: The first five results from a Google Maps API nearbysearch, ranked by proximity to the Mapped Location. See https://developers.google.com/places/web-service/search#PlaceSearchResponses for more details on the fields in the results.

- Matched as many violations as possible to a business using FuzzyWuzzy
- Looked into the types of businesses that have been reported for COVID violations and how behavior changed after an outbreak at a location

![](https://github.com/savyrosea/COVID19_Violations_Nashville/blob/main/pictures/Lines.PNG)

