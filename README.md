**Methods**
 -  Data Acquisition:
    - Observation records of the Common Five-lined Skink (Plestiodon fasciatus) were downloaded from iNaturalist. Land cover data were taken from the USGS NLCD 2021, and Gwinnett county boundary and hydrography layers were taken from Gwinnett County GIS.
  - Data Preparation:
    - NLCD raster data was reclassified into six general habitat types and clipped to the Gwinnett County boundary. This was overlaid with Gwinnett County road centerlines in addition to rivers and ponds. The reclassified habitat types are as follows:
       - Water
       - Developed land
       - Forest
       - Shrub & Grass
       - Agriculture
       - Wetlands
    - Raster values were taken from the reclassified land cover raster and mapped to each skink observation with the Sample Raster Values tool in QGIS, thus assigning every skink observation one of six habitat classes.
   - Habitat Analysis:
     - Frequency of skink observations in each habitat class was summarized and used to calculate habitat availability. This was done using pixel counts of each classified raster habitat type. Then, habitat availability was compared to observed habitat use.
   - Cartography:
     - A finalized map was created in QGIS displaying skink observations over simplified land cover including a legend, scale bar, north arrow, and data sources.


**Results**

| Habitat       | County % | Skink % |
| ------------- | -------- | ------- |
| Water         | 0.95     | 0       |
| Developed     | 73.11    | 62.1    |
| Forest        | 20.14    | 27.2    |
| Shrub & Grass | 0.18     | 1.0     |
| Agriculture   | 3.77     | 1.0     |
| Wetlands      | 1.84     | 8.7     |


**Conclusion**

  - While most observations occured in developed areas, devloped land makes up nearly three quarters of Gwinnett County. Relative to habitat availability, skinks were observed disproportionately more often in forested and wetland habitats. This suggests that these habitat types may be more suitable for skinks than expected based on abundance alone.


**GIS Workflow:**

- Download iNaturalist skink observations
        
- Import observations to QGIS
            
- Download NLCD 2021 land cover map
           
- Clip raster to Gwinnett County boundaries
           
- Reclassify land cover into six habitat classes
            
- Extract habitat values to skink observations
            
- Summarize habitat frequencies
          
- Calculate habitat availability
            
- Compare habitat use to habitat availability
            
- Create final thematic map


**Tools Used**

- QGIS 4.2
- Clip Raster by Mask Layer
- Raster Calculator
- Reclassify by Table
- Sample Raster Values
- Raster Layer Unique Values Report
- Layout Manager


**Data sources:**

  - https://www.inaturalist.org/taxa/73788-Plestiodon-fasciatus
  - https://gcgis-gwinnettcountyga.hub.arcgis.com/
  - https://www.mrlc.gov/data/type/land-cover
