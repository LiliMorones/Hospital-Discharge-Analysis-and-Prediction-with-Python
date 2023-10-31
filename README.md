
# Hospital Discharge Analysis and Prediction with Python

## Description

The purpose of this project was to practically apply the concepts acquired during the Mcoder.AI Data Science Bootcamp. It focuses on the analysis of a hospital discharge database in Aguascalientes, Mexico, with the aim of developing skills in data integration, cleaning, preprocessing, exploration, and visualization.

A crucial aspect of this project was the construction of a classification model designed to predict the reason for patient discharge. The primary objective was to provide tools to support decision-making in the field of healthcare, enabling a better understanding of the factors that influence patient outcomes.

This project represented an opportunity to apply the knowledge and competencies gained in the field of data science, contributing to a vital area such as healthcare management and the enhancement of hospital processes.

## Results

Exploratory data analysis revealed that patients discharged for the reason of mortality tended to exhibit characteristics distinct from the average among other groups. These patients typically had higher ages, longer hospital stays, a higher number of comorbidities, and a greater number of medical procedures, when compared to the average of other groups.

For the classification model, we experimented with several algorithms, including Random Forest, K-Nearest Neighbors (KNN), Support Vector Machine (SVM), and XGBoost. It was XGBoost that delivered the most promising results, achieving an accuracy of 90.43% and a precision of 90% in predicting patients who would be discharged due to mortality.

Furthermore, the most influential variables in the model were identified as the initial diagnosis, the primary condition, age, length of hospital stay, the number of comorbidities, and the number of medical procedures. These findings align with the insights obtained during the initial data exploration.


## Project Structure

The contents of this project are organized as follows:

Data Integration: In the "Data Integration" folder, you will find code that uses the pandas library to load multiple datasets and merge them into a single CSV file. This process ensures data consistency, as some information was categorized or named differently in certain columns. Additionally, the code filters and selects data only for patients residing in the state of Aguascalientes and for General Hospitals belonging to the Secretary of Health. Irrelevant columns are removed from consideration.

Data Cleaning and Preprocessing: In the "Data Cleaning and Preprocessing" folder, you will find code for further data cleaning and the transformation of numeric keys into corresponding descriptions for categorical variables, facilitating data visualization.

Data Visualization: The "Data Visualization" folder contains code for visualizing the data, primarily utilizing the matplotlib and seaborn libraries.

ML Models: In the "ML Models" folder, you will find code for testing various classification models and optimizing an XGBoost model for predicting patient discharge reasons (deceased or not). This is primarily accomplished using the scikit-learn and XGBoost libraries.


## Variable Descriptions

### Discharges Table 'Egresos':

The variables presented below are just a subset of the variables contained in the complete database, encompassing only those variables that were retained or created from existing data for the purpose of data visualization.

ID: Identifier for each recorded discharge event.   

CLUES: The hospital from which the discharge originates.

INGRE: The date when the patient was admitted to the hospital.   

EGRESO: The date when the patient was discharged from the hospital.   

DIAS_ESTA: The length of the patient's hospital stay, expressed in days.  

EDAD: The patient's age, expressed in years.  

SEXO: The patient's gender (Male or Female).  

PESO: The patient's weight, expressed in kilograms.

TALLA: The patient's height, expressed in centimeters.

DERHAB: The patient's entitlement to healthcare services.

MUNIC: The patient's municipality of residence within the state of Aguascalientes.  

TIPSERV: The type of service for which the patient was admitted, which can be either 'Normal' or 'Short stay.'

PROCED: The patient's source of admission, such as 'Urgencies' if coming from the emergency area, 'Referred' if transferred from another hospital, or 'External Consultation' if referred by a specialist.  

DIAG_INI: The illness for which the patient was admitted to the hospital.  

AFECPRIN: The primary illness for which the patient was hospitalized.  

VEZ: Specifies whether it is the patient's first time being treated for the primary illness or if it is a subsequent treatment.  

CAUSAEXT: Specifies the cause of the patient's injury, when applicable.  

INFEC: Indicates whether the patient contracted an intrahospital infection during their stay.  

MOTEGRE: Indicates the reason for the patient's discharge, which can be for improvement, cure, death, among others.  

NUMPROMED: Indicates the number of medical procedures (surgical, therapeutic, and diagnostic) to which the patient has been subjected.  

NUMAFEC: Indicates the number of comorbidities the patient has.  

CAT_EDAD: Indicates the age category to which the patient belongs.  

CAT_DIASESTA: Indicates the category of days of stay to which the patient belongs.  

DIABETES: Indicates whether the patient has Type II diabetes mellitus.  

HIPERTENSION: Indicates whether the patient has primary essential hypertension.  

OBESIDAD: Indicates whether the patient has obesity.

### Affections Table 'Afecciones':

ID: Identification of the discharge event related to patient comorbidities.  

NUMAFEC: Number of comorbidities for the same patient.  

AFEC: Description of the comorbidity.

### Procedures Table 'Procedimientos':

ID: Identification of the discharge event related to procedures applied to the patient.  

NUMPROMED: Number of medical procedures for the same patient.  

PROMED: Description of the procedure.  

TIPO: Type of medical procedure, which can be diagnostic, surgical, therapeutic, or mixed.  

ANEST: Type of anesthesia used during the procedure.

QUIROF: Indicates whether an operating room was used for the procedure.
## Data Source

Author: Dirección General de Información en Salud.

Data Source: Secretaría de Salud/DGIS 2010-2022. Retrieved from the June 2023 update.

Link to the original database: http://www.dgis.salud.gob.mx/contenidos/basesdedatos/da_egresoshosp_gobmx.html.

Data was used in accordance with the "Términos de Libre Uso de la Información de la SSA/DGIS" (Terms of Free Use of Information from SSA/DGIS).
## Clarifications

This repository includes only the Python code developed during the project. The datasets used have not been included for the sake of convenience. If you wish to access the datasets, please refer to the 'Data Source' section

The project was originally conducted in Spanish, but this file and all code comments have been translated into English for better understanding by a global audience.