---
qms_version: 2.2.0
sop_version: 2.1.2
---

# SOP Document and Record Control
<!-- [13485:4.1.3e,4.3.4e,4.2.4g,7.5.1a,7.5.6e,7.5.9,7.5.9.1]-->

## General

|                           |                                      |
|---------------------------|--------------------------------------|
| **Document ID**           | CSC PR.013                           |
| **Author**                |                          |
| **Approval**              |                          |
| **QMS Version**           | 2.2.0                                |
| **SOP Revision**          | 2.1.2                                |
| **Regulatory References** | ISO 13485:2016 Section, 4.2.4, 4.2.5 |

## Purpose
This SOP describes how documents and records are handled. The goal is to understand how documents are
typically structured and in what states they can be as they move from draft to release. It's similarly
important to always have the most recent document available at the specified location while ensuring that
any changes to documents can be traced.

## Scope
This SOP covers all documents and records under this quality management system.


## Role and Responsibilities

| Role                       | Responsibility                                                                                  |
|----------------------------|-------------------------------------------------------------------------------------------------|
| Quality Management Officer | (QMO):  Ensure that processes needed for the company’s quality management system are documented |
| Process Owner              | Overall responsibility for documenting and processes                                            |
| Project Lead               | Ensuring adequate records are created                                                           |


## 1. General Considerations

**Documents** are expected to change over time, whereas **records** are created once and not altered
significantly afterwards.

All documents are written in English.

### 1.1 Document and Record Labelling and Versioning

#### 1.1.1 Labelling
Documents are named according to the schema described in Medical Physics QMS D WI.001 "Structure & Classification of 
Controlled Documents". 
Each document name must be unique, and the document ID will have a prefix to make it easy to identify and search for:

| Level            | Subsection naming example |
|------------------|---------------------------|
| Policy           | CSC PL.001                |	
| Procedure        | CSC PR.001                |
| Work Instruction | CSC WI.001                | 	
| Form             | CSC F.001	                |
| Information      | CSC I.001                 |
| Labels           | CSC L.001                 |
| Certificate      | CSC C.001                 |		

All documents are managed using the GitHub repository hosted at: https://github.com/GSTT-CSC/CSC-QMS. Every document 
that exists in the 'main' branch is a released document. 

#### 1.1.2 Versioning

The QMS repository in GitHub undergoes releases at specific milestones to reflect external audits, certification, changes
to process and documentation, and additional records. Releases are snapshots in time of the QMS status where an overview of
recent changes are communicated to the team (i.e. presented in the morning stand-up). This will typically occur monthly, 
although it can be performed ad-hoc, such as after urgent changes to practice as a result of reportable incidents. 

Each Document in the QMS will contain a reference to the QMS version, SOP version, Form Version and Record Version, as
appropriate for the document.

Version numbers are of the form `X.Y.Z` where X is the major version, Y is the minor version and Z is the patch. This 
is in compliance with the Semantic Versioning 2.0.0.standard (https://semver.org). Reasons for incrementing version of
each number are as follows: 

| Level                                 | X (Major change)                                           | Y (Minor change)                                             | Z (Typos)                                      |
|---------------------------------------|------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|
| QMS GitHub repository release version | Major release, after certification, annual external audits | Automation changes , or large SOP overhauls                  | Small SOP changes, typos, record updates       |
| Standard Operating Procedure (SOP)    | Major change in practice.                                  | Minor change in practice e.g. additional checks, subsections | Typos and phrasing changes                     | 
| Form                                  | Major overhaul/reformat of the form to reflect SOP         | Minor changes such as adding a new section, to reflect SOP   | Typos and phrasing changes, to reflect the SOP | 
| Record (technical file only)          | Change of practice e.g. template change, SOP change        | Continued filling in of form e.g. additional requirements    | Typos and phrasing changes                     | 

It is the joint responsibility of the staff member making the change a change and the approver to ensure each version is
correct.

Previous versions of documents that are 'archived' are accessible via the 'Releases' menu at the GitHub repository.


### 1.2 Document Type Abbreviations

| Abbreviation | Description                                        |
|--------------|----------------------------------------------------|
| SOP          | Standard Operating Procedure (Process Description) |
| TP           | Template                                           |


### 1.3 Retention Periods
<!-- [13485:4.2.5] -->

QMS documents and records shall be stored for at least 10 years after their archival date.

Technical Documentation shall be stored for at least 10 years after the lifecycle of the respective device has
ended.

### 1.4 Review Periods

We review our QMS documents typically once per year to ensure they remain up to date.

Our core and safety processes as defined in the quality management manual must be reviewed at minimum once per
year.

All other processes and associated documents can be reviewed every three years once they have been reviewed
before without any findings.

In case of audit findings or related corrective action, it is up to the discretion of the QMO to apply shorter
review periods (e.g. 6 months).

### 1.5 QMS Document List

We keep an overview list of all QMS documents, including document type, release date, next review date and
respective process owners.



## 2. Process Steps

### 2.1 Handling of Documents
<!-- [13485:4.2.4c,7.1b] -->

#### 2.1.1 Creation of Documents or Changes to Documents
<!-- [13485:4.2.4d] -->

All SOP or TPL documents are committed in the Quality Management System (QMS) which is a GitHub repository hosted 
at: https://github.com/GSTT-CSC/CSC-QMS. Any records or documents related to a device are committed in the respective
device's repository.

Before creating or editing a document, you must create an `Issue` on the GitHub repository. This is done by clicking
on the "New Issue" button in the top right corner of the GitHub page. 

Once you have created an issue, you can ask any clarification questions or solicit feedback on the proposed document or
proposed changes.

Before commencing any drafting or editing, you must create a new branch in the QMS repository. The branch name should
conform to the following schema:
    
`#ISSUE_NUMBER_SHORT_DESCRIPTION`

Where "ISSUE_NUMBER" is the issue number of the issue you created and "SHORT_DESCRIPTION" is a short description of the
issue that this branch is based on.

An example would be:
`#15_change_record_naming_schema`

The formatting of a document in the QMS should follow the following style:
> # Document Title

> ## table of regulatory requirements/sections

> ## table of general file information (author, version etc.)

> ## Purpose

> ## Scope

> ## Definitions

> ## Roles and Responsibilities

> ## 1. numbered heading 1

> ### 1.1 numbered subheading 1


Standard Operating Procedures (SOP) should specify a process owner responsible to typically update, review and release 
all associated documents.

A QMS change can trigger a substantial change. Before release, it shall be checked whether it may impact the
organization's process landscape and hence, overall organizational conformity with regulatory
requirements. The QMO is responsible to evaluate such potentially major changes as part of the Change
Evaluation List (reference change management process).

Each document must have a series of Unique Identifiers (UID's) to ensure full traceability and version control. These 
must be present in the '.yaml' front matter of the markdowns of each document to allow for QMS automation of internal audit
and compliance. Additionally, the UID's must be present in a 'General' table at the start of the document. 

The specific UID's required by each document is as follows: 

| Doc type                                  | Front matter                                                                                                                                                                                   | 'General' table contents                                                                                                          |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Information sheet <br> (CSC I.XXX)        | --- <br> qms_version: X.X.X <br> info_version: X.X.X   <br> title: XXX<br>---                                                                                                                  | **Document ID**<br> **Document Version**<br> **Author**<br> **Approval**<br>  **QMS Version**                                     |
| SOP <br> (CSC PR.XXX)                     | --- <br> qms_version: X.X.0<br> sop_version: X.X.X<br> title: XXX<br>---                                                                                                                       | **Document ID**<br> **Document Version**<br> **Author**<br> **Approval**<br> **QMS Version**                                      |
| Policy <br> (CSC PL.XXX)                  | --- <br> qms_version: X.X.X<br> policy_version: X.X.X<br>title: XXX<br> ---                                                                                                                    | **Document ID**<br> **Document Version**<br> **QMS Version**<br>  **Author**<br> **Approval**                                     |
| Template (QMS) <br> (CSC F.XXX)           | --- <br> qms_version: X.X.0X <br>sop_version: X.X.X<br>sop_id:CSC PR.XXX<br>template_version: 2.0.1<br>title: XXX<br>---                                                                       | **Template ID**<br> **Template Version**<br> **QMS Version**<br> **SOP ID**<br>  **SOP Version**<br> **Author**<br>  **Approval** |
| Template (Technical file) <br>(CSC F.XXX) | --- <br> qms_version: X.X.X<br> sop_id: CSC PR.XXX<br> sop_version: X.X.X<br> template_id: CSC F.XXX<br> template_version: X.X.X<br> record_version: <br> record_id: XXX<br> title: XXX<br>--- | **Template ID**<br> **Template Version**<br> **QMS Version**<br> **SOP ID**<br>  **SOP Version**<br> **Author**<br>  **Approval** |


| Participants |
|--------------|
| Any employee |

| Input   | Output               |
|---------|----------------------|
| Content | New Document (draft) |

#### 2.1.2 Documents Ready for Review
<!-- [13485:4.2.4a,4.2.4b] -->

Once a document is ready for review, its author must create a Pull Request on the GitHub repository to merge their 
branch with the `main` branch.

Importantly, the author selects appropriate reviewers for the Pull Request by selecting their GitHub username in the
"Reviewers" section of the Pull Request page.

| Participants    |
|-----------------|
| CSC Team Member |

| Input            | Output                  |
|------------------|-------------------------|
| Document (draft) | Document (under review) |

#### 2.1.3 Review of Documents
<!-- [13485:4.2.4a,4.2.4b] -->

The respective reviewer(s) review the document.

If a document is related to the QMS, such as a protocol, procedure, form, template or policy document, a reviewer can be 
the QMO, a CSC Quality representative. The reviewer must not be the same staff member submitting the Pull Request. 

If changes are required, they create comments in the Pull Request 
or inline on the documents. If the review is successful, they select Approve Changes. The Quality representative or QMO 
can then merge the Pull Request with the `main` branch.

| Participants                                         |
|------------------------------------------------------|
| Quality Representative and/or designated reviewer(s) |

| Input                   | Output                       |
|-------------------------|------------------------------|
| Document (under review) | Document (review successful) |

#### 2.1.4 Release of Documents

The Quality Representative merges the branch with the `main` branch and tagging the release of the documents with a new
version number in line with the versioning schema mentioned above.

The permission to merge branches is controlled by the QMO to prevent unauthorized merges.

The Quality Representative decide if employee training is required. In general, training for minor changes/corrections 
is not necessary.

| Participants                 |
|------------------------------|
| QMO, Quality Representative  |

| Input                        | Output              |
|------------------------------|---------------------|
| Document (review successful) | Document (released) |


#### 2.1.5 Archiving of Documents

Documents get archived if they become obsolete or a newer released version becomes available. Previous versions of 
documents that are 'archived' are accessible via the 'Releases' menu at the GitHub repository.
We observe retention periods as outlined in this SOP and delete documents as soon as the retention period expired.

| Participants           |
|------------------------|
| Quality Representative |

| Input               | Output              |
|---------------------|---------------------|
| Document (released) | Document (archived) |

### 2.2 Handling of Records

#### 2.2.1 Creation of Records

We create records as required by our processes. If available, we use templates and checklists for the creation
of records.  Naming conventions as outlined for documents do not apply. Records should include an author name
and the date of creation.

| Participants    |
|-----------------|
| CSC Team Member |

| Input                                      | Output     |
|--------------------------------------------|------------|
| Content, Template Document (if applicable) | New Record |

#### 2.2.2 Review and Release of Records

Unless specified differently in a template or SOP, records do not typically require a review and release
process.

| Participants                           |
|----------------------------------------|
| Designated reviewer(s) and approver(s) |

| Input                 | Output                     |
|-----------------------|----------------------------|
| Record (under review) | Record (review successful) |

#### 2.2.3 Storage of Records

Records are not necessarily stored in our QMS folder. They also may reside in other applications as specified
per respective processes. This is where records are typically stored:

> Add all your tools which stores data which is mentioned in your QMS.

 * *GitHub (Issues, Pull Requests)*
 * *Sharepoint*
 * *CSC Website (gstt-csc.github.io)*


#### 2.2.4 Changes to Records

Records are not significantly altered after creation / release. Where significant changes are required, we
rather create a new record and archive the old one. Non-substantial changes (e.g. spelling mistakes) are
considered corrections only, assessed and added on a case-by-case basis.

| Participants    |
|-----------------|
| CSC Team Member |

| Input             | Output           |
|-------------------|------------------|
| Record (released) | Record (updated) |

#### 2.2.5 Archiving of Records
<!-- [13485:4.2.4h] -->

Records are archived if they become obsolete or a new released version becomes available. For that, the
process owner moves the records to a respective archiving location. If possible, we follow the general
considerations for document names and add the archiving date to the record name. We observe retention periods
as outlined in this SOP and delete records as soon as the retention period expired.

| Participants           |
|------------------------|
| Quality Representative |

| Input             | Output            |
|-------------------|-------------------|
| Record (released) | Record (archived) |


### 2.3 Regular Backups

The GitHub repository containing all documents, records, templates and certificates should be backed up to
mitigate against issues arising from losing access to the GitHub platform. The repo should be zipped and transferred
manually to the CSC shared directory on MT-CSC > Documents > Policy > CSC-QMS > Backups, with the naming format as 
"CSC-QMS-V.V.V_DDMMYYY.zip"

---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
