# NSCLC_patient_identification

Searches were performed based on two distinct approaches:- 
- the use of ICD codes to identify patients
- the use of keywords in notes to identify patients
- Drugs can be used to identify NSCLC patients, whether on their own or in combination with ICD codes

medicines - codes
medical conditions - codes

Improve current patient identification approach:
Step 1: 
1. write text processing in sql (remove all punctuations)
2. confirm html tags 
2. based on identified keyowrds, search keywords in clean notes using sql queries

References: 
1. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6894100/
We focused on only primary lung cancer, and therefore metastasis is not considered in the system.

NLP methods:
1. symbolic rule-based approach using SNOMED CT to automatically extract lung cancer stages from free-text pathology reports based on the tumor, node, metastasis (TNM) stage. [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2995652/)
2.  Warner et al. automatically extracted overall stage of lung cancer from narrative texts in EHR [11](https://pubmed.ncbi.nlm.nih.gov/26306621/) using exact stage (e.g., stage I and stage IV) and inexact stage (e.g., “early stage”)
3. used pathology reports to detect metastatic status (including histological type, tumor grade, specimen site, metastatic status indicators and the procedure) and metastasis site [13](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5543353/)
4. We used the histological types in the 2015 World Health Organization Classification of Lung Tumors [17] as our keywords to extract histological types.(https://pubmed.ncbi.nlm.nih.gov/26291008/)


# ToDo: 
## Improve current patient identification approach 
### Step 1: SQL
- write text processing in sql (remove all punctuations)
- confirm html tags
- based on identified keyowrds, search keywords in clean notes using sql queries
### Step2: Review notes and patterns
### Step3: NLP
- mets keyowrds related to lung cancer
- Biomarkers - check if this info is available or not
- specific medications or surgery or regional radiation therapy

