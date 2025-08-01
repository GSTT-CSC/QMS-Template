---
qms_version: 2.2.1
policy_version: 2.0.6
---


![image](https://gstt-csc.github.io/assets/img/CSC-logo-trans-sm.png) 

# CSC-QMS
<!-- [13485:4.2.1b,4.2.1e,8.5.1] -->


Quality management system for in-house computing projects
<br>
[View Repo](https://github.com/GSTT-CSC/CSC-QMS) . [Report Error](https://github.com/GSTT-CSC/CSC-QMS/issues) . [Request Document](https://github.com/GSTT-CSC/CSC-QMS/issues)

# Quality Manual, Policy and Objectives
## General
The documents in this repository pertain to the CSC Quality Management System for computing projects developed in-house.

|                           |                           |
|---------------------------|---------------------------|
| **Document ID**           | CSC PL.001                |
| **Document Version**      | 2.0.6                     |
| **Author**                |                           |
| **Approval**              |                           |
| **QMS Version**           | 2.2.0                     |
| **Regulatory References** | see below                 |


### Regulatory References

| ISO 13485:2016 Section | Document Section |
|------------------------|------------------|
| 4.1.1                  | 1.               |
| 4.1.2                  | 4.               |
| 4.2.1 b)               | (All)            |
| 4.2.2                  | (All)            |
| 5.3                    | 2.               |
| 5.4.1                  | 2.               |



## Summary

The Quality Manual describes the scope of the Quality Management System, its documented procedures and a
description of their interactions.

## 1. Scope
<!-- [13485:4.1.1,4.2.1c,4.2.2a] -->

The QMS described in this Quality Manual applies to all standalone software medical devices developed by the Clinical 
Scientific Computing team at Guy's & St Thomas' NHS Foundation Trust.

### Role of Company

Guy's & St Thomas' NHS Foundation Trust is the largest and one of the UK's busiest and most successful foundation 
trusts, with a long history of high quality care, clinical excellence, research and innovation. Royal Brompton and 
Harefield hospitals became part of Guy's and St Thomas' in February 2021, bringing together world-leading expertise and 
research in heart and lung disease.

Guy's & St Thomas' NHS Foundation Trust is also a manufacturer of software medical devices.

### Applicable Standards and Certifications

The following table only gives an overview of the most relevant regulation and standards. For a comprehensive
overview, see the list of applicable standards.

| Standard / Regulation / Law | Why Applicable?                               |
|-----------------------------|-----------------------------------------------|
| UK MDR 2002                 | Devices placed "service" within GSTT          |
| ISO 13485:2016              | QMS required by essential requirements of MDD |
| ISO 14971:2019              | Risk management for medical devices           |
| IEC 62304:2006              | Software development for medical devices      |
| IEC 62366-1:2015            | Usability evaluation for medical devices      |


| Standard      | Certificate                                                                                                        | 
|---------------|--------------------------------------------------------------------------------------------------------------------|
| ISO13485:2016 | [MD 796362.pdf](records/certification/MD 796362.pdf) |

### Non-Applicable Requirements

#### ISO 13485:2016

The following sections of ISO 13485:2016 are non-applicable because all products developed under this QMS are 
stand-alone software:

| Section | Title                                                                                             | Rationale                                                                                                                                                                 |
|---------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 6.4.2   | Contamination control                                                                             | The CSC Team develop software only                                                                                                                                        |
| 7.5.2   | Cleanliness of product                                                                            | The CSC Team develop software only                                                                                                                                        |
| 7.5.4   | Servicing activities                                                                              | The CSC Team develop software only. <br><br> Software updates are controlled under change management and are not considered servicing.                                    | 
| 7.5.5   | Particular requirements for sterile medical devices                                               | The CSC Team develop software only                                                                                                                                        |
| 7.5.7   | Particular requirements for validation of processes for sterilisation and sterile barrier systems | The CSC Team develop software only                                                                                                                                        |
| 7.5.9.2 | Particular requirements for implantable medical devices                                           | The CSC Team develop software only                                                                                                                                        |
| 7.6     | Control of Monitoring and Measuring equipment                                                     | Any measurements for quality/performance of processes will be made by ad-hoc software built by the Development Lead of a particular project or the Quality Representative |


#### MDR 2002
SaMD developed within the QMS by the CSC Team are deployed within GSTT for use internally only and will not be distributed
outside The trust, so are considered to be put "in service" rather than on the market as per MDR Article 5 and therefore
exempt from the full regulation. The QMS is compliant with the conditions for exemption. 



## 2. Quality Policy & Objectives
<!-- [13485:4.1.3a,4.2.1a] -->
### Quality Policy
<!-- [13485:5.1b,5.3e] -->

We are guided by our values: putting patients first, taking pride in what we do, respecting others, striving to be the 
best and acting with integrity.

As part of King's Health Partners, an academic health sciences centre, we are pioneers in health research, and provide 
high quality teaching and education. This partnership helps us provide the latest treatments alongside the best possible
care.

We are committed to complying with all applicable legal requirements in order to facilitate the translation of software 
medical devices from R&D into routine clinical care. This is balanced with a need to adopt modern processes of the 
internet-era to respond to people’s raised expectations and the rise of data-driven technologies.

As developers of software medical devices that could have an impact on safety, we commit to minimising clinical risks 
in compliance with appropriate legal and professional standards to ensure we support safe and effective care. In order 
to facilitate this, we commit to a radically open and transparent development process that allows scrutiny from all 
stakeholders and encourages a culture of honesty, inclusiveness and collaboration.

As members of a vibrant academic health sciences centre, we commit to working in collaboration with our partners in 
academia and colleagues in the wider GSTT Trust to facilitate the translation of research work into products that can 
contribute to patient care in a safe and efficient manner.

In the spirit of continuous improvement, we will review this quality policy on an annual basis to ensure we continue to 
effectively communicate with everyone within our organisation the goal of the QMS as well as to ensure it is fit for 
purpose on top of the shifting landscape of digital health.


### Quality Objectives
<!-- [13485:4.1.3d,5.1c,5.4.1,5.4.2a] -->

In order to meet the Quality Policy we define the following objectives and their respective measurements and targets:

| Objective                                                                                                            | Measurement                                               | Target                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|--------------------------|
| Minimise the number of QMS-related documents that exist outside of software product git repositories, e.g. records.  | Number of documents on shared drive                       | >90% of records          |
| Minimise the time from when new code is ready to be release to application deployment.                               | Time from tagged release in github to clinical deployment | 2 weeks                  |
| Minimise manual documentation generation                                                                             | Number of documents written without a template            | 5                        |
| Increase the number of collaborative developments supported by QMS                                                   | Number of additional developments                         | >2 developments per year |
| Increase the number of contributors and reviewers of QMS documents                                                   | Number of staff trained in QMS management                 | 1/3 of core team         |
| Comply with all applicable requirements in ISO 14971:2019, BS EN 62304:2006, BS EN 62366:2015 and DCB0129, UKMDR2002 | Internal/External audit                                   | All standards and Regs   |

The quality objectives will be reviewed at management reviews and on a frequent basis to ensure they remain inline with
the CSC department goals. 

### Applicable Projects

Not all work projects conducted by the CSC are required to adhere to full ISO 13485:2016 quality management system. 
The criteria for applicable projects are:

- It must be a medical software development project.
- It will be deployed clinically within GSTT.
- It is a medical device in accordance with the MHRA classification scale.

## 3. Roles
<!-- [13485:5.1e,5.5.2a,5.5.2b,5.5.2c] -->

**The CEO** is responsible for ensuring that the organisation complies with all legal requirements as well delivering 
safe and effective care as judged by the Care Quality Commission. The responsibility to comply with The Medical Devices 
Regulations 2002 is delegated to the Medical Director who is supported by the Chief Biomedical Engineer. The Quality
Management Officer (QMO) works with the Chief Biomedical Engineer to ensure that the QMS effectively supports the 
development of software medical devices.

**The Head of Medical Physics** represents the role of top management. They are responsible for:
- The allocation of resources to the CSC department for quality management
- Participate in management review meetings annually to review the QMS  for continuing suitability, adequacy and 
effectiveness. 
- Designate a management representative

**The QMO** is appointed by top management (Head of medical Physics) as the management representative. They are responsible to:

* ensure that processes needed for the company’s quality management system are documented
* ensure appropriate internal communication processes are followed to communicate the effectiveness of the QMS with the organisation
* report to top management on the effectiveness of the quality management system and any need for improvement
* ensure the promotion of awareness of applicable regulatory requirements and QMS requirements throughout the
  organisation
* allocate resources as appropriate so the QMS can function successfully  

**CSC Staff Members** are responsible for:
- following procedure and work instructions whilst performing their duties for the development of clinical software. 
- ensuring they are adequately trained, participating in training, and maintaining up-to-date training logs. 
- ensuring patient safety and the highest standards of quality in all work they do
- contributing to the continual improvement of the QMS through 
  - SOP development, 
  - becoming quality reps, 
  - becoming process owners, 
  - contributing to the implementation of Continuous and Preventative Actions
- supervising CSC collaborators and ensuring their work complies with this QMS. 

**Quality Representatives** are CSC team members with quality management expertise who have the following additional 
responsibilities (in line with D I.008 Role of the Quality Representative):
- reviewing and approving changes to CSC QMS documents
- controlling and issue external documents
- adding new staff to the CSC QMS
- attend Medical physics Quality System Review meetings
- providing training on QMS processes and activities, updating training and amending authorisation logs
- inform Head of Section of any  problems resulting from lack of training
- assisting with internal and external audits
- generating management review reports
- implementing and verifying CAPA actions, and analysis effectiveness of solutions 
- update the CSC QMS to reflect the latest changes in standards and regulations 


**Process Owners** are CSC staff members with specialist expertise who are allocated ownership over 
specific processes. They are responsible for: 
- reviewing and approving changes to SOP's and work instructions related to their process
- delivering training, creating training materials and questionnaires, and recommending trained and competent staff 
for authorisation to perform their process.
- defining KPI's to measure quality and effectiveness of the process for continual improvement. 

**The Quality Manager** is a member of GSTT Medical Physics who is independent of the CSC team and who has certification 
to perform ISO13485 internal audits. They are responsible for performing regular internal audits of this QMS.
- scheduling internal audits
- performing internal audits on at least an annual basis, generating and storing audit reports, and disseminating them 
to the QMO.
- following up on the resolution of non-conformities

<br>

The organisation chart in Fig 1 describes the department hierarchy within the CSC.  
<br>

Fig 1. CSC organisation chart within Medical Physics
![image](assets/department-hierarchy-diagram.png)

The staff filling these roles are found in CSC I.001 Roles. 


## 4. Staff Qualifications and Training
<!-- [13485:5.3b,5.3d] -->

- The CSC department normally uses only staff who are permanently employed by, or under contract to, the Guys’ & St 
Thomas’ Hospital Foundation Trust.


- For each task to be performed, the CSC Department uses staff who have the appropriate combination of academic and/or 
professional qualifications, training, experience, and skill. The use of staff undergoing training is acceptable, 
provided that they are supervised and that the proportion of these to the qualified staff is not such as to have an 
adverse effect on the quality of the work undertaken. <br>


- The CSC Department has documented policy and procedures to ensure that existing and new staff have and maintain
relevant academic and/or professional qualifications, technical skills, and professional expertise. <br>   


- The CSC department maintains an up-to-date record of the relevant competence, academic and professional 
qualifications, training, and experience of all staff concerned with calibrations and tests. These records are held by
the HR Department of Guy’s and St Thomas’ Hospital Trust, accessible to the Head of Clinical Scientific Computing.

- Records specifically related to the training and experience in  calibrations are held by the QMO/Quality Representatives
in the CSC-I-003 Authorisation Log within the CSC QMS.

- Job descriptions of all core CSC Department staff are held by the Head of Clinical Scientific Computing in the Trust HR portal.

- Further details on Human Resource Management are outlined in CSC-PR-015 Human Resources Administration.

## 5. Management Review and Audit Schedules
<!-- [13485:5.3a] -->

The schedules for internal/external audits and management reviews can be found in:

| CSC I.004  | Schedules  |
|------------|------------|


## 6. Processes

<!-- [13485:4.1.2a,4.1.2b,4.1.2d,8.1] -->
<!-- STANDARD OPERATING PROCEDURES -->

The list below contains the procedures and processes associated with the CSC QMS. Processes and procedures relating to 
the Clinical Scientific Computing QMS are designed with a risk-based approach and are continually reviewed and improved 
as a result of GitHub issues, CAPAs, Internal and External Audits, and Management Reviews.  

The interrelation between processes is described in: 

| CSC PL.002 | Process Interaction |
|------------|---------------------|

### 6.1 Standard Operating Procedures
<!-- [13485:4.1.3a,4.2.1c,4.2.1d,4.2.2b,4.2.2c] -->

| Id         | Title                                | Process owner           | Review <br>Date | KPI (metric)                                                                                                                | Threshold                              |
|------------|--------------------------------------|-------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| CSC-PR-001 | Design and Development               | Quality Representative  | 05/24           | Number of stakeholders contributing to requirements gathering                                                               | >3                                     | 
| CSC-PR-002 | Clinical Risk Management System      | Quality Representative  | 05/24           | Number of hazards identified (> 10 hazards per project), <br> Number of stakeholders contributing to requirements gathering | >10 hazards <br> <br> > 3 stakeholders | 
| CSC-PR-003 | Verification and Validation          | Quality Representative  | 05/24           | Verification tests code coverage                                                                                            | > 90% code covered                     | 
| CSC-PR-004 | Labelling                            | Quality Representative  | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-005 | Monitoring and Surveillance          | Quality Representative  | 05/24           | -                                                                                                                           | -                                      | 
| CSC-PR-006 | Feedback Management                  | Quality Representative  | 05/24           | Timeframes for initial response to feedback                                                                                 | within 10 working days                 | 
| CSC-PR-008 | MLOps                                | Quality Representative           | 08/24           | -                                                                                                                           | -                                      | 
| CSC-PR-009 | Third Party Software Validation      | Quality Representative  | 05/24           | All third party software used for QMS and development is validated                                                          | -                                      | 
| CSC-PR-010 | Control of Non-Conforming Product    | Quality Representative  | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-011 | Management Review                    | Quality Representative  | 05/24           | Management reviews held annually                                                                                            | -                                      | 
| CSC-PR-012 | Integration and Deployment           | Quality Representative  | 05/24           | -                                                                                                                           | -                                      | 
| CSC-PR-013 | Document and Record Control          | Quality Representative  | 05/24           | Number of QMS records in the CSC-QMS GitHub repository                                                        | >95 %                                  | 
| CSC-PR-014 | Incident Reporting                   | Quality Representative  | 05/24           | All incidents reported within the timeframe specified by the applicable regulation                                          | 100%                                   | 
| CSC-PR-015 | Human Resources Administration       | Quality Representative  | 05/24           | All staff cross-trained <br> Performance Development Reviews are performed annually                                            | All staff                              | 
| CSC-PR-016 | Corrective and Preventative Action   | Quality Representative  | 05/24           | Resolution of CAPAs within their defined timeframes                                                                         | -                                      | 
| CSC-PR-017 | Reviewing GitHub Pull Requests       | Quality Representative  | 05/24           | GitHub Issues resolved within 60 days                                                                                       | 100% of issues                         | 
| CSC-PR-018 | Purchasing and Purchase Verification | Quality Representative  | 05/24           | -                                                                                                                           | -                                      | 
| CSC-PR-020 | On-Boarding                          | QMO                     | 05/24           | All new staff to be formally onboarded                                                                                      | All staff                              | 
| CSC-PR-021 | Change Management                    | Quality Representative  | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-022 | Control of Q-Pulse Documents         | Quality Representative  | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-023 | Clinical Investigation               | Quality Representative  | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-024 | Sensitive Data Disclosure            | Quality Representative          | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-025 | Software Release Guidelines          | Quality Representative          | 05/24           | -                                                                                                                           | -                                      |
| CSC-PR-027 | Internal Quality Audit               | Quality Representative  | 05/24           | Any issues raised at internal audit to be resolved within 3 months                                                          | 3 months                               |

<br />

<!-- TEMPLATES -->

### 7. Templates


| ID        | Title                                                      | 
|-----------|------------------------------------------------------------|
| CSC-F-001 | Training Log Template                                      |
| CSC-F-002 | Incident Reporting Template                                |
| CSC-F-003 | Management Review Report Template                          |
| CSC-F-005 | Software Validation Form Template                          |
| CSC-F-006 | Field Safety Notice Template                               |
| CSC-F-007 | Internal Audit ReportTemplate                              |
| CSC-F-008 | Design Plan Template Template                              |
| CSC-F-009 | Clinical Risk Management Template                          |
| CSC-F-010 | System Requirements Specification Template                 |
| CSC-F-011 | Post Market Surveillance Plan Template                     |
| CSC-F-012 | Clinical Safety Case Report Template                       |
| CSC-F-013 | Hazard log Template                                        |
| CSC-F-014 | Literature Review Template                                 |
| CSC-F-015 | Quality Improvement and Patient Safety Submission Template |
| CSC-F-016 | System Architecture Diagram Template                       |
| CSC-F-017 | Software Description Template                              |
| CSC-F-018 | Medical Device Regulations Classification Template         |
| CSC-F-019 | System Design Specification Template                       |
| CSC-F-020 | Verification and Validation Plan Template                  |
| CSC-F-021 | Verification and Validation Result Template                |
| CSC-F-022 | Unresolved Anomalies Template                              |
| CSC-F-023 | Deployment Plan Template                                   |
| CSC-F-024 | Cyber Security Template                                    |
| CSC-F-025 | Documentation-Level Evaluation Template                    |
| CSC-F-026 | Release Documentation Template                             |
| CSC-F-027 | Training Data Template                                     |
| CSC-F-028 | Instructions for Use Template                              |
| CSC-F-029 | Service Level Agreement                                    |
| CSC-F-030 | Acceptance Criteria Template                               |
| CSC-F-031 | Revision Level History Template                            |


<br />

### 8. Information documents

| ID        | Title                |
|-----------|----------------------|
| CSC-I-001 | Roles                |
| CSC-I-002 | Third Party Software |
| CSC-I-003 | Authorisation Log    |
| CSC-I-004 | Schedules            |


---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
