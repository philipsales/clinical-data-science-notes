---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: ODM Standardized Vocabuary 
  language: python
  name: python3
---

# OMOP CDM and Vocabulary #

## Resources
- ETL convetion
    - [CDM ETL Specification PEDSNet](https://pedsnet.org/documents/206/ETL_Conventions_for_use_with_PEDSnet_CDM_v3.1_OMOP_V5.2.pdf)
- Links
    - [Cohort/Phenotype Knowledge Library](https://phekb.org/phenotypes/)
- Paper
    - [Electronic phenotyping with APHRODITE and the Observational Health Sciences and Informatics (OHDSI) data network](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5543379/)
- OHDSI Discussion
    - [Patient Story](https://www.endometriosis-uk.org/laurens-story)
    - [OHDSI Book](https://ohdsi.github.io/TheBookOfOhdsi/StandardizedVocabularies.html)
    - [OHDSI CMD slides](https://www.ohdsi.org/wp-content/uploads/2018/10/20181010-OHDSI-Vocabulary-CDM-Tutorial.pdf)
    - [OHDSI CDM wiki](https://ohdsi.github.io/CommonDataModel/index.html)
    - [OHDSI CDM paper](https://www.sciencedirect.com/science/article/pii/S153204641200069X?via%3Dihub)
    - [OHDSI github](https://github.com/OHDSI/CommonDataModel)

## Tools
- [Query Library](https://data.ohdsi.org/QueryLibrary/)
- [Query Library wiki](https://github.com/EHDEN/QueryLibrary)



## OMOP Vocabulary ##

### Disease Hierarchy ##
> **Important when building cohort of people**
- A concept has **descendants (more specific)** and **ancestors (more general)**
- ICD does not represent the true nature of disease
    - disease cannot be represented by a flat file
- ICD is useful for
    - statistics
    - billing purposes
    - administrative purposes
- SNOMED does the perfect representation of disease heirarchy
    ![Images](images/disease_hierarchy.png)
    - a ICD10 diagnosis of `Atrial fibrillation` also means diagnosis of 
        - Atrial Arrythmia
        - Supraventricular Arrythmia
        - Cardiac Arrythmia
        - ...
        - Disease of the cardiovascular system
        
### Relationships ###
- concept_relationship
    - `is a` - pointing up
    - `subsumes` - pointing down
- **getting heirarchy for a concept of a condition**
    ```sql
    SELECT max_levels_of_separation, concept_id, concept_name
    FROM concept_ancestor
    JOIN concept
        ON ancestor_concept_id = concept_id
            WHERE descendant_concept_id = 313217 --Atrial fibrillation
            -- WHERE descendant_concept_id = 44784217 -- Cardiac Arrythmia
                ORDER BY max_levels_of_separation
                
    ```
- **getting concept_relationship and concept_name**
    ```sql
    SELECT cr.*, c.concept_name, c.standard_concept, c.vocabulary_id
        FROM `learnclinicaldatascience.mimic3_demo_omop.concept_relationship` cr
        JOIN `learnclinicaldatascience.mimic3_demo_omop.concept` c
            ON cr.concept_id_2 = c.concept_id
        WHERE cr.concept_id_1 = 44825429
    ```
- **getting associated drugs with specific ingredients using descendants**
    ```sql
    SELECT 
    COUNT(DISTINCT(de.person_id))
    FROM `learnclinicaldatascience.mimic3_demo_omop.drug_exposure` de
    WHERE de.drug_concept_id IN (
        SELECT ca.descendant_concept_id
        FROM `learnclinicaldatascience.mimic3_demo_omop.concept_ancestor` ca
        WHERE ca.ancestor_concept_id = 1310149 --warfarin
    )
    ```
- **getting associated drugs with medication class using descendants**
    ```sql
    SELECT 
    COUNT(DISTINCT(de.person_id))
    FROM `learnclinicaldatascience.mimic3_demo_omop.drug_exposure` de
    WHERE de.drug_concept_id IN (
        SELECT ca.descendant_concept_id
        FROM `learnclinicaldatascience.mimic3_demo_omop.concept_ancestor` ca
        WHERE ca.ancestor_concept_id = 4283987 --ANTICOAGULANTS (VA CLASS)
    ```

### Drug Hierarchy ###
![Images](images/drug_hierarchy.png)

### Vocabulary ERD ###
![Images](images/vocabulary_erd.png)

### Concept Relationship Table ####
![Images](images/concept_relationships.png)

## OMOP CDM Overview ###
1. patient centric
    - individual is storing information
    - not summary level data
1. vocabulary and data model are blended
1. domain-oriented
1. accommodates data from various sources
    - data registries
    - emr
    - surveys
1. preserves data provenance
    - provenance: avoiding to lose raw data
1. extendable and evolving
1. database platform independent 

## OMOP CDM Role ##
The CDM is designed to support the conduct of research 
1. identify and evaluate **associations between interventions** from:
    - drug exposure
    - procedures
    - healthcare policy changes 
1. identify **outcomes caused by these interventions** (condition, procedure, drug exposure)
    - outcomes can be 
        - efficacious (benefit) 
        - adverse (safety risk)
1. identify **specific patient cohorts** ay be defined for treatments or outcomes
    - e.g., those taking a certain drug or suffering from a certain disease
    - using clinical events (diagnoses, observations, procedures, etc.) that occur in predefined temporal relationships to each other
1. support the generation of **reliable scientific evidence** about:
    - disease natural history
    - healthcare delivery
    - effects of medical interventions
    - the identification of demographic information
    - health care interventions 
    - health outcomes.

## OMOP CDM Domains ##
![Images](images/cdm_domains.png)

## OMOP CDM Standard Concepts ##
![Images](images/cdm_standard_concepts.png)


## OMOP Table ##
- that requires pre-population 
1. PERSON
1. OBSERVATION_PERIOD
1. CONCEPT
1. VOCABULARY
1. DOMAIN
1. CONCEPT_CLASS
1. CONCEPT_RELATIONSHIP
1. RELATIONSHIP
1. CONCEPT_SYNONYM
1. CONCEPT_ANCESTOR
1. DRUG_STRENGTH

## OMOP CDM Principles ###
![Images](images/cdm_principles.png)

## OMOP ETL flow ###
![Images](images/etl_flow.png)

## OMOP CDM ##
![Images](images/omop_cdm.png)

### Condition ###
![Images](images/cdm_condition.png)

### Drug Exposure ###
![Images](images/cdm_condition.png)

### Drug Era ###
![Images](images/cdm_condition.png)

### Measurement ###
![Images](images/cdm_measurement.png)

### Observation ###
> **observation periods define the spans of time a person is eligible to have recorded clinical observations, but does not require that one or more observations are actually observed**

> **OBSERVATION_PERIOD table contains records which uniquely define the spans of time for which a Person is at-risk to have clinical events recorded within the source systems, even if no events in fact are recorded (healthy patient with no healthcare interactions).**

![Images](images/cdm_observation.png)

### Person ###
![Images](images/cdm_person.png)

### Occurence ###
![Images](images/cdm_occurence.png)

### Procedure Occurence ###
![Images](images/cdm_procedure_occurence.png)

### Visit ###
![Images](images/cdm_visit.png)
