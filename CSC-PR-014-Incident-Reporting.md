---
qms_version: 2.2.0
sop_version: 2.0.2
---

# Incident Assessment SOP
<!-- [13485:8.2.3]-->

## General  

|                           |                              |
|---------------------------|------------------------------|
| **Document Id**           | CSC PR.014                   |
| **Document Version**      | 2.0.2                        |
| **Author**                |                   | 
| **Approval**              |                  |
| **QMS Version**           | 2.2.0                        |
| **Regulatory References** | ISO 13485:2016 Section 8.2.3 |


## Purpose

This SOP serves as a layout for how to report incidents and to assess whether the incident has had or could have a 
potentially negative impact on the state of health. 

## Scope

This SOP lays out the procedure to be followed to report incidents related to medical devices. 

## Definitions
| Acronym | Definition                                                                               |
|---------|------------------------------------------------------------------------------------------|
| CSC     | **Clinical Scientific Computing**                                                        |
| CQC     | **Care Quality Commission**                                                              |
| QMS     | **Quality Management System**                                                            |
| CAPA    | **Clinical and Product Assurance**                                                       |
| MDSO    | **Medical Device Safety Officer**                                                        |
| FSCA    | **Field Safety Corrective Actions**                                                      |
| MHRA    | **Medicines and Healthcare Regulatory Authority**                                        |
| DATIX   | Web based reporting and risk management software for health and social care institutions |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training to fulfil the responsibilities.

| Role            | Description                                  | Responsibility                                                            |
|-----------------|----------------------------------------------|---------------------------------------------------------------------------|
| QMO             | Head of Department or delegated staff member | Quality Management Officer manages the investigation of incidents.        |


## 1. Incident Reporting Actions
All incidents that occur as a result of the use of an application built under this quality management system must be 
reported to the CSC department by either:
* creating a new issue on the corresponding GitHub repository
 or
* emailing the CSC department on *********, where a member of the CSC team will create an issue on the GitHub repository

The CSC QMO team will then institute an internal report and fill the incident report template (CSC F.002) and then report the incident
to DATIX by filling out an IR1 form through the following link (on a Trust PC). 

- http://gti.gstt.local/services/healthsafety/health-safety-main-pages/i-am-interested-in/accidents-and-incidents-reporting.aspx

By reporting to DATIX an internal investigation will be prompted.

Once the incident report has been filled in, it must be stored in the sharepoint directory under /Policy/QMS/Incidents.
Once an incident is reported, the CAPA SOP should be followed to resolve the issue.
After the incident has been reported to DATIX, the QMO will update the GitHub issue with the links to the internal 
report and to the DATIX.

If a DATIX is reported against the CSC department that relates to an application built under this QMS, the QMO will complete an 
incident report and start an internal investigation and a CAPA. An issue must be logged in the against the project in 
the relevant GitHub repository.


## 2. Incident Assessment Framework

The following sections describe how to fill in the incident report template.
The incident report must accompany the GitHub issue. The report will contain the DATIX report ID, 
date of incident and incident description which will need to follow the guidelines below. 
The following criteria are based on the MEDDEV 2.12/1 rev. 8 guidance document. Any event which meets **all
three criteria listed below** is considered an incident and must be reported to the competent national
authorities. The following criteria can be also used to document appropriately why an event is not to be considered a 
reportable incident.

### 2.1 General Event Description and Occurrence

**Criterion**: *An event has occurred that could be considered a reportable incident.*

The incident report template section: "General Event Description and Occurrence"  needs to be filled in if an event has 
occurred that could be considered a reportable incident. For examples of possible event categories see MEDDEV 2.12/1 
rev. 8 guidance. The incident assessment must also consider information resulting from testing, reading the instructions
for use or scientific data that indicate implications.

### 2.2 Relationship Between the Device and Event

**Criterion**: *A (direct or indirect) causal relationship is suspected between the device and the event.*

In the section "Relationship Between the Device and Event" of the incident report template the person reporting the 
incident needs to describe if there is a direct or indirect causal relationship between the device and the event.
When assessing the relationship between the device and event the QMO/CSC team member must take the following points into 
consideration:*

* *the opinion of subject-matter-experts (e.g. physicians)*
* *the QMO/CSC team members' assessment;*
* *previous / similar events and incidents*

From a risk management perspective, this decision should be made conservatively, i.e. if the situation is
complex and/or potentially caused by multiple medical devices, the MDSO should have a tendency to
assess this as "applicable" even if the matter still remains unclear.*

### 2.3 Event Outcomes

**Criterion**: *The event led, or might have led, to one of the following outcomes:*
- *death of a patient, user or other person*
- *serious deterioration in state of health of a patient, user or other person*

In the section "Event Outcomes" of the incident report template the person reporting the incident needs to describe if 
the event led, or might have led, to outcomes that would have resulted in a serious deterioration in state of health in
at least one of the following:

* life-threatening illness
* permanent impairment of a body function or permanent damage to a body structure
* a condition which requires medical or surgical intervention to prevent one of the above
* any indirect harm as a consequence of an incorrect diagnostic result when used within manufacturer's
  instructions for use
* events where serious medical consequences have not occurred but could
 occur in the future under similar circumstances

## 3. Guidance for Assessment

| Guidance Document                                                                                         | Explanation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Intended Purpose**<br>*See MEDDEV 2.12/1, section 4.6 'Definitions'; See MDD Article 1.2 paragraph (g)* | The use for which the device is intended according to the data supplied by the manufacturer on the labelling, in the instructions for use and/or in promotional materials.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Incident**<br>*See MEDDEV 2.12/1, section 4.6 'Definitions' and annex I for examples*                   | Any malfunction or deterioration in the characteristics and/or performance of a device, as well as any inadequacy in the labeling or the instructions for use which, directly or indirectly, might lead to or might have led to the death of a patient, or user or of other persons or to a serious deterioration in their state of health.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Direct or Indirect Harm**<br>*See MEDDEV 2.12/1, section 4.6 'Definitions'*                             | A physical injury or damage to the health of people, or damage to property or the environment.In the majority of cases, diagnostic devices will, due to their intended use, not directly lead to physical injury or damage to health of people. These devices are more likely to lead to indirect harm. Harm may then occur as a consequence of the medical decision, action taken/not taken on the basis of information or result(s) provided by the device or as a consequence of the treatment of cells or organs outside of the human body that will later be transferred to a patient.<br>Examples of indirect harm include misdiagnosis, delayed diagnosis, delayed treatment, inappropriate treatment, absence of treatment transfusion of inappropriate materials. Indirect harm may be caused by imprecise results, inadequate quality controls, inadequate calibration, false positive or false negative results.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Field Safety Corrective Actions**<br>*See MEDDEV 2.12/1, section 4.6 'Definitions'*                     | FSCA is an action taken by a manufacturer to reduce a risk of death or serious deterioration in the state of health associated with the use of a medical device that is already placed on the market. Such actions, whether associated with direct or indirect harm, should be reported and should be notified via a field safety notice.<br><br>FSCA may include: the return of a device to the supplier; device modification; device exchange; device destruction; advice given by manufacturer regarding the use of the device and/or the follow-up of patients, users or others (e.g. where the device is no longer on the market or has been withdrawn but could still possibly be in use).<br><br>Manufacturers can as part of ongoing quality assurance identify a failure of a device to perform according to the characteristics specified in the information for use provided by the manufacturer. If the failure might lead to or might have led to death or serious deterioration in the state of health associated with the use of a medical device and has an impact on a product that has already been placed on the market the manufacturer must initiate a FSCA.<br><br>Examples of failure modes may include software anomalies (e.g. incorrect correlation between patient sample and the obtained result, invalid controls or invalid calibrations).<br><br>A device modification can include:<br>\- Permanent or temporary changes to the labelling or instructions for use \(for example: advice for revised quality control procedures such as use of third party controls\, more frequent calibration or modification of control values\)\.<br>\- Software upgrades following the identification of a fault in the software version already in the market\. This should be reported regardless of whether the software update is being implemented by customers\, field service engineers or by remote access\.<br><br>Advice given by the manufacturer may include modifications to the clinical management of patients or samples to address a risk of death or a serious deterioration in state of health related to the characteristics of the device. For diagnostic devices, corrective action taking the form of the recall of patients or patient samples for retesting or the review of previous results constitutes FSCA. |

## 4. Reporting to National Authorities

If the incident resulted in an adverse event, the incident should be reported against the application to the MHRA 
using the Yellow Card system. 

- https://www.gov.uk/report-problem-medicine-medical-device

If the incident resulted in a significant accidental or unintended exposure of radiation (imaging or radiotherapy) the
Radiation Safety department should be contacted for the incident to be reported to the CQC.

In addition, all incidents involving patient cause by a medical device produced by the CSC must be raised by the QMO to
the attention of Clinical Engineering, as the department responsible for medical devices in the Trust. 

### 4.1 Timescales for Reporting Incidents

The QMO should notify the MHRA immediately upon becoming aware that an incident may have been caused as a result of 
the use of an application built under this QMS. CSC team members must inform the QMO immediately if they receive 
notification of any incidents.

The maximum permitted time between the QMO or CSC team member first becoming aware of the incident and notifying the 
MHRA is:

**Serious public health threat**: No later than 2 calendar days after becoming aware
**Death or unanticipated serious deterioration in state of health**: No later than 10 calendar days after becoming aware
**Others**: No later than 30 calendar days after becoming aware

For incidents relating to radiation exposure, the QMO should notify the Radiation Safety department immediately, 
which will escalate the incident to the CQC.

---

## Related documents

| Document Title                   | ID        |
|----------------------------------|-----------|
| Incident Report Template         | CSC F.002 |

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).
