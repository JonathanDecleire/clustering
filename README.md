# Chipotle clustering challenge

![clustering](https://files.realpython.com/media/K-Means-Clustering-in-Python_Watermarked.14dc56523461.jpg)

## Context
Name of the project: Chipotle clustering challenge
Context of the project: BeCode, Liège Campus, AI/Data Operator Bootcamp, February 2021
Objective of the project: 
- be able to use geopandas, matplotlib (and seaborn) to visualize clustered data onto a map.
- be able to determine appropriate clustering methods and variables to cluster.
- be able to allot the right amount of time for the tasks and present the results onto a readable GitHub page.


### Description
In this project we create a Python script to run, test and improve our cluster model.
Clustering is useful for exploring data. If there are many cases and no obvious groupings, clustering algorithms can be used to find natural groupings. Clustering can also serve as a useful data-preprocessing step to identify homogeneous groups on which to build supervised models.

After loading and plotting the data of the Chipotle stores on the US map we decided to perform clustering analysis. 
The first method was to perform a dendrogram to see whether we could gain some useful insights. Unfortunately the information displayed was not conclusive.
Therefore as a second step we decided to narrow down the number of states we were going to use based on a threshold we fixed at 70 by state. We further narrowed down our search by cities in those states with the highest density of locations. Finally we only kept the cities where the number of Chipotle locations were greater than 10. This gave us a more interesting dendrogram but not sufficiently conclusive.

The next method was to use KMeans with our whole dataset and use k=24 as the number of clusters to base our model. We displayed the different clusters created on the US map as well and color-coded the different clusters. We then needed to create a function that would calculate the Euclidean distance between the locations in the cluster and the center point. The goal being to minimize the distance to be find a location as close as possible to outlets.

We then used the silhouette_score technique to score the prediction of the clustering and we achieved a 0.72 score. We also built an elbow curve to have a graphical view of the optimal number of clusters to be used.

Another method we decided to use was DBscan to make a comparison to what had been done so far. We achieved a prediction score of the clustering of 0.3478.


### Usage
You can run the corresponding notebook to tune the hyperparameters and measure and the perfomances of our model.
Otherwise, you have only to run the main.ipynb file which computes and displays evrythink.

### Steps
- Plot the US map
 - Visualize our data on this map.
 - Plot a dendrogram of our data to help us decide the appropropriate clustering resolution.
 - Compare and analyse different clustering methods using intrinsic analysis to decide on a chosen method.
 - Choose a centroid/adress to live.
### Libraries and environment
```bash
pip install -r requirements.txt
pip install sklearn
pip install pandas
pip install matplotlib
pip install geapandas
pip install numpy
pip install seaborn
```
### Authors
Realized by : 11.02.2021 by : 
    
Abdellah El Ghilbzouri   
Imad HajRashid  
Jonathan Decleire  
Ousmane Diop   
 



