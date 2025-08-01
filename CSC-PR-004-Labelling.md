---
qms_version: 2.2.0
sop_version: 2.0.2
---

# Labelling and Available Information SOP
<!-- [13485:4.2.3a,4.2.3b,4.2.3d,7.5.1e,7.5.8] -->

## General 

|                           |              |
|---------------------------|--------------|
| **Document ID**           | CSC PR.004   |
| **Document Version**      | 2.0.2        |
| **Author**                |   | 
| **Approval**              |  |
| **QMS Version**           | 2.2.0        |
| **Regulatory References** | UK MDR 2002  |

## Purpose
This document describes the processes for labelling the SaMD and providing information to comply with regulatory standards  .  

## Scope
This procedure must be followed during the development of all CSC computing projects that will directly affect patient 
care or interact with live clinical system or databases.

## Definitions
The following table provides the list of documents to be completed during the design and development phase of the project.

| Acronym | Definition                                                                                        |
|---------|---------------------------------------------------------------------------------------------------|
| SOUP    | **Software of Unknown Provenance** - Software used in the project that is not approved by the QMS |
| QIPS    | **Quality Improvement and Patient Safety**                                                        |
| XNAT    | **eXtensible Neuroimaging Archive Toolkit** - (imaging informatics platform)                      |                                                                                                  
| ML      | **Machine Learning**                                                                              |
| AI      | **Artificial Intelligence**                                                                       |
| MLOps   | **Machine Learning Operations** -  (related to DevOps)                                            |
| PID     | **Patient Identifiable Data**                                                                     |
| KPI     | **Key performance Indicators**                                                                    |
| PR      | **Pull Request** - Github review action                                                           |

## Roles and Responsibilities
At the start of the project the following roles must be allocated. 

| Role                    | Responsibility                                                                |
|-------------------------|-------------------------------------------------------------------------------|
| Clinical Safety Officer | Provide expertise and leadership in risk evaluation for the application.      |
| Development lead        | Generate the labelling information and additional documents                   |
| Clinical Lead           | Provide clinical expertise for labelling and clinical evaluation requirements |

## 1. Method
<!-- [13485:4.2.3e] -->

Under UK MDR 2002, each project must be labelled appropriately to ensure the application is used only as intended and 
to alert the user of its functionality, associated risks, regulatory compliance. 


Within each project the following must be included:

- Product Name / unique identifier
- Manufacturer/institution name and address
- Date of release, and version
- General description of the application
- Intended use
- Foreseeable misuse
- Warnings and precautions
- Expected degree of accuracy for the result
- Work instructions
- Installation instructions and connecting devices
- Classification ( MHRA class I, IIa, IIb, III)
- Clinical investigation (conducted as per Annex X of directive 93/42 <a href="https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=CONSLEG:1993L0042:20071011:en:PDF"> Link</a>)


This information must be stored in the project readme, and must include hyperlinks to key technical documentation. It must be reviewed and completed before the deployment.
