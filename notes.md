## Observations

We might be able to treat lat/lon as a combined categorical variable. The question is whether there's a signficant spatial trend to the CO2 behavior. A cursory map look doesn't reveal anything obvious.

We're trying to predict CO2 emissions as provided by the Copernicus Atmosphere Monitoring Service.

We'll be evaluated vs. true data for 2020 using RSME. 

This whole thing is pointless with regard to CCSS if we're talking about the location of direct air capture facilities. I highly doubt localized CO2 emissions make a significant difference in atmospheric CO2 concentration. 


Since 2020 was such a weird year with COVID, we might want to 

5 CSV submissions per day, made by one person on the team. 


There are big spikes in local emmisions in the winter (January) and summer (July and August).

I would expect colder climates to have a bigger January peak and warmer climates to have a bigger summer peak.

CO2 concentrations are higher in the Northern Hemisphere. However, the variance on earth's surface between high and low concentration areas is insignificant. A high-concentration area might have a 2% higher concentration of CO2 than a low-concentration area. 
https://upload.wikimedia.org/wikipedia/commons/5/5f/AIRS_Carbon_Dioxide_Vertical.png
https://earthsky.org/earth/6-things-to-know-carbon-dioxide-co2-greenhouse-gas/
Therefore we can conclude that atmospheric emissions monitoring is not useful for Direct Air Capture (DAC) location planning. It could, however, be useful for considereing locations for point source carbon capture and storage (e.g., from power plants)

The data given to us is clearly derived/modeled off of some observational data. This is clear because it's too perfect. 

Theory about how it works:
* They derive annual data according to some trend.
* There are four "zones" that they use that are somewhat geographic in nature: continental US, Mexico, East coast, and Canada. 
* These zones have specific profiles for months, whereby monthly rates are assumed to be a determinate fraction of the annual emmissions.
* Yearly numbers since 2012 follow a clear geometric decay trend. We can perfectly model 2020 annual numbers by station if we calculate the polynomial equation for each station.


I believe the training data was derived from the original CAMS global emission inventories dataset. The original dataset has points defined globally and evenly spaced in a grid. Points are at lats and lons spaced 0.1 apart. These points all end with XX.X5. However in our training dataset, the points are at XX.X0. I'm guessing this data was made by averaging the existing data or by adding some kind of offset to it.