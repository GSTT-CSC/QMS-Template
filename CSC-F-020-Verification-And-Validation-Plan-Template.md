---
qms_version: 2.2.0
sop_id: CSC PR.003
sop_version: 2.0.1
template_id: CSC F.020
template_version: 2.0.1
record_version: 
record_id: VVP-001
title: Verification and Validation Plan

---

# Verification and Validation Plan
<!-- [13485:7.3.2c,7.3.2e,7.3.4a,7.5.1a]-->

## General 

|                           |               |
|---------------------------|---------------|
| **Template ID**           | CSC F.020     |
| **Template Version**      | 2.0.1         |
| **QMS Version**           | 2.2.0         |
| **SOP ID**                | CSC PR.003    |
| **SOP Version**           | 2.0.1         |
| **Regulatory References** |               |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |

### Purpose and Scope

This document describes a set of activities which will be used for the verification and validation of the software

This document applies to {{device.name}} release {{device.version}}.


### Definitions

| Term    | Definition                                        |
|---------|---------------------------------------------------|
| SRS     | Software Requirements Spec                        |
| SDS     | Software Design Spec                              |


### Roles and Responsibilities

| Role             | Name | Responsibilities                                                                      |
|------------------|------|---------------------------------------------------------------------------------------|
| Development lead |      | Completing documentation <br>  Generating Unit tests <br >Performing validation tests |
| ML Lead          |      | Reviewing ML activities                                                               |
| Clinical Lead    |      | Review Verification and validation test                                               |
| CSO              |      | Ensure Risks controls and verified/validated                                          |

| Document id                               | Purpose                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Software Requirements Specification (SRS) | Describes what the software needs to accomplish.  It is largely written by the project lead during the requirements gathering and analysis stage, and is reviewed by the project lead during the release.  Software developers may clarify and extend the document slightly during the unit implementation and testing activity                            |
| Clinical Risk Management plan (CRMP)      |                                                                                                                                                                                                                                                                                                                                                            |
| Software Design Specification (SDS)       | Describes how the software accomplishes what the SRS requires.  A significant portion is written by the project lead during the architectural design, but many details and specifics are added by software developers during the unit implementation and testing activity. It is reviewed for consistency by the project lead during the release activity. |
| Device Classification                     |                                                                                                                                                                                                                                                                                                                                                            |
| Verification and validation results       | Presents the results of tests which were run, when, and by who.                                                                                                                                                                                                                                                                                            |
| Release Record                            | Describes the verifications steps performed by the project lead during the release.                                                                                                                                                                                                                                                                        |


### 1. Verification plan
<!-- [13485:7.3.6]-->

#### 1.1 Unit tests overview 

The main method of verifying the code has been written correctly is to generate and perform unit tests. 

- Unit tests will be created to cover > 90% of the code. 
- Tests will be written for each item in the design specification. 
- Unit tests will be reviewed at key stages of the development process.
- Each Pull Request should only be merged where all unit tests pass. 


#### 1.2 Unit tests

| Design Spec. Item | Unit Tests | Expected Results |
|-------------------|------------|------------------|


### 2. Validation plan
<!-- [13485:7.5.6,7.5.6c]-->

#### 2.1 Validation Test Overview

Validation tests are typically manual checks and tasks performed to ensure the correct application has been built.
- Validation tests are performed by the software developer to check that the software meets all items identified in the 
System requirements specification. 
- In addition, validation tests can also capture design specification items that cannot be verified with automated unit
tests. 
- It is ok if some tests do not trace to any particular requirements, however all requirements must be covered by some 
tests (if they are not, add tests).


#### 2.2 Validation tests
<!-- [13485:7.3.7]-->


| Design Spec. Item | Test(s)   | Expected result     |
|-------------------|-----------|---------------------|


| Requirements Spec. Item | Test(s)   | Expected result   | 
|-------------------------|-----------|-------------------|



