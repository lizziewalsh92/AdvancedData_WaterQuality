# Folder Directory

### **DEP Sample Site Analysis**: 
Analysis of the DEP's 2024 water sample analyses. These samples were taken from 1,000 street-side sampling stations across the city, which is available on OpenDataNYC [here](https://data.cityofnewyork.us/Environment/Drinking-Water-Quality-Distribution-Monitoring-Dat/bkwf-xfky/data_preview). Jupyter Notebook file used to analyze this data was: NYCOpenData_2024Water.ipynb. *Note: this data was not used in the article as samples were clean.

### **MCL Comparisons**: 
Tables that compare various contaminant Maximum Contaminant Levels across New York State, the U.S., Canada, the European Union, and California. *Note: this information was removed from the article for brevity.

### **WATER TANK AND LEAD PIPE DATA**: 
I used NYC's OpenData set "Free Residential at-the-tap Lead and Copper Data" [here] (https://data.cityofnewyork.us/Environment/Free-Residential-at-the-tap-Lead-and-Copper-Data/k5us-nav4/data_preview), which was made public 02/26/2018, to create the lead map. 35,205 samples were collected and analyzed beginning in 2014, and no sample analyses have been added since October 2023, though the data set information is "updated annually". Water tank map was created using the "NYC Drinking Water Tank Inspections and Audits Compliance Results" [here] (https://data.cityofnewyork.us/Health/NYC-Drinking-Water-Tank-Inspections-and-Audits-Com/rytv-g5ui/data_preview) and Self-Reported Water Tank Inspections; this data set was last updated on April 29, 2025. Also includes Jupyter notebook files analyzing and cleaning this data, and preparing it for visualization in Datawrapper. Jupyter Notebook files used to analyze the bulk of the data were: Tap_Lead_Copper Analysis.ipynb, CONCAT_2014-2023 Data.ipynb, Water Tank Data.ipynb

  [Map of contaminated water tanks, 2020-present](https://www.datawrapper.de/_/nBf2l/?v=9)
  
  [Map of over-limit lead samples across the city, 2014-2023](UPDATE)

### **Supplementary Analyses**: 
Additional raw data and Jupyter notebook files used to query and slice sample data.

### **TANK + LEAD INTERACTIVE**: 
HTML file and corrresponding lead data for resident interactive. Lead data was taken from the feature layer of the DEP's December 2024 [map of lead service lines](https://nycdep.maps.arcgis.com/apps/View/index.html?appid=fe8c7a4dd6d24959ac765660ba3a7c1a). Water tank data was taken from OpenDataNYC (see WATER TANK AND LEAD PIPE DATA).


# Analysis Methodology
This is the first public-facing tool of its kind to examine both key sources of water contamination in New York City.

The project began as a personal investigation into tap water quality in New York City apartments. In my search for data, I found that the official DEP water sampling data published and advertised yearly doesn’t reflect what comes out of our faucets; those samples are taken from upstate reservoirs and public street stations before hitting private water lines. The NYLCV's 2023 citywide historical water line report, though a touchstone for residents seeking information on the materials in their water lines, may not represent current lead levels in all NYC buildings, as some lines have been remediated. 

I turned to NYC OpenData and identified the three datasets that offer insight into real-time water quality: 2020-2025 city water tank inspection reports and two separate datasets of apartment-specific lead and copper testing results requested by residents. I cleaned and merged the two lead datasets to collate all available data from 2014-2023, converted lead results into standardized units that aligned with New York State’s Maximum Contaminant Levels, and dropped duplicates. I used the first draw results for analysis, as second draw values (water sampled after five minutes of water running) are not representative of resident tap use. Using Python and Excel functions countifs, averageifs, and dataset slicing, I summarized lead findings by zip code, showing how many samples exceeded legal thresholds, how far they exceeded them, and compared trends across the city. I converted these results into United Hospital Fund (UHF42) codes, the standard for geographic visualizations of public health. In copy, I compared contaminant levels against state, national, and international standards.

In my water tank data analysis, I filtered out outdated inspection entries, leaving only the most recent inspection results for each tank. I excluded structural issues from relevant violations, and sliced the dataset to focus on contaminants like sediment, insect debris, and E. coli. Using Excel and Python, I quantified how many tanks were inspected, how many failed contaminant inspections, and built a clean dataset that powered the interactive Datawrapper map.  

I integrated water tank data and the DEP's water line map into a custom interactive webpage, using JavaScript, CSS, and HTML code that allows users to enter their address and receive a summary of their building's water line status and most recent water tank inspection results. The full code, datasets, and visualizations are hosted on GitHub and Squarespace. 

## Key considerations: 
Readers should note that resident-requested lead sample data is collected at the discretion of the occupant and does not portray a normalized, summative, or conclusive analysis of lead levels across all neighborhoods. Resident-requested lead sample data from 2024-2025 was not available. This investigation illustrates the need for updated, comprehensive, publicly-available lead contamination data that is accessible to all New Yorkers.

## Link to full methodology: 
https://docs.google.com/document/d/1cVuOvbrFrNtfyHa5HmcUpniVJdXF60PveEYRAV85UiM/edit?tab=t.0
