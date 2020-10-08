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

- [ETL Framework - A Framework for Classification of Electronic
Health Data Extraction-Transformation-Loading
Challenges in Data Network Participation](https://d3c33hcgiwev3.cloudfront.net/v3QLEQrMEem5_xLqNrIdUA_bfa9c0500acc11e9a21b976d3b0c3f75_Ong---2017---A-Framework-for-Classification-of-Electronic-Health-Data-ETL-Challenges-in-Data-Network-Participation.pdf?Expires=1602115200&Signature=ic~BktJhNyAgrwUQkWc-r-SfoJ6ME6439AtZ5dnNZc5HQtO-2yq3uHK4DbB~VIUOgESCFz695g90VX0N4H8xajuegM6spV8JdRclv2ZnqbyFfCNR7lpcUvQDvARQYRdUna2kbGTj3qWTLZaodDL6t3bV3y-sCEuBzJk-9O0KDY8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

- [Data Profiling Tool - White Rabbit](https://d3c33hcgiwev3.cloudfront.net/v3QLEQrMEem5_xLqNrIdUA_bfa9c0500acc11e9a21b976d3b0c3f75_Ong---2017---A-Framework-for-Classification-of-Electronic-Health-Data-ETL-Challenges-in-Data-Network-Participation.pdf?Expires=1602115200&Signature=ic~BktJhNyAgrwUQkWc-r-SfoJ6ME6439AtZ5dnNZc5HQtO-2yq3uHK4DbB~VIUOgESCFz695g90VX0N4H8xajuegM6spV8JdRclv2ZnqbyFfCNR7lpcUvQDvARQYRdUna2kbGTj3qWTLZaodDL6t3bV3y-sCEuBzJk-9O0KDY8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

- [White Rabbit Instructions](https://d3c33hcgiwev3.cloudfront.net/eaZcmQrNEemP8Qpm209XvA_846c3c100acd11e982a70b671e3968a0_White-Rabbit-Wiki-Instructions.pdf?Expires=1602115200&Signature=GYREPe25cAayacqLItmn8Mv4dRRyZAe4C7ZrIJRoenDYykX~TvkOkuUL44g~aLjV-43dD6z-r7gDsDs2qRM5mL5y89fKxPjniwl-F3Ebblm1e8kOl097N7toFa1MfNd4xo-5KAtSXbHtZD0WBPai4pORfXfj6VYpWH6fnJxVICE_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
- [White Rabbit Sample Output](https://d3c33hcgiwev3.cloudfront.net/xEnpQwAHEem5Kg7DUflKxA_c4753ee0000711e9a289791da6d76b4f_ScanReport_MIMIC_Full_MIMIC.xlsx?Expires=1602115200&Signature=R2wUjN7Ke5OiQtuXpezmm099K6wBI1pKrazGnDRFCGcZe0BEVpiHB9IOqBLkB9XSdgcUXigt3Y6LaN9P8HS-tAAtPOVh55shM4mIxRd3K5O1faWpnl5mI6ajoJmen7K5aKHED0hZ~BWRuqm7EUCAP3PXZweQsXCV5qVLqdBY8-Y_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

## Week 3 -  Extract-Transform-Load and Terminology Mapping 

### Structural versus Terminology Mapping
1. Structural Mapping a.k.a `Syntactic Mapping`
    - ERD redesigning to accommodate other fields
    - Dats Model Transformation
        - relational to star-schema
        - relational to object oriented model
        - document based to relational models
    - mainly involves
        - sql joins
        - data ypes
1. Structural Mapping a.k.a `Semantic Mapping`
    - mainly involves
        - formats
            - date to string
            - number to string
            - etc..
        - missing values
            - null 
            - yes/no flags
        - valuesets
            - ICD10 to SNOMED Codes
            - Male to "M"
            - pre-coordination vs post-coordination
                - "Hypertension with renal disease" vs "hypertension; Renal Disease"
             
             
### Components of ETL
1. Data Profiling
    - understanding the raw and native data statistics
1. Data Mapping
    - moving data from source to destination model/table
1. Terminology mapping
    - conversion of terms for conformity to CDM

### Data Profiling with `White Rabbit`
- understand the source data
    - what are the values present
    - how often are used
- `note`: medical data are usually `long-tailed`
    - few terms are use frequently and more terms are less used
    
### Data Mapping with `Rabbit in a Hat` ETL Tool
- information loss
    - when there is no target term/column to map the source column
