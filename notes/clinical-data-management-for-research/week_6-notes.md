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
## Resources
- Paper
    - [Preparing raw clinical data for publication: guidance for journal editors, authors, and peer reviewers](https://www.bmj.com/content/340/bmj.c181)
    
## Week 6 -  Benefits, Scope, and Validated Instruments

### Survey Data Collection
- define, test, and validate instruments before launch
- **Survey Desing Process**
    1. define scope
        - define specific aims
        - define population of interest
        - define sample size
        - determine marketing strategy, e.g. incentives
        - anonymizing data collection
    1. consider existing instruments
        - review literature similar concepts
        - reuse existing instrument
        - ensure instrument validation is consistent with the study, population, modality, environment
    1. questionnaire planning and development
        - question should be concise and targeted to single concept
        - one question one concept 
        - relate questions directly to answering specific aims of study
        - avoid `nice to know` questions
            - prone to respondent fatigue
        - plan each wording
            - avoid acronyms
            - avoid jargon
            - use neutral and non biased  words
            - use short specific words
            - use familiar terms/concepts
        - plan question of recall
            - short series of related questions
            - focus on recent past
            - define reference time frame
                - e.g. during the last 8 days ...
        - grouping similar questions 
            - group demographics and sensitive questions
        - consider open/closed questions as appropriately
        - strucutre answers properly
        - include `Others (please satisfy)`
        - make questions and answers match
        - include units of measurement
            - e.g. how tall in centimeters
        - consider comon question types
            - e.g. checkboxes, radiobutton
        - consider visual analog scales
            - enables less respondent perception + memory bias in answer
            - e.g. pain scale, slider type bar
        - consider `Likert Scales`
            - should be `equi-distant`
            - e.g. Never, Very Rarley, Rarely, etc...
        - consider branching logic
            - decrease survey fatigue
            - increase data validity
    1. assembling teh data collection instrument
        - introduce survey with sufficient information, intent, and expectation
            - purpose of study 
            - time it will take
            - how data will be used
            - if identified/de-identified method
            - any incentive opportunities
            - any additional instructions needed
        - finish in respectful manner
            - thank the participant
            - review information about results dissemination
        - break up long survey into sections
            - section per page/web page
            - use branching logic
            - use progress indicator
         - consider formatting
             - large fontsize
             - high contrast
             - lots of white spaces
             - alignment consistency
             - space for answer in open-ended questions
    1. testing/refinement - pilot results
        - allow time for **usability testing**
            - evaluate the following
                - time required
                - readability and clarity
                - spelling and grammer
                - layout
                - general appearance
                - mutual exclusivity of respnose choices
                - lack of bias in questions
        - allow time for **functional testing**
            - evalute the following:
                - question flow
                - branching logic
                - user workflow - are testers following instructions?
                - data coding
        - allow time for **data testing**
            - evalute the following:
                - does every question relate to specific aims?
                - does question response make sense?
                - how many answers left blank?
                - how many questions answered `do not know`?
                - are testers completing the survey?
                - are answers consistent with branching logic?
                - is there variance in qudstions responses?
    1. survey administration
        - consider modes
            - paper, emr, sms
        - consider environment
            - waiting area, home/mail
        - consider invited participants
            - mail or hand delivery of instrument
        - consider open participation
            - stack of paper survey instrument with instruction
    1. data analysis
        - build electornic database platform to house collected data
        - build database platform at the beginning study
        - use practice data to test database
        - test full cycle data flow
            - pilot data collection -> database storage -> SPSS package -> Mock analysis