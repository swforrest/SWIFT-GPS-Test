# SWIFT-GPS-Test
Stationary test data used in the paper - Moving wildlife tracking forward under forested conditions with the SWIFT GPS algorithm 

CSV files - these are the data files after post-processing locations on a computer with an internet connection, and after generating extra columns for analysis

In reference to the index starting at ~4-6, the first locations were removed as tags were calculating locations as they were being put out. This is to ensure that all tags were in place for any locations used in the analyses. 

CSV column description:

Index - index of location number

Status - whether location was successful (3 or more satellites)

Sats - number of satellites

RTC-date - Real-Time Clock date: the date recorded by the clock on-board the device (in GMT time)
RTC-time - Real-Time Clock time: the time recorded by the clock on-board the device (in GMT time)
FIX-date - the actual date calculated from satellite data
FIX-time - the actual time calculated from satellite data
Delta(s) - the difference between RTC-time and FIX-time in seconds
Latitude - latitude recorded by the device (after post-processing locations on a computer with an internet connection)
Longitude - longitude recorded by the device (after post-processing locations on a computer with an internet connection)
Altitude(m) - altitude recorded by the device (after post-processing locations on a computer with an internet connection)
HDOP - horizontal dilution of precision
eRes - Lotek proprietary error metric
Temperature(C) - temperature recorded by device
Voltage(V) - NA without solar panel
COLUMNS GENERATED IN R
Date - RTC-date with simpler name
FixDate - FIX-date with simpler name
Time - FIX-time with simpler name
DateTimeGMT - FIX-time transformed to POSIXct format (this will depend on how you import the csv file) (in GMT time)
DateTimeNZ - converted to POSIXct format (this will depend on how you import the csv file) (in local NZ time)
RefDist - the distance between the 'true' location recorded by Garmin GPSmap 60CSx (accuracy of <10m for 95% of locations) and the lat/long recorded by the SWIFT fix GPS device

