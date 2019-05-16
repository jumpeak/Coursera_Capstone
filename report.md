## Coffee Shop in New York

### Introduction

What is the best place to open new coffee shop in New York? Having available only foursquare data I'll try to find out what neighborhoods are good to open new coffee shop there. My aim is to find not a single ultimate solution but a set of options or possibilities, recommendations to help in decision to open new coffee shop.

### Data

First, I'll get foursquare data about venues with category "coffee shop" using foursquare "search" request. Each neighborhood coordinates approximately calculated as average of coordinates of geojson polygon points. Search radius is set to 1 mile, letting the search area to envelop some parts of adjacent neighborhoods. This assumption is made because people walk through nearby neighborhoods seamlessly. 
Next - I'll find out what venues people visit before visiting coffee shops, for this purpose I'm going to use foursquare "nextvenues" search feature.

### Analysis

First look at Coffee Shops density in New York City. Most of coffee shops are in the center  - that is not surprising. 
![Coffee venues density](/images/coffee_dens.png) 

Next step is to retrieve venues, that people visit before visiting coffee shops. For this purpose, I'll search for all nearby venues, then for every found venue will request foursquare "nextvenues" to get top 5 venues visited after this one, next - check if there is venues with category "Coffee Shops" in top 5 nextvenues, and if it is - add the checked venue to a dataframe.
Let's call the venues visited before coffee shop venues "pre-venues". Now we can explore categories of collected pre-venues: 
![pre venues top](/images/venues_barh.png) 
 
Results are interesting, Gym coupled with Gym/Fitness Center category takes top place. If you're are going to open a coffee shop - you should keep this in mind. Have you heard of researches of relations between coffee and sports?
Now let's look at pre-venues density on the map: 
![pre-venues density](/images/pre_venues_dens.png) 

As you see, the situation is different in comparison with the coffee shops venues.
To compare coffee shops density and pre-venues density I'm introducing one simple metric - "coffee shop count / pre-venue count" relation. Put it on the map too: 
![compare](/images/compare_1.png) 

As you see, we got one bright outlier! Howard Beach is the most interesting neighborhood, as it has only 8 coffee shop venues alongside with 45 pre-venues. This may be the best place to open a new coffee shop, but other circumstances left out of this research and still got to be noticed.
However this outlier shadows other neighborhoods that may be a nice place for a new coffee shop too. Next I'll suppose that neighborhoods with compare ratio of 1 or more are equally good enough (i.e. they have equal or more pre-venues than coffee shop venues)
Adjasted metric comparision now highlights all neighborhoods: 
![compare](/images/compare_1.png) 

### Conclusion

The final map shows the neighborhoods to pay attention to if you want to open a new coffee shop in New York.
Keep in mind that it’s only a partial research and many important things are left out of scope. So the result is not a solution, yet it provides insights about coffee shops in the city.
Further research requires more data including rent prices, transport lines, nearby venue ratings, customer per day etc. With more data will come more complex metrics and machine learning techniques will be required.



