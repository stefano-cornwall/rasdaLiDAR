# Ingest and query voxel data into rasdaman
This set of script serve to 
1) ingest voxel (volumetric pixels) and auxiliary data arrays into a rasdaman server
2) query the voxel cube and cross it with auxiliary data

We used a template dataset from the three town of Luton, bedford and Milton Keynes in the UK.
Auxiliary data include NDVI vegetation index.

- lidarSM.json 
This is used to ingest all GeoTIF files covering the spatial cube x-y-z and stored in a  "/home/user/lidar/dataSM/". 
The filename has the information on the z axis height (0.50cm gap each) which is not stored in the metadata, so a regular expression read the filename and place the layer in the spatial cube appropriate location.
data have EPSG:27700 geographic projection (GB National grid)

- ndvi2D.json
This is used to ingest a 2D map ov vegetation index into a rasdaman server. 
