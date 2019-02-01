## MUSC Machine Understanding of Clinical Notes.

### Background 

MUSC has millions clinical notes of different types of clinical notes that with a wide variety of information.         
These notes can contained an entire summary of a hospital stay, or a simple progress update. In order for these notes to
drive insights at scale for patient populations, Natural Language Processing is needed to accomplish systematic feature 
extraction.  The can eventually become the backbone of a new generation AI Models that will not only be powerful, but will 
inherently explainable. 

### Project Description

MUSC needs a python based dockerized web application that can intake both JSON or Text Files, and return parsed xml or JSON payloads.
This service needs to perform all the NLP steps under the hood.  The final destination of the container will be a 
kuberneties cluster inside MUSC's Azure instance. The NLP preformed under the hood needs to leverage Apache CTAKES.

### Team Requirements
The team that accepts the project should be fiuent 

### Deliverables

+ Docker Container with python based web API to conduct NLP
    *  Contained Must be able to launch with a UMLS credential argument  
+ Service Testing Script to ensure service is functioning correctly
    * Input requirements: curl raw text file, json payload, zipfile of text docs
    * Optional python based NLP cleaning step for raw text file 
    * CPE Collection Process Engine (collects documents for a local director)
    * Processes Notes via apache CTAKES, using UMLS Analyical Engine( Fast UML Lookup)
    * Optional xml parsing to JSON Payload step, based document ids
    * Outputs xml file, JSON Payload, zipfile with xmls


### Areas for Innovation        

CTAKES testing at MUSC has shown that in some cases medication amounts are not correctly detection by CTAKEs. The
optional prepossessing  step is intended to provided an chance for rule based NLP functions to increase CTAKEs
performance.  

### Test Data
Sample notes are provided with CTAKEs Package, 

### Provided by MUSC

+ Overall project guidance
+ assistance getting CTakes working locally 
+ UMLS Credentials in the case the UMLS cannot be obtained by the team.
 

### CTAKES 

Apache CTAKES is an open source platform that has the ability to a structure xml file from a raw text file input.  
It is a rule based system uses the Unified Medical Language System (UMLS) system. This will provide the core NLP engine
for the project.  
using https://www.nlm.nih.gov/research/umls/ 
https://ctakes.apache.org/

