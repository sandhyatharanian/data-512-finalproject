## Mission Emergency - Investigate analysis on Cincinnati 911 Calls

## Abstract 
In 1966, the National Academy of Sciences published "[Accidental Death and Disability: The Neglected Disease of Modern Society](https://www.ems.gov/pdf/1997-Reproduction-AccidentalDeathDissability.pdf),” a landmark report highlighting how accidental death and injury, particularly from motor vehicle crashes, had become an epidemic in the U.S. The report urged a series of steps to reduce these needless deaths and injuries, including exploring the “feasibility of designating a single, nationwide, telephone number to summon an ambulance”  which resulted in the inception of 911 system. This final project explored the causes for contributing to the emergencies, average response time, and temporal variation within days of the week, and time of day for emergency calls in Cincinnati.


## Dataset Details

The dataset used for this project is obtained from the City of Cincinnati's computer aided dispatch (CAD) database which contains fire incident responses including emergency medical services (EMS) calls, fires, rescue incidents, and all other services handled by the Fire Department. This dataset contains emergency call data from 1/1/2015 and is updated daily. The dataset is available as a public domain which allows to freely share and use the data for any purpose and without any restrictions.

Link to the website can be found [here](https://data.cincinnati-oh.gov/Safety/Cincinnati-Fire-Incidents-CAD-including-EMS-ALS-BL/vnsz-a3wp). <br/>
Link to the **dataset** can be accessed using the API Endpoint which can be found [here](https://data.cincinnati-oh.gov/resource/vnsz-a3wp.json).

## Dataset Description

The data is collected for all available months using the API endpoint and the raw data is read into a dataframe. Next, the data is processed, transformed and finally saved as 6 separate `.csv` files with the naming convention – “cincinnati911_year.csv”. The final data is a combination of all 6 .csv files with the below column description.

| Column | Value |
| ------ | ----- |
|Day of Week| Specifies the day in which the incident took place|
|Hour| Specifies the hour at which the incident took place|
|Month| Specifies the month in which the incident took place|
|year| Specifies the year in which the incident took place|
|address_x|This attribute is the street name that the incident occurred on|
|agency|The agency that responded|
|arrival_time_primary_unit|This attribute is when the first CFD apparatus arrived on scene at the incident|
|beat|This attribute indicates what fire response area the incident belongs to|
|cfd_incident_type|This attribute shows the breakdown of the incident type classification|
|cfd_incident_type_group|The high-level incident type category for each incident|
|closed_time_incident|This attribute is when the incident is marked complete in the CAD system|
|community_council_neighborhood|The listed neighborhood of the incident using community council defined boundaries|
|create_time_incident|This attribute is when the response data was submitted into the CAD system|
|dispatch_time_primary_unit|This attribute is when first apparatus was dispatched to respond to an incident|
|disposition_code|The disposition code retreived from the disposition_text|
|disposition_text|The disposition of each incident is the outcome of the incident response|
|event_number|The unique identifier of the incident|
|incident_type_desc|The text description of the corresponding problem code|
|incident_type_id|The problem code of the incident that is used to describe the issue|
|latitude_x|The latitude coordinates of the incident|
|longitude_x|The longitude coordinates of the incident|
|neighborhood|The listed neighborhood of the incident using the SNA|
|response_rate_minutes|Difference between arrival_time_primary_unit and create_time_incident|
|call_type| Lists whether the call is emergency or non-emergency|
|reason|The high-level incident type based on cfd_incident_type_group|
|series|The high-level grouping of average response time|
|time_of_the_day| Indicates when the incident occurred during the day|


## Input Files 

For this analysis, I have used the 6 csv files saved in the [Input Data Files](https://github.com/sandhyatharanian/data-512-finalproject/tree/main/Input%20Data%20Files) folder. I have split files based on the year due to GIT's size constraints.

The names of the 6 csv files are listed below - 

- cincinnati911_2015.csv
- cincinnati911_2016.csv
- cincinnati911_2017.csv
- cincinnati911_2018.csv
- cincinnati911_2019.csv
- cincinnati911_2020.csv

**Note-** 

 - Download the `.csv` files and upload them to the jupyter environment before proceeding to use the `.ipynb` notebook.
 - The dataset was checked for blank/null values. 

## Output Files

 - Data retrieval and scrubbing - [A7 Data Retrieval - Scrubbing.ipynb](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/A7%20Data%20Retrieval%20-%20Scrubbing.ipynb) 
 - Final project Code - [A7 Final Project - Mission Emergency.ipynb](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/A7%20Final%20Project%20-%20Mission%20Emergency.ipynb) file. 
 - Visuals - Output visuals are sorted as per the order of execution in the jupyter notebook and stored [here](https://github.com/sandhyatharanian/data-512-finalproject/tree/main/Output%20Visuals).
 
## Directory tree structure

 * [data-512-finalproject](https://github.com/sandhyatharanian/data-512-finalproject)
   * [Input Data Files](https://github.com/sandhyatharanian/data-512-finalproject/tree/main/Input%20Data%20Files)
         * [cincinnati911_2015.csv](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Input%20Data%20Files/cincinnati911_2015.csv)
         * [cincinnati911_2016.csv](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Input%20Data%20Files/cincinnati911_2016.csv)
         * [cincinnati911_2017.csv](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Input%20Data%20Files/cincinnati911_2017.csv)
         * [cincinnati911_2018.csv](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Input%20Data%20Files/cincinnati911_2018.csv)
         * [cincinnati911_2019.csv](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Input%20Data%20Files/cincinnati911_2019.csv)
         * [cincinnati911_2020.csv](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Input%20Data%20Files/cincinnati911_2020.csv)
   * [Output Visuals](https://github.com/sandhyatharanian/data-512-finalproject/tree/main/Output%20Visuals)
    * [#1 Distribution of emergency vs non-emergency calls.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%231%20Distribution%20of%20emergency%20vs%20non-emergency%20calls.JPG)
    * [#2 Distribution of 911 calls by incident and service type.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%232%20Distribution%20of%20911%20calls%20by%20incident%20and%20service%20type.JPG)
    * [#3 YOY trend in emergency vs non-emergency call.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%233%20YOY%20trend%20in%20emergency%20vs%20non-emergency%20call.JPG)
    * [#4 Top reasons for emergency calls.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%234%20Top%20reasons%20for%20emergency%20calls.JPG)
    * [#5 Top reasons for non-emergency calls.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%235%20Top%20reasons%20for%20non-emergency%20calls.JPG)
    * [#6 YOY trend in average response rate.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%236%20YOY%20trend%20in%20average%20response%20rate.JPG)
    * [#7 Distribution of 911 calls based on time of the day.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%237%20Distribution%20of%20911%20calls%20based%20on%20time%20of%20the%20day.JPG)
    * [#8 Associations between the day of the week and hour.JPG](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/Output%20Visuals/%238%20Associations%20between%20the%20day%20of%20the%20week%20and%20hour.JPG)
 * [.gitignore](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/.gitignore)
 * [A7 Data Retrieval - Scrubbing.ipynb](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/A7%20Data%20Retrieval%20-%20Scrubbing.ipynb)
 * [A7 Final Project - Mission Emergency.ipynb](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/A7%20Final%20Project%20-%20Mission%20Emergency.ipynb)
 * [LICENSE](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/LICENSE)
 * [README.md](https://github.com/sandhyatharanian/data-512-finalproject/blob/main/README.md)


## Python packages used

- pandas version 1.0.3
- numpy  version 1.18.1
- seaborn  version 0.10.0
- matplotlib version 3.1.3
- tabulate version 0.8.7
- sodapy version 2.1.0

Note - Packages used along with its version can be found using **pip list** command.

## Required resources

- [Fire Disposition Codes](https://data.cincinnati-oh.gov/api/views/vnsz-a3wp/files/0b9dac12-3a5f-4771-b33e-edc049ba0c21?download=true&filename=Fire%20Disposition%20Codes.pdf)
- [Cincinnati Fire Incidents (CAD) Data Dictionary](https://data.cincinnati-oh.gov/api/views/vnsz-a3wp/files/b149e911-467c-4828-9701-434e95cded55?download=true&filename=Cincinnati%20Fire%20Incidents%20(CAD)%20Data%20Dictionary.pdf)


## License Information

License information for the dataset can be found [here](https://opendatacommons.org/licenses/pddl/1-0/).
