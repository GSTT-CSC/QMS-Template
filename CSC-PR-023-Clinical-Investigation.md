---
qms_version: 2.2.0
sop_version: 2.0.2
---

# Clinical Investigation SOP

## General  

|                           |                                                        |
|---------------------------|--------------------------------------------------------|
| **Document Id**           | CSC PR.023                                             |
| **Document Version**      | 2.0.2                                                  |
| **Author**                |                                             | 
| **Approval**              |                                             |
| **QMS Version**           | 2.2.0                                                  |
| **Regulatory References** | - UK MDR 2002 <br><br> -  MDD Directive 93/42 Annex 10 |


## Purpose

This SOP describes the process of completing a clinical investigation for SaMD being deployed into clinical practice. 

## Scope

This SOP relates to SaMD, built by the CSC Team, that is intended to be deployed into clinical use within GSTT. 

## Definitions
| Acronym | Definition                                                                               |
|---------|------------------------------------------------------------------------------------------|
| CSC     | **Clinical Scientific Computing**                                                        |
| CQC     | **Care Quality Commission**                                                              |
| QMS     | **Quality Management System**                                                            |
| CAPA    | **Clinical and Product Assurance**                                                       |
| MDSO    | **Medical Device Safety Officer**                                                        |
| FSCA    | **Field Safety Corrective Actions**                                                      |
| MHRA    | **Medicines and Healthcare Regulatory Authority**                                        |
| DATIX   | Web based reporting and risk management software for health and social care institutions |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training to fulfil the responsibilities.

| Role                    | Responsibility                                    |
|-------------------------|---------------------------------------------------|
| Clinical Lead           | Generate clinical evaluation plan and report <br> |                                                                    |
| Development Lead        | Generate clinical evaluation plan and report <br> |                                                                    |
| Clinical Safety Officer | Approvals                                         |                                                                    |


## 1. Introduction

A clinical investigation must be conducted prior to the release of a new application into clinical use, to ensure the
product performs as required/described. Clinical investigations will also assess whether any un-desirable side effects 
under normal use conditions constitutes to a risk when weighed against the intended performance of the device. 
 
## 2. Method

### 2.1 Generate Clinical Evaluation Plan

A Clinical Evaluation Plan shall be created which shall include the following:

- **Developer claims** - Clearly outline all performance claims of the device. 


- **Environment** - The software should be installed into the intended use environment, so that it can be run alongside the current standard of care.


- **Data** - Define the data to be collected, storage method, pseudonymisation process. Be mindful of the affected patient population and ensure sufficient representation of affected subgroups. Use AI fairness guidance when curating your data and generating your results (e.g. AI Fairness 360).


- **Sample size** - Choose an appropriate number of investigations that can guarantee the validity of the conclusions. The sample size must be sufficient to allow statistically significant analysis of subgroup populations to be carried out. An example of how such a 
calculation has been done in the past can be found on the Notion board -> Instructions & Guides -> Sample size calculation for ScaphX. 


| Participants                                                                                        |
|-----------------------------------------------------------------------------------------------------|
| Clinical Lead <br> Development Lead <br> Medical Practitioner with expertise in the clinical domain |

| Input                             | Output                   |
|-----------------------------------|--------------------------|
| Clinical Evaluation Plan template | Clinical Evaluation Plan |

### 2.2 Data Collection and Evaluation


- **Critical evaluation of investigations** - All data points to be critically evaluated against performance claims.


- **Adverse clinical events** - Any adverse clinical events should be raised, investigated and reported to the notified authority is required.  


- **Evaluate all features** - Evaluate all features of the product against their effect on the patient.


- **Hazard Log evaluation** - The Hazard Log should be evaluated, and updated if necessary, to reflect experiences during the clinical evaluation. 



| Participants                         |
|--------------------------------------|
| Clinical Lead <br> Development Lead  |

| Input                           | Output                         |
|---------------------------------|--------------------------------|
| Clinical Evaluation Plan        | Clinical Investigation results |

### 2.3 Generate Clinical Evaluation Report

- **Report** - A clinical evaluation report should be generated containing all relevant data, analysis and conclusions.  


- **Signatories** - The report must be signed by medical practitioner leading the study, the CSO and development lead when
all conclusions are agreed upon. 


| Participants                        |
|-------------------------------------|
| Clinical Lead <br> Development Lead |

| Input                          | Output                     |
|--------------------------------|----------------------------|
| Clinical investigation results | Clinical Evaluation Report |


