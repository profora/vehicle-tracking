# Vehicle Tracking System
This product intend for to track your vehicles which, when and where their located. Normally each vehicle will have one GPS unit to give information back to the central system.

## Product Requirement
1. GPS unit install one each vehicle
2. GPS unit and control system will communicate through web IP
3. Each single movement vehicle on prepared time interval will send data
4. Critical and important notice should send to the server

## Preparation guideline
1. Install PostgreSQL server, PHP 7.1 with PostgreSQL
2. Create VechicleTracking database in PostgreSQL
3. Build all stored procedures need for the project
4. Create PostGIS extension on VechicleTracking database
5. Plug VechicleTracking database to RESTful API
6. Prepare some IP and web sockets to receive the data from the GPS unit
7. Record each action of GPS unit on the database system
8. Make data visualization on frontend client using RESTful API
9. Prepare business intelligent for frontend client
10. Monitor product activity and usages
11. Create proper documentation for each component of the product


## Development environment
1. `brew install postgresql` to download PostgreSQL
2. `brew install jpeg` to link later on PostGIS
3. `brew install postgis` to install PostGIS in PostgreSQL server
4. Select your database and run the following SQL to get extension to your database
```sql
-- Enable PostGIS (includes raster)
CREATE EXTENSION postgis;
-- Enable Topology
CREATE EXTENSION postgis_topology;
-- Enable PostGIS Advanced 3D
-- and other geoprocessing algorithms
-- sfcgal not available with all distributions
CREATE EXTENSION postgis_sfcgal;
-- fuzzy matching needed for Tiger
CREATE EXTENSION fuzzystrmatch;
-- rule based standardizer
CREATE EXTENSION address_standardizer;
-- example rule data set
CREATE EXTENSION address_standardizer_data_us;
-- Enable US Tiger Geocoder
CREATE EXTENSION postgis_tiger_geocoder;
```
