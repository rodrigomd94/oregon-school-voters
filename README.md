# Oregon School Boards Voter Data
For this project we want to visualize voter data for the Oregon school Boards. The main attributes we want to visualize per district are:
  - Voter gender ratio
  - Voter ages
  - Total amount of voters
  - Votes per political party
  
For this, we will begin by cleaning and processing the data and finish by creating a geojson with all the necessary attributes needed as a base for a Mapbox map (see last cell for the final map).

The base datasets that we are using are:
  - `voters.csv`: This dataset contains the voter data for each school board, including total and percentage of votes for each political party, average ages, and total number of voters.
  - `genders.csv`: This dataset contains the voters' gender percentages for each district.
  - `districts.csv`: This dataset contains many attributes but we are interested with the names and GEOID of the districts. This dataset shares the same names of districts as the other datasets, so we will use it to join the GEOID to the other datasets. The GEOID is then used to join all the data into the geojson.
  - `s_districts.geojson`: This is a geojson file containing the geometries and GEOID of the school districts. The data originally comes from US Census Bureau TIGER Files. It was previously converted to geojson and projected to the EPSG 4326 CRS in order to be able to visualize it with Mapbox.
