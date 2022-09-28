## Problem statement:
progression-free survival - In this task I've used ML model for classification. 
Initially problem started with extracting dates for progression, extracting progression information from unstructured data. 
Specifically, we'd like to identify which patients had a doctor specifically mention disease progression, 
what date the progression occurred on, and what drug regimen the patient was on.

## References - 
1. the research paper which we discussed (they used cnn) (https://ascopubs.org/doi/full/10.1200/CCI.20.00020)
2. the github repo  which we discussed  (https://github.com/Sanger2000/Predicting-Lung-Cancer-Disease-Progression-from-CT-reports))

## Data descreption:
Data set we considered only two labels - 
1. progression
2. other

Notes: As per SQL developer's inputs currently we are just considering progression inclusive keywords and whenever there is progression exclusive keywords available in the note they are specifically just deleting those notes. 
so at the end they just have created a data with inclusive keywords only.

Our Data:
| Variables      | 
| ----------- | 
| MRN	|
| Visit ID	|
| Key_word	|
| note_type	|
| Key_word	|
| note_content	|
| HOSPITAL_ID	|
| note_date	|
| Drug Regimen	|
| Date of Progression	|
| Diagnosis Desc	|
| Diagnosis Date  |


## Approaches
### Approach 1: MIT research document
- attached on pdf file named `MIT Research.pdf`
- I've incorporated all the points have been performed in MIT research in order to understand desease progression

### Approach 2: Rules based
- we have used `Rules-Based Progression Identification 20210920.xlsx` keywords and rule based approach to understand the progression in sql

### Approach 3: Conducted the survey in order to come up with an better approach 
- attached the pdf file of survey named `Disease Progression NLP based initial survey.pdf`

### final Approach:
- Sentence level Bert classification 
- file name - `bert-for-sequence-classification.ipynb`
- Simple classification model we used to classify `progression` and `no progression`.
- Datasets used for model training `other.csv` and `nlp_progression_without_date.csv`
- we have perfomed data clearning on notes and thats notes we considered for training column name `clean_report_text`
- achieved model accuracy `93%`
- detailed discussion is performed in jupyter notebook

