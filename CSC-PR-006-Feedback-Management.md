---
qms_version: 2.2.0
sop_version: 2.0.2
---

# SOP Feedback Management
<!-- [13485:8.2.1,8.2.2,8.2.2f]-->

## General

|                           |                                                                     |
|---------------------------|---------------------------------------------------------------------|
| **Document ID**           | CSC PR.006                                                          |
| **Document Version**      | 2.0.1                                                               |
| **Author**                |                                                      |
| **Approval**              |                                                         |
| **QMS Version**           | 2.2.0                                                               |
| **Regulatory References** | ISO 13485:2016 Sec. 8.2.1 and 8.2.2 </br> IEC 62304:2006 Sec. 6.2.1 |

## Purpose

This SOP describes how to respond to feedback and complaints.

## Scope

The processes in this document must be followed for all computing projects where the end-user provides feedback about the 
software, requests a change to the software or makes a complaint related to the software.

## Definitions
| Acronym  | Definition                                                                                        |
|----------|---------------------------------------------------------------------------------------------------|
| CSC      | **Clinical Scientific Computing**                                                                 |
| ML       | **Machine Learning**                                                                              |
| AI       | **Artificial Intelligence**                                                                       |
| PR       | **Pull Request** (on GitHub)                                                                      |
| PACS     | **Picture Archiving and Communication System**                                                    |
| Ticket   | Feedback or compliant information recorded into a defined format. In the CSC this is completed via GitHub issues, with defined templates for each feedback type.                                  |
| Ticketing System   | The management system used for tickets. CSC uses GitHub issue management as the ticketing system.                                      |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training to fulfil the responsibilities.

| Role                    | Description        | Responsibility                                                                                                                 |
|-------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Software developer      | CSC Team Member    | Considers feedback and responds appropriately, either with further discourse or implementation of change to software           |
| Product/process owner   | Head of Department | Takes ultimate responsibility for decisions on feedback or complaints                                                          |


## General Considerations

### Support Availability

Software support is typically available between 9am–5pm, Monday–Friday, UK time. Feedback can be provided at any time
and processed according to priority.

### Feedback Channels

Feedback can be provided in the following ways:
* Raising an Issue on the corresponding CSC GitHub repository
* Contacting the CSC Team via email: CSCTeam@gstt.nhs.uk
* Contacting one of the software developers via email – contact addresses of CSC Team Members are available on the CSC website.

### Feedback Prioritisation

Feedback, change requests and complaints should be assessed and prioritised as low-, medium- or high-priority.

All complaints should be considered high priority. 

### Feedback Classification
<!-- [13485:8.2.3]-->

All feedback is classified into one of the following categories. If the CSC Team is not sure how to
classify a ticket, it consults the QMO.

| Feedback Category                                              | Feedback Description                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Support Inquiry                                                | Any request for help that can be resolved by providing the end-user with (usability) information.                                                                                                                                                                                                                                                                                           |
| Change Request                                                 | Any request to add, modify or remove software functionalities.                                                                                                                                                                                                                                                                                                                              |
| End-User Complaint                                             | Any complaint that can be related to our products or organization and which is not classified as an "issue with potential negative influence on patient health".                                                                                                                                                                                                                            |
| Issue with potential negative influence on the state of health | Any end-user complaint related to:<br>problem with the medical device that could cause or may have caused or did in fact cause a death or serious deterioration in the state of health.<br>problem with the medical device that significantly impaired the performance criteria of the device (based e.g. on the information given in the intended use, user manual or marketing material). |
| Data Privacy Inquiry                                           | Any request relating patient sensitive data used within a piece of software (e.g.: personal medical images used in a ML application, patient data contained in an spreadsheet.)                                                                                                                                                                                                             |

| Serious Deterioration of the State of Health                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A serious deterioration of the state of health includes at least one of the following:<br>life-threatening illness,<br>permanent impairment of a body function or permanent damage to a body structure,<br>a condition which requires medical or surgical intervention to prevent one of the above,<br>any indirect harm as a consequence of an incorrect diagnostic result when used within manufacturer's instructions for use. |

## Process Steps
<!-- [13485:7.2.3c]-->

### 1. Documentation of Feedback
<!-- [13485:8.2.2a]-->

The CSC Team receives feedback through a feedback channel. Based on the Feedback received, the CSC Team 
member then documents at minimum the following information, if it has not already been automatically documented (i.e.: 
as an Issue on GitHub):

* Date of feedback
* Description of the issue (e.g. software version, runtime environment, operating system, if available: screenshots / images)
* Affected users, contact details and user locations
* Steps to reproduce the problem

| Participants    |
|-----------------|
| CSC Team        |

| Input                         | Output                                                |
|-------------------------------|-------------------------------------------------------|
| Received feedback / complaint | Structured documentation of feedback in ticket system |


### 2. Evaluation of Feedback
<!-- [13485:8.2.2b]-->

The CSC Team classifies the feedback according to the categories outlined in the General Considerations section
of this process. The CSC Team assess the priority of the feedback (low/medium/high). Depending on the feedback 
category it takes respective actions:

**Support Inquiry:**

The CSC Team actively supports the end-user in solving the issue by answering questions or
providing additional user training.

**Change Request:**

The feedback is escalated to the rest of the team to discuss implementation and potentially initiate the change management process.

**Complaint:**

* If the end-user complaint constitutes a persistent problem related to the software that cannot be
  resolved by providing user information or training (e.g. software bugs), it is forwarded to the CSC Team
  to initiate the problem resolution process.
* If the end-user complaint is related to an organizational issue (e.g. if it involves the Radiology team or the PACS team), the
  CSC Team involves other teams within the organization where necessary to provide the user with
  a satisfactory response.
* If the end-user complaint may constitute a systematic issue, the feedback is additionally forwarded to the
  Quality Management Officer (QMO) to initiate the process for corrective and preventive actions (CAPA). The CAPA process is detailed in CSC-PR-016-Corrective-and-Preventive-Action.md.  

**Data Privacy Inquiry:**

* **If the feedback related to a data privacy enquiry regarding the QMS,** the QMO must respond with information on the safety controls implemented in GitHub, e.g. Githooks, Staff training, Separation of code and data.
* **If the feedback is related to a particular app,** the QMO or a QR must respond via email to user to ensure privacy on this subject.
  * For presence of a patient in Training data - the XNAT anonymisation script can be explained
  * For National Data OptOut (NDO), the Head of CSC will instigate a dataset removal process.
* All data handling conforms to GSTT internal practices and should have direct traceability to relevant permissions. QMO/QR can provide details on the approvals where queried

**Issue with a Potential Negative Impact on the State of Health:**

All issues with a potential negative impact on the state of health must be reported immediately, but no later
than on the same day, to the Medical Device Safety Officer. 

All product-related feedback shall be checked for a potential impact on the risk management file or product requirements
of the respective device and shall be taken into consideration for device post-market surveillance.

**No Further Action:** 

Where the feedback analysis results in no further action required on behalf of the CSC team, the CSC staff member will 
inform the user who submitting the complaint of the reason why no further action will be taken and that the ticket will
be closed. 

Where responsibility for the cause of the feedback lies with an external party, the CSC team will share relevant information 
with the third party, within GDPR rules. 


| Participants    |
|-----------------|
| CSC Team        |

| Input               | Output                                      |
|---------------------|---------------------------------------------|
| Documented feedback | Classified feedback and decision on actions |

### 3. Validation of Actions
<!-- [13485:7.2.2b]-->

If the feedback is requires a bug fix or leads to a change request, the change should be actioned by following the
CSC PR.021 Change Management SOP. 

The CSC Team proactively receives updates regarding the status of actions per ticket from other teams.

Once the actions are considered completed (e.g. for change requests: decision to implement a feature or not is
made), the CSC Team informs the user and validates if the actions taken are resolved to the user's satisfaction. 
If so, the validation is documented in the ticket, and the ticket is closed. If not, this process is re-initiated.

If the end-user does not respond, validation is tried at least a second time before the ticket is closed.



| Participants    |
|-----------------|
| CSC Team        |

| Input               | Output                                  |
|---------------------|-----------------------------------------|
| Implemented actions | Validation of actions, ticket is closed |

> Optionally, depending on the features that your ticket system provides, consider adding a process step to
> assign each ticket a status (open, pending input, closed).

---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
