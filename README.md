### Current spatial and data files

Please note that these files are works in progress. Both the data and data formats are subject to change as we add covenants and refine our processes.

These files represent the covenants that have been successfully mapped and do not include unmapped covenants.

#### Ramsey County covenants shapefile
covenants-mn-ramsey/covenants-mn-ramsey.shp

#### Ramsey County covenants GeoJSON
covenants-mn-ramsey.geojson

#### Ramsey County covenants CSV
covenants-mn-ramsey.csv

#### Hennepin County covenants compatibility GeoJSON
Please note that the official version of the Hennepin County covenants is [published here](https://conservancy.umn.edu/handle/11299/217209). However, this file is provided in order to facilitate quicker mapping of the Hennepin County data alongside the Ramsey County data. It is a copy of the official shapefile, with fieldnames and date formats changed to match the new Ramsey County data.

covenants-mn-hennepin.geojson


### Spatial notes
GeoJSON and shapefile are unprojected WGS-84 (SRID:4326)

(Note: Legacy Hennepin shapefile, available elsewhere is projected UTM.)

### Data fields in downloadable files

| Field name  | Data type | Description |
| ------------- | ------------- | ------------- |
db_id  |  Integer  |  Internal database primary key  |
workflow  |  Varies  |  Internal workflow ID  |
cnty_name  |  String  |  County name  |
cnty_fips  |  String  |  County 5-digit FIPS code  |
doc_num  |  String  |  Government document number of historical property deed  |
deed_year  |  Integer  |  Year of historical deed/covenant. Since covenants are often repeated in subsequent deeds when a property is sold, we have attempted to identify the earliest deed with the racial covenant.  |
deed_date  |  Date, YYYY-MM-DD  |  Date deed recorded. Primary date for Ramsey County covenants. Present in many Hennepin County covenant entries, but not all  |
exec_date  |  Date, YYYY-MM-DD  |  Date deed was executed. Primary date for Hennepin County covenants, missing in Ramsey County.  |
cov_text  |  String  |  Text of racial covenant  |
seller  |  String  |  Name of historical seller, also known as "grantor." Not transcribed in Ramsey County.  |
buyer  |  String  |  Name of historical buyer, also known as "grantee." Not transcribed in Ramsey County.  |
street_add  |  String  |  Street address of modern parcel match, according to county records.  |
city  |  String  |  City of modern parcel match, according to county records.  |
state  |  String  |  Minnesota  |
zip_code  |  String  |  5-digit ZIP of modern parcel match, according to county records.  |
add_cov  |  String  |  Addition listed in historical deed  |
block_cov  |  String  |  Block listed in historical deed  |
lot_cov  |  String  |  Lot number or range listed in historical deed  |
cnty_pin  |  String  |  Modern county parcel PIN. Not currently accurate, will be fixed in future exports.  |
add_mod  |  String  |  Addition of modern parcel match.  |
block_mod  |  String  |  Block of modern parcel match.  |
lot_mod  |  String  |  Lot number of modern parcel match.  |
ph_dsc_mod  |  String  |  Physical description of modern parcel match.  |
join_strgs  |  String  |  A concatenated string of all addition/block/lot combinations used by the Mapping Prejudice automated system to attempt a join to a modern parcel.  |
geocd_addr  |  String  |  Geocoded address of parcel centroid. Hennepin County only.  |
geocd_dist  |  Float  |  Distance (in meters) of the geocoded address point from the closest parcel polygonal boundary. A value of ???0??? indicates the current address point falls within the parcel boundary. Hennepin County only. |
match_type  |  String  |  Ramsey County only. Generally, parcels are matched automatically by using addition/block/lot combinations. But in cases where manual join work is required, the user can specify what type of join was used. Options: "Automatic match", "Multiple single lots", "Partial lot", "Simple lot", "Something else"  |
manual_cx  |  Boolean  |  Whether or not a user has manually corrected the Zooniverse consensus output  |
dt_updated  |  Timestamp  |  Last change to record in database  |
zn_subj_id  |  Integer  |  Zooniverse subject ID  |
zn_dt_ret  |  Timestamp  |  Date deed was retired in Zooniverse  |
image_ids  |  String  |  List of raw deed image handles  |
med_score  |  Float  |  Median Zooniverse consensus score, indicating how many users agreed precisely on various fields. Maximum is 1.0 for complete agreement.  |
plat_dbid  |  Integer  |  Primary ID of plat record in Mapping Prejudice database.  |
