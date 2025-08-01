---
qms_version: 2.2.0
sop_version: 2.0.3
---

# Corrective and Preventive Action (CAPA)
<!-- [13485:8.2.2f,8.5.2,8.5.3]-->

## General

|                           |                                            |
|---------------------------|--------------------------------------------|
| **Document Id**           | CSC PR.016                                 |
| **Document Version**      | 2.0.3                                      |
| **Author**                |                            |
| **Approver**              |                                |
| **QMS Version**           | 2.2.0                                      |
| **Regulatory references** | ISO 13485:2016 Section 8.5.1, 8.5.2, 8.5.3 |

## Purpose
This SOP describes how CAPAs are implemented and tracked.

## Scope
Covers all corrective and prevention actions in management of this QMS and all projects currently and previously 
undertaken within this QMS.

## Definitions

| Acronym | Definition                           |
|---------|--------------------------------------|
| CAPA    | **Corrective and Preventive Action** |
| QMO     | **Quality Management Officer**       |
| QR      | **Quality Representative**           |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training to perform the role.

| Role                     | Description               | Responsibility                                                                                                                 |
|--------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Clinical Safety Officer  | Clinician                 | Provide expertise and leadership in all activities associated with the evaluation of clinical risk management for the product. |
| Product  owner           | Head of Department        | Takes ultimate responsibility for deployed product                                                                             |
| QMO                      | Head of CSC Department    | Quality management officer co-ordinates CAPA activities relating to the QMS                                                    |
| QR                       | Member of CSC Department  | Quality representative co-ordinates CAPA activities relating to the QMS on QMO's behalf if the QMO is not available to do so   |


## Process Steps

### 1. Input for CAPA
<!-- [13485:8.2.1,8.5.2a]-->

Various events may lead to creation of CAPA. Examples include:

 * Product or QMS non-conformities.
 * Failures in CSC systems, e.g. XNAT, Head Node administration.
 * Customer complaints.
 * Internal bug reports, e.g. by developers.
 * Audit findings.
 * Post-market surveillance findings, including trends.
 * Management review findings, including trends.

These inputs may be received from any person inside or outside the company. A CAPA should be triggered if the issue:
- affects patient safety.
- could cause regulatory non-compliance.
- is a repeat of other issues in the QMS, or applications developed under the QMS, representing a trend. 
  - A minimum of 3 similar issue reports would represent a trend and trigger a CAPA.  

The QMO has the ability to trigger a CAPA for any issue raised and may delegate this and any other QMO-specific
authorities to a QR if the QMO is unavailable to do so for any reason. In these cases, where actions and decisions are
specified to be taken by the QMO in the following sections, these can be performed by a QR in the QMO's stead.

The QMO is responsible for guiding these reporters to the appropriate CAPA input form and tracking its resolution.
Similarly, CAPAs are created and tracked using git issues. A GitHub issue template is provided at 
`./resources/.github/ISSUE_TEMPLATE/CAPA.yml` which can be copied into projects to serve as the template for raising 
CAPAs and tracking their resolution through Issues. The template contains the fields given in the example below.


| Participants |
|--------------|
| QMO          |

| Input                           | Output       |
|---------------------------------|--------------|
| Non-conformity, complaint, etc. | CAPA created |

### 2. Decision on Next Steps, Immediate Action
<!-- [13485:8.5.2a,8.5.2c,8.5.3b]-->

If immediate action is necessary (e.g. product recall, notification of authorities), the QMO consults the Medical 
Device Safety Officer.  Immediate action is carried out without undue delay (see ISO 13485 para. 8.5.2).

If changes are required as an immediate of preventative action, please follow CSC PR.021 Change Management protocol.

In any case, the QMO discusses the next steps with the person closest to the issue, e.g. for software bugs, the 
project's lead software developer.

| Participants                    |
|---------------------------------|
| QMO                             |
| Medical Device Safety Officer   |

| Input | Output                    |
|-------|---------------------------|
| CAPA  | CAPA, updated with action |

### 3. Root Cause Analysis
<!-- [13485:8.5.2b,8.5.3a]-->

The QMO coordinates a root cause analysis with the person closest to the issue. The preferred method for this
is "Five Whys". The result is added to the git issue.

| Participants                      |
|-----------------------------------|
| QMO                               |
| Other CSC team members (optional) |

| Input | Output                        |
|-------|-------------------------------|
| CAPA  | CAPA, updated with root cause |

### 4. Risk assessment

A risk assessment should be completed to ensure the actions do not introduce additional risks, such as: 
- non-compliance with the applicable standards and regulations
- patient safety
- data integrity and security
- undue delays to development and production

Significant risks should be mitigated to minimise impact and likelihood by including additional actions to the CAPA, 
if required.


### 5. Timeframes for completion 

The time frames within which to complete CAPAs are set by the QMO based on criticality and reviewed regularly at the
bi-weekly CSC team 'stand-up' meetings. 

### 6. Implementation of Action
<!-- [13485:8.5.2d,8.5.3c]-->

The QMO coordinates defining and implementing corrective and preventive action. Additionally, the QMO takes
into account adverse negative implications and verifies that the actions do not adversely affect the ability
to meet applicable regulatory requirements or the safety and performance of the medical device. Actions and outcomes are
documented in the GitHub issue.

Actions may include:
- Updates to QMS documentation, or application documentation.
- Change in code.
- Review of data used in project development. 
- Review of training logs, implementation of additional training/retraining. 

Actions should be commenced without undue delay. 

If changes are required to the application developed by the CSC team, then this should follow the CSC PR.021 Change 
Management SOP. If changes to the software are out of the current scope of the QMS as per the CSC PL.001 Quality Manual and are deemed significant, the notified body shall be contacted.

The QMO assigns a quality representative to complete CAPA actions, with additional CSC team members or resources as 
required. 

Where a CQC/MHRA reportable incident has occurred and a CAPA is raised as a result, the timeline for completion of CAPA
activities is defined by CQC/MHRA reportable incident schedule. All other CAPAs should be resolved timeframes set by the
QMO or person the QMO has designated responsibility for the issue. 

| Participants                        |
|-------------------------------------|
| QMO                                 |
| Other CSC team members (optional)   |

| Input | Output                         |
|-------|--------------------------------|
| CAPA  | CAPA, updated with action plan |

### 7. Verification and Check of Effectiveness
<!-- [13485:5.4.2b,8.5.2e,8.5.2f,8.5.3d,8.5.3e] -->

The QMO conducts the verification and effectiveness review of the implemented action. These are defined as
below. Thereafter, the QMO resolves the CAPA issue.

* Verification: Documenting proof of implementation of actions taken.
* Effectiveness: Review of the effectiveness of actions taken.

| Participants |
|--------------|
| QMO          |

| Input | Output                                                             |
|-------|--------------------------------------------------------------------|
| CAPA  | CAPA, updated with verification, effectiveness review, closed date |

---



Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
