---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Healthcare Data Quality and Governance 
  language: python
  name: python3
---

# Healthcare Data Quality and Governance #

## Week 1 - Why Data Quality Matters ##

### 4 Aspects of Operational Data Quality
1. **Accurate**
    - correct patient
    - correct care
    - accurate patient history
    - avoid mistakes
        - wrong procedure, drug, person, etc.
    - clearly stated information
    - problem
        - create duplicate work
        - makes care more difficult
        - wrong or harmful care
1. **Completeness**
    - record all important events
    - what has been done
    - what has not been done
    - at any time in patient care
    - accurately bill for care
    - no missing care/billing events
    - problem
        - create safety issue
        - risk over or under-medicating
        - gaps in understanding patient's course of care
1. **Timeliness** 
    - record care in a timely manner
    - problem
        - cannot make informed decisions
1. **Auditability** 
    - ensure nothing is missed
    - see what care has been given
    - have a record of who did what
    - ensure patient privacy
    - avoid malpractice
    - allows approve and disprove events
    
### 4 Kind of Uses for Healthcare Data    
1. Billing information
1. Tracking patient care
1. Tracking prescription
1. Operational business

### Aggregate Analysis
1. Trendspotting
1. Low-risk decisions
    
### Data Quality Requirement
1. Low
    - low risk decisions
        - counting admissions
        - restocking inventory
1. Medium 
    - operational
        - financial planning
        - scheduling and staffing
        - workflow
        - workload balancing
1. High 
    - clinical decision support
    - population identification for care programs
1. Highest
    - performance measurement, appraisal, and compensation
    - legally mandated reports
    - scientific studies
        - statistical validty
        - reproducible
        
## Week 2 - Measuring Data Quality ##

### Metadata
- Description
    - information about the data
        - format
        - storage
        - data type
        - additional fields
        - range of expected values
    - answers the following
        - who collected?
        - where it was collected?
        - when it was entered?
        - what time it was collected?
    - defines contents of data fields
    - describe data schema
    - data dictionaires describe metadata
    - schema
    - compliance with data standards
    - versioning
    - automatically recorded/generated
  
### **Data Provenance** / **Data Lineage**
- ***`core of data quality`***
- description
    - historic record of data and its origins
        - input
        - entries
        - systems
        - processes
    - record of how data move thru the systems
    - record of what happens to the data
        - full lifecycle
            - creation
            - transformation
        - data pipeline
        
### 5 Components of Data Quality ###
1. **Completeness**
    - missing data  provides incomplete picture
    - causes of incomplete data
    - indication of the following:
        - failed to capture events
        - data is inaccessible
        - time lags in flow of data from system to system
1. **Correctness**
    - answers the following:
        - was data collected reliably?
        - does it matchethe expected values/ranges in real world samples?
        - was it an accurate measure?
        - was it recorded accurately?
1. **Concordance**
    - answers the following:
        - does it match common definition for the purpose it was recorded?
        - can data from different systems or times be compared?
        - does data match similar data collected elsewhere?
1. **Plausibility**
    - answers the following:
        - does the data make sense?
        - is the data what one would expect in a typical situations?
        - does the data contradictory or anomalies from real world samples?
1. **Currency**
    - answers the following:
        - is the data relevant to the timeframe we are studying?
        - do you have data elements that are collected at different times?
        - has the data that has been recorded for the time that is meaningful?

### **Data Validation Methods**
- description
    - checking the accuracy of data sources before using, importing, and processing
    - a form of `data cleansing`
    - validation vs verification deals with issues of
        1. Conformance
        1. Completeness
        1. Plausibility
- answers the following
    - does the data conform to standards?
    - are data values present and complete?
    - are present data values plausible?
    
### Validation vs. Verification
| | Validation | Verfication |
| --- | --- | --- |
| description | alignment of data with values and standards reflected in external benchmarks | how data values match our understanding of local practice |
| scope | standard | internal and local |
| focus | how data fits broader sense | relates data of what we already know |

### 4 Commmon Data Validation Methods
1. **Benchmarking**
    - referencing to existing literature or ground truth data
    - answers the following
        - does the data reflect normal ranges
1. **Data Characterization**
    - examining the data lifecycle
    - track how data is entered and managed
    - answers the following
        - what system does data interact with?
        - what processes are the data exposed to?
        - how does data move between systems?
        - how are the systems connected?
1. **Applying statistical method**
    - clinicians or professionals who work with data
    - common steps
        1. validate if data make sense
        1. examine patient record
        1. dive into details
        1. assess expectation vs reality
1. **Reviewing data with SME**
    - measure suspected outliers
    - measure expected ranges
    
### **SBAR Communication Framework**
- acronym 
    1. **Situation**
        - concise statement of problem
        - answers the following
            - whats the problem?
            - what is happening?
            - why is this an issue
            - why we must address it?
    1. **Background**
        - answers the following
            - what are the conditions underlying the activity?
            - what factors contribute to the situation?
            - what constraints exist?
    1. **Analysis**
        - answers the following
            - what have we found?
            - what do findings mean as we move forward?
            - what are optiosn for resolving the situation?
    1. **Recommendation**
        - provide solution
        - lay rationale for decision
- description
    - tools help us respond complex issues that may impact many teams
    - framework for communication information among members

    
## Week 3 - Monitoring, Managing, and Improving Data Quality ##

### Establish the Culture of Quality
1. quality at every lifecycle 
    - **Information Lifecycle**
        1. Data Capture
        1. Data Warehousing
        1. Aggregation and Transformation
        1. Analysis
        1. Reporting
1. monitoring
    - checks and edits
    - clinical workflows support data collection
    
### Data Quality from the baseline
1. create a baseline data profile 
1. identify deficiencies in collected data
    - missing data
        - possible causes
            - workflow problem
            - technology/interface issue
    - inconsistent data
    - duplicate data
    - patient identification issue
    - data changing across systems
    
### Managing Data Quality: Handling Changes
- cause of changes
    - system
    - workflow
    - technology
    - data quality
- change control systems
    1. change review
    1. quality assessment
    1. acceptance testing
    1. documentation
    1. impact assessment

## Week 4 - Sustaining Data Quality through Governance ##
### Data Governance Definition
- description
    - the practice of managing data assets through their lifecycle to ensure they meet organizational quality and data integrity standards
    - geared towards making sure that others can trust their data which is especially important when making patient care decisions
- essentials
    - agreements, policies, and procedures
        1. who collects data
        1. who uses data
        1. how data is used
        1. why data is used
        1. reuse of data
            - train artificial intelligence
            - same research reproducibility
        1. how data is validated
- **`Why data governance matters?`** 
    - recognizes data's value
    - identifies who's responsible for describing the value
    - creates policies and procedures
    - monitors and protects value as data is created and monitored
    - defines who owns data
        - group of people who make up the rules how data should be collected
    - determines legal and ethical consideration
    - directs the terminlogy
    - assigning meaning to measures
    - governance adds clarity
        - use of context
        - unit of measure
        - meanings for different audience
    | Role | Description | Unit of Measure|
    | --- | --- | --- |
    | Administrator | Occupancy Rate | Day |
    | Infection Control | Measure of Risk infection | Hours and Minutes |
    - provide context to what data means
    - improves communication
    - improves consistency
    - creates consensus among stakeholders
    - data for patient care
        - billing transactions represent patient care
        - capturing care elements add value to data
        - allows broader use of data
- **`Data Stewards`**
    1. analyst with expertise working with the system the data is kept
        - supports the flow of data
        
### Data Governance Committees
- List of Stakeholders
    - clinicians
    - analyst
    - insurers
    - public health
    - community leaders
- Data Governance Committees
    - scope of work 
        1. unique perspectives for each group
        1. learn to speak common language
        1. multiple system and perspectives 
        1. setting priorities
        1. ensuring value of data asset
            - making sure data is usable over time
    - committee members
        1. **Data Owners/Caretakers**
            - caretakers and guardians of data as it is entered into the systems
            - the health system
            - ensures data is accurate
        1. **Data Stewards**
            - manage and monitors system
            - ensure accomplishing specific goals
            - maintains consistency and accuracy of data over time
            - ensures system works together to support business needs
        1. **Data Users**
            - downstream userse
                - analyst
                - researchers
    - different groups to compose the committee
        1. **Clinical Operations**
            - patient management
            - managing inventory
            - infection control
            - clinical quality
            - creating schedules
            - managing hospital work
            - reducing medical errors
        1. **Business Operations**
            - future planning for hospital
            - negotiating contract with payors
            - managing and controlling costs
            - identifying charges for billing
        1. **Researchers**
            - hospital as an organization
            - public health research
            - patient outcomes
            - clinical trials
                - drug effectiveness
                - medical devices
                - medical procedures

### Data Governance Systems
- purpose of systems
    - manage data
    - document data
    - describe metadata
    - data dictionaries
    - broader use of data
- systems that manages data
    - data transformation (ETL)
        - operational to warehouse
        - must be documented
    - data mapping
        - mapping between systems
        - source and destination systems
        - contextualization
        - key to reuse of data
        - use data standards
    - data catalog
    - data and metadata for workflows
    - managing data changes

## Resources
### Week 1 - Why Data Quality Matters ##
- Paper
    - [Data quality assessment for comparative effectiveness research
in distributed data networks](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4306391/pdf/nihms-491345.pdf)

### Week 2 - Measuring Data Quality ##

- Paper
    - [Methods and dimensions of electronic health record data quality assessment: enabling reuse for clinical research](https://academic.oup.com/jamia/article/20/1/144/2909176)
- Dataset
    - [California Health Open Data](https://data.chhs.ca.gov/group/healthcare)
    - [New York Health Open Data](https://healthdata.ny.gov/)

## Week 3 - Monitoring, Managing, and Improving Data Quality ##
## Week 4 - Sustaining Data Quality through Governance ##
- Paper
    - [Big Data, Bigger Outcomes](http://library.ahima.org/doc?oid=105683#.X4hKsZMzZhG)