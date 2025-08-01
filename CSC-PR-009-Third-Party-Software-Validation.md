---
qms_version: 2.2.0
sop_version: 2.0.2
---

# SOP Software Validation
<!-- [13485:7.5.6c,7.5.6d,7.5.6e,7.5.6f,7.5.6g]-->

## General

|                           |                                                                      |
|---------------------------|----------------------------------------------------------------------|
| **Document ID**           | CSC PR.009                                                           |
| **Document Version**      | 2.0.2                                                                |
| **Author**                |                                                        |
| **Approval**              |                                                          |
| **QMS Version**           | 2.2.0                                                                |
| **Regulatory References** | ISO 13485:2016 Sec. 4.1.6 and 6.3 and 7.6<br>IEC 62304:2016 Sec. 9.8 |

## Purpose

This SOP ensures that the CSC developers only work with validated third-party software and software libraries (e.g. 
Docker, Python, numpy, pydicom, etc.) to avoid erroneous software affecting the safety and performance of software 
developed by the CSC team which may be used in a medical setting. The process outlines requirements for validation of 
third-party software before use.

## Scope

The processes in this document must be followed for all software where the application being developed is intended to be 
used within a clinical setting, directly or indirectly influences patient care, or uses patient data. It also 
covers projects that involve the use of machine learning algorithms.

This process also distinguishes between the software used to assist SaMD development and the software integrated into
the SaMD (SOUP). 

## Definitions
| Acronym | Definition                                          |
|---------|-----------------------------------------------------|
| QMO     | **Quality Management Officer**                      |
| ML      | **Machine Learning**                                |
| AI      | **Artificial Intelligence**                         |
| MLOps   | **Machine Learning Operations** (related to DevOps) |
| SOUP    | **Software of Unknown Provenance**                   |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate 
training to fulfil the responsibilities.

| Role                    | Description        | Responsibility                                                                              |
|-------------------------|--------------------|---------------------------------------------------------------------------------------------|
| Software developer      | CSC Team Member    | Considers, documents and validates all third-party software used within the project         |
| Process owner           | Head of Department | Takes ultimate responsibility third-party software used within the project                  |                                                                 |


## 1. Process Steps

**Important note**: the CSC team software developer need only follow these processes once a working software prototype 
has been created. The developer should not waste time creating documentation for software that will not be used 
in a clinical setting.

### 1.1 Information Collection and Preliminary Assessment of Third-party Software


#### 1.1.1 QMS and department Infrastructure software

The introduction of new software into the development process is discussed by the CSC team at bi-weekly stand-ups. 
Once the CSC team member has established that the software will be used for a purpose such as those outlined in the 
Scope section of this document, the CSC team member should:

* Create a log to record all the third-party software used in the project, including version numbers. This document 
should be maintained throughout development, so that other users can understand what third-party software has been used.
* Establish which third-party software is used in the project. Third-party software includes, but is not limited to:
  * Enterprise-grade or software developed by commercial companies, e.g.: Docker, PyTorch, TensorFlow, XNAT etc.
  * Programming languages: Python, C++, etc.
  * Open source software libraries: numpy, scikit-image, matplotlib, pydicom, etc.
  * Software developed by, or in collaboration with, individuals or small groups: dcm2niix, mirtk, etc.

In order to identify the third-party software used in the project, the CSC developer should consider the software used
at every step of the software pipeline. 


#### 1.1.2 Software of Unknown Provenance (SOUP) in applications

SOUP is a “software item that is already developed and generally available, and that has not been developed for the
purpose of being incorporated into the medical device (also known as “off-the-shelf software”) or a software item
previously developed for which adequate records of the development process are not available.” [IEC 62304] 

All python packages that are packaged/integrated into the developed application software code is considered SOUP and
must be risk assessed at the project level. 

SOUP can be identified by: 
* Use software tools to establish all the libraries used within the project, e.g.: `pip list`, which produces a text 
  output of all packages, sub-dependencies and corresponding versions.
  * Alternatively, examine any files which install software dependencies, such as the `requirements.txt`
* Examine if the installation instructions specify particular software, such as installed via command line, e.g.: 
  `apt-get install itksnap` or `brew install rabbitmq`
* External software packages incorporated into the final developed application that was not design to be incorporated 
into medical device or for which the development process is not known. 


### 1.2 Software Validation Form

Once the CSC team member has identified all the third-party software used in the project, the CSC team member must 
complete a Software Validation Form (CSC F.005) for each third-party software. If a different project uses the same 
third-party software or library, the CSC team member can use an existing Software Validation Form and adapt it to this 
project, ensuring that any parts of the form are updated appropriately (e.g.: version number).

The form contains advice on filling out each section. Changes to the evaluation process will be reflected in the latest 
version of the CSC F.005 template.

A python library is incorporated into the SaMD is considered as SOUP and will require risk assessment and verification.
This process is covered in _CSC PR.001 Design and Development SOP Section 3.2 SOUP_. 

### 1.3 Release

If validation was not successful:

 * Document the validation results in the list of computerized systems and classify the system as "blocked" /
   "not released for use".

If validation was successful:

 * Document the validation results and sign the validation report as part of the computerized system
   validation form.
 * Release the computerized system by adding it to the list of computerized systems.
 * Inform relevant staff about the approval of the system.

| Responsible |
|-------------|
| QMO         |

| Input                    | Output                             |
|--------------------------|------------------------------------|
| Software Validation Form | Completed Software Validation Form |
| Software List            | Updated List of Software           |
|                          | Notification sent                  |

### 1.4 Monitoring of Third-Party Software

If any of the software or libraries in the project change, the CSC team member should update accordingly the spreadsheet 
(or equivalent file) documenting all the software used within the project.

The CSC team member should also update the Software Validation Forms for any software which has changed. The CSC team 
member should also create a new Software Validation Form if new third-party software or libraries have been introduced 
to the project.

The CSC team member should consider any user feedback or errors relating to specific third-party software.


### 1.5 Decommissioning of Third-Party Software

 In case it is decided to decommission a piece of third-party software used within the project, the CSC team member 
 must document:
* Why the third-party software needs to be decommissioned
* What, if any, effects this will have on the wider software
* Document any third-party software used in place of the decommissioned software (e.g.: if an alternative third-party 
  library performs an equivalent task more quickly)


### 1.6 Exclusions to software validation

Software used in development and QMS activities are validated in a risk based process. If a software poses negligible risk
to the QMS or final developed application they can be exempt from the software validation process.
Integrated Development Environments (IDE's) used for software development are excluded from for the following reasons:
- Whilst the IDE PyCharm is recommended for developer, each CSC developer is expected to use the best tools available to
them to complete tasks at hand. 
- IDE's provide a negligible risk of introducing bugs to the software applications as the manufacturers of industry 
standard IDE's perform validation to a high level. 
- Performing local validation of each new version of each IDE would place a prohibitively large burden on the CSC. 
- IDEs do not integrate any of their functionality into the code being developed. Application verification and
validation tests will be written to identify any bugs in the final deployed application. 

### 1.7 Revalidation

Validated software does not need to be revalidated periodically except for in the following cases:
1. **The software has been upgraded** - previous tests should be repeated and additional tests performed to evaluate 
any functional changes reported by the manufacturer in the release.
2. **Issues have been raised against the software** - via a user reported issue, CSC reported issue, incident, or CAPA, where
the appropriate use of the software has been called into question. In these cases additional tests and risks must be
evaluated. 



---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
