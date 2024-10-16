# IAQ_database_data_handling
The repo provides instructions and sample codes for standardizing and uploading your data to the first global pilot IAQ database

First of all, thank you for your time and effort in submitting your data. Collectively, we are creating the first global pilot IAQ database that will allow for answering crucial research questions towards a better and more sustainable built environment.  

**1. Instructions on how to contribute to the first global pilot IAQ database**

**Overview**
To facilitate data collection and database construction, we kindly ask you to standardize your IAQ data format before uploading the data file. This instruction shows the desired formats for time-integrated measurements (such as VOC results from active samplers) and time series data, respectively, as well as how to prepare them. 

**For time series data**

This type of measurement applies to all measurements that have associated timestamps. Please use the long format, i.e., each contaminant species takes a column. Mandatory columns include timestamp, contaminant concentrations, and building, space, and instrument identifiers that match metadata.

An example of the target format is shown as follows. 

 <img width="414" alt="image" src="https://github.com/user-attachments/assets/9ce97eb1-d62e-414a-b41b-241c6154a792">

The name of identifier columns should be exactly “Building identifier”, “Space identifier”, and “Instrument identifier”. The name of the concentration column should include the unit following the name of the contaminant, separated by a comma. Example: “CO2, ppm”. The same applies to temperature, humidity data. 

Data across multiple buildings and spaces can be either concatenated (vertically) together or submitted individually, as long as they have the same structure and the building and space identifiers are clearly labeled. However, please separate data from different instruments unless they have identical columns. 


**For time-integrated data**

This type of measurement mostly applies to VOCs and bio-contaminants. Please also use the long format, i.e., each contaminant species takes a column. Mandatory columns include contaminant concentration, and building, space, and instrument identifiers that match metadata. The start and end time of measurement are highly recommended (if not provided, the start and end year of the study will be used to label the data). For VOCs, please also include CAS numbers in the header (the second row) if available. 

An example of the target format is shown as follows. 

 <img width="452" alt="image" src="https://github.com/user-attachments/assets/e2dec497-726d-4664-a191-d287b7fccf69">


The name of identifier columns should be exactly “Building identifier”, “Space identifier”, and “Instrument identifier”. The name of the start and end time of measurement should be exactly “Start time” and “End time”, respectively. The name of the concentration column should include the unit following the name of the contaminant, separated by a comma. Example: “Benzene, ppb”. 

Data across multiple buildings and spaces can be either concatenated (vertically) together or submitted individually, as long as they have the same structure and the building and space identifiers are clearly labeled. However, please separate data from different instruments unless they have identical columns. 

**2. Instructions on how to contribute to the first global pilot IAQ database**

**Overview**

The aim of collecting metadata is to label the actual IAQ data with relevant building-, space-, and instrument-related information, so the end user can filter and analyze the data according to their interest. After thorough considerations, we decided to collect five types of metadata: study, contributor, building, space, and instrument. Under each category, metadata are further attached with three levels of importance.

$${\color{red}Mandatory}$$ : metadata that are crucial for creating a structured database, without which one cannot submit actual IAQ data. 

$${\color{orange}Recommended}$$: metadata that are very helpful for attaching building-related information and exploring the database. 

$${\color{green}Optional}$$:: metadata that are useful but difficult to collect; or metadata that are for acknowledging your effort.  

Link to the web tool:
https://iaqdb-dev.epfl.ch/#/contribute

Depending on the scale of the study, we provide two methods for submitting metadata. For smaller studies involving a few buildings, please consider using the structured metadata collection form and manually fill in it. For larger studies consisting of data from many buildings, please consider downloading the spreadsheet template and upload it once finished. The web tool is capable of parsing information from the template, and you will also be able to confirm or edit the parsing result. 

<u>Using the online data entry form</u>

The online data entry form is still in the developer mode. It contains three main pages. 
1)	Study information. Currently, mandatory information includes name of your study and at least one contributor with a valid email address. 

<img width="373" alt="image" src="https://github.com/user-attachments/assets/a00a79de-731d-490d-870e-65bf3df4634b">

Click “Add Contributor” to add name and email address. Up to two contributors can be added per study. 

<img width="369" alt="image" src="https://github.com/user-attachments/assets/4ffa3367-bd3f-405a-9b57-bd2abc0efadf">

2)	Buildings and spaces information. 
Please start from “Add Building”. Mandatory information includes identifier (must be unique within your study, for linking with actual IAQ data), Country, City, and Building type. 

<img width="406" alt="image" src="https://github.com/user-attachments/assets/13299981-f5b2-4b7e-8e17-274d3cf729f3">

Within a building, you may add multiple spaces. Adject outdoor space or personalized monitoring is also considered a “space” here. However, only add them if there is an associated indoor space. Mandatory information includes identifier (must be unique within the building, for linking with actual IAQ data) and space type. 
3)	Instrument information. Please add instruments used in the study one by one. Mandatory information is identifier (must be unique within your study, for linking with actual IAQ data). 

<img width="360" alt="image" src="https://github.com/user-attachments/assets/4196398a-81a8-4326-9de0-c4183a5a47f3">

4)	Afterward, please proceed to upload your actual IAQ data. The data should be in “standardized” formats (separate instructions available) and must contain building, space, and instrument identifiers that can be used to match metadata. 


<u>Using the spreadsheet template</u>

The template can be downloaded and then uploaded as shown in the screenshot below. It includes macro functions so please choose to enable macros when opening the file. 

<img width="452" alt="image" src="https://github.com/user-attachments/assets/d6a13cef-8b3f-484c-9e12-568139ad98e9">

An example is provided to illustrate the expected input format. Please delete the existing rows when filling in the sheets. Please do not add or delete columns or change their names. 

Please fill in the first five sheets in order, ranging from Study to Instrument and ignore the “Drop-down list” sheet that is only intended for creating drop-down selections. 
Special notes:
1)	Under sheet Study, the form asks for whether the study investigated any indoor environmental impact on occupants (e.g., comfort and health) and any other environmental parameters. These two questions allow for multiple selection. However, for removing an answer, you will need to clear the cell and start again (the multiselection doesn’t allow for removing an answer). 

<img width="452" alt="image" src="https://github.com/user-attachments/assets/77646e04-da6f-4618-a49c-0f9764f41d2b">

2)	Under sheet Contributor, up to two names can be provided. Please provide at least one email address for us to contact you in case of incomplete data. You can indicate whether you hope to have your email address available to end users or not here. 
3)	Under sheet Building, please assign a unique identifier to each of the buildings in the study, which can be string or numeric. 
4)	Under sheet Space, please carefully check to which building each of the spaces belong. Then, please assign a unique identifier to each of the spaces within the building, which can be string or numeric. Then, please match the building type according to building identifier using the provided “VLOOKUP” function. The building type will determine the list of space types available to choose from. 

<img width="366" alt="image" src="https://github.com/user-attachments/assets/73ffa302-b7d1-4995-8ce1-3e77b34f6eaf">

5)	Under sheet Instrument, please try to provide complete information about the sensors used for measurements. 

After you upload the spreadsheet template, the web tool will capture the relevant metadata. You will be able to upload actual data after confirming the metadata are complete and correct. 

Afterward, please proceed to upload your actual IAQ data. The data should be in “standardized” formats (separate instructions available) and must contain building, space, and instrument identifiers that can be used to match metadata. 


**Contact information**

Dr. Bowen Du
Human-Oriented Built Environment Lab (HOBEL)
School of Architecture, Civil and Environmental Engineering
École polytechnique fédérale de Lausanne (EPFL)
bowen.du@epfl.ch

