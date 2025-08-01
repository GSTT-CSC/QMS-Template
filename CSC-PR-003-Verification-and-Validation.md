---
qms_version: 2.2.0
sop_version: 2.0.1
---

# Verification and Validation SOP
<!-- [13485:7.1c,7.3.2e,7.3.4a,7.3.4c]-->

## General 


|                           |                |
|---------------------------|----------------|
| **Document ID**           | CSC PR.003     |
| **Document Version**      | 2.0.1          |
| **Author**                |     | 
| **Approval**              |    |
| **QMS Version**           | 2.2.0          |
| **Regulatory References** | ISO 13485:2016 |

## Purpose
This document describes the processes for the verification and validation of software requirements.  

## Scope
This procedure must be followed during the development of all CSC computing projects that will directly affect patient 
care or interact with live clinical system or databases.

## Definitions
The following table provides the list of documents to be completed during the design and development phase of the project.

| Acronym | Definition                                                                                        |
|---------|---------------------------------------------------------------------------------------------------|
| SOUP    | **Software of Unknown Provenance** - Software used in the project that is not approved by the QMS |
| QIPS    | **Quality Improvement and Patient Safety**                                                        |
| XNAT    | **eXtensible Neuroimaging Archive Toolkit** - (imaging informatics platform)                      |                                                                                                  
| ML      | **Machine Learning**                                                                              |
| AI      | **Artificial Intelligence**                                                                       |
| MLOps   | **Machine Learning Operations** -  (related to DevOps)                                            |
| PID     | **Patient Identifiable Data**                                                                     |
| KPI     | **Key performance Indicators**                                                                    |
| PR      | **Pull Request** - Github review action                                                           |

## Roles and Responsibilities
At the start of the project the following roles must be allocated. 

| Role                    | Responsibility                                                                                                                 |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Clinical Safety Officer | Provide expertise and leadership in all activities associated with the evaluation of clinical risk management for the product. |
| Development lead        | Generate and action the validation and verification plans                                                                      |
| Clinical Lead           | Provide clinical expertise for verification and validation activities.                                                         |

## 1. Introduction

Verification and validation is necessary to ensure the user requirements, risk mitigations steps and regulatory 
obligations are fulfilled during the development process. 
Put simply, 

- Verification ensures we have built the software **right**
- Validation ensures we have built the **right** software

Verification and validation activities should commence at the design planning stage, after the user requirements and 
design specifications have been approved. 

The developer should determine a schedule to review the outputs of these activities at regular intervals, or at key 
milestones, by the clinical lead, the CSO, and the wider development team. Regular review confirms the project is being 
developed safely and to specification, and manages any changes to the risk assessment and user requirements that could 
be identified at different stages of the development lifecycle. 

## 2. Verification
<!-- [13485:7.3.2c,7.3.6]-->

A plan to perform the following verification actions must be created as part of the design plan. The verification plan
must be reviewed and approved by the Clinical Lead and CSO before the project moves forward with development. 
The verification activities play a part in successful risk management mitigations and regulatory compliance in medical 
software development. 

### 2.1 Unit Tests 
Unit tests on individual functions should be created to verify that given inputs provide expected outputs. After the 
design requirements are approved, the developer must make a plan to apply unit tests to each measurable function within 
the software. These can be written collaboratively with key stakeholders in the project or other CSC team members with 
relevant experience.

Unit tests:
  - should be implemented in all software being developed through this QMS.
  - should be written to address elements of the system design specification.
  - should be written to reflect risk mitigations identified in the risk assessment.
  - can also be applied on a group of software elements (ie integration tests)

E.g. Where Python is used as the programming language, pytests should be written for each method. Through
GitHub/Bitbucket pipelines the pytests will be performed when pull requests are reviewed.

### 2.2 Best Coding Practice
Best coding practices should be followed for the chosen programming language(s) of the project. The following table 
provides examples of guidelines of commonly used languages:

| Language | Guideline                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|
| Python   | [PEP8](https://www.python.org/dev/peps/pep-0008/)                                                                 |
| C#       | [Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions) |
| Shell    | [Shell best practices](https://google.github.io/styleguide/shellguide.html)                                       |
| Docker   | [Docker Best Practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)                                                                                         |

PRs on GitHub should check adherence to these guidelines.

### 2.3 Other verification actions
All internal software used for the development of the project has the appropriate software validation completed, e.g. 
for XNAT or MONAI.


### 2.4 Verification Review
- All unit tests that fail should be investigated and fully resolved. 
- PRs should not be approved if any unit tests are failing.
- The results of the unit tests must be reviewed and approved by persons who did not program the unit tests.
- On subsequent development cycles, where extra user requirements or risk mitigation items are produced, the 
development lead is responsible for implementing additional unit test to verify these new functions.

## 3. Validation 
<!-- [13485:7.3.2c,7.3.7,7.5.6,7.5.6c,8.1a]-->
The validation process consists of high level tests and checks that makes sure the solution fits the requirements of 
all stakeholders. A validation plan must be completed as part of the design plan before development commences. It must 
be created after the risk mitigation actions and User requirements have been approved. 
The validation plan should:
- determine tests to check each user requirement is fulfilled, where unit tests cannot measure clear KPI's.
- review the validation tests at regular intervals throughout the development process, working to the most recently
approved requirements specification and risk assessment.
- ensure that any non-conformities and deviations are resolved.

### 3.1 Installation and hardware
<!-- [13485:7.5.1a]-->
- The developer must check that the software can be installed on a different system than the developer's own system.
- The 'requirements.txt' file for python libraries must be up-to-date and without conflicts. 
- The developer must check that the software can be installed on the any hardware specified in the user 
requirements/system design requirements. 
- Instructions must be provided to install software and ensure a basic test of functionality can be run. 
(e.g.: provide this in README.md of the Git Repo, or ReadTheDocs page, etc.)
- Minimum hardware requirements should be provided for all software 




