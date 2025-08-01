---
qms_version: 2.2.0
sop_id: CSC PR.001
sop_version: 2.0.1
template_id: CSC F.008
template_version: 2.0.2
record_version:
record_id: DP-001
title: Design Plan
---

# Design Plan 
<!-- [13485:7.1c,7.2.1c,7.3.2a]-->

## 1. General

|                           |               |
|---------------------------|---------------|
| **Template ID**           | CSC F.008     | 
| **Template Version**      | 2.0.1         |
| **QMS Version**           | 2.2.0         |
| **SOP ID**                | CSC PR.001    |
| **SOP Version**           | 2.0.1         |
| **Regulatory References** |               |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |

## 2. Purpose

This document describes a set of activities which will be used during software risk management, development, and 
maintenance of {{device.name}}. It is written primarily for software developers.

{{device.name}} is assigned a Class {{device.mhra_classification}} software safety class, which means non-serious injury could occur if the
software fails.

All the software items that compose the software system are also presumed to have the same Class. The primary purpose 
of this document is to help developers ensure {{device.name}} is safe and useful while also allowing developers to be 
productive. The secondary purpose is to comply with BS EN 62304:2006 and ISO 13485:2016.


## 3. Scope

This document applies to {{device.name}} release {{device.version}}.

## 4. Definitions 

| Item | Definition |
|------|------------|
|      |            |


## 5. Roles and Responsibilities
<!-- [13485:7.3.2d]-->

| Role | Responsibilities |
|------|------------------|
|      |                  |

## 6. Related Documents
<!-- [13485:7.3.2f]-->

| Document ID                             | Purpose                                                                                                                               | Link |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------|
| Software Requirement Specification      | Describes the user requirements, risk control to be implemented, and regulatory requirements need for design planning.                |      |
| Clinical Risk Management Plan (CRMP)    | Lays out the clinical risk management frameworks, activities, and results.                                                            |      |
| Hazard Log                              | The outputs of Risk analysis, assessment and mitigation processes conduct with key stakeholders.                                      |      |
| Software Design Specification (SDS)     | Logs the outputs of the design activities in detail, tracing tasks back to the requirements                                           |      |
| Verification and validation plan        | Describes the framework for ensuring the applications is built safely effective and to specification using automated and manual tests |      |
| Verification and validation test record | Present the results of the automated and manual test to demonstrate the correct application has been built safely.                    |      |
| Release Record                          |                                                                                                                                       |      |
|                                         |                                                                                                                                       |      |


___

### Development Standards
<!-- [13485:7.3.4d]-->

- This application has been developed within an ISO 13485:2016-certified quality management system.
- The development of this medical software application follows BS EN 62034:2006.
- Clinical risk management activities have been conducted in accordance to DCB0129 and DCB0160, based on ISO 14971:2019
- This application has been design and developed following the usability standard ISO 62366:2015.
- This application uses python 3 as the main programming language and conforms to PEP8 coding conventions.


### Development methods

This project uses a part mixed agile/waterfall software development lifecycle development to benefit from the input and concerns 
from a range of stakeholders as new requirements and risks as identified, but only releases safe and effective application into the clinical environment.


### Development Tools

This project utilises the following tools for development:

| Software                                             | Software Validation Report |
|------------------------------------------------------|----------------------------|
| PyCharm 2022.1.1 (Professional Edition)              | (add report from QMS)      |
| XNAT (eXtensible Neuroimaging Archive Toolkit   <br/ | (add report from QMS)      |

### Testing Plan

All final tests must include the Git hash or other objective reference that can be used to identify the exact software tested.

Tests will be used throughout development to verify and validate the correct application is being built in a safe and effective way. A verification and validation plan will be created for the project using CSC PR.003 Verification and Validation SOP.

Unit test must be written for each modular unit of functionality/code. Unit tests should aim to provide > 90% coverage of the code.

All unit tests pass and that all integration tests pass, or the cause of the failure is understood and justified.

This plan should include a pass/fail criteria for the entire test suite.

### Quality Assurance 

The activities below are designed to meet the ISO 13485:2016 quality control standard.

### Risk Management

The Risk Assessment, Risk Control and other activities below are intended to meet DCB0129 clinical risk management standard.


## Activities 

---

### Activities diagram

A diagram will be produce to show the sequence of activities required for the development of the project.

### Exploratory analysis

Analysis will be conducted on the dataset or subset of the dataset for complete understanding and characterisation of 
biases, completeness, format and complexity. The analysis will be shared to inform stakeholders during planning 
activities such as requirements gathering. 

### Planning
<!-- [13485:7.1b]-->

All software activity outputs will be stored in this Git repository, the associated GitHub issues, or the associated 
GitHub pull requests, unless explicitly noted otherwise. The software developers working on the project are responsible 
for keeping all software activity outputs within version control at the times specified in the activity descriptions.

In the Software Design Specification, record details about the project's build process, including tool versions, 
environment variables, etc. Also document how the software can be reliably delivered to the point of use without 
corruption or unauthorized change.

Keep this planning document up to date as the project commences.

In conjunction with the manufacturer's management, review and update as appropriate the:

- qualitative risk severity categories
- qualitative risk probability categories
- qualitative risk levels

contained within hazard log.

### Milestone Review Planning

Each design and development milestone should be planned and tracked throughout the project. At each milestone a review of key work should take place. This can be done by a co-developer (peer review) or by a project development supervisor. 

| Milestone                             | Expected Completion Date | Review of work completed by | Review outcome|
|---------------------------------------|--------------------------|-----------------------------|---------------|
| Requirements gathering                |                          |                             |               |
| Architectural design                  |                          |                             |               |
| Detailed design                       |                          |                             |               |
| Software development                  |                          |                             |               |
| Integration and systems testing      |                          |                             |               |
| Release                               |                          |                             |               |

_Add or remove milestones as appropiate to the project._

### Requirements Analysis

Important software requirements should be enumerated at the start of the project.

When software requirements are added or changed, re-evaluate the medical device risk analysis and ensure that existing 
software requirements and system requirements, are re-evaluated and updated as appropriate

### Architectural Design

A diagram for the system architecture and how it integrates with other clinical systems will be created and regularly
review to reflect the development of the system requirements specification, system design specification and hazard log.


### Clinical Risk Management 

Activities pertaining to clinical risk management are performed in accordance with the clinical risk management plan.

### Risk Controls

Risk controls are implemented against hazards identified in risk assessment that exceed the acceptable level of risk, 
as determined by the CSO. Where risk controls must be linked to a requirement; when none are applicable, a requirement
must be added.

### Division of Labour

There are many ways to divide new requirements work into change requests. Change requests associated with requirements 
which will be implemented soon may be split into smaller change requests, while requirements which may not be worked on
for several months can be captured in a single large change request.


### Release Planning

A plan to determine how each software version will be released. This should include what features are planned to be released within each version, the timeline for the releases and how the software will be released detailing the release process. The release process should include details of release, documentation creation or updates, verification and validation of new software version and if required updates to the clinical risk management hazard log and clinical safety case. Please refer to CSC-PR-025-Software-Release-Guidelines.md for further information on the software release process.  

### Detailed design

In the system design specification, write a detailed design for each software item, including functions, classes, 
procedures and modules as appropriate. Detailed designs for interfaces between software items and external components 
(hardware or software) should be included as appropriate.

Once the detailed design is completed, a pull request should be assigned to the project lead to review the design to 
verify is it not more complicated than it needs to be to fulfil the all the system requirements, and is free from 
contradiction.

### Unit implementation and testing

Unit tests will be implemented following the suggestions and structure in the verification and validation plan.

### Integration

Merge the approved Git branch into the master Git branch, correct any merge conflicts that occur.
Once the branch has been merged successfully, delete the branch in GitHub.

### Integration and systems testing

The final integration prior to a release must formally record the test output in a test record. The test record must include:

- The list of tests that passed or failed
- Verification that the results meet the pass/fail criteria listed in the Test Plan
- The version of the software being tested (e.g., the Git commit hash)
- The name of the person who ran the tests.

Any test failures found during the formal release system testing shall be recorded as problem reports.
If any change requests are implemented in response to these problem reports the tests must be re-run.
If it is deemed unnecessary to re-run the tests, the justification as to why shall be included in the test record

Output: Test record and problem reports

Verification: Ensure code changes:

- The original problem is fixed and the problem report closed
- Any adverse trends have been reversed.

