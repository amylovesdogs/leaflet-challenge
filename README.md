# leaflt-challenge
DU Data Analysis Module 15 Leaflet Challenge

The USGS is interested in building a new set of tools that will allow them to visualize their earthquake data. They collect a massive amount of data from all over the world each day, but they lack a meaningful way of displaying it.
This code containts a way to visualize USGS earthquake data.

## Part 1: Create the Earthquake Visualization

## Part 2: Gather and Plot More Data (Optional with no extra points earning)


## Formatting Resources
The following items are here in case I need to have formatting examples. Not relevant to the current project.
### Precipitation Analysis
The following analysis is done:
1. Find the most recent date in the dataset.
2. Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.
3. Select only the "date" and "prcp" values.
4. Load the query results into a Pandas DataFrame. Explicitly set the column names.
5. Sort the DataFrame values by "date".
6. Create a bar chart using the DataFrame plot method.
7. Use Pandas to print the summary statistics for the precipitation data.

### Station Analysis
The following analysis is done:
1. Query to calculate the total number of stations in the dataset.
2. Query to find the most-active stations (that is, the stations that have the most rows) by doing the following:
* List the stations and observation counts in descending order.
* Determine which station has the greatest number of observations.
3. In a single query, calculate the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.
4. Query to get the previous 12 months of temperature observation (TOBS) data by doing the following:
* Filter by the station that has the greatest number of observations.
* Query the previous 12 months of TOBS data for that station.
* Plot the results as a histogram with bins=12.


Part 2 is a flask app that provides the following API routes. The flask app can be found in **SurfsUp/app.py**. All values returned are in JSON format. All dates in routes must be in YYYY-MM-DD format.

* **/** List all the available routes.
* **/api/v1.0/precipitation** Returns the las 12 months of precipitation data
* **/api/v1.0/stations** Returns the las 12 months of temperature data for the most active weather station
* **/api/v1.0/<start_date>** Return the minimum, maximum and average temperatures for all dates starting with <start_date>
* **/api/v1.0/<start_date>/<end_date>** Return the minimum, maximum and average temperatures for all dates between <start_date> and <end_date> inclusive.
