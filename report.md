## Coffee Shop in New York

### Introduction

What is the best place to open new coffee shop in New York? Having available only foursquare data I'll try to find out what neighbourhoods are good to open new cofee shop there. My aim is to find not a single ultimate solution but a set of options or possibioities, recomendations to help in decision to open new cofee shop.

### Data

First, I'll get foursqare data about venues with category "coffee shop" using foursquare "search" request. Each neighborhood coordinates approximately calculated as average of coordinates of geojson poligon points. Search radius is set to 1 mile, letting the search area to envelop some parts of adjacent neighborhoods. This assumption is made because people walk through nearby neighborhoods seamlessly.
Next - I'll find out what venues people visit before visiting cofee shops, for this purpose I'm going to use foursuare "nextvenues" search feature.

### Data Analysis

First look at Coffee Shops density in New York City. Most of coffee shops are in the center quite prospective.

Next step is to retrieve venues, that people visit before visiting coffee shops. For this purpose I'll search for all nearby venues, then for every found venue will request fursquare "nextvenues" to get top 5 venues visited after this one, next - check if there is venues with category "Coffee Shops" in top 5 nextvenues, and if it is - add the checked venue to a dataframe.
Let's call the venues visited before coffee shop venues "pre-venues". Now we can explore categories of colected pre-venues:

Results are interesting, Gym coupled with Gym/Fitness Center category takes top place. If your are going to open a coffee shop - you shoil keep this in mind. Have you heard of researches of relations between coffee and sports?

Now let's look at pre-venues density on the map:

As you see, situaton is different in comparison with coffee shops venues.

To compare coffee shops density and pre-venues density I'm introducing one simple metric - "coffe shop count / pre-venue count" relation. Put it on the map too:

As you see, we got one bright outlier! Howard Beach is the most interesting neighborhood, as it has only 8 coffee shop venues alongside with 45 pre-venues. This may be the best place to open a new coffee shop, but other circumstances left out of this research and still got to be noticed.



