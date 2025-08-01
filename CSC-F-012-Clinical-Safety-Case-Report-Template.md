---
qms_version: 2.2.0
sop_id: CSC PR.002 
sop_version: 2.0.1
template_id: CSC F.012
template_version: 2.0.2
record_version: 
record_id: CSCR-001
title: Clinical Safety Case Report
---

# Clinical Safety Case Report 

## General 

|                           |                                  |
|---------------------------|----------------------------------|
| **Template ID**           | CSC F.012                        |
| **Template Version**      | 2.0.1                            |
| **QMS Version**           | 2.2.0                            |
| **SOP ID**                | CSC PR.002                       |
| **SOP Version**           | 2.0.1                            |
| **Regulatory References** | ISO14791 <br>DCB0129 <br>DCB0160 |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |

## Document Management

### Revision History

| Version | Date        | Author | Summary of Changes |
|---------|-------------|--------|--------------------|
| 0.1.0   | 01/01/2000  |        | First Draft        |

### Reviewers

| Review Name | Title/Responsibility                 | 
|-------------|--------------------------------------|
|             | Head of CSC /Clinical Safety Officer |
|             |                                      |


### Approval

| Review Name | Title/Responsibility | Date | Version |
|-------------|----------------------|------|---------|
|             |                      |      |         |

### Related Documents

| Document Reference Number | Title | Version | Status |
|---------------------------|-------|---------|--------|
|                           |       |         |        |

## Purpose

This document reports the implementation, results and effectiveness of the clinical risk management activities outline 
in the clinical risk management plan.

## Scope

This document applies to {{device.name}} {{device.version}}.

## Out of Scope 

This CSCR does not cover use or trials outside of GSTT CSC MLOps and AIDE environment or performed by other teams and
institutions.

## Roles and Responsibilities 

| Role                    | Responsibilities |
|-------------------------|------------------|
| Clinical Safety Officer |                  |
| Clinical Lead           |                  |
| Development Lead        |                  |

## Definitions

| Term   | Definition                     |
|--------|--------------------------------|
| SRS    | Software Requirements Spec     |
| SDS    | Software Design Spec           |
| CSCR   | Clinical Safety CAse Report    |
| CRMP   | Clinical Risk Management Plans | 
| SWIFT  | Structure What If              |


## Executive Statement

_Summary of the Clinical Safety Case Report findings and outcomes. This may include the purpose of the report, clinical context, summary of high value risks identified and their mitigations and any key findings and conclusions. This section should not go into detail but provide an overall summary of the report._

| Initial | Residual | Risk Rating | Definition                                                                                                                                                                              |
|---------|----------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|         |          | 5           | Unacceptable level of risk. Mandatory elimination or control to reduce risk to an acceptable level                                                                                      |
|         |          | 4           | Unacceptable level of risk. Mandatory elimination or control to reduce risk to an acceptable level                                                                                      |
|         |          | 3           | Undesirable level of risk. Attempts should be made to eliminate or control to reduce risk to an acceptable level.  Shall only be acceptable when further risk reduction is impractical. |
|         |          | 2           | Acceptable where cost of further reduction outweighs benefits gained.                                                                                                                   |
|         |          | 1           | Acceptable, no further action required                                                                                                                                                  |


## Introduction

_Purpose of the Clinical Safety Case Report and phase of lifecycle it relates to._

## System Definition / Overview

_Description of the Health IT System; identification of Health IT System part and version number; description of the 
clinical environment it is to be used in; description of any existing systems it replaces or interfaces with; number of
users and patients._

## Clinical Risk Management System
_Description of the Manufacturer’s clinical risk management system; identification of key personnel, their roles and 
responsibilities; identification of clinical risk management governance structure._

The clinical risk management system is described in the Clinical Risk Management Plan document, which follows DBC0129
[1]. The clinical safety case has been developed in accordance with the CSC QMS [2].

Clinical safety activities have been undertaken by the CSC team under the supervision and with collaboration with 
the CSO. Persons responsible for this process are listed at the start of this CSCR.

## Medical Device Declaration

The {{device.name}} application has a Class {{device.mhra_class}} MHRA classification.   

[Guidance for MHRA classification](https://ec.europa.eu/docsroom/documents/10337/attachments/1/translations)


## Clinical Risk Analysis
_Hazard identification; description of patient safety consequences; explanation of hazard causes and contributory 
conditions; identification of existing mitigating controls; estimation of clinical risk; identification of participating
personnel._

Risk analysis methods are explained in the Clinical Risk Management Plan.

Hazard identification, risk evaluation and risk control meetings were conducted with key stakeholders throughout the
design and development stages.

## Clinical Risk Evaluation
_Evaluation of initial level of risk of each identified hazard using pre-defined criteria._

Risks are evaluated against the severity and likelihood scales in appendix 1, taken from DCB 0129.


## Clinical Risk Control
_Identification, justification, implementation and verification of adequate risk controls; residual clinical risk 
evaluation and completion of controls._ 

The risk controls identified against causes for risks which are evaluated as un-acceptable in the risk acceptability 
chart in Appendix 2.



## Hazard Log
The hazard log is available at <a href="documentation/release/hazard_log.md">release/hazard_log.md</a>

## Test Issues
Summary of any outstanding test issues and the impact on clinical safety.

## Summary Safety Statement
Statement from the Clinical Safety Officer summarising the safety position of the Health IT System in the context of 
the intended deployment. 

## Quality Assurance and Document Approval
Evidence of appropriate quality, review and approval regimes.

## Configuration Control / Management
Evidence of appropriate configuration control being used.


## References

- [1] DCB 0129
- [2] DCB 0160
- [3] ISO 14971:2019

---
## Appendices

### Appendix 1

#### Likelihood 


| Likelihood | Interpretation                                                                       |
|------------|--------------------------------------------------------------------------------------|
| Very High  | Certain or almost certain; highly likely to occur                                    |
| High       | Not certain but very possible; reasonably expected to occur in the majority of cases |
| Medium     | Possible                                                                             |
| Low        | Could occur but in the great majority of occasions will not                          |
| Very Low   | Negligible or nearly negligible possibility of occurring                             |


#### Severity 


| Severity classification | Interpretation                                                                                                                                                                                                                       | Number of patients affected |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| Catastrophic            | Death <br><br> Permanent life-changing incapacity and any condition for which the prognosis is death or permanent life-changing incapacity; severe injury or severe incapacity from which recovery is not expected in the short term | Multiple                    |
| Major                   | Death <br><br> Permanent life-changing incapacity and any condition for which the prognosis is death or permanent life-changing incapacity; severe injury or severe incapacity from which recovery is not expected in the short term | Single                      |
| Major                   | Severe injury or severe incapacity from which recovery is expected in the short term <br><br> Severe psychological trauma                                                                                                            | Multiple                    |
| Considerable            | Severe injury or severe incapacity from which recovery is expected in the short  <br><br> Severe psychological trauma                                                                                                                | Single                      |
| Considerable            | Minor injury or injuries from which recovery is not expected in the short term.<br><br>Significant psychological trauma                                                                                                              | Multiple                    |
| Significant             | Minor injury or injuries from which recovery is not expected in the short term.<br><br> Significant psychological trauma                                                                                                             | Single                      |
| Significant             | Minor injury from which recovery is expected in the short term <br><br> Minor psychological upset; inconvenience                                                                                                                     | Multiple                    |
| Minor                   | Minor injury from which recovery is expected in the short term; minor psychological upset; inconvenience; any negligible severity                                                                                                    | Single                      |

### Appendix 2 

#### Risk Calculation


| Likelihood   |           |                |                  |           |                  |
|--------------|-----------|----------------|------------------|-----------|------------------|
| _Very High_  | 3         | 4              | 4                | 5         | 5                |
| _High_       | 2         | 3              | 3                | 4         | 5                |
| _Medium_     | 2         | 2              | 3                | 3         | 4                |
| _Low_        | 1         | 2              | 2                | 3         | 4                |
| _Very Low_   | 1         | 1              | 2                | 2         | 3                |
| **Severity** | _Minor_   | _Significant_  | _Considerable_   | _Major_   | _Catastrophic_   |


#### Risk acceptability matrix 

| Risk Level | Comment                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5          | Unacceptable level of risk <br> Mandatory elimination of hazard or addition of control measure to reduce risk to an acceptable level                                                                                        |
| 4          | Unacceptable level of risk <br> Mandatory elimination of hazard or addition of control measure to reduce risk to an acceptable level                                                                                        |
| 3          | Undesirable level of risk <br> Attempts should be made to eliminate the hazard or implement control measures to reduce risk to an acceptable level. <br>Shall only be acceptable when further risk reduction is impractical |
| 2          | Acceptable where cost of further reduction outweighs benefits gained or where further risk reduction is impractical                                                                                                         |
| 1          | Acceptable, no further action required                                                                                                                                                                                      |
