---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Clinical Data Models
  language: python
  name: python3
---

# MIMIC-III Data Models #

## Resources
- [ Data Quality Assessment Terminology and Framework](https://d3c33hcgiwev3.cloudfront.net/fkVrCgrOEemP8Qpm209XvA_7e56a8a00ace11e99ff16dafffcf4ae2_Kahn---2016---A-Harmonized-Data-Quality-Assessment-Terminology-and-Framework-for-the-Secondary-Use-of-Electronic-Health-Record-Data.pdf?Expires=1602115200&Signature=eL0CUF-~L3ODe3SAEfSrQjWzRKjNtWqrhjIyWt3eZqcew1J0k1pmOyS64Ub2TK1zNvO8bcjFsF8cBQVsQhAxNXvTTcM1wfzetRw2mxun4DG2HFJ7n9NNF5v~hXSDhFcbkoyhAbRbWKXSsUr3udJnRANXqter2xLuoTplyf6Vs7E_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
- [A Comparison Of Data Quality Assessment
Checks In Six Data Sharing Networks](https://d3c33hcgiwev3.cloudfront.net/MOi60ArOEem5_xLqNrIdUA_30fb0a100ace11e9be2dd9993e1c644d_Callahan---2017---A-comparison-of-Data-Quality-Assessment-Checks-in-Six-Data-Sharing-Networks.pdf?Expires=1602115200&Signature=eJpiEb9fBzTpSTY~42xzeUmF0~dEB--Wq3iSHZMKVPVzUqII3wmgefK5P6JdjLzNfGIenImYASeJ4GHhxazjh46xcmPxlCMp6zQEywVUNqSbPLwL730NgyF-keK76BF8dudp6oG-cVqT6cUWTSz6hBLrPQq6OrNWZDaojSxMQqQ_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

## Week 4 - Data Quality Assessments

## I. Components of Data Quality
### 1. Data Quality Dimensions
- measures the data quality features
- case to case basis
- example
    - completeness, conformance, etc..

### 2. Data Quality Measures 
- usually summary measures
- are grouped into data quality dimension
- may appear in multiple data quality dimensions
- example
    - mean, median, min, max, etc..

### 3. Data Quality Rules 
- measures the thresholds of acceptability
- use case or business objective independent
- requires expert knowledge or literature benchmark
- can provide insights to potential data quality issues
- rules trigger based on data quality measures
- pre-specified limits
    - warnings
    - red flags
    - hard stop rules
- Global Rules
    - high level overview
- Use-case Specific Rules
    - use-case specific 
- Sample DQ Rules
    1. FDA Sentinel Project
        - numeric warning for laboratory test names
    1. OMOP Achilles DQ Tool
        - number of duplicate condition occurence concepts per person
    1. Pediatric Health Information System (PHIS)
        - CPT codes encoded are invalid for >= 2% of cases or >= 25 cases
- Types of Sample Rules
    1. plausibility atemporal
    1. conformance value
    1. completeness
    1. conformance relational
    1. plausibility temporal
    
  
## II. Other Qualifier of Data Quality
### Instrinsic Data Quality
- Overall quality of data without any reference to specific use of the data
- General sense of data quality that could reveal sufficient issues to deem a dataset unusable or usable
- High level overview of key strenghts/weakenesses of the data
- DQ measures and rules that are independent of any specific use
- example
    - missing laboratory data must not exceed 20%
    
### Fitness for Use
- DQ measures and rules designed for a specific use case
- example


## III. Sources of Data Quality Issues
- arises in all stages of data lifecycle
    1. Entry
    1. Storage
    1. Management
    1. Extraction
    1. Analytic Computation
    1. Reporting and Display
- different common types of data quality problems
    1. missing data
    1. entity outliers
    1. no matching concept
    1. past event
    1. inconsistent null distributions
    1. post-death fact
    1. temporal (overall amount of data) outlier
    1. unexpected flactuation in records
    1. pre-birth fact
    1. future event
    1. numerical outliers
    1. missing expected concepts
    
## IV. Tools for Data Quality Assessment 
### 1. `White Rabbit` 
- assess the following
    1. Data model conformance (data types)
    1. Completeness/Missingness
    1. Atemporal density
    
### 2. Raw `SQL` 
- assess the following
    1. Distribution
        - Continuous (numeric)
            - mean, median, mode
        - Categorical
            - histogram
    1. Temporal Density
    
### 3. ODHSI `ACHILLES` tools 
- Toolkit
    1. ACHILLES (data quality measures)
        - large library of precomputed data quality measures in `r` script
    1. ACHILLES Heel (data rules) 
        - DQ rules for alerts an warnings across all tables and models also in `r` script
    1. ACHILLES WEB (data visualization)
        - incorporated into ATLAS

## V. Data Quality Rules
    
## Terminology
1. Atemporal 
    - do values, distributions, or densities agree with expected values 
    - example, is the prevalence of diabetes implied by the data in line with the known prevalence?
1. Temporal 
    - are changes in value in line with the expectation?
    - example, are immunization sequences in line with recommendations? 