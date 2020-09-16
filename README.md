# Exploring Air Quality Data  

***A personal project to investigate the background air quality of Warrington (north west England) with an emphasis on data visualisation. Sample charts below. See the jupyter notebook A2_WAR_AQ.ipynb for discussion and python code.***

---

The locations of Automatic Urban and Rural Network (AURN) sites monitoring background levels of air pollutants (ie away from the kerbside) in north west England are shown on the map below. The size of the marker represents the relative nitrogen dioxide (NO2) level calculated from the ten year mean (2010-2019). NO2 results from combustion and is often a good indicator of general air pollution. Unsurprisingly the most rural areas (Ladybower and Glazebury)  have the lowest levels of NO2, and the largest urban areas (Manchester and Salford) have the highest levels.

![map](https://github.com/wriggy/air-datavis/blob/master/vis/F1_no2_aurn_sitemap.png)

Ten year means were calculated as shown in the barcharts below. Not all pollutants are measured at all sites. Specifically since ozone is not measured at the Warrington site, the nearby urban area of Liverpool Speke has been highlighted instead for comparison.

![means](https://github.com/wriggy/air-datavis/blob/master/vis/F2_no2_pm_o3_means.png)

There are strong seasonal variations in air pollution levels so smoothed time series have been plotted. The aim is to reveal underlying trends over the decade and to suggest how the different sites compare. Each point is an average of the preceding 365 daily means and the WHO guideline limit for the annual mean is shown for context. </br></br>*To minimise artefacts due to missing data, thresholds were set of 20 hours per daily mean and 75% of daily means per annual mean.*

![trends](https://github.com/wriggy/air-datavis/blob/master/vis/F3_no2_rolling_annual_means.png)

To get a view on how air quality varies throughout the day and over the year, ten years of pollutant data were split into month categories and averaged by hour (GMT). The resultant plots show how morning and afternoon peaks vary throughout the year. Note British Summer time is 1 hour later than GMT and runs from late March to late October. So any rush hour effects would appear 1 hour earlier in GMT.

![diurnal variations](https://github.com/wriggy/air-datavis/blob/master/vis/F6_Warrington_no2_diurnal_variation.png)

The data were split into categories and the quantiles calculated to give some insight into the influence of weekday, season and wind on pollutant levels. Each bar plotted represents the inter quartile range ie the middle three quarters of the hourly measurements in that category. The median values are also shown, connected by black lines.

![correlations](https://github.com/wriggy/air-datavis/blob/master/vis/F9_WAR_correlations.png)

To explore the impact of winds on the dispersion of local pollutants I looked at the particulate data around bonfire night (November 5th) together with modelled wind speed data for Warrington, 2010-2019. 2012 had the lowest mean modelled wind speed averaging about 1m/s for the 12 hours from 6pm on November 5th. 2016 had the highest at 7.3 m/s.

![bonfire night](https://github.com/wriggy/air-datavis/blob/master/vis/F10_bonfire_night_war_pm25.png)
