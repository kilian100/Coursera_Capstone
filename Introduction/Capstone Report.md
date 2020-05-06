# Coursera_Capstone

## **Peer-graded Assignment: Capstone Project - The Battle of Neighborhoods part 1**

###  **1) Introduction**

**A- Business Problem**

The purpose of this Project is to help people in exploring better facilities around their neighborhood. It will help people making smart and efficient decision on selecting great neighborhood out of numbers of other neighborhoods in Paris 16, Paris .

Lots of people are migrating to France and needed lots of research for good housing prices and reputated schools for their children in Paris. This project is for those people who are looking for better neighborhoods in Paris. For ease of accessing to Cafe, School, Super market, medical shops, grocery shops, mall, theatre, hospital, like minded people, etc.

This Project aim to create an analysis of features for a people migrating to Paris 16 to search a best neighborhood as a comparative analysis between neighborhoods. The features include median housing price and better school according to ratings, crime rates of that particular area, road connectivity, weather conditions, good management for emergency, water resources both freash and waste water and excrement conveyed in sewers and recreational facilities.

It will help people to get awareness of the area and neighborhood before moving to a new city, state, country or place for their work or to start a new fresh life.

**B- Problem Which Tried to Solve**

The major purpose of this project, is to suggest a better neighborhood in a new city for the person who are shiffting there. Social presence in society in terms of like minded people. Connectivity to the airport, bus stand, city center, markets and other daily needs things nearby.

Sorted list of house in terms of housing prices in a ascending or descending order
Sorted list of schools in terms of location, fees, rating and reviews


 ### 2) Downloading and Prepping Data
 Describe the data that you will be using to solve the problem or execute your idea. Remember that you will need to use the Foursquare location data to solve the problem or execute your idea. You can absolutely use other datasets in combination with the Foursquare location data. So make sure that you provide adequate explanation and discussion, with examples, of the data that you will be using, even if it is only Foursquare location data.
 
- Will use Paris dataset from : https://opendata.paris.fr/explore/embed/dataset/arrondissements/table/?location=12,48.85889,2.34692&basemap=jawg.streets&dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6ImFycm9uZGlzc2VtZW50cyIsIm9wdGlvbnMiOnt9fSwiY2hhcnRzIjpbeyJhbGlnbk1vbnRoIjp0cnVlLCJ0eXBlIjoiY29sdW1uIiwiZnVuYyI6IkFWRyIsInlBeGlzIjoibl9zcV9hciIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiMwMDMzNjYifV0sInhBeGlzIjoibl9zcV9hciIsIm1heHBvaW50cyI6NTAsInNvcnQiOiIifV0sInRpbWVzY2FsZSI6IiIsImRpc3BsYXlMZWdlbmQiOnRydWUsImFsaWduTW9udGgiOnRydWV9

- We will also use data from Housing statistics : https://www.pap.fr/actualites/immobilier-les-prix-montent-partout-en-ile-de-france/a21568

- And from School Rating journals in France: https://www.letudiant.fr/palmares/classement-lycees/academie-paris.html


**Foursquare API Data:**
We will need data about different venues in different neighborhoods of that specific borough. In order to gain that information we will use "Foursquare" locational information. Foursquare is a location data provider with information about all manner of venues and events within an area of interest. Such information includes venue names, locations, menus and even photos. As such, the foursquare location platform will be used as the sole data source since all the stated required information can be obtained through the API.

After finding the list of neighborhoods, we then connect to the Foursquare API to gather information about venues inside each and every neighborhood. For each neighborhood, we have chosen the radius to be 100 meter.

The data retrieved from Foursquare contained information of venues within a specified distance of the longitude and latitude of the postcodes. The information obtained per venue as follows:

1. Neighborhood
2. Neighborhood Latitude
3. Neighborhood Longitude
4. Venue
5. Name of the venue e.g. the name of a store or restaurant
6. Venue Latitude
7. Venue Longitude
8. Venue Category

### 3) Methodology Section

**Clustering Approach:**

To compare the similarities of two cities, we decided to explore neighborhoods, segment them, and group them into clusters to find similar neighborhoods in a big city like New York, Toronto or Paris. To be able to do that, we need to cluster data which is a form of unsupervised machine learning: k-means clustering algorithm.

**Using K-Means Clustering Approach**

The main objective of K-means clustering is to minimize the distance of data points from the centroid of it's cluster and maximize the distance from other cluster centroids. That is we try to reduce this error. K-means can group data only unsupervised based on the similarity of customers to each other. So, in this step, we have to find the closest centroid to each data point here our neigbourhoods.

![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2003.45.40.png)
Fig1

**Most Common venues near Neighborhood**
We determined here the 10 most common venues near our neighborhoods
![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2003.46.37.png)
Fig2

### **Work Flow**

we used Foursquare to mine  near-by places of the neighborhood.


### **4) Results Section**

**Map of Clusters in Paris**

The first part was to produce the map of Paris using our geolocation algorithm

![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2003.47.09.png)
Fig3

**Average Housing Price by Clusters in Paris**

![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2003.48.44.png)
Fig4

AHP Distribution
![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2004.48.29.png)
Fig5

From this graph, we can see that, the location with the highest average housing price is Paris 6th Neighbourhood with 13700€ per m2, and the location with the lowest Average Housing Price is Paris 19 with 8580€ per m2. The Mean AHP is 10936€ per m2 and more than 75% of the locations have AHP more than 12412.5 which is only 1857€ away from the 1st 50% of the distribution and 2682€ from the 1st 25%.    

**School Ratings by Clusters in Paris**

![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2003.48.52.png)
Fig6

SR Distribution
![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2004.46.45.png)
Fig7

From the above diagram, we can see that most locations have high school ratings varying from 9 to 6 based on the general results of the area during official exams. 
**Cross Tables showing Top School Rating and Average_Housing_Price per Neigbourhood**

![](https://github.com/kilian100/Coursera_Capstone/blob/master/Screenshot%202020-05-06%20at%2003.49.02.png)
Fig8

By combining both diagrams we have the locations and their Average Housing Prices(AHP) crossed with the school ratings(SR). We can Therfore see that some locations have high AHP but low SR like Paris 1st Neighbourhood with a rating of 6 but an AHP of 13210€ per m2. Others like Paris 19 have high SR and low AHP, which is the most suitable area with regards to the AHP and SR. Again, the location is immediately surrounded by supermarkets, restaurants and pools, which are suitable for individuals getting into paris for the first time as they have all they need nearby.

### **5. Discussion Section**

The major purpose of this project, is to suggest a better neighborhood in a new city for the person who are shiffting there. Social presence in society in terms of like minded people. Connectivity to the airport, bus stand, city center, markets and other daily needs things nearby.

It'll be more interesting to include other aspects like security and exposure to disasters like now the coronavirus. Being in a location which may reduce the impact or the risk of being affected by such unforseen contingencies.

### **6. Conclusion Section**

In this project, using k-means cluster algorithm I separated the neighborhood into 5 different clusters , which have very-similar neighborhoods around them. Using the charts above results presented to a particular neighborhood based on average house prices and school rating have been made.
We analyzed Paris' neighbourhood and saw the most common venues in the city's neighbourhood, then in an attempt to minimize the distance from the different points and venues we produced a k-means map of our sample data.
We then had the different clusters (5) which we the grouped and examined. We then compared these results with two other factors, ie, the Average housing price and the School Ratings. 
We thus conclude that the most appropriate location with the lowest AHP and highest SR is the 19th Paris Neigbourhood.



