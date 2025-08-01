---
qms_version: 2.2.0
sop_id: CSC PR.003
sop_version: 2.0.1
template_id: CSC F.021
template_version: 2.0.1
record_version: 
record_id: VVR-001
title: Verification and Validation Results

---

# Verification and Validation Results
<!-- [13485:7.3.2c,7.3.2e,7.3.4a,7.3.4c,7.5.1a]-->

## General

|                           |               |
|---------------------------|---------------|
| **Template ID**           | CSC F.021     |
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

This document presents the test results of all verification and validation tests to prove each system design 
specification item and each system requirements is successfully implemented.

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


### Related Documents

The following documents are related to design and development activities and contains records 

| Document id                               | Purpose                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Software Requirements Specification (SRS) | Describes what the software needs to accomplish.  It is largely written by the project lead during the requirements gathering and analysis stage, and is reviewed by the project lead during the release.  Software developers may clarify and extend the document slightly during the unit implementation and testing activity                              |
| Clinical Risk Management plan (CRMP)      |                                                                                                                                                                                                                                                                                                                                                              |
| Software Design Specification (SDS)       | Describes how the software accomplishes what the SRS requires.  A significant portion is written by the project lead during the architectural design, but many details and specifics are added by software developers during the  unit implementation and testing activity.  It is reviewed for consistency by the project lead during the release activity. |
| Device Classification                     |                                                                                                                                                                                                                                                                                                                                                              |
| Test Record                               | Describes a set of tests which were run, when, and by who.  It also must include enough details to reproduce the testing setup.                                                                                                                                                                                                                              |
| Release Record                            | Describes the verifications steps performed by the project lead during the release.                                                                                                                                                                                                                                                                          |


### 1. Verification Test results
<!-- [13485:7.3.6]-->

#### 1.1 Unit tests overview 

The main method of verifying the code has been written correctly is to generate and perform unit tests. 

- Unit tests will be created to cover >90% of the code. 
- Tests will be written for each item in the design specification. 
- Unit tests will be reviewed at key stages of the development process.
- Each Pull Request should only be merged where all unit tests pass. 

##### 1.2 Test Environment Configuration 

[TODO: describe the environment configuration used to run the unit tests, eg python env, requirements list, docker, 
GitHub actions, etc ]

#### 1.3 Unit tests

| Design Spec. Item Id | Unit Tests | Expected Results | Results | Performed By   | Date |
|----------------------|------------|------------------|---------|----------------|------|

 
### 2. Validation Test Results
<!-- [13485:7.3.6,7.5.6,7.5.6c]-->

#### 2.1 Validation test Overview

Validation tests are manual checks and tasks performed to ensure the correct application has been built.
- Validation tests are performed by the software developer to check that the software meets all items identified in the 
System requirements specification. 
- In addition, validation tests can also capture design specification items that cannot be verified with automated unit
tests. 

#### 2.2 Validation Test environment configuration

[TODO: describe the environment configuration used for the manual tests]

#### 2.3 Validation tests

| Design Spec. Item id | Test(s)    | Performed by     | Expected result     | Result | Date  |
|----------------------|------------|------------------|---------------------|--------|-------|


| Requirements Spec. Item Id | Test(s)   | Performed By | Expected Result   | Result  | Date  |
|----------------------------|-----------|--------------|-------------------|---------|-------|
