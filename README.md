# Query-Patient-Information-TCGA

# Description

Given an existing TCGA dataset, queries patients by demographic or gender and adds the new information to an existing matrix of features.

This code was written for a project to identify which mutations in cancer patients are promising targets for gene therapy treatments. This project was conducted during the Summer of 2018 in the Rabadan lab at Columbia Medical Center in New York, NY.

For more information on the project and results, see the paper attached entitled "ProjectSummary_BoostingTOBIPerformance.pdf."

# Files

**Name: getPatientInfo.py**

Description: Gets gender/race information for a dataset by querying the TCGA API and creates a new Excel sheet named "[dataset name]-patient-data.xlsx" where the first column contains the case ID, the second column contains the submitter ID, and the third column contains the corresponding data. For each feature, a new sheet will be added.

To run: Run in terminal with the TCGA category as the first input parameter, then the different responses expected.

Example: getPatientInfo.py cases.demographic.gender male female

**Name: downloadxmldata.py**

Description: Obtains tumor stage information for a dataset by querying the clinical XML files for each patient file and saving the extracted information to a new sheet in "[dataset name]-patient-data.xlsx." If no information found, the error code is "no data."

To Run: Run in terminal with the dataset name as the first input parameter.

Example: downloadxmldata.py TCGA-SKCM

**Name: addPatientInfoColumnsDictionary.py**

Description: Matches the patient information stored in "[dataset name]-patient-data.xlsx" with the raw downloaded data in "[dataset name]-raw.xlsx" and creates a new Excel sheet containing all of the information called "[dataset name]-added.xlsx."

To Run: Run in terminal with the dataset name as the first input parameter.

# Credits

Francesco Brundu (Mentor)
Raul Rabadan (PI)
