---
qms_version: 2.2.0
sop_version: 2.0.3
---

# SOP Change Management
<!-- [13485:4.1.4c,7.2.3d,7.3.2e,7.3.9,8.2.2f] -->

## General

|                           |                                                                                                                         |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Document ID**           | CSC PR.021                                                                                                              |
| **Document Version**      | 2.0.3                                                                                                                   |
| **Author**                |                                                                                                            |
| **Approval**              |                                                                                                             |
| **QMS Version**           | 2.2.0                                                                                                                   |
| **Regulatory References** | **ISO 13485:2016** <br> 7.3.9 <br><br> **BS EN 62304:2006** <br> 6.2.3/4/5 <br> 6.3.1/2 <br> 7.4.1/2/3 <br> 8.2.1/2/3/4 |

## Purpose

This SOP describes how to manage changes to the design and development of SaMD produced by the CSC Team.

## Scope

The processes in this document must be followed for all computing projects where requests for changes to the software 
need to be actioned.

## Definitions
| Acronym | Definition                                         |
|---------|----------------------------------------------------|
| CSC     | **Clinical Scientific Computing**                  |
| ML      | **Machine Learning**                               |
| AI      | **Artificial Intelligence**                        |
| PR      | **Pull Request** (on GitHub)                       |
| MHRA    | **Medicines and Healthcare Regulatory Authority**  |
| CQC     | **Care Quality Commission**                        |
| CRM     | **Clinical Risk Management**                       |


## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training to fulfil the responsibilities.

| Role                    | Description              | Responsibility                                                      |
|-------------------------|--------------------------|---------------------------------------------------------------------|
| Development Lead        | CSC Team Member          | Manage the implementation and review of the changes to the project |
| Product/process owner   | Head of Department       | Takes ultimate responsibility for the implemented changes               |
| Clinical Safety Officer | Clinician trained in CRM | Assess the clinical risk as a result of changes to the software     |


## 1. Control of Design and Development Changes
<!-- [13485:7.5.6a]-->

### 1.1 Scenarios for changes
Changes may be required at different stages of the software development lifecycle. Such situations can include:
- where additional risks and risk controls are identified during development
- where requirements are added during the development
- where validation tests fail
- where user acceptance testing fails 
- where features are requested after deployment 
- where a reportable incident that affects patient health occurs after deployment



### 1.2 Change review
<!-- [13485:4.1.4a,4.1.4b] -->

The proposed change must be reviewed to gain a thorough understanding of the impact on the software's function, 
performance, and usability.

Where change requests are bug fixes, these should be prioritised and completed without delay. 

Change requests that are not bug fixes must be evaluated against whether it:
- is a substantial change, and technically feasible
- introduces new risks, and whether these are acceptable
- impacts existing risk control measures
- makes sense in the context of the software use cases, and the CSC department aims.
- requires any additional regulatory considerations, such as changing the
MHRA medical device classification, or the software classification under BS EN 62304:2016.

Furthermore, significant changes may require alerting a notified body. The MDF4900 form must be completed and sent to
the notified body, where contact details are available from the QMO.

| MDF4900 Template | <a href=records/notified-body-comms/MDF4900-Change-Notification-and-Work-Authorisation-Form.pdf>Document Link |
|------------------|---------------------------------------------------------------------------------------------------------------|

Significant changes include, but are not limited to:
- The change puts the QMS out of scope written on Certificate AND in the CSC PL.001 Quality Manual e.g.
developing AI product which is not text or imaging based - like audio/ ECG / Genomics / etc
- The change makes additional clauses applicable which were previously non applicable, as stated in the CSC PL.001 
Quality Manual.
- The change makes the developed software a Class 3 SaMD, would require significant additional safety considerations 
and alerting the notified body.
- There are changes to the ISO13485 Standard itself, all projects and documentation should be reviewed and alert the 
notified body for reassessment.
- There are changes to the implementation of UKMDR - under which NHS hospitals must adhere to.


### 1.3 Logging and tracking changes

Changes should initially be raised as an issue against the GitHub repository of the application to start the 
conversation around the considerations above.
- The original change request/issue should be linked in GitHub where applicable to ensure traceability. 
- Once the change has been confirmed with the Clinical Lead it should be added as a new item
in the system requirements specification, stating the date added as well.
- In the cases where a change means that a requirement must be amended, this change must be logged and dated in the
system requirements specification to ensure full traceability.
- The hazard log must also be updated if any risks are identified as a result of the change, and risk controls that
mitigate the risks must be implemented. 

### 1.4 Change validation and verification

- Additional requirements must follow the normal development process, which includes adding an item to the 
design specification. A unit test must be created to verify the design spec item has been implements. Where this is not
possible a validation test must be added.

- Additional risk controls raised from this change must also be verified and validated.

### 1.5 Change approval and release
<!-- [13485:7.5.6g]-->


- If the change is implemented before the software has been first deployed, the approval process follows the normal
process described in CSC PR.012 Integration and Deployment, where the unit tests and validations tests are approved as
part of the user acceptance criteria, and the Clinical Safety Report is approved by the CSO.

- If actioned after initial deployment, the change will be deployed as a new release, or part of a new release 
containing multiple changes. Table 1. below shows what constitutes to particular release types. 

- If the system requirements specification has been amended, then all previous and new unit tests and validation tests
must pass before deploying the new release. Where additional risks have been introduced by the change or risk controls 
have been analysed for residual risks, these must be approved by the CSO prior to release. 

Guidance on how to make a release can be found in CSC PR.025 Software Release Guidelines SOP.

_Table 1. Types of software releases._

| Release       | Description                                                                                                                       | Version Increment |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------|-------------------|
| Bug fixes     | includes bugs/corrections identified at verification/validation/user acceptance testing stages of deployment of major released.   | 1.0.1             |
| Minor Changes | Includes minor fixes, additional safety checks                                                                                    | 1.1.0             |
| Major changes | Additional feature/new functionality. Major re-write or changes to critical code. Corrections as a result of reportable incidents | 2.0.0             |


## References
