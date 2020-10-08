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
- Papers
    - [Common Data Models (CDMs) to Enhance International Big Data Analytics: A Diabetes Use Case to Compare Three CDMs](https://d3c33hcgiwev3.cloudfront.net/cT5eWgAFEemAgQrXx6bp4g_7166f4c0000511e99b75572b09ecdbb4_Harshana-et-al.---2018---Common-Data-Models-_CDMs_-to-Enhance-International.pdf?Expires=1602288000&Signature=ZQUF0rcpDbDcLYDRzGC8KmvwzBUfce0wZCbFCl04MU9vfnUeLWh8BcJQHW4B1NeGpFjCaY1wJ772X~AtChmAKkSjW96KYXkvqLGN-7uiDrEEQgK5PXSa8ymdXPQtlePoELGWuRxE47qMieanZS8uwG~NMXO8ZSa9r8KPB2p-j7M_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 

    - [Serving the enterprise and beyond with informatics
    for integrating biology and the bedside (i2b2)](https://d3c33hcgiwev3.cloudfront.net/cUBaKwAFEemAgQrXx6bp4g_7165bc40000511e9ac516f5d6962b7b8_Murphy-et-al.---2010---Serving-the-enterprise-and-beyond-with-informatics.pdf?Expires=1602288000&Signature=UU1qip7NLwqXK-oWN1dqxKGo-GJCxqxeVxlwboeEhbsmClL51tIIYWMwaO7IZzhjBsw9v2mSIVfZF2a~YDDQ1uZtfX1AqyiR6nxiGWTHWaw2EifJPmIerySleBe08GA~iEZ~aS3aMNHE2OfaekoE0fyyn851nmMFU9fDcFm6xTA_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
    
    - [Data Model Considerations for Clinical
Effectiveness Researchers](https://d3c33hcgiwev3.cloudfront.net/cRTRhwrHEemYdRIT0BhLtg_714afbe00ac711e980d6e7465a739109_Kahn---2012---Medical-Care.pdf?Expires=1602288000&Signature=T2FHJaprnAgz7Lv5XQF1HZ4OSbzQS4IfIZsyasnPPBSmMg4LqBZR36Fq9SuSpnPfUqdBAjuzSeG9485IDTu0CEdaMge5~As0ZwKVrxtmdTgeOztKnMSAcDTGL68SnnwHFdbapDg0D6VEPnYdcGwlUQJaeRcSRMeIKcOgXIK4a6M_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
    
    - [Identifying Appropriate Reference Data Models for
Comparative Effectiveness Research (CER) Studies Based
on Data from Clinical Information Systems](https://d3c33hcgiwev3.cloudfront.net/VOZjwArJEemP8Qpm209XvA_551897500ac911e9be2dd9993e1c644d_Identifying-Appropriate-Reference-Data-Models-for-.9.pdf?Expires=1602288000&Signature=h5Mzh-MJKtCVYIFQbUvLe2TK4Ycve9XcNHYMJHK3ObKavANbMNMWNF0utlckWlRHoYAj42ZJdqL80SOfgG409VTm7XXiFlECbxxkRi3K1zUF4cm4ob3G6Jvb7TlTJ20ZvzlX34HM4aF90OtyK1i-F0VN8tC1qi1~zZ4UhYfHVp4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

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
- funded by US FDA and managed by Harvard ,USA only
- features
    - no GUI, but uses distributed query system called `PopMedNet` 
    - uses SASS or SQL Scripts
    - `relational data model`
- workflow
    - data partners can look at a query before executing it on their data
    - data partners can decline to execute query
    - data partners can look at the results before sending it to the requestor
- query process
     ![Images](images/Sentinel_query.png)
- strict local control
    - strong data model governance
- main users
    - FDA CDER (Center Drug Evaluation and Research)
    - FDA CBER (Center for Biologics Evaluation and Research)
- integrates `billing` and `clinical` data
- focus on rapid adverse drug event detection
- Schema 
 ![Images](images/Sentinel_CDM.png)


#### PCORNet 
- (PCORNet) Patient Centered Outocme Research Institute
- features
    - leveraged much of its design form `Mini-Sentinel` project
    - uses SASS or SQL Scripts
    - `relational data model`
    - uses distributed query system 
        - data stays in local institution
        - query executed locally
        - SQL sent to institution
        - summary results sent to central location
- workflow
    - similar to sentinel
        - uses the same distributed query platform
        - additional model to existing sentinel data model
        - same data governance principle of sharing summary results only
- most complex data network composed of
    - Clinical Data Research Networks (CDRNs) 
        - by large healthcare institutions
    - Patient-Powered Research Networks (PPRNs) 
        - by disease-specific registries
    - Health Plans Research Networks (HPRNs) 
        - insurance
- user community is much broader and diverse than is Sentinel, which effectively exists only to serve the FDA
- Schema 
 ![Images](images/PCORNet_CDM_v4.png)

### Different Sources of Biomedical Data
 ![Images](images/biomedical_data.png)
 
### OpenMRS Schema 
 ![Images](images/openMRS_schema.png)
 
### [Clinical Data Warehouse for Research](https://d3c33hcgiwev3.cloudfront.net/VOZjwArJEemP8Qpm209XvA_551897500ac911e9be2dd9993e1c644d_Identifying-Appropriate-Reference-Data-Models-for-.9.pdf?Expires=1601683200&Signature=RoC6YBZ1QnB2CfSC3prcxVTS9V0hYjtvrIb32iYp5m3Tsq8bs7qQmX8VGDocuJvxkDF6ygHpnM48zuLfFYcSH7ujjWTuMvcmNNRS-ROlC8CuZKyNfT4PThvDwCCGL0bM5~GCqAiZ~3XpClF9gY5X4P0GD4ceuw1NWVWeejd-2gQ_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
 ![Images](images/CDW_schema.png)

### MIMIC-III Schema 
 ![Images](images/MIMIC-III_schema.png)

 



$$ \theta \sum \frac{1}{2} $$