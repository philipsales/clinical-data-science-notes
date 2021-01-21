---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Data Management for Clinical Research 
  language: python
  name: python3
---

# Data Managemet for Clinical Research #

## Week 1 - Research Data Collection Strategy


## Resources
- [HIPAA 18 identifiers](https://cphs.berkeley.edu/hipaa/hipaa18.html)

### Clinical Research
- ***3 Categories***
    1. Patient-oriented research
    1. Epidemiological and behavior studies
    1. Outcomes research and health service research
- ***2 Types of Clinical Research Studies***
    1. Observational Studies -> `observe`
        - meaures exposures and outcomes
            - can be prospective or retrospective
        - no interventions
    1. Clinical Trials -> `intervene`
        - interventional study
            - how well new medical approaches work in people
            
### Data Management Lifecycle
- General Scope 
    1. Collection
    1. Representation
    1. Formatting
    1. Documentation
    1. Monitoring
    1. Access and Sharing
    1. Updates
    1. Security
    1. Quality Control
    1. Transformations
    1. Destruction
    
### HIPAA 18 Identfiers
1. Names;
2. All geographical subdivisions smaller than a State, including street address, city, county, precinct, zip code, and their equivalent geocodes, except for the initial three digits of a zip code, if according to the current publicly available data from the Bureau of the Census: (1) The geographic unit formed by combining all zip codes with the same three initial digits contains more than 20,000 people; and (2) The initial three digits of a zip code for all such geographic units containing 20,000 or fewer people is changed to 000.
3. All elements of dates (except year) for dates directly related to an individual, including birth date, admission date, discharge date, date of death; and all ages over 89 and all elements of dates (including year) indicative of such age, except that such ages and elements may be aggregated into a single category of age 90 or older;
4. Phone numbers;
5. Fax numbers;
6. Electronic mail addresses;
7. Social Security numbers;
8. Medical record numbers;
9. Health plan beneficiary numbers;
10. Account numbers;
11. Certificate/license numbers;
12. Vehicle identifiers and serial numbers, including license plate numbers;
13. Device identifiers and serial numbers;
14. Web Universal Resource Locators (URLs);
15. Internet Protocol (IP) address numbers;
16. Biometric identifiers, including finger and voice prints;
17. Full face photographic images and any comparable images; and
18. Any other unique identifying number, characteristic, or code (note this does not mean the unique code assigned by the investigator to code the data)

### Research Data Planning
1. Invest time in having Good Data Planning Upfront
    - garbage in - garbage out
1. Define all data you will collect before seing first research subject
    - ethics and study reliability
    - avoid inconvenience to participants
1. Alway follow Good Practice
    - develop primary hypothesis
    - define primary and secondary outcome measurements necessary to test hypothesis 
    - let your hypotheses shape your data collection strategy
    - by collecting about everything you will get nothing
    - come up with something small and build up and around it
    - don't go fishing when doing clinical study
    - think about 1-2 hypothesis that going to test definitely rather than full-fledge `collect everything and decide later`
    - be exact and discrete when defining variables
        - Blood pressure vs Systolic and Diastolic BP
        - Blood Surgar vs Metabolic Panel/Profile
    - review each measurement for best ***data type***
        - nominal vs categorical vs continuous
    - ***code categorical variables*** during data collection 
        - to limit choices 
        - don't code continuous variables
        - to lessen data cleaning
    - always include a set of ***confounding factors***
        - e.g. race, gender -> age, height, weight
        - e.g. height, weight -> BMI
    - store ***raw data fields*** rather than calculated values
        - e.g. age vs birthdate
    - allow possibility of ***missing data*** in fields
        - ***`develop codes for missing values`***
            - not applicable (000)
            - not collected (001)
            - doesn't remember (002)
            - will not disclose (003)
        - do not use physically possible values as the code
            - e.g. if age unknown, enter '99' - 99 can be a valid age
    - for quantitative study, minimize ***open-ended free-form text*** data entry 
    - develop standard operating procedure manuals
        - e.g. data collection forms should be reviewed prior to deployment
        - have practice data as test cases
        - perform full cycle test
    - form design should be iterative and targeted to make collecting easy
    - create security safeguards
        - do not email sensitive data with identifiers 
            - HIPAA identifiers have 18 points  
    - think of the data-sharing exchange policy
        - data dictionary (i.e. terminology and vocabulary) and SOP
    - enforce ***data integrity and validation***
        - form validation and field type check
        - check `double-data entry` or duplicate data
            - two members of the study team enter the same data for the same patient record. Their work is then compared for concordance.
        - keep audit trails of data changes
            - logs to record who and what
            
### Data Collection Modality
- Consideration
    1. Structure of Data
        1. Case Report Form
            - e.g. classic forms 
        1. Complex Machine-Captured Data
            - e.g. EEG, ECG, Radiology Images
        1. Unstructured data
            - e..g transcription, free-text
    1. Physical Location
        1. In Person data collection
            - who will do data entry
                - patient or study personel
            - e.g. routine visit vs dedicated visit
        1. Remote Data Collection
            - paper form
                - e.g. survey, buubles/scantron, OCR
            - electronic data capture (EDC)
                - e.g. browser, specialized software
            - phone
                - e.g. sms, interactive voice promopt/response
    1. Existing or New Data
        1. Re-using existing Data
            1. EMR
                - lab values, clinical notes
            1. previous studies
            1. registries and publicly available data
