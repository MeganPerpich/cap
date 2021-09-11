#install.packages("PWFSLSmoke")
#install.packages('MazamaSpatialUtils')
??PWFSLSmoke
library(PWFSLSmoke)
library(MazamaSpatialUtils)
library(AirSensor)


#####Minneapolis map

library(leaflet)
minneapolis_map <- leaflet() %>%
  addTiles() %>%
  setView(lng=-93.26384, lat=44.97997, zoom=11)

minneapolis_map

monitor_map <- monitor_leaflet(minnesota_fire)
monitor_map

sensor_map <- pas_leaflet(pas_example)
sensor_map


######Air Quality Monitors Minneapolis 2015

minnesota_2015 <-
  monitor_loadAnnual(2015) %>%
  monitor_subset(stateCodes = 'MN')

minneapolis_2015 <-
  minnesota_2015 %>%
  monitor_subset(monitorIDs = c('270530962_01', '270530963_01', '270531909_01')) 

monitor_timeseriesPlot(
  minnesota_2015,
  style='aqidots',
  pch=16,
  xlab="2015"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2015")


#####Air Quality Monitors Minneapolis 2016
minnesota_2016 <-
  monitor_loadAnnual(2016) %>%
  monitor_subset(stateCodes = 'MN')

minneapolis_2016 <-
  minnesota_2016 %>%
  monitor_subset(monitorIDs = c('270530962_01', '270530963_01', '270531909_01')) 

monitor_timeseriesPlot(
  minnesota_2016,
  style='aqidots',
  pch=16,
  xlab="2016"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2016")


#####Air Quality Monitors Minneapolis 2017

minnesota_2017 <-
  monitor_loadAnnual(2017) %>%
  monitor_subset(stateCodes = 'MN')

minneapolis_2017 <-
  minnesota_2017 %>%
  monitor_subset(monitorIDs = c('270530962_01', '270530963_01', '270531909_01')) 

monitor_timeseriesPlot(
  minnesota_2017,
  style='aqidots',
  pch=16,
  xlab="2017"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2017")


######Air Quality Monitors Minneapolis 2018

minnesota_2018 <-
  monitor_loadAnnual(2018) %>%
  monitor_subset(stateCodes = 'MN')

minneapolis_2018 <-
  minnesota_2018 %>%
  monitor_subset(monitorIDs = c('270530962_01', '270530963_01', '270531909_01')) 

monitor_timeseriesPlot(
  minnesota_2018,
  style='aqidots',
  pch=16,
  xlab="2018"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2018")


######Air Quality Monitors Minneapolis 2019

minnesota_2019 <-
  monitor_loadAnnual(2019) %>%
  monitor_subset(stateCodes = 'MN')

minneapolis_2019 <-
  minnesota_2019 %>%
  monitor_subset(monitorIDs = c('270530962_01', '270530963_01', '270531909_01')) 

monitor_timeseriesPlot(
  minnesota_2019,
  style='aqidots',
  pch=16,
  xlab="2019"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2019")


######Air Quality Monitors Minneapolis 2020

minnesota_2020 <-
  monitor_loadAnnual(2020) %>%
  monitor_subset(stateCodes = 'MN')

minneapolis_2020 <-
  minnesota_2020 %>%
  monitor_subset(monitorIDs = c('270530962_01', '270530963_01', '270531909_01')) 

monitor_timeseriesPlot(
  minnesota_2020,
  style='aqidots',
  pch=16,
  xlab="2020"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2020")


######### AIr Quality Sensors Minneapolis 2015

library(AirSensor)

pas <- example_pas
air_sensors_minneapolis <-
  pas %>%
  pas_filterNear(
    longitude = -93.26384,
    latitude = 44.97997, 
    radius = "10 km"
  )

if ( interactive() ) {
  pas_leaflet(air_sensors_minneapolis)
}




monitor_timeseriesPlot(
  air_sensors_minneapolis,
  style='aqidots',
  pch=16,
  xlab="2020"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Air Quality Monitors Minneapolis 2020")


initializeMazamaSpatialUtils()

example_sensor <- pat_createNew(
  label = "SCAN_14",
  pas = example_pas,
  startdate = "2018-08-14",
  enddate = "2018-09-07"
) 
pat_createAirSensor(parameter = 'pm25', FUN = AirSensor::PurpleAirQC_hourly_AB_01)

save(example_sensor, file = "data/example_sensor.rda")


library(AirSensor)
setArchiveBaseUrl("http://data.mazamascience.com/PurpleAir/v1")




###air sensor 




minneapolis <-
  minnesota_fire %>%
  monitor_subset(monitorIDs = 'PA_108334') #specific code from air quality
  #monitor that can be found through monitor_leaflet(minnesota fire) command

monitor_timeseriesPlot(
  minneapolis,
  style='aqidots',
  pch=16,
  xlab="2020"
)
addAQIStackedBar()
addAQILines()
addAQILegend(cex=0.8)
title("Minneapolis Smoke")  #creates specific smoke annual plot for specific city

minneapolis_area <- minnesota_fire %>% monitor_subsetByDistance(longitude = minneapolis$meta$longitude, latitude = minneapolis$meta$latitude, radius = 50)
monitor_leaflet(minneapolis_area) #creates specific aqi level map for city

##

###

###

####

#####
library(leaflet)
minneapolis_map <- leaflet() %>%
  addTiles() %>%
  setView(lng=-93.26384, lat=44.97997, zoom=11)

minneapolis_map



airnow_data_2017 <- airnow_loadAnnual(2017) %>%
  monitor_subset(stateCodes='MN') %>%
  monitor_dailyStatistic() %>%
  monitor_timeseriesPlot(style = 'gnats', ylim=c(0,300), xpd=NA)
title("Minnnesota 2017 -- AirNow Daily Average PM2.5")

airnow_data_2017

