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

# Clinical Data Models #

## Resources
- [MIMIC IV Website](https://mimic-iv.mit.edu/)
- [MIMIC III Website](https://mimic.physionet.org/)
- [MIMIC III Schema Official](https://mit-lcp.github.io/mimic-schema-spy/relationships.html)
- [MIMIC III Schema](https://cloud.githubusercontent.com/assets/26095093/23737659/454872b0-0449-11e7-987d-639b0415dca4.png)

- [MIMIC III Repository](https://github.com/MIT-lcp/mimic-code)
- [Finding the Missing Link for Big Biomedical Data](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.452.9557&rep=rep1&type=pdf)

## Week 1 - Introduction 

### Common Data Model
- Definition
    - specifies the single location , specific table and column name, allowed values for each data element
    - tailored to be specific to the clinical problem that data partner networks is trying to study (i.e. Disease specific network)
- Benefits
    1. Reduces reformat of different output
    1. Ability to include more data partners to participate in a data request
    1. Ensures same query logic that is applied to all data partners
    
### Open Source Research Commond Data Model
1. i2b2 (Informatics for integrating Biology & the Bedside) 
1. OMOP - OHDSI Consortium
1. Sentinel - USA FDA
1. PCORnet - Patient Centered Outcomes Research Institute

#### i2b2 (Informatics for integrating Biology & the Bedside) 
- Harvard, non-profit
- derived from existing Research Patient Data Registry ((RPDR)
- focus on finding patient eligible to enrol in clinical trials
- included biomarker, genomics, and clinical data
- with > 300 user institutions 
- Data Model + Application
- `Folder` based terminiologies/queries
- Schema
 ![Images](images/i2b2_schema.png)
 
#### OMOP 
- (OMOP) Observational Medical Outocmes Partnership 
- (OHDSI) Observational Health Data Science and Informatics 
- drug surveillance/adverse event detection
- started by US FDA and moved to OHDSI for broad clinical research or `evidence generation`
    - Columbia University
- strong international oreintiation
     ![Images](images/OMOP_heirarchy.png)
- most focuseds on analytics
- Data Model (CDM version6 )
 ![Images](images/OMOP_CDM_v6.png)
 
#### Sentinel 
- funded by US FDA and managed by Harvard 
- USA only
- no GUI, but uses distributed query system called `PopMedNet` 
    - Data partners can look at a query before executing it on their data
    - Data partners can decline to execute query
    - Data partners can look at the results before sending it to the requestor
    - uses SASS or SQL Scripts
- query process
     ![Images](images/Sentinel_query.png)
- strict local control
    - strong data model governance
- main users
    - FDA CDER (Center Drug Evaluation and Research)
    - FDA CBER (Center for Biologics Evaluation and Research)
- integrates `billing` and `clinical` data
- focus on rapid adverse drug event detection
- `relational data model`
- Schema 
 ![Images](images/Sentinel_CDM.png)


#### PCORNet 
- (PCORNet) Patient Centered Outocme Research Institute
- leveraged much of its design form `Mini-Sentinel` project
- most complex data network composed of
    - Clinical Data Research Networks (CDRNs) 
        - by large healthcare institutions
    - Patient-Powered Research Networks (PPRNs) 
        - by disease-specific registries
    - Health Plans Research Networks (HPRNs) 
        - insurance
- `relational data model`
- Schema 
 ![Images](images/PCORNet_CDM_v4.png)

### Different Sources of Biomedical Data
 ![Images](images/biomedical_data.png)
 
### OpenMRS Schema 
 ![Images](images/openMRS_schema.png)
 
### MIMIC-III Schema 
 ![Images](images/MIMIC-III_schema.png)

 



$$ \theta \sum \frac{1}{2} $$