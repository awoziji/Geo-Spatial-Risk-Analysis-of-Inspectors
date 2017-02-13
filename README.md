
This python program uses a nearest neighbor algorithm to determine whether building inspectors visited a target site the day they were assigned the inspection. It uses two datasets: the route sheet of sites they were assigned to inspect and data from the inspector's smart phone that periodically sends latitude and longitude coordinates to Verizon's Field Force Management database.

The program implements these steps:
  1. Imports data into a pandas data frame and cleans the data.
  2. Places a 1000 foot radius (a geofence) around the building that is on the route sheet (the building that is to be inspected).
  3. Calculates the closest point that the inspector came to the location.
  4. If the inspector enters the geofence (is within 1000 feet of the center of the building) of the target building,  label it as              inspected, if not, label as not inspected.
  5. Calculate the inspector’s closest distance and address to the target building.
  6. Enhance validation of the results using fuzzy logic address matching.
  
  
A map produced in Tableau showing results:
  
![was building inspected](https://cloud.githubusercontent.com/assets/11237613/22387459/b943eaec-e4a9-11e6-8b92-95e30aa92bdd.png)

