# NYC_Yellow_Taxi_Trip_DataAnalysis
# For NYC yellow taxi trip information, go through this website- https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

📝Dataset Description

The NYC Yellow Taxi Trip dataset is a publicly available dataset released by the NYC Taxi and Limousine Commission (TLC). It contains detailed trip-level information for all yellow taxi rides that took place in New York City in a specific month.I am taking 2025 January month's dataset.The Taxi Zone Lookup file contains the official mapping of NYC taxi zones, including each zone’s LocationID, Borough, Zone, and Service Zone. This file is merged with the main trip dataset to convert numeric pickup and drop-off LocationIDs into meaningful location names for deeper analysis.

🎯 Objectives for NYC Yellow Taxi Data Analysis
Identify common trip patterns across NYC.
Determine peak taxi activity hours.
Map high-demand pickup and drop-off zones.
Examine vendor usage and trip distribution.
Understand relationships between trip distance, duration, and fare.
Analyze tip behavior in relation to trip characteristics.
Explore payment method trends and preferences.
Assess airport and congestion-related trip dynamics.
Detect outliers and anomalies in trip data.

🧾Data Dictionary

1)Trip Dataset

VendorID
A code indicating the TPEP provider that provided the record.
1 = Creative Mobile Technologies, LLC
2 = Curb Mobility, LLC
6 = Myle Technologies Inc
7 = Helix

tpep_pickup_datetime
The date and time when the meter was engaged.

tpep_dropoff_datetime
The date and time when the meter was disengaged.

passenger_count
The number of passengers in the vehicle.

trip_distance
The elapsed trip distance in miles reported by the taximeter. RatecodeID
The final rate code in effect at the end of the trip.
1 = Standard rate
2 = JFK
3 = Newark
4 = Nassau or Westchester
5 = Negotiated fare
6 = Group ride
99 = Null/unknown

store_and_fwd_flag
This flag indicates whether the trip record was held in vehicle memory before sending to the vendor, aka “store and forward,” because the vehicle did not have a connection to the server.
Y = store and forward trip
N = not a store and forward trip

PULocationID
TLC Taxi Zone in which the taximeter was engaged.

DOLocationID
TLC Taxi Zone in which the taximeter was disengaged.

payment_type
A numeric code signifying how the passenger paid for the trip.
0 = Flex Fare trip
1 = Credit card
2 = Cash
3 = No charge
4 = Dispute
5 = Unknown
6 = Voided trip

fare_amount
The time-and-distance fare calculated by the meter. For additional information on the following columns, see https://www.nyc.gov/site/tlc/passengers/taxi-fare.page
extra Miscellaneous extras and surcharges.

fare_amount
that is automatically triggered based on the metered rate in use.

tip_amount Tip amount
this field is automatically populated for credit card tips. Cash tips are not included.

tolls_amount
Total amount of all tolls paid in trip.

improvement_surcharge
Improvement surcharge assessed trips at the flag drop. The improvement surcharge began being levied in 2015.

total_amount
The total amount charged to passengers. Does not include cash tips.

congestion_surcharge
Total amount collected in trip for NYS congestion surcharge.

airport_fee
For pick up only at LaGuardia and John F. Kennedy Airports.

cbd_congestion_fee
Per-trip charge for MTA's Congestion Relief Zone starting Jan. 5, 2025.


2)Zone-Name dataset

LocationID
A unique numeric identifier assigned to each NYC taxi zone. Used to map pickup and dropoff locations in the main trip dataset.

Borough
The borough (e.g., Manhattan, Brooklyn, Queens, Bronx, Staten Island) where the taxi zone is located.

Zone
The specific neighborhood or area name within the borough. Represents the actual pickup/dropoff zone.

service_zone
The taxi service zone category assigned by NYC TLC (e.g., Yellow Zone, Green Zone, Boro Zone, Airport Zone). Used for analysis of trip patterns by service type.
