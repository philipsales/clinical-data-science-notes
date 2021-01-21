---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Data Science in Stratefied Healthcare and Precision Medicine
  language: python
  name: python3
---

#  Data Science in Stratefied Healthcare and Precision Medicine #

## Network Modelling
- Network Modeling
    - based on graph theory
        - study of graphs
            - mathematical structure to model pairwise relations between objects
            - representation of nodes connected by edges
            - elements of graph
                1. nodes (verticies, points)
                1. edges (arcs, lines)
            - main types of graph
                1. undirected graph
                1. directed graph
                    - one way relation/direction
                1. weighted graph
                    - each edge have numerical weights
                    - either directed or undirected
            - `adjacency matrix`
                - data structure use to store network graph representations
            - `topology`
                - how nodes are arrange within a network
- Types of Biological Networks 
    1. Protein-Protein Interaction Networks
        - application: Huntington's disease
    1. Metabolic Networks
        - application: Type II Diabetes
    1. Genetic Interaction Networks
    1. Gene or Transcriptional Regulatory Networks
    1. Cell Signalling Networks
        - application: Human Epithelial Cancer 
- Network Analysis Application in Disease Treatment
    1. Cancer Systems Biology
        - analysis of how intracellular networks of normal cells become cancer cells. 
        
## Probabilistic Modelling
1. Prbabilistic Modeling
    - based on `Theory of Probability`
        - considers randomness in predicting future events 
   - valuable in population health
1. Statistical Methods 
    1. Correlation
        - focus on association
    1. Regression
        - use to make predictions
        - may imply causality in `controlled environment`
        
## Natural Language Processing
### Common Task
1. Sentence boundary detection
1. Speech tagging
1. Named entity recognition
1. relationship extraction

### Types of Task
1. Low Level
    1. Sentence boundary detection
        - deciding where sentences begin and end
    1. Tokenization
        - recognition of individual toekns such as 
            - word 
            - punctuation 
            - hyphen
            - forward slashes
    1. Part-of-Speech Tagging
        - a.k.a `part-of-speech assignment` to individual words
        - process of marking up word in a text that is corresponding to a particular part-of-speech
            - for example, its relationship to adjacent and related words in phrase, sentence, or paragraph
    1. Morphological Decomposition
        - study of structure of words 
        - the process of establishing the `morphenes` 
            - smallest meaningful unit of language
            - decomposition into root word, prefix, suffix
    1. Shallow Parsing
        - a.k.a `chunking`
        - identifying the main components of sentences such as
            - noun
            - verbs
            - adverbs
            - links
    1. Problem-Specific Segmentation
        - process of diving text into meaningful units such as
            - words
            - topics
            - sections
1. High Level
    1. Spelling or Grammatical error identification and recovery
        - mostly interactive, require UI
    1. Named Entity Recognition
        - task of finding and classifying names in text
        - indentifying specific words or phrases also known as entities and arrange into predefined categories such as
            - persons
            - locations
            - disease
            - genes
            - medication
    1. Word Sense disambiguation
        - assigning the appropriate meaning or sense to a given word in a text
        - e.g. B-E-A-R as verb versus noun
    1. Negation and Uncertainty Identification
        - inference wheater a named entity is present or absent, positive or negative, and quantifies uncertainty
        - can be `explicit` or `implied`
    1. Relationship Extraction
        - determining the relationships between entities or events
        - e.g. treatment with, caused by, occurs with
    1. Temporal Interferences
        - inferring something has occured in the past or may occur in the future 
        - e.g. symptoms began after medication ... was administered
    1. Information Extraction
        - finding and understanding limited relevant parts of text, where it collects information from many pices of text
        - enables information to be organized
   
        
    
### Computational Methods of NLP 
1. Rule-based
1. Machine Learning
    - Support Vector Machine (SVM)
        - can be taught as large margin classifier
    - Neural Networks and Deep Learning
        - practical application: word embeddings
            - process where words or phrases from the vocabulary are mapped to vectors, turning text into numbers
    - Hidden Markov Model
        - probabilistic sequence model

## Process Modelling
Types of Modelling
1. Business Process Modelling Notation (BPMN)
    - process-oriented approach
    - graphical illustration of business processes in a business model
    - e.g. cancer care pathway
1. PROFORMA
    - tailored for medicine
    - designed for modelling clinical processes and medical guidelines
1. Unified Modeling Language (UML)
    - object-oriented
    - general purpose visual modeling language in the field of software engineering
 
## Graph Data Models
3 Main Types
    1. Resource Description Framework (RDF)
    1. Property Graph
    1. Hypergraphs
    