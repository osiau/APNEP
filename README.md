# APNEP
This repository includes APNEP data files used to analyze wetland loss minimization and community resilience.

This repository consists of three folders of data used for analysis: boundaries, community resilience, and wetland suitability. The wetland suitability folder contains data for both APNEP goals of wetland conservation and restoration. The coordinate reference system used for all data varies by file but should be included in the metadata files in each folder. 

## boundaries
This folder contains the APNEP boundary used to clip the rest of the data. It also includes counties, census tracts, and points of interest for the study area.

## community_resilience
This folder contains data about population migration, disadvantage, and rural capacity.

## wetland_suitability
This folder contains suitability data for both conservation and restoration goals. The files that end in _suitability mean that their values were changed to reflect suitability. For example, in the open water raster all values where water exists are 0 while any other area within the study area is 1 to demonstrate suitability. 
