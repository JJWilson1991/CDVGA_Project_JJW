# Temporal and Spatial Patterns in Distemper Virus Cases Reported to SCWDS, 1975-2013
Class Project repository for Jonathan Wilson


# Data, Processing and Analysis Scripts
All code, figures, and text are reproducible from the project repository.

## Raw Data
Raw Data is located in the raw_data subfolder, within the data folder. This contains the files "SCWDS_CDVdata", "Canine_Distemper_Virus_Reports", "2013_GAcensus_data" and "GA_County_Area". The contents of these raw data are detailed in "CDV_codebook".

## Processed Data
Processed Data is located in the "processed_data" subfolder. The code to process the data is with "processing_code"" inside of the "code" folder.

## Data Exploration and Analysis
The files to run the various explorations and analyses on the cleaned data are within "processing_code", inside of the "code" folder. Figures of interest are saved as png files with the "results" subfolder.

## Manuscript and Supplemental figures
These can be found within the "products" subfolder.

##Executing the Project Code
Run the markdown files in the following order to reproduce project:

1.	code -> processing_code 
Run the files “CDV_Processing” and ”Month_Data_Processing”, these will load and clean the raw data and save the processed data into the “data/processed_data folder”.

2.	code -> analysis_code
Run the files; “ExploratoryAnalysis”, ”MappingCode”, ”SpatialAnalysis”, and ”TimeSeries”. These will reproduce the analyses conducted in the project and save the various results figures into the “results” folder.

3.	products -> manuscript
Run the file “JJW_Project_Manuscript.rmd” to reproduce the manuscript as an html. Run the “Supplemental_Materials.rmd” file to reproduce the supplemental figures not included in the main manuscript.
