
![image](/assets/CSC-QMS-logo.png) 

# QMS-Template Work Instructions

This template has been developed from the Guy's and St Thomas' NHS Foundation Trust Clinical Scientific Computing (CSC)
Quality Management System for Software as a Medical Device. To make this template useful for your department, you will
need to edit the documents to remove references to GSTT CSC and add references to your department and its processes. You 
should also adapt the documents to meet local policies and protocols.

## Setup
1. Create a 'GitHub Organisation' for your local team. 
2. Clone this repository to your local Organisation.
3. Get a GitHub Teams subscription if possible. To get a free subscription you will need to be approved for a GitHub non-profit discount and show you are registered as non-profit organisation. NHS Foundation Trusts are non-government, non-commercial, public good entities. This is supported using the following references 

    - https://www.nuffieldtrust.org.uk/files/2019-11/foundation.pdf
    - https://www.legislation.gov.uk/ukpga/2006/41/section/43
    - https://www.legislation.gov.uk/ukpga/2006/41/section/30
    - https://www.datadictionary.nhs.uk/nhs_business_definitions/nhs_foundation_trust.html

    You may also need to send a copy of your Trusts constitution. You can request this from the Office of the CEO of your Trust.  

4. Buy and read the regulations and standards relevant to your department 

| Standard / Regulation / Law | Link                                                                                                                      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| UK MDR 2002                 | https://www.legislation.gov.uk/uksi/2002/618/contents                                                                     |
| ISO 13485:2016              | https://knowledge.bsigroup.com/products/medical-devices-quality-management-systems-requirements-for-regulatory-purposes-3 |
| ISO 14971:2019              | https://knowledge.bsigroup.com/products/medical-devices-application-of-risk-management-to-medical-devices-5               |
| IEC 62304:2006              | https://knowledge.bsigroup.com/products/medical-device-software-software-life-cycle-processes                             |
| IEC 62366-1:2015            | https://knowledge.bsigroup.com/products/medical-devices-application-of-usability-engineering-to-medical-devices           |

5. Create a QMS backup schedule with GitHub actions
6. Change the version of each document according to your local versioning policy

## Assign Roles
1. Assign roles to your staff. The QMS must have a Quality Management Officer who is responsible for the QMS and named top management - typically someone with control over resources (e.g., Head of Medical Physics). The roles are defined in CSC-PL-001-Quality-Manual.md. Once roles have been assigned, fill in the CSC-I-001-Roles information document. 
2. Assign an internal auditor who is independent of the development process (there may be a medical physics auditor who would be suitable for this - ideally with an ISO 13485 auditor training certificate). 
3. Add your Quality Representatives as CODEOWNERS in `.github/CODEOWNERS`
4. Assign authors to edit and create the documents

## Edit Quality Manual (CSC-PL-001-Quality-Manual)
The quality manual introduces the QMS and should include details about your department and hospital including any local
processes. To make this document useful, make sure to edit the following sections.  
* Applicable Standards and Certifications
* Quality Objectives
* Replace the organisation chart 

## Edit Process Interaction (CSC-PL-002-Process-Interaction)
1. Develop a QMS Process diagram based on your local department. An example of our process diagram can be seen in Figure 1.
2. Replace the organisation chart   

## Third-Party Software Validation 
Complete validation forms for any locally used third party software. In GSTT we have validated the use of GitHub and 
XNAT which are routinely used in our development processes.   

## Staff Training 
Ensure all staff are trained as required by your local department and have appropriately onboarded to your department.
The SOP CSC-PR-020-Onboarding.md is an example of what GSTT do when a new staff member starts. Staff should undertake
regular training in key processes in the department. The information document CSC-I-003-Authorisation-Log.md details the
training that GSTT delivers to the staff on different processes, which can be used an example for what training may be
needed (suggestion - start with QMS training).    

Please note - The GSTT CSC team will be releasing training courses on how to use the QMS. Release date is TBC. 

## Schedules
Create the following schedules - 
* Weekly QMS meeting
* Annual management review
* QMS training 

## Test your adapted QMS
1. Complete the above steps and edit the documents to represent your department and its processes 
2. Create a test project
3. Run your project through each of these processes and fill out the documents 
4. Determine if any gaps are present or if any further documents need to be created


### Other useful public repos
|                                                                                  |                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **[LINK: CSC Project Template](https://github.com/GSTT-CSC/project-template)**   | A template repo that all CSC projects are started from. Integrates the the QMS for appropriate documentation, and MLOps to integrate with our machine learning pipeline for training models on our infrastructure.   |
| **[LINK: CSC MLOPs](https://github.com/GSTT-CSC/MLOps)**                         | A CSC open source python package for machine learning operations - Training ML models using docker, with data from XNAT, and logging models and training artefacts in MLFlow.                                        |




