# Data Science Capstone
This repository contains my final work on the Data Science Capstone, from IBM

The main work in this repository is an analysis of Covid-19 cases in Brazil per region. 

- [This file](https://github.com/marcellongvb/datasciencecapstone/blob/master/Introduction%20and%20data%20description.pdf) contains an introduction about the study and the data in use.

- The main work can be viewed in [this notebook](https://github.com/marcellongvb/datasciencecapstone/blob/master/Analysis_of_Covid_19_in_Brazil.ipynb). The notebook is very big, so github may not show a preview. If this is the case, you can also view the work in the [IBM watson studio notebook](https://dataplatform.cloud.ibm.com/analytics/notebooks/v2/4b93e207-5631-4f27-9e50-0af44a2479ae/view?access_token=36c21b9adeab75bda3cb1890aefe047843c15fb90d242fd11884a9baffcf218c).

## Considerations

I noticed some bad things and some errors after finishing the work. These things are:

- To correct fields of accumulated number of cases is correctly which are clearly wrong. This happens when the accumulated number of cases for a city is one day is greater than zero, then for the next day is 0. This can be corrected by creating a function that copies the entry in a previous day and pastes in later days where the number is missing. This helps the K-means clustering to make more correct clustering;

- To correct the cities with wrong geographical coordinates. The geolocator found wrong geographical coordinates for some cities in some regions. I corrected one of them to show how it can be done, but I did not do the same for every city. This would make the maps more correct.

- Cluster cities by the daily number of cases and deaths. I did not do that as I felt the daily numbers oscillates too much and it should no be good for the method. But this can be overcomed if we use moving averages for the treatment. This smoothens the curves and is very efficient for detecting tendencies. With this numbers, it could be possible to cluster cities in different other patterns for tendencies in the numbers of cases and deaths then it is possible to be done with the accumulated numbers.
