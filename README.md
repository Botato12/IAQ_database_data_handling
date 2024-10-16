# IAQ_database_data_handling
The repo provides instructions and sample codes for standardizing and uploading your data to the first global pilot IAQ database

**1. Instructions on how to contribute to the first global pilot IAQ database**

First of all, thank you for your time and effort in submitting your data. Collectively, we are creating the first global pilot IAQ database that will allow for answering crucial research questions towards a better and more sustainable built environment.  

**Overview**
To facilitate data collection and database construction, we kindly ask you to standardize your IAQ data format before uploading the data file. This instruction shows the desired formats for time-integrated measurements (such as VOC results from active samplers) and time series data, respectively, as well as how to prepare them. 

**For time series data**
This type of measurement applies to all measurements that have associated timestamps. Please use the long format, i.e., each contaminant species takes a column. Mandatory columns include timestamp, contaminant concentrations, and building, space, and instrument identifiers that match metadata.

An example of the target format is shown as follows. 
 

The name of identifier columns should be exactly “Building identifier”, “Space identifier”, and “Instrument identifier”. The name of the concentration column should include the unit following the name of the contaminant, separated by a comma. Example: “CO2, ppm”. The same applies to temperature, humidity data. 

Data across multiple buildings and spaces can be either concatenated (vertically) together or submitted individually, as long as they have the same structure and the building and space identifiers are clearly labeled. However, please separate data from different instruments unless they have identical columns. 


**For time-integrated data**
This type of measurement mostly applies to VOCs and bio-contaminants. Please also use the long format, i.e., each contaminant species takes a column. Mandatory columns include contaminant concentration, and building, space, and instrument identifiers that match metadata. The start and end time of measurement are highly recommended (if not provided, the start and end year of the study will be used to label the data). For VOCs, please also include CAS numbers in the header (the second row) if available. 

An example of the target format is shown as follows. 
 

The name of identifier columns should be exactly “Building identifier”, “Space identifier”, and “Instrument identifier”. The name of the start and end time of measurement should be exactly “Start time” and “End time”, respectively. The name of the concentration column should include the unit following the name of the contaminant, separated by a comma. Example: “Benzene, ppb”. 

Data across multiple buildings and spaces can be either concatenated (vertically) together or submitted individually, as long as they have the same structure and the building and space identifiers are clearly labeled. However, please separate data from different instruments unless they have identical columns. 


Sample codes
Examples of the data standardization process are demonstrated. Please refer to “data_standardization.ipynb” for the Python version and “data_standardization.Rmd” for the R version.





Contact information
Dr. Bowen Du
Human-Oriented Built Environment Lab (HOBEL)
School of Architecture, Civil and Environmental Engineering
École polytechnique fédérale de Lausanne (EPFL)
bowen.du@epfl.ch
![image](https://github.com/user-attachments/assets/a48b8fc1-3e68-4d22-9b0b-c6548d9961d7)
