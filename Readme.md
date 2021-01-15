# kathmandu-osm-analysis
This repository contains Python scripts that check OSM data completeness and recency for tourism amenities in Kathmandu.

First, OSM data within a given geojson bounds is extracted using the `osmnx` python library. After this, by making requests to the Overpass API, we look at the latest date at which each entity is modified. Finally, after joining these two datasets, we generate summary statisics and time series plots to understand attribute coverage and data recency.

Currently, we have performed completeness and recency analysis for the following amenities in Kathmandu:

## Analysis and results
This section describes what we have found so far regarding the state of OSM data

### Table 1: Count of amenities by type 

| Amenity                     | Count  |
|-----------------------------|--------|
| Hotels                      |   578  |
| Guest houses                |   291  |
| Restaurants                 |  1324  |
| Bars                        |   62   |
| Nightclubs                  |    8   |
| Cafes                       |   696  |
| Travel and   tour operators |   396  |


### Table 2: Amenities by secondary attribute availability

| Amenity                     | name | email | phone  | opening_hours | beds | rooms | stars |
|-----------------------------|:----:|:-----:|:------:|:-------------:|:----:|:-----:|:-----:|
| Hotels                      |  61% |  11%  |   20%  |      10%      |  0%  |   3%  |   3%  |
| Guest houses                |  42% |  11%  |   23%  |      12%      |  0%  |   1%  |   0%  |
| Restaurants                 |  60% |   4%  |   14%  |      14%      |   -  |   -   |   -   |
| Bars                        |  32% |   5%  |   17%  |      21%      |   -  |   -   |   -   |
| Nightclubs                  |  56% |   0%  |   11%  |       0%      |   -  |   -   |   -   |
| Cafes                       |  54% |   3%  |   12%  |      16%      |   -  |   -   |   -   |
| Travel and   tour operators |  64% |  32%  |   36%  |      26%      |   -  |   -   |   -   |

### Table 3: Amenities by date of last modification in OSM

| Amenity                     | Pre-covid | During the   pandemic | % pre covid | % during the pandemic |
|-----------------------------|-----------|-----------------------|-------------|-----------------------|
| Hotels                      | 544       | 34                    | 94%         | 6%                    |
| Guest houses                | 279       | 12                    | 96%         | 4%                    |
| Restaurants                 | 1175      | 149                   | 89%         | 11%                   |
| Bars                        | 54        | 8                     | 87%         | 13%                   |
| Nightclubs                  | 5         | 3                     | 63%         | 38%                   |
| Cafes                       | 589       | 107                   | 85%         | 15%                   |
| Travel and   tour operators | 359       | 37                    | 91%         | 9%                    |

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
