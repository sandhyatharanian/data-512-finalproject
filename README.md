## Mission Emergency - Investigate analysis on Cincinnati 911 Calls

## Abstract 

The 911 system was designed to provide a universal, easy-to-remember number for people to reach police, fire or emergency medical assistance from any phone in any location, without having to look up specific phone numbers. In 1966, the National Academy of Sciences published "[Accidental Death and Disability: The Neglected Disease of Modern Society](https://www.ems.gov/pdf/1997-Reproduction-AccidentalDeathDissability.pdf),” a landmark report highlighting how accidental death and injury, particularly from motor vehicle crashes, had become an epidemic in the U.S. The report urged a series of steps to reduce these needless deaths and injuries, including exploring the “feasibility of designating a single, nationwide, telephone number to summon an ambulance”  which resulted in the inception of 911 system. This final project explored the causes for contributing to the emergencies, average response time, and temporal variation within days of the week, and time of day for emergency calls in Cincinnati.


## Data used

The dataset used for this project is obtained from the City of Cincinnati's computer aided dispatch (CAD) database which contains fire incident responses including emergency medical services (EMS) calls, fires, rescue incidents, and all other services handled by the Fire Department. This dataset contains emergency call data from 1/1/2015 and is updated daily. The dataset is available as a public domain which allows to freely share and use the data for any purpose and without any restrictions.

Link to the website can be found [here](https://data.cincinnati-oh.gov/Safety/Cincinnati-Fire-Incidents-CAD-including-EMS-ALS-BL/vnsz-a3wp). <br/>
Link to the **dataset** can be accessed using the API Endpoint which can be found [here](https://data.cincinnati-oh.gov/resource/vnsz-a3wp.json).

## Output Files:
 - Code - [Bias in data.ipynb](https://github.com/sandhyatharanian/data-512/blob/main/data-512-a2/Assignment%202%20Bias%20in%20data.ipynb) file. 
 - Visuals - Output visuals are sorted as per the order of execution in the jupyter notebook and stored [here](https://github.com/sandhyatharanian/data-512/tree/main/data-512-a2/Output%20Visuals).

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


## directory tree in your markdown and an elementary description of each folder/file. 
