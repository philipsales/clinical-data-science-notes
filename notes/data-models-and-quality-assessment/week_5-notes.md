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
- [Final Assignment](https://docs.google.com/presentation/d/1Gelkq4mvVL6C72AQ2IlZK1mf-XmqbD0P1bEb8zU1PtI/edit#slide=id.p)

- [Nero Data Science Platform](https://med.stanford.edu/starr-omop/nero.html)
- Paper
    - [Starr-OMOP](https://arxiv.org/pdf/2003.10534.pdf)

## Week 4 - Practical Application 

## I. High Level ETL Process 
### 1. Extract
- data exporting
- data validation

### 2. Transform
- data cleansing
- data manipulation

### 3. Load
- data loading
- data quality checking

## II. ETL Process 
### Step 1. Understand source and target models
- ERDs, data dictionaries 
- DML, DDL
- table and column definitions

### Step 2. Profile source data tables
- access intrinsic data quality 

### Step 3. Create ETL Mapping
- structural and semantic mappings

### Step 4. Write transformation code
- work down list list of source and target tables

### Step 5. Executing the transformations to create target table(s)
- SQL-centric or programming langauge-centric

### Step 6. Data Quality Assessment
- pre-transformatino vs post-transformation

### Step 7. Documentation
- What was done
- decision/assumptions made
- edge cases/unusual situations
- `Other` documentation
    - Data quality findings
    - assumptions/short cuts/known issues
    - Conventions used to
        - Process bad data
            - missing data
            - out-of-range
            - wrong format
        - Termininology mapping decisions
            - inexact match
