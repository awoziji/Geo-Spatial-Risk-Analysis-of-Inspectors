# Inspection-Tracking-Nearest-Neighbor
Inspection tracking using nearest neighbor machine learning algorithm and text matching using fuzzy logic

This program uses a nearest neighbor algorithm to determine whether building inspectors visited the site they were assigned to inspect. It uses two datasets: the route sheet of sites they were assigned to inspect and data from the inspector's smart phone that periodically sends latitude and longitude coordinates to Verizon's Field Force Management database.

The program implements these steps:
  1. Imports data into a pandas data frame and cleans the data.
  2. Places a 1000 foot radius (a geofence) around the building that is on the route sheet (the building that is to be inspected).
  3. Calculates the closest point that the inspector came to the location.
  4. If the inspector enters the geofence (is within 1000 feet of the center of the building) of the target building,  label it as              inspected, if not, label as not inspected.
  5. Calculate the inspector’s closest distance and address to the target building.
  6. Enhance validation of the results using fuzzy logic address matching.

