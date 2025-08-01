---
qms_version: 2.2.0
sop_version: 2.0.1
---

# Disclosure of sensitive data SOP
## General

|                           |                |
|---------------------------|----------------|
| **Document ID**           | CSC PR.024     | 
| **Document Version**      | 2.0.1          |
| **Author**                |  |
| **Approval**              |    |
| **QMS Version**           | 2.2.0          |
| **Regulatory References** |                |

## Purpose
The purpose of this SOP is to establish a systematic approach to handling sensitive data disclosures on GitHub repositories, with a focus on text data. The procedure addresses various scenarios based on the repository's privacy settings and the type of data being disclosed.

## Scope
This SOP applies to all individuals and teams who handle sensitive data and might disclose such sensitive data on remote repositories. It includes all types of text/tabular sensitive data and covers both private and public GitHub repositories.


## Definitions
| Acronym | Definition                                                                               |
|---------|------------------------------------------------------------------------------------------|
| CSC     | **Clinical Scientific Computing**                                                        |
| QMS     | **Quality Management System**                                                            |
| CAPA    | **Clinical and Product Assurance**                                                       |
| DATIX   | Web based reporting and risk management software for health and social care institutions |


## Roles and Responsibilities

| Role                     | Description               | Responsibility                                                                                                                 |
|--------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Clinical Safety Officer  | Clinician                 | Provide expertise and leadership in all activities associated with the evaluation of clinical risk management for the product. |
| Product  owner           | Head of Department        | Takes ultimate responsibility for deployed product                                                                             |

## Pre-requisites

A data leak on a remote repository occurs when sensitive information is unintentionally committed and pushed to GitHub.

- Data leaks can include but are not limited to:

- Personal data: Direct patient identifiers such as names, phone numbers, addresses, patient reports/results.

- Security credentials: This includes usernames, passwords, API keys, tokens, or other information that can be used to gain unauthorized access to systems/platforms/data.

Even if you have deleted sensitive data from your GitHub repository, rebased, or rewritten the history, ***the information might still be present in the cache.*** 
GitHub's caching systems do not immediately clear on these actions, meaning that cached or 'dangling' commits may still be accessible after being removed from the repository's visible history. 

## Process Steps

### 1. Assess the disclosure 
#### a. Identify the causes 

- Identify the leaked sensitive data and determine the extent of the disclosure. Keep a record of the leaked data for traceability.
- Investigate and log leak source: how did the data end up in the repository? 
- Evaluate the potential impact of the leak on affected individuals.
  
#### b. Identify the timeline and specific commits/branches

- Investigate the repository's commit history and branch activities to identify when and how the sensitive data was pushed. Log the specific commits, branches, and potential PRs involved in the data leak. 
- Assess the duration of the exposure and the potential number of individuals who may have accessed the data during that time. It includes people who might have forked, cloned the repository in the meantime.

#### c. Report the leak to the team  
- Raise a CAPA and inform the team before taking any of the next actions.

  
### 2.1. Data Leaking in GitHub Public Repository
#### a. Remove Sensitive Data
- Ensure to keep a record of the leaked data for traceability, as the pushed file(s) will be removed.
- Use BFG Cleaner tool to remove sensitive data from the repository's history, including commits, branches, and tags. A Step-by-step tutorial can be found here https://rtyley.github.io/bfg-repo-cleaner/.
- Review Commit History: Inspect the repository's commit history to ensure the complete removal of sensitive data and verify that no residual traces remain. Use git log command.
#### b. Escalate the issue
- Determine with the CSO what the next steps are (DATIX).
  
***DO NOT ask github to clear cache.***

### 2.2. Data Leaking in GitHub Private Repository
#### a. Remove sensitive data
- Use BFG Cleaner: Similar to the process for public repositories, employ the BFG Cleaner tool to eliminate sensitive data from the repository's history.
- Verify Data Removal: Thoroughly inspect the commit history and repository files to ensure that all sensitive data has been removed. Use git log command.

Even after implementing these steps, there may still be residual cache data or dangling commits persisting in the repository. Confirm with CSO that all the steps were correctly followed and proceed to the next steps.

#### b. Contact GitHub support to remove cached data
-  Read [GitHub guidance](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) about sensitive data as their policy might have been updated.
-  [Open a ticket](https://support.github.com/request/remove-data?tags=docs-generic) for GitHub Team to remove cached data associated with the leaked sensitive information. The URL of the dangling commits will be asked. 

### 3. Mitigate further data exposure 
- Determine the reasons why the existing preventive measures were unsuccessful in stopping the data leak. Currently, these measures include manual checking, the inclusion of csv, txt, and ipynb file types in .gitignore files and the use of pre-commit hooks.
- Take action: strengthen pre-commit hooks: Enhance the existing pre-commit hooks.
