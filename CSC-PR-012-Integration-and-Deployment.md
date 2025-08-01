---
qms_version: 2.2.0
sop_version: 2.0.2
---

# Software Deployment SOP
<!-- [13485:7.2.1a,7.3.4b]-->

## General

|                           |                              |
|---------------------------|------------------------------|
| **Document ID**           | CSC PR.012                   |
| **Document Version**      | 2.0.2                        |
| **Author**                |  |
| **Approval**              |                  |
| **QMS Version**           | 2.2.0                        |
| **Regulatory References** |                              |

## Purpose

This document describes the processes for integration and deployment of clinical software within GSTT.

## Scope

This procedure must be followed during the integration and deployment of all CSC projects which directly affect patient care or interact with clinical systems.

## Definitions

| Acronym | Definition                    |
| ------- | ----------------------------- |
| CSC     | Clinical Scientific Computing |
| UAT     | End-user Acceptance Testing   |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate training to perform the role.

| Role                    | Description                               | Responsibility                                                                                                                  |
| ----------------------- | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Software Owner          | Head of Department                        | Approves software deployment, takes responsibility for clinical risk of deployed software                                       |
| Software Developer      | Development Lead                          | Provides software technical support and training during the deployment process                                                  |
| Clinical Lead           | Clinician                                 | Approves software deployment, approves clinical safety case report, takes responsibility for clinical risk of deployed software |
| Clinical Safety Officer | Clinician                                 | Provides expertise and leadership in all activities associated with the evaluation of clinical risk management for the product. |
| Software End-users      | Clinical users, technical support, others | Receive training to use software, perform UAT, use the deployed software                                                        |

## 1. Introduction

Once sufficient testing and validation of the software has been performed, the software can be deployed into the clinical setting for its intended use. The software will affect clinical systems and potentially the clinical diagnosis and clinical treatment of patients, therefore a robust deployment procedure will ensure safety, drive adoption and continued usage.

The term _deployment_ denotes the process of making new software available to the end users. This includes installation, acceptance testing, user training and initial performance monitoring.

Following deployment, all CSC projects are subject to continuous monitoring and surveillance. This document describes deployment activities. CSC-PR-005 describes post-deployment activities.

## 2. Procedure
<!-- [13485:8.2.6]-->

The deployment of a software solution must follow a Deployment Plan which describes the schedule of deployment activities. The Deployment Plan must be discussed by all stakeholders and agreed upon in advance of the software deployment.

### 2.1 Deployment Plan Overview

The Deployment Plan should include the following activities and the anticipated completion dates of each activity:

- Software and system requirement fulfillment checks
- Deployment timeline agreement
- Software end-user training
- Software installation
- Software end-user acceptance testing
- Risk mitigation
- Documentation
- Sign-off

The Deployment Plan should be revised if any activities reveal problems which must be resolved before deployment can be completed.

## 3. Deployment Plan Activities
<!-- [13485:6.3a]-->

### 3.1 Fulfillment of Software & System Requirements

The end-users must check that the software solution proposed for deployment meets the original software requirements. The end-users must ensure that the system requirements
(e.g.: hardware, networking infrastructure) meet the specification agreed for the software solution to be performant.

Once the stakeholders have agreed that the software and wider system requirements are fulfilled, the software developers should create a "Release" version of the software
(e.g.: in the Release section on GitHub), which will be used for deployment. The software developers should update any relevant files or code to reflect the
version number of the Release.

### 3.2 Deployment Timeline Agreement

All stakeholders should agree upon the timeline during which the software solution will be deployed.

### 3.3 Software End-user Training
<!-- [13485:7.2.dc,7.2.2d]-->

All software end-users should undergo training to ensure that they can effectively use the deployed software. Each end-user who attends a training session must sign
an attendance sheet, which should be made available to the Head of Department or an appropriate line manager. If in-person training is infeasible, virtual training can
be provided instead. In the event of virtual training, the session(s) should be recorded.

Roles should be assigned appropriately to end-users (e.g.: Software Administrator, Clinical User, etc.) and appropriate system permissions should be granted to those users.

Feedback communication channels should be identified to end-users during training (e.g.: GitHub Issues, email, etc.) and software developers should ensure those channels
have been arranged and opened.

The Head of Department head or line manager of the end-users group are responsible for ensuring that end-users are appropriately trained to use the software solution in clinical practice.

The CSC development leads are must be involved in training the end users in correct use of the applications. User 
instructions and training materials such as presentations, and questionnaire must also be provided by development lead.

Training is different for each application depending on complexity but may include: 
- presentation slides with screenshots
- training that is appropriate for the role e.g. routine users vs admins
- examples of normal use
- expected misuse and what not to do
- troubleshooting and interpreting common error messages
- time frames after which to escalate issues
- communication channels for escalating issues


### 3.4 Software Installation

All relevant stakeholders (including the CSC team, CSO, Head of Department, Clinical Lead, Trust IT where applicable) should agree upon the date that the software solution
will be deployed to the end-user systems and how the software will be installed (e.g.: in-person, remotely).

### 3.5 Software End-user Acceptance Testing

End-users should devise a set of tests to verify that the installed software solution performs according to the software and system requirements
and to ensure that any risk controls have been implemented. End-users should arrange a period of time during which to perform the End-user Acceptance
Testing (UAT) of the deployed software solution.

All unit and integration tests should pass when the software solution is executed on the end-user systems. All risk controls arising from the Clinical Risk Management
process should pass their associated verification and validation tests, or undergo manual validation at UAT where applicable. End-users should provide feedback to the
software developers if any tests fail. The software developers should act upon any failures, such as by updating the software and releasing a new version. The process
of making changes to the software should follow the CSC PR.012 Change Management SOP.
The end-users should repeat the tests until all tests are passed successfully. All SOUP validation should be evaluated and approved.

As part of the UAT process, a Clinical Safety Case Report must be generated and approved by the CSO.

### 3.6 Documentation



All documentation relevant to the software solution should be made available to the end-users. This includes, but is not limited to: software manuals,
training documentation, clinical risk management file (approved by CSO), completed surveillance and monitoring plan for continuous use of the software.

**MDR compliance** - The following documentation needs to be readily available upon request by the MHRA/CQC/notifiable bodies via the README of the repository:

- the name and address of the manufacturing health institution;
- the details necessary to identify the devices;
- a declaration that the devices meet the general safety and performance requirements under ANNEX 1 of MDR 2002 as applicable.
- the documentation specified in Annex 1 of MDR 2002 as applicable.

### 3.7 Sign-off

Once the activities described above (in section 3) have been completed, the software solution can be approved and signed-off by the Software Owner and the Clinical Lead.
Once sign-off is performed, the software solution can be used for clinical purposes.

## 4. Post-deployment Surveillance and Monitoring

After the software solution has been deployed, the ongoing performance of the software must be surveilled, monitored and audited annually to ensure the continued
appropriateness and safe operation of the software solution (see: CSC-PR-005).

## 5. Communication through Field Safety Notices

The CSC department will issue Field Safety Notices to communicate to the host department any information or required actions
for the deployed application regarding:

- Concerns for the use of the application
- Modification of deployed application and how it affects functionality
- Removal from routine clinical use

Field Safety Notices will be sent via GSTT Trust Email to the Head of Department and to any other responsible persons
nominated during deployment activities. Records of Field Safety Notices will be kept in the Project Repository.
