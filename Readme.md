# kathmandu-hub-osm-analysis
This repository contains Python scripts that check OSM data completeness and recency for tourism amenities in Kathmandu.

First, OSM data within a given geojson bounds is extracted using the `osmnx` python library. After this, by making requests to the Overpass API, we look at the latest date at which each entity is modified. Finally, after joining these two datasets, we generate summary statisics and time series plots to understand attribute coverage and data recency.

Currently, we have performed completeness and recency analysis for the following amenities in Kathmandu:

## Analysis and results
Table below describes what we have so far regarding the state of OSM mapping:


## Codes, charts, and datasets
### Hotels 
In OSM hotels are mapped using the infrastructure tag `tourism=hotel`. Here are some links around the analysis:

1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Hotels.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Hotels in Kathmandu Valley](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/hotels.csv): a list of hotels in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  

### Guest houses
In OSM, guest houses are mapped using the infrastructure tag `tourism=guest_house`. Here are some links around the analysis:
1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Guest%20Houses.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Guest houses in Kathmandu Valley](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/guest_houses.csv): a list of guest houses in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  

### Restaurants
In OSM restaurants are mapped using the infrastructure tag `amenity=restaurant`. Here are some links around the analysis:
1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Restaurants.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Restaurants in Kathmandu Valley](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/restaurants.csv): a list of restaurants in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  

### Cafes
In OSM cafes are mapped using the infrastructure tag `amenity=cafe`. Here are some links around the analysis:
1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Cafes.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Cafes in Kathmandu Valley](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/cafes.csv): a list of cafes in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  

### Nightclubs
In OSM night clubs are mapped using the infrastructure tag `amenity=nightclubs`. Here are some links around the analysis:
1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Nightclubs.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Nightclubs in Kathmandu Valley](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/nightclubs.csv): a list of nightclubs in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  

### Bars
In OSM bars are mapped using the infrastructure tag `amenity=bar`. Here are some links around the analysis:
1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Bars.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Bars in Kathmandu Valley](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/bars.csv): a list of bars in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  

### Travel and tour operators
In OSM travel and tour operators are mapped using the infrastructure tag `shop=travel_agency`. Businesses that provide adventure experiences such as rafting, trekking, bungy jumping , etc., are also mapped under the same category. Here are some links around the analysis:
1. [IPython Notebook](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/OSM%20Analysis%20-%20Travel%20and%20Tours.ipynb): this file contains both code as well as results from the analysis.
2. [CSV - Travel and tour operators](https://github.com/c2m2-asia/kathmandu-hub-osm-analysis/blob/main/tour_operators.csv): a list of travel and tour operators in Kathmandu with secondary attributes such as name, email, phone number, opening hours, and so on.  