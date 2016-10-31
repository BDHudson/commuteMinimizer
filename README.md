# commuteMinimizer

"So if you have a 20-mile commute to work, multiply it out: 40 miles each workday times 50 cents a mile. And there are 2,500 of those workdays in every decade, so that 'not too bad' commute is burning at least $50,000 every ten years." [Reuters](http://www.reuters.com/article/us-usa-commute-costs-idUSKBN0E721M20140527)

The average american spends 26 minutes commuting in their car, each way, to work. Collectively 126 million people in the US commute, losing 30 billion hours of time a year [grist.org](http://grist.org/living/americans-spend-30-billion-hours-a-year-commuting-and-its-killing-them/). If the average commuter can cut their travel time in half, they stand to save over $25,000 over a decade.  

## The current state of the art

This project aims to develop a web tool that can weight the commutes of multiple people and the other locations visited frequntly in a person's life (an elderly parent's house, a child's school, etc.) and highlight neighborhoods that would minize the cost of commuting to work. 

The current state of the art tool on the web is depoloyed by [Trulia](https://www.trulia.com/local/seattle-wa/driving:1%7Ctransit:0%7Cposition:47.653594;-122.315186%7Ctime:60_commute)
![Figure1](https://github.com/BDHudson/commuteMinimizer/blob/master/images/Trulia_Example.png)

This tool offers a great start - but doesn't go far enough. I propose make two improvement to its current framework. First, I will allow multiple locations to be provided. Often one person's commute isn't enough information - for example married couples with children may need to weigh both work locations and the child's school. Second, I would allow each location to be weighted by how often the location is visited in a given week. For example, perhaps a child's school is less important in the decision for a family to move, because they will graduate to another school in another location in the near future. 

## Data Sources

The project would be conducted with [OpenStreetMap data}(http://wiki.openstreetmap.org/wiki/Downloading_data). Critically, its coverage is global. Street centerlines for test cities would be the main data need. To start, traffic would not be incorporated into the analysis, but could be if it can be reliably/affordably accessed via an API. 

[Leaflet](http://leafletjs.com/) will be explored as a web platform. Initial protyping will be done with QGIS, python tools including pandas, networkX, Shapely, and Fiona. 

## explain the analysis you are performing.

## Proof of concept 
![Figure2](https://github.com/BDHudson/commuteMinimizer/blob/master/images/GoogleAPI_routesImage.png)

As a proof of concept, have created a series of route maps created by making requsts to Google's Map API. 

