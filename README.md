This module consists of 4 functions that perform velocity analysis on time series data. 
It includes functions to fit time series data, calculate uncertainties, and extract site coordinates. 
The module is designed to work with data stored in CSV files and can process multiple files at once. 
It is mainly applicable to tectonic movement data, but you may be able to find other uses!

More Details on the Functions:
fit_timeseries(tlist, ylist)
This function fits a linear model to a given time series data. It takes two parameters:

tlist: The list of time values.
ylist: The list of corresponding data values.
The function returns a tuple containing the slope of the linear fit and its uncertainty.

fit_velocities(filename, tname, ename, nname, uname)
This function fits time series data from a CSV file. It takes the following parameters:

filename: The path to the CSV file containing the data.
tname: The column name for the time values in the CSV file.
ename: The column name for the East (E) component of velocity data.
nname: The column name for the North (N) component of velocity data.
uname: The column name for the Up (U) component of velocity data.
The function returns site and the velocity components (E, N, U) along with their uncertainties.

get_coordinates(filename, lat, lon, elev)
This function extracts the mean latitude, longitude, and elevation from a CSV file. It takes the following parameters:

filename: The path to the CSV file containing the data.
lat: The column name for latitude data.
lon: The column name for longitude data.
elev: The column name for elevation data.
The function returns the mean latitude, longitude, and elevation.

fit_all_velocities(folder, pattern, tname, ename, nname, uname, lat, lon, elev)
This function processes multiple CSV files in a folder and performs velocity analysis on each file. It takes the following parameters:

folder: The path to the folder containing the CSV files.
pattern: A pattern to match the CSV files (e.g., '*.csv').
tname: The column name for the time values in the CSV files.
ename: The column name for the East (E) component of velocity data.
nname: The column name for the North (N) component of velocity data.
uname: The column name for the Up (U) component of velocity data.
lat: The column name for latitude data.
lon: The column name for longitude data.
elev: The column name for elevation data.
