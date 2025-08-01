---
qms_version: 2.2.0
sop_version: 2.0.1
---

# SOP Control of Non-Conforming Product
<!-- [13485:8.3.1,8.3.2,8.3.2a,8.3.2b,8.3.2c,8.3.3,8.3.4]-->

## General

|                           |                            |
|---------------------------|----------------------------|
| **Document ID**           | CSC PR.010                 |
| **Document Version**      | 2.0.1                      |
| **Author**                |                 |
| **Approval**              | H               |
| **QMS Version**           | 2.2.0                      |
| **Regulatory References** | ISO 13485:2016 Section 8.3 |

## Purpose
The purpose of the document is to describe the process of control products that become non-conformant to user 
requirement, expected use or applicable regulations. 


## Scope

This process relates SaMD applications design and developed by the CSC team under this QMS.

## Definitions
| Acronym | Definition                            |
|---------|---------------------------------------|
| CSC     | **Clinical Scientific Computing**     |
| QMS     | **Quality Management System**         |
| QMO     | **Quality Management Officer**        |
| SaMD    | **Software as a Medical Device**      |
| KPI     | **Key Performance Indicators**        |
| CAPA    | **Corrective and Preventive Actions** |


## Roles and Responsibilities


| Role                        | Responsibility                                                                                                   |
|-----------------------------|------------------------------------------------------------------------------------------------------------------|
| Head of Department/QMO      | Leading activities for controlling non-conforming products                                                       |
| CSC Quality Representatives | Raising and escalating reports of non-conforming applications and support the resulting actions decided by QMO.  |


### 1. Non-comformant products

An application developed by the CSC that is deployed clinically can become non-comformant if:
- A bug is found that results in the application performing out of specification
- a change in applicable regulations means the application is non-comformant
- A change in the clinical setting causes the application to not function as intended
- trend analysis of quality metrics shows a deterioration in the quality of results produced by the application

### 2. Response to non-conformant product before deployment

Where products are determined to be non-conformant prior to delivery, the QMO or CSC team member will create an action 
to eliminate the non-conformance. 

### 3. Response to non-conforming product detected after delivery

Where a CSC staff member becomes aware of a non-conforming product they will inform the Head of CSC to the issue. An
issue will be raised in GitHub which will trigger the CAPA process in CSC PR.016 Continuous and Preventative Actions. 

The following immediate actions should be considered on a case-by-case basis:
- removal of the application from clinical use and revert to standard of practice
- raise a non-conformance against the product under the Medical Physics QMS.

The QMO will then decide on the appropriate course of action through the CAPA system, which may include:
- planning activities to eliminate the detected non-conformity
- updated to the applications documentation
- training CSC staff to effectively to eliminate the non-conformity, and prevent it being repeated in other projects
- take action to preclude its original intended use
- authorising its use, release or acceptance under concessions. 
  - The CSC will only release a product under concession if justification is provided, approval by the Head of the 
  department for which the application is deployed, and applicable regulatory requirements are met. 
  - Records of the acceptance of the application by concession will be stored in the GitHub Repository.

An Field Safety Notice (CSC-F-006) will be provided to the host department to explain the issues and the immediate decisions regarding 
the on-going use of the application.

## 4. Rework

Re-work to remove the non-conformity (as part of the CAPA process) will be conducted by the CSC team using processes 
defined by Design and Development. Timeframes for completion will be agreed with the QMO or the Head of the department 
who will take ownership of the product once deployed. The resolution to the identified non-conformance will be added to
requirements specification and the routine development process will be followed for risk assessment and verification, to 
ensure all re-work activities are recorded and verified before the product is re-deployed.



