# Directory

### **DEP Sample Site Analysis**: 
Analysis of the DEP's 2024 water sample analyses. These samples were taken from 1,000 street-side sampling stations across the city, which is available on OpenDataNYC [here] (https://data.cityofnewyork.us/Environment/Drinking-Water-Quality-Distribution-Monitoring-Dat/bkwf-xfky/data_preview)

### **MCL Comparisons**: 
Tables that compare various contaminant Maximum Contaminant Levels across New York State, the U.S., Canada, the European Union, and California.

### **WATER TANK AND LEAD PIPE DATA**: 
Primary datasets of resident-requested lead pipe samples and water inspection reports. Also includes Jupyter notebook files analyzing and cleaning this data, and preparing it for visualization in Datawrapper.
  [Map of contaminated water tanks, 2020-present] (https://www.datawrapper.de/_/nBf2l/?v=9)
  [Map of over-limit lead samples across the city, 2014-2023] (https://www.datawrapper.de/_/Bzzc4/?v=6)
  [Map of over-limit lead samples, 2021-2022] (https://www.datawrapper.de/_/ykxO3/?v=6)

### **Supplementary Analyses**: 
Additional data and Jupyter notbeook files used to analyze data.

### **TANK + LEAD INTERACTIVE**: 
HTML file and corrresponding lead data for resident interactive. Lead data was taken from the feature layer of the DEP's December 2024 [map of lead service lines] (https://nycdep.maps.arcgis.com/apps/View/index.html?appid=fe8c7a4dd6d24959ac765660ba3a7c1a)


# Analysis Methodology

This project began as a personal investigation into whether the tap water in my New York City apartment was truly safe to drink. I quickly discovered that official DEP water sampling data doesn’t reflect what comes out of our faucets—those samples are taken from upstate reservoirs and public street stations. To find more relevant data, I turned to NYC OpenData and identified three datasets that offered insight into the water actually reaching residents: five years of city water tank inspection reports, and two separate datasets of apartment-specific lead and copper testing results requested by residents. I chose to analyze the lead datasets separately to avoid duplication errors and converted all results into standardized units that aligned with New York State’s Maximum Contaminant Levels. Using Python and Excel functions like countifs, averageifs, and dataset slicing, I summarized lead findings by zip code, showing how many samples exceeded legal thresholds, how far they exceeded them, and overall trends across the city.

For the water tank data, I focused on the most recent inspection results for each tank, filtering out outdated or irrelevant entries. I excluded structural issues and highlighted violations tied to bacterial or physical contaminants such as sediment, insect debris, and E. coli. Using Excel and Python, I quantified how many tanks failed inspections and built a clean dataset that fed into an interactive Datawrapper map with bolded tooltips showing key violations. I also compared all contaminant levels against state, federal, and international standards. Finally, I integrated the findings into a custom interactive webpage by writing JavaScript functions that allow users to enter their address and receive a summary of possible lead exposure and water tank risks. The full code, datasets, and visualizations are hosted on GitHub and Datawrapper. This is the first public-facing tool of its kind to examine both key sources of water contamination in NYC apartments.
