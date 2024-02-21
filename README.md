# TABLEAU CITIBIKE ANALYSIS

FIND THE TABLEAU PUBLIC WORKBOOK [HERE](https://public.tableau.com/app/profile/shawn.woodbury/viz/CitibikeFinalProject_17079762881950/CitibikeStory)

<img src="Images/citi-bike-logos-idi5hDpjWW.png">

## Overview

This project utilizes November 2023 data from [Citibike NYC](https://citibikenyc.com/system-data) to examine the relationships between days of the week and hours of the day on the ridership qualities of Citibike users. 2023 was chosen to maximize the relevance of data. November was chosen to emphasize stations which are popular, even in the off-season (and this, presumably get more use year-round), and to optimize the performance of the visualizations.

 By examining patterns in station usage, we can isolate popular vs. unpopular stations, find their locations and ridership characteristics (rideable types, memberships vs. casual). Once identified, we can identify patterns and commonalities among the popular and unpopular stations that may lead to optimization of future station locations.

 ## Dashboard 1: "Hourly Ridership Snapshot" - How to read

 This section examines the "Hourly Ridership Snapshot Dashboard". The dashboard contains 4 visualizations as well as a city map, outlining all CitiBike Stations. 

 ### Viz 1: Total Ridership By Hour

This visualization outlines overall ridership per hour across the whole month. It then splits the riders among classic bike and e-bike users. Through examination of this visualization, we can isolate two peak usage hours: 8am and 5pm. These can be seen to correspond to typical rush hours, illustrating that these users may be largely commuters.

### Viz 2: Total Riders by Rideable Type

This visualization examines the proportion of e-bike to classic bike users. The viewer can utilize the slider to isolate particular hours of the day 12am ("hour 0") - 11pm ("hour 23") and see the number of riders as well as their proportion. The results suggest a disproportionate use of Classic Bikes with E-Bikes only comprising a maximum of 3.11% of ridership during any given measurement period. This may be due to a lack of availability (there are more classic bikes in the fleet) or due to the weather conditions as the dataset is for November.

### Viz 3: Ridership By Starting Station

This visualization outlines the top and bottom 14 stations of origin (where riders pick up their rideables) as measured by the total number of riders beginning their rides at each station during November. Users can select "Highest Ridership" or "Lowest Ridership" from the dropdown to the left of the charts, Select the timeframe to measure (as discussed in the above visualization), hover over the bars to find out more information about each station, or click on a bar to isolate that station in the map above the charts (discussed below). As an example, we can outline that the top 3 stations across the period are as follows:

<ol>
    <li>W. 21st St. & 6th Avenue</li>
    <li>E 41st St. & Madison Avenue</li>
    <li>W. 31st St. & 7th Avenue</li>
</ol>

### Viz 4: Ridership By Ending Station

This visualization is identical to viz 3, except that it outlines the same information from stations of termination (i.e. where rideables are returned)

### MAP 1: Station Map

This map gives visual/geographical information for all stations. The stations are represented by dots on the map and are filled in the following colors for differentiation: 

<ul>
    <li> RED: Less than 100 riders </li>
    <li> LIGHT BLUE: 101-5,000 riders </li>
    <li> DARK BLUE: 5,001-10,000 riders</li>
    <li>FUCHSIA: More than 10,000</li>
</ul>

You can also change the measured day of the week with the dropdown menu on the upper left side of the map. This allows you to change the day of the week measured and select one, many or all days. Hovering over these dots will give you the station name, coordinates, and ridership number for the selected time period.

The map works with the "Ridership by Starting Station" and "Ridership by Ending Station" bar graphs to allow you to isolate each individual station from the bar graph, and see it's representative dot in the above map by clicking on the bar for that station.

### Dashboard 1 -- Analysis

Several trends become clear when examining the data from the "Hourly Ridership Dashboard" which is of interest to station placement optimization.

First, of the top 14 most popular starting and ending stations, only 10 zip codes are represented, and all are within the 100** (i.e. 10001, 10018, etc.)area codes. None of the lowest ridership stations are within this zip code area, leading to a clear differentiation of the high traffic vs. low-traffic regions. Furthermore, we can infer that stations which are too close together inhibit ridership and should be avoided to maximize cost efficiency of station building and maintencance.  

From examining the "Total Ridership By Hour" line graph, we can see that the two peak hours are 8am and 5pm which, when combined with the knowledge that all top stations are in the largely commercial zip codes of 100** would suggest that the CitiBike users from these stations are largely using the bikes for commuting between commercial locations.

Additionally, we have learned that Classic bikes largely outperform E-bikes for ridership. That, despite being 20% of CitiBike's fleet, they are utilized as an option only a max of 3.11% of the time. This, however may be a product of either the additional cost associated with renting E-bikes, or the seasonality of the data. Further examination of this phenomenon over a larger timescale is necessary for causal determination. 

 ## Dashboard 2: "Picture of a Successful Station" - How to read

 Having established the most and least utilized starting station, and having created some hypotheses for this popularity, we can now take a closer look at the most successful stations to find out their characteristics so they can be replicated in future stations. "Picture of a Successful Station" dashboard allows us to isolate each station using the map, and look at their vital statistics such as the average ride distance (direct distance from starting to ending station), average ride duration, membership status vs. casual riders, and day of week and time of day utilization. 

 ### Map 2: Top 14 Stations

 The provided map on this dashboard features only the top 14 most popular stations as established by Dashboard 1. Each of the stations are represented by a dot on the map and is color-coded to show total ridership across the total measurement period. 
 
 <ul>
    <li>BLUE: 5,001-10,0000 riders</li>
    <li>FUCHSIA: More Than 10,000 riders</li>
</ul>

Like Map 1, you can hover over each dot to find the station name, latitude, longitude and number of riders. Clicking on any dot will isolate that station and the remaining visualizations will change to reflect the properties of that station alone. Clicking in the general map area will de-select this stations, reverting the remaining visualizations to represent the entire 14 station set.

### viz 1: Starting to Ending Station Distance

This visualization calculates the average ride distance traveled from each station to the end station (where each rider returned their rideable). As no mileage information was represented in the data for each individual rideable, this only represents direct (straight line) difference in mileage between the 2 stations, NOT the total distance traveled. It would be necessary to isolate rideable odometer data to establish this measure. Still, the available distance allows us to approximate the general travel area.

Hovering over any bar will serve the user the station name and it's relative average trip distance. 

### Viz 2: Average Travel Duration

The Average Travel Duration bar chart represents the temporal difference (in minutes) between when a rider picks up their rideable and when they return it to the ending station. This difference is averaged for each station.

Hovering over any bar will serve the user the station name and it's relative average trip duration in minutes

### Viz 3: Popular Days and Times

This visualization represents the popular days and times for the selected stations. On the horizontal axis, you will find the days of the week, and on the vertical axis, you will find the times of day (0 for midnight through 23 for 11pm). The dark red squares indicate the highest ridership periods, and the dark blue represents the lowest ridership periods for selected stations. Please consult the scale on the left side of the chart for details of how the scale is represented chromatically.

### Viz 4: Member vs. Casual Riders
 
This pie chart represents the relative proportions of members versus casual riders for the selected stations. The blue slice represents member riders, and the pink slice represents the casual riders for these stations. You will note above or below each slice, the percentage of each rider category as well as the total number of riders from each category. 

### Dashboard 2 -- Analysis

Based on the visualizations from the "Picture of a Successful Station" dashboard, we can glean several insights about the characteristics of popular stations.

The average distance between the start and end points for riders from the top 14 stations is approximately 1.074 miles. This would suggest that rides are largely local, commuter, and/or out-and-return rides, and that the minimal distance for stations from one another should be no less than 1 mile to maximize ridership and minimize station upkeep and building costs.
The average duration of rides from these stations backs up this hypothesis, witht the average duration being approximately 13.23 minutes. Though this might be affected by seasonality, it is worth noting that long rides are substantially less common among the most utilized stations.

The day of the week and hour of the day are highly consequential to the utilization of stations, with the most high traffic times being mid week and during the evening rush hour (Wednesday at 5pm to be specific). The second highest traffic time would be mid-week at 8am. Both of these statistics back up the commuter theory. 

When examining the membership vs. casual rider pie chart, it becomes apparent that the vast majority of riders from the top 14 stations (91.74% across the measurement period) are members. There is, however, opportunity for conversion of the remaining 659 (8.26%) of riders who are doing so casually. With the other metrics in mind, this suggests that members are signing up with the intention of using CitiBike as a commuter option, which would have opportunities for buildout of hubs outside of the 100** area codes.

## Conclusions:

When deciding where to build and locate stations, it would behoove CitiBike to consider areas of high commuter traffic. It would also be wise to consider a radius of approximately one mile from station to station as a minimum given that popular stations average that riding distance. Furthermore, any emphasis would likely be more effective on classic bike traffic (though, again, this is subject to cost and seasonality considerations). While members comprize the largest swath of riders, there is ample opportunity for conversion of casual riders, especially within commercial districts.
