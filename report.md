## Coffee Shop in New York

### Introduction

What is the best place to open new coffee shop in New York? Having available only foursquare data I'll try to find out what neighbourhoods are good to open new cofee shop there. My aim is to find not a single ultimate solution but a set of options or possibioities, recomendations to help in decision to open new cofee shop.

### Data

First, I'll get foursqare data about venues with category "coffee shop" using foursquare "search" request. Each neighborhood coordinates approximately calculated as average of coordinates of geojson poligon points. Search radius is set to 1 mile, letting the search area to envelop some parts of adjacent neighborhoods. This assumption is made because people walk through nearby neighborhoods seamlessly.
Next - I'll find out what venues people visit before visiting cofee shops, for this purpose I'm going to use foursuare "nextvenues" search feature.

