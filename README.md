
This python program uses a nearest neighbor algorithm to determine whether building inspectors visited a target site the day they were assigned the inspection. It uses two datasets: the route sheet of sites they were assigned to inspect and data from the inspector's smart phone that periodically sends latitude and longitude coordinates to Verizon's Field Force Management database.

The program implements these steps:
  1. Imports data into a pandas data frame and cleans the data.
  2. Places a 500 foot radius (a geofence) around the building that is on the route sheet (the building that is to be inspected).
  3. Calculates the closest point that the inspector came to the location.
  4. If the inspector enters the geofence (is within 500 feet of the center of the building) of the target building, the building was   inspected.
  5. Calculate the inspector’s closest distance and address to the target building.
  6. Determine the location of the inspector if not at the inspection site.
  7. If the phone has a signal drop, determine if inspector went to the inspection site using path analysis.
  
  
A map produced in Tableau showing results of perfect match (inspector went to all of the sites)
Blue = DOB Inspection Site
Orange = FFM Data

  
![abu_mahmod_10_4](https://user-images.githubusercontent.com/11237613/33667894-273ca51c-da6c-11e7-9cb5-3623229c7fbc.png)

