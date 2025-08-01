---
qms_version: 2.2.0
sop_id: CSC PR.002
sop_version: 2.0.1
template_id: CSC F.009
template_version: 2.0.1
record_version: 
record_id: CRMP-001
title: Clinical Risk Management Plan
---

# Clinical Risk Management Plan

## General

|                           |              |
|---------------------------|--------------|
| **Template ID**           | CSC F.009    |
| **Template Version**      | 2.0.1        |
| **QMS Version**           | 2.2.0        |
| **SOP ID**                | CSC PR.002   |
| **SOP Version**           | 2.0.1        |
| **Regulatory References** |              |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |

## Scope

This document applies to the {{device.name}} version {{device.version}}. 

## Purpose

This purpose of this document is to describe the activities involved in the clinical risk management process

This document is meant to be read and agreed-upon by the project owners, the CSC team, and the Clinical Safety
Officer (CSO) during design and development.

The document also provides traceability for risk controls throughout the project.

## Roles and Responsibilities 

| Role                          | Responsibilities                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------|
| Development Lead              | - Completing documentation <br>  - Gathering requirements <br >- Organising meetings with stakeholders |
| Clinical Lead                 | - Organising meetings with stakeholders <br>  - Providing requirements                                 |
| Clinical Safety Officer (CSO) | - Final approval of clinical risk management activities.                                               |

## Related documents

| Document Title                   | ID       |
|----------------------------------|----------|
| Hazard Log                       | HZ-001   |
| Clinical Safety Case Report      | CSCR-001 |
| Verification and Validation Plan | VVP-001  |


## Definitions

| Term | Definition                    |
|------|-------------------------------|
| CRMF | Clinical Risk Management File |
| CRMP | Clinical Risk Management Plan |
| CSCR | Clinical Safety Case Report   |


## Introduction

The Clinical Risk Management Plan (CRMP) contains the risk policy and defines the criteria for risk acceptance. It also 
refers to relevant QMS processes and activities which will be conducted for application-specific risk management as part
of the software development process. 

### Impact of DCB0129 and DCB0160 on the project 

Since the CSC department will be both the Manufacturer and user of the software, the project will therefore adhere to 
all applicable requirements of DCB0129 and DCB0160 in this regard.
---

## Activities 

Activities will be followed according to the protocol "CSC.PR.002 Clinical Risk Management System SOP"

#### Schedule and Activities Logging

Meetings for CRM activities will have a dedicated agenda sent to all participating stakeholders prior to the event. 

The agenda and meeting notes will be logged within the project repository as an issue with a CRM tag. 

CRM meetings will be scheduled at key milestones in the software development process to revise the hazard log:
- Generation of the initial hazard log 
- Updating hazard log during development
- Approval of the Clinical safety case report 
- in lieu of clinical evaluation results and learnings

#### Stakeholder Engagement 

The follow stakeholders will be consulted hazard identification and risks assessment. 

| Name | Role |
|------|------|
|      |      |
|      |      |

---

### Hazard identification

The hazard identification technique will be used to list the hazards involved in the clinical pathway because of 
the proposed application. A "fish-bone" diagram for each hazard will be created to analyse the sources of the associated
risks. 

All hazards, risk analyses and evaluation will be recorded in the hazard log. 

#### Severity of risk

Severity classification table:

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


#### Likelihood of risk 

Likelihood classification table:

| Likelihood | Interpretation                                                                       |
|------------|--------------------------------------------------------------------------------------|
| Very High  | Certain or almost certain; highly likely to occur                                    |
| High       | Not certain but very possible; reasonably expected to occur in the majority of cases |
| Medium     | Possible                                                                             |
| Low        | Could occur but in the great majority of occasions will not                          |
| Very Low   | Negligible or nearly negligible possibility of occurring                             |

### Assessment of Risk

| Likelihood   |           |                |                  |           |                  |
|--------------|-----------|----------------|------------------|-----------|------------------|
| _Very High_  | 3         | 4              | 4                | 5         | 5                |
| _High_       | 2         | 3              | 3                | 4         | 5                |
| _Medium_     | 2         | 2              | 3                | 3         | 4                |
| _Low_        | 1         | 2              | 2                | 3         | 4                |
| _Very Low_   | 1         | 1              | 2                | 2         | 3                |
| **Severity** | _Minor_   | _Significant_  | _Considerable_   | _Major_   | _Catastrophic_   |


### Risk Acceptability 

Table X described the acceptability of estimated risks

| Risk Level | Comment                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5          | Unacceptable level of risk <br> Mandatory elimination of hazard or addition of control measure to reduce risk to an acceptable level                                                                                        |
| 4          | Unacceptable level of risk <br> Mandatory elimination of hazard or addition of control measure to reduce risk to an acceptable level                                                                                        |   
| 3          | Undesirable level of risk <br> Attempts should be made to eliminate the hazard or implement control measures to reduce risk to an acceptable level. <br>Shall only be acceptable when further risk reduction is impractical |
| 2          | Acceptable where cost of further reduction outweighs benefits gained or where further risk reduction is impractical                                                                                                         |
| 1          | Acceptable, no further action required                                                                                                                                                                                      |


### Risk Controls
<!-- [13485:7.2.1a]-->

Where risks exceed the acceptable level, risk controls will be implemented to reduced/remove likelihood of the causes of
the hazard occurring. Risks controls will be reflected a new system requirement item and system design item if not 
already represented. The effectiveness of each risk control with be verified with a unit test or a manual validation 
test. 

### Evaluation of overall residual risk

The residual risks after risk controls are applied will be calculated. If the residual risk remains the higher than the
acceptable risk level, further risks controls will be applied until it become unreasonably burdensome to do so, upon 
which a decisions will be made with the CSO to accept the risk.

### Risk Management Review

When the application development has finished and the clinical investigation has concluded without any further 
amendments to the Hazard Log, a Clinical Safety Case report will be approved by CSO. 

### Deployment and Post-Deployment Activities
<!-- [13485:7.2.1a]-->

During and after deployment the hazard log will be updated in response to incidents, near misses and post deployment
surveillance activities. 



