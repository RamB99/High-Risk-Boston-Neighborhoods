# High-Risk-Boston-Neighborhoods

This was a personal project that I did as part of the IBM Data science course. Essentially, we had freedom to pick a topic, and our task was to answer a business 
or societal related question. I chose to do something that has (currently impacting**) impacted all of us- COVID-19. 
My goal was to identify locations where there is a high chance of exposure to coronavirus in Boston. 

I used location data for all of Boston's neighborhoods to get the latitude and longitude values and put them in a dataframe. 
I used this dataframe to make API calls using Foursquare to get the list of common venues for each neighborhood. This gave me a lot of data about every possible venue
that existed in each neighborhood, and I used a mean to get the most common venues for each neighborhood.
Once I had this, I decided to perform a k-means clustering algorithm in order to segment each neighborhood based on its "risk". This risk was determined by the types of
venues that were frequent for each neighborhood. Venues that allowed for more in-person contact or close proximity where the virus would have an easier time spreading
were given a higher risk score (from a scale of 1-10) with venues that were more open (like parks) a lower risk score. The risk score would be totaled for each 
neighborhood, and the mean for each cluster determined the overall risk rating of the neighborhoods. 
After this, I used folium to display the segmented neighborhoods and clusters to make it easier to visualize where the riskier areas of Boston were in terms of COVID-19.
