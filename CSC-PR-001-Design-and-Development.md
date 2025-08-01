---
qms_version: 2.2.0
sop_version: 2.0.4
---

# Design and Development Procedure
<!-- [13485:5.2,7.1c,7.3.1,7.3.2e] -->

## General

|                           |                                                                                                      |
|---------------------------|------------------------------------------------------------------------------------------------------|
| **Document ID**           | CSC PR.001                                                                                           |
| **Document Version**      | 2.0.3                                                                                                |
| **Author**                |                                                                                           | 
| **Approval**              |                                                                                          |
| **QMS Version**           | 2.2.0                                                                                                |
| **Regulatory References** | **ISO 13485:2016:** <br> 7.1 a, b, c <br> 7.2.1, 7.2.2, 7.2.3 <br> 7.3.1, 7.3.2, 7.3.3, 7.3.4, 7.3.5 |

## Purpose
This document describes the design and development processes for computing projects undertaken by the Clinical
Scientific Computing Team in Medical Physics at Guy's and St Thomas' NHS Foundation Trust.

## Scope
The processes in this document must be followed for computing projects where the solution is intended to be 
used as software as a medical device (SaMD). 

## Definitions
| Acronym  | Definition                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SOUP     | **Software of Unknown Provenance** - Software item that is already developed and generally available and that has not been developed for the purpose of being incorporated into the medical device |
| QIPS     | **Quality Improvement and Patient Safety**                                                                                                                                                         |
| XNAT     | **eXtensible Neuroimaging Archive Toolkit** - (imaging informatics platform)                                                                                                                       |                                                                                                  |
| ML       | **Machine Learning**                                                                                                                                                                               |
| AI       | **Artificial Intelligence**                                                                                                                                                                        |
| MLOps    | **Machine Learning Operations** -  (related to DevOps)                                                                                                                                             |
| PID      | **Patient Identifiable Data**                                                                                                                                                                      |
| CT       | **Computerised Tomography**                                                                                                                                                                        |
| MRI      | **Magnetic Resonance Imaging**                                                                                                                                                                     |
| PET      | **Positron Emission Tomography**                                                                                                                                                                   |            
| SaMD     | **Software as a Medical Device**                                                                                                                                                                   |

## Roles and Responsibilities
<!-- [13485:7.3.2d]-->

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training.

| Role                          | Responsibility                                                    |
|-------------------------------|-------------------------------------------------------------------|
| Clinical Safety Officer (CSO) | Appointed to oversee the clinical risk management of the product  |
| Development lead              | Responsible for organising and completing all development actions |
| Product owner                 | Takes ultimate responsibility for the deployed product            |


## 1. Prerequisites
<!-- [13485:8.1a]-->
This section outlines the actions and documents that must be completed before commencing the design of the project. 

### 1.1 Project Proposal
<!-- [13485:7.3.2f]-->
The project proposal form must be completed before commencing the design and development process. The proposal 
must accurately describe the following:
- the problem
- the clinical setting i.e. department
- key stakeholders
- end users
- clinical background
- the clinical systems the problem affects
- understanding of the current pathway and how the solution could integrate 
- peer-reviewed literature to demonstrate evidence for problem and/or solution
- definition of the clinical lead
- data source and format 
- anticipated times frames
- list of commercially available solutions (if any) 
- anticipated resourcing needs including personnel, infrastructure, equipment

### 1.2 Literature Review
The initial meetings with the proposer should uncover the base knowledge and understanding of the problem and how it 
affects the wider clinical setting. A review of the literature should be completed prior to commencing the project 
design process. Given the rate of new publications in the healthcare AI field, literature should be reviewed continuously
through the duration of the project.

The Development Lead should obtain from the proposer a list of peer-review publications related to the problem. 
All staff assigned as project Development Lead must have access to the King College London library. 

### 1.3 Administration
<!-- [13485:6.3c,7.3.5]-->
For each new project the following administrative tasks need to be completed:
- Create a GitHub repository in https://github.com/GSTT-CSC using a unique ID for the project title. The ID will 
be the agreed internal name of the project <br><br>
- Designate the roles of Clinical Lead, Development Lead, and Clinical Safety Officer (CSO):
  - All roles must be filled by persons authorised to perform their required tasks. A competency log must be maintained 
    in the project repository.   
  - The person filling each role should commit to routine meetings for key milestones throughout the software
development lifecycle. 
  - These roles must be documented on the project's title page (README.md) in the GitHub repository. <br><br>
  - Determine preferred method of communication with all stakeholders e.g. preferred email address. 
- Determine the product owner of the software after deployment. This will typically be the head of the department that
the application has been designed for and deployed in. This should be confirmed in writing and stored in the project 
repository. <br><br>
- Schedule regular meetings at an agreed frequency with key stakeholders to review the progress of the project. Agree 
key milestones with the Clinical Lead and CSO for systematic review of design and development stages. 

### 1.4 Medical software classification
<!-- [13485:7.3.4d]-->
- Determine classification of the medical device under MEDDEV 2.4/1 and record this in the project repository.
  - https://ec.europa.eu/docsroom/documents/10337/attachments/1/translations/en/renditions/pdf
  - Type I, IIa, IIb, or III.<br><br>
- Determine the software classification under IEC 62304 and record this in the project repo.
  - Type A, B, or C. <br><br>
  
### 1.5 Registering Projects as Quality Improvement
- If the project requires access to patient data in a non-research setting it may need to be registered as a quality improvement project. Please ensure you follow your local processes. 

### 1.6 Data Transfer 
- Any clinical data intended for use in the development of the project should be stored in XNAT. The procedure for
creating a project on XNAT and managing data is described in CSC PR.007 "Uploading to XNAT". 


## 2 Design Plan
<!-- [13485:7.3.2a,7.3.2b,7.3.3,8.2.6]-->

A design plan is required to ensure that a customer-focused, safety-driven approach to software development is 
implemented through the project. The Development Lead will map the customer requirements and clinical risk management 
mitigation items to actions in the design specification to ensure all considerations are met during the development 
process. They must also formulate plans for verification and validation activities and have them approved by the 
Clinical Lead and CSO prior to the development process. 

### 2.1 Exploratory Analysis
- Exploratory analysis should be conducted using a sample dataset that is representative of the wider population 
involved in the development of the project 
- this subset of data should be transferred to XNAT and pseudonymised before the exploratory analysis is started. 
- the subset should be representative of the wider dataset and include data with and without the clinical indication in
question. Patient Identifiable Data should ever be stored on local laptops
- the results of the analysis should be presented to the clinical lead and used to better understand problem and inform 
the design plan and risk assessment.

### 2.2 System Requirements Specification
<!-- [13485:6.3b,6.3c,7.1a,7.2.1a,7.2.1c,7.2.2a,7.2.2c]-->


The development lead is responsible for organising sessions with the clinical lead and with stakeholders to compile a 
list of system requirements. The list below contains a non-exhaustive list of considerations to discuss with 
stakeholders to gather requirements.

**Regulatory**
- Applicable standards and regulations

**Security**
- Access restrictions
- Other security controls

**Data**
- Input data format that need to be processed 
- Output format of the application
- Local population demographics, to be reflected in training data.
- Data definitions and database requirements

**Validation**
- Quality objectives e.g., quality metrics, ranges, threshold values

**Structure**
- Information derived from previous designs
- SOUP (including versions)

**Connectivity**
- Platform for delivery
- Destination of the output data
- Access e.g. Citrix, remote desktop, Trust PC
- Interfaces between medical systems e.g., Trust IT integration for PACs, individual software APIs, application plugins. 

**Workload and use**
- Maximum turnaround time
- Past complaints, failure reports, adverse events of similar products
- The workload e.g. number of CTs per weekday
- The expected uptime time e.g., 95% clinical work hours
- Usability and maintenance
- Number and frequency of users to be supported
- Workflow integration
- Training requirements e.g., workshops, training, documents

**User interfaces**
- User interface design and requirements

**Safety**
- Software driven alarms, warnings, operator messages
- Safety considerations for patients and staff

**Deliverables**
- Readable documentation e.g. Design Spec, Unit test reports, Hazard Log etc

**Operation, monitoring and maintenance**
- Content of surveillance plan including metrics to monitor once deployed.
- Requirements related to methods of operation and maintenance
- User maintenance requirements e.g., user rights

**ML considerations**
- Minimum sensitivity, specificity, true/false positive/negative rates
- Turnaround time for inference
- Expected frequency of retraining
- Training data biases to acknowledge

**Legacy Software**
- Incident/complaints
- Gap analysis against new requirements
- Risk assessment and risk controls from previous software.

**Hardware**
- Hardware required to operate e.g., servers, imaging equipment, on-site devices, GPUs
- Compatibility considerations with existing infrastructure
- Maintenance or upgrades required for hardware

The requirements should be complete, unambiguous, able to be verified or validated, and not conflicting. 

Each requirement should be logged in a user requirements specification with a unique ID in the form SRS_XXX e.g. SRS_001,
which will allow it to be referenced in the Design Specification. 
Requirements should be developed between the clinical lead, stakeholders, and the project lead. Different methods for 
gathering requirements can include the following: 
- questionnaires
- workshops
- meetings/interviews
- patient/staff feedback

The process of gathering requirements can cover multiple sessions/days, where the requirements list may have multiple 
revisions. Each change of a requirement must be dated and approved for good traceability.


### 2.3 User Interface Design
- For projects where the solution required user interaction through an interface, the project lead should gather 
- specific requirements for the user interface 
- any wire frames or interface template designs should be drawn up and referenced in the design plan.

### 2.4 Risk Management
<!-- [13485:7.2.1c,7.3.4d]-->

Risks should be considered at all stages of the medical software development lifecycle to ensure that solutions 
deployed in the clinical environment have been built to the highest standard of safety where all risks have been 
identified, characterised, and mitigated or accepted. 

Risk management for software projects that are developed under this QMS must adhere to the following standards:

| ID        | Standard or Regulation                                                            |
|-----------|-----------------------------------------------------------------------------------|
| DCB-0129  | Clinical Risk Management: its Application in the Manufacture of Health IT Systems |
| ISO-14971 | Application of risk management to medical devices                                 |

The CSO is responsible for implementing all risk management activities described in CSC PR.002 Clinical Risk
Management System.  

### 2.5 Review of requirements
<!-- [13485:7.3.5]-->

A final review of the software requirements should be performed prior to commencing developments. They should include 
the identified risk controls as separate items in the software requirements if not already represented. The software
requirements specification document should be approved in GitHub by the clinical lead. If the clinical lead does not 
have a GitHub account, then a CSC team member can approve the SRS on the clinical leads' behalf, provided the team 
member is not the Development lead and is trained in requirements gathering. 

### 2.6 System Design Specification
- The Development Lead is responsible for the creation of a system design specification which defines the system-level
development requirements that satisfy all points in the requirements specification and the identified risk mitigations 
- these describe the practical steps to satisfying the user requirements and risk mitigation steps
- each item in the design specification must have a unique ID 
- the design specification items must reference the user requirement ID's or risk mitigation action ID's that they 
satisfy for traceability, if applicable.
- the design specification must be reviewed and approved prior to development.  

### 2.7 System Architecture Diagram
The Development Lead shall create a system architecture diagram to describe the interaction between functional sub-units
that make up the system, and how the system connects to other external systems. The system diagram should be stored with
in the Project repository and displayed in the project README. 

### 2.8 Software Development lifecycle Process 
The Development Lead shall decide on the software development lifecycle process. A diagram describing the actions 
involved in this process should be added to Project Repository.

### 2.9 Verification Plan
<!-- [13485:7.3.2c,7.3.6,7.3.7]-->
A verification plan must be made to cover the required verification activities described in CSC PR.003 Verification
and Validation. The plan should identify key points throughout the development process for the recorded verification
outputs to be analysed.

### 2.10 Validation Plan
<!-- [13485:7.3.2c]-->
A validation plan must be created to map how the user requirements are met and how the risk mitigation actions have been 
successfully implemented. The plan must include acceptance criteria for the finished solution. Validation tests should
also be conducted.
The process for implementing validation activities is described in CSC PR.003 Verification and Validation. 

### 2.11 Systematic review 
<!-- [13485:7.3.5]-->

Key milestones for systematic review of the project must be agreed between the development lead, clinical lead and the 
CSO to ensure the design and development process meets the requirements and to address any issues. These reviews can 
contain other subject-matter experts and stakeholders as appropriate. 

The systematic review must include review of documentation completed to date, outstanding issues, and any results of 
verification and validation tests. Records of each review must be logged as an issue in the project repository, using 
systematic review issue template.  

Suggested milestone for performing a systematic review:
1. Once the requirements specification and first draft of hazard log has been created, prior to development. 
2. After a proof of concept has been developed. 
3. Deployment of first version, prior to retrospective study. 
4. Before prospective study
5. Final sign off before releasing clinically


## 3 Development
<!-- [13485:7.1b,7.3.2a,7.3.8]-->

This section of the protocol describes general processes for safety software development. For projects where ML 
applications are developed, the CSC PR.008 Machine Learning Operations should be followed. The MLOps SOP supersedes this
procedure if conflicting actions are found. 

The development process must follow the development plan. Where requirements changes are identified during the 
development process, the CSC PR.021 Change Management SOP CSC PR.021 must be followed.

The CSC has not implemented a process for the transfer of 'design and development outputs' to 'manufacturing' as
required by ISO13485:20.16 clause 7.3.8 as we believe the design and development process and manufacturing significantly
overlap in the context of software development due to its iterative nature. Software development is 'manufacturing' for 
SaMD, and software development can influence the design for a variety of reasons, including discovery of new risks, new
functionality of embedded libraries, ML model architecture etc. 


### 3.1 Data preparation

#### 3.1.1 Pseudonymisation
- Any data used in development must be free of patient identifiable information
- where medical images such as CT, MRI, PET, ultrasound, and x-ray etc. are used for training, verification or testing 
of a solution, must be at least pseudonymised prior to use. The recommended practice is to upload the data to a 
dedicated XNAT project where approved pseudonymisation templates can be applied automatically. See CSC PR.007 "Uploading
to XNAT".
- where numerical or written data is stored in spreadsheets or databases, de-identification of patient information via 
a pseudonymisation protocol should be applied
- a look-up table that maps pseudonymised dataset entries the corresponding patient should be in a password-protected 
Excel document and stored in a directory on the S:/ drive within the GSTT Intranet. 

#### 3.1.2 Bias Identification in Datasets
- Patient data used in the development of medical software may contain inherent bias in characteristics such as age, 
gender, ethnicity, and BMI. Patient demographics behind the dataset must be analysed and any identified biases must be 
discussed with the clinical lead and CSO for validity before continuing with the project.
- Each dataset must be labelled with the following demographic information as a minimum: 
  - age spread
  - sex split
  - ethnicity composition (where possible).

#### 3.1.3 Data Labelling
- Data labelling is the process of correctly assigning tags to raw data to classify groups within the dataset e.g. 
presentation of disease symptoms in a medical image 

- in order to create a high quality dataset for ML model training, labels must be assigned by a person with sufficient 
expertise, or multiple people if "double reading" is required. Their expertise should be documented within the 
project. 
 

#### 3.1.4 Dataset Versioning and identification
- Good dataset versioning must be practiced throughout the different stages of data preparation to ensure that best 
practices are followed
- dataset should be labelled with the version to facilitate good traceability during ML model development
- version id numbers should increment when additional pre-processing operations have been performed.

#### 3.1.5 Duplicate Instances Identification
- Ensure that duplicate instances within datasets are identified, in particular by engaging with anyone involved with data labelling/data preparation.
- Remove potential duplicates to avoid skewing model performance. May involve Python's pandas drop_duplicates function or other project-specific methods.
- Document the number and handling of these duplicates in a data manifest, update the dataset version identifier.
  
### 3.2 Software of Unknown Provenance (SOUP) 

- The Development lead must produce a list of all software of unknown provenance used in the development of the project.
This must be stored in the project repository.  
- The list must include the following: 

|  ID | Software System | Package Name | Programming Language | Version | Website                                          | Last verified at | Risk Level | Requirements               | Verification Reasoning                                                    |
|-----|-----------------|--------------|----------------------|---------|--------------------------------------------------|------------------|------------|----------------------------|---------------------------------------------------------------------------|

- Software developed and maintained with respect to IEC 62304 requirements or with respect to medical devices 
regulations are not SOUP.
- The following item are considered SOUP:
  - Open source libraries 
  - Python packages
  - Operating Systems
  - Any software not built under IEC62304

Any SOUP in used the project must under verification tests, and the results of the test must be analysed and approved
prior to deployment.

### 3.3 Integrated Development Environments (IDE)
<!-- [13485:7.5.1b]-->
- The development lead must choose an IDE that best suits the chosen coding language and integration with the GitHub 
repository.


### 3.4 Unit Testing
- Unit tests verify that functions or groups of functions in the code provide the expected output for a given input. 
As a rule of thumb, unit tests should be used extensively, and cover 100% of the code if the solution is a medical device 
or 80% if it is not.
- Unit tests are described in CSC PR.003 "Verification and Validation".


### 3.5 Model Training - MLOps
<!-- [13485:7.5.1b]-->
- Where ML is a component of the project, the medical imaging processing python library PyTorch should be used, 
or its derivative MONAI.
- for projects that involve training and deploying of an ML algorithm, the development processes should 
follow CSC PR.008 "Machine Learning Operations".

### 3.6 Installation and Deployment Instructions
The Development Lead must write:
- instructions for the usage of the application upon completion of development
- instructions for installation of application into the environment specified by the user in the requirements.

The CSC PR.012 "Deployment and Integration" SOP must be followed to complete the deployment activities. 

### 3.7 Product Acceptance criteria
<!-- [13485:7.1d,8.2.6]-->

In preparation for the deployment activities, the clinical lead and relevant stakeholders must define the acceptance 
criteria. These should be created from the perspectives of the product specification, the end users, and clinical safety,
and training. 

The acceptance criteria should at least:
- Product meets all user requirements
- Passing all verification tests
- Passing all validation tests
- Delivery and approval of Clinical Safety report
- Completion and delivery of Hazard log
- Staff training considerations

Records of acceptance criteria should be stored in the projects' GitHub Repository. 

### 3.8 Changes to the design and development
<!-- [13485:7.2.2,7.2.2b]-->

There are situation where changes must be made to applications, such as bug fixes, user complaints, feature requests,
validation test failures etc. 
- Changes as a result of feedback should be analysed by CSC PR.006 Feedback Management. 
- Changes as a result of other reasons such as identification of errors in house, updates to the software etc. should
be controlled by the CSC PR.021 Change Management SOP. 


## Related documents

| Document Title               | ID        |
|------------------------------|-----------|
| Design Plan Template         | CSC F.008 |
