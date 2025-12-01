# Team 

## Team Nyla Upal and Liam Ward



## Data Source

What data source did you work with?     
We chose to work with bus route and stop data from the Washington Metropolitan Area Transit Authority API. We chose this as it had continuously updating data on the buses, and it gave their longitude and latitude so they would be able to be displayed on a map.     

## Challenges / Obstacles

What challenges did this data choice present in data gathering, processing and analysis, and how did you work through them? What methods and tools did you use to work with this data?        
In order to get the continuous data from the bus position api, we used Apache Kafka to have a producer that got the positions of all the buses every 30 seconds. We then also had a consumer that read from the created bus positions topic and then wrote the bus information to a duckdb file. From this, the app file creates a dashboard using streamlit that has the live positions of the buses. Initially just using the bus position only gave the disconnected positions of the buses, so we had to use the path details api to get the entire routes and display those on the map as well. We also had issues getting the streamlit platform to refresh and update, which is why we had to use the streamlit autorefresh package to have it refresh every 30 seconds as the producer pulled updated positions. 

## Analysis

Offer a brief analysis of the data with your findings. Keep it to one brief, clear, and meaningful paragraph.   



## Plot / Visualization

Include at least one compelling plot or visualization of your work. Add images in your subdirectory and then display them using markdown in your README.md file.

## GitHub Repository

https://github.com/liamward26/Transit-Dash
