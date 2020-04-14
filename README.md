#  How to create Heatmaps in R.. Here the code you need


################################################################################
### World Ozone and Ultraviolet Radiation Data Centre (WOUDC)
### Heatmaps of Time Space Measurement Completeness 
###  Created by Dr. Souleymane SY  CNR-IMAA, Potenza, IT - Contact: souleymane.sy@imaa.cnr.it
###  April--2020 under C3S-512 
### see https://woudc.org/data/stations/?lang=en  for more information on WOUDC datasets
###################################################################################
Here the different steps you need to follow..

1- First of all installing and loading all required packages

if (!require("ncdf4")) {
   install.packages("ncdf4", dependencies = TRUE)
   library(ncdf4)
   }


2) Reading your data from "your file .cvs ou .nc"  and transforms it into matrix 

3) Extract  Data, Time, Station Identification Number from the matrix

4)  List of stations, Date of measurement and  Number of years
### Here put your stations ID name example: ListStation=c("STATION-1","STATION-2","STATION-3",...,"STATION-N")
### List of all STATION ID Numbers as define in https://woudc.org/data/stations/?lang=en

5) This step consist to arrange the station by latitude order i.e. from 90S to 90N (it is optional)

6) Reading all Data and transform them into a "Ozone_Array" of to 2 dimensions (station and time)

7) Reshape  "Ozone_Array" Data in to a matrix of 3 dimensions (Stations, Years, Month) 

8) 1- Creating a matrix of 1 or NA values (i.e when data exist, put 1 otherwise put NA values)
###    2- Creating a matrix of a sum of all existing monthly values variant from 0 to 12

9) Define colors and array for x and y labels (indicating time from 1-1-1958 to 31-12-2019 displayed as YYYY - only)

10) Customizing and plotting different heatmaps by latitudes

and Now you got your plots.....









