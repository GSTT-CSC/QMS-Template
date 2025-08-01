---
qms_version: 2.2.0
sop_version: 2.0.2
---

# GitHub Review SOP
<!-- [13485:7.3.9]-->

## General

|                           |              |
| ------------------------- |--------------|
| **Document ID**           | CSC PR.017   |
| **Document Version**      | 2.0.2        |
| **Author**                |   |
| **Approval**              |  |
| **QMS Version**           | 2.2.0        |
| **Regulatory References** |              |

## Purpose

This document describes the procedure for reviewing and approving GitHub pull requests.

## Scope

This process should be followed during QMS documentation maintenance and improvement activities, and for all software
development projects undertaken within this QMS.

## Definitions

| Acronym  | Definition                        |
|----------|-----------------------------------|
| PR       | **Pull request**                  |
| QMS      | **Quality Management System**     |
| CSC      | **Clinical Scientific Computing** |

## Roles and Responsibilities

| Role        | Responsibility                                               |
|-------------|--------------------------------------------------------------|
| Developer   | The person submitted a change to a file or project in Github |
| Reviewer    | The person reviewing the submission.                         |

## 1. Introduction

This QMS uses GitHub for version control and logging the change history of all QMS documentation and all software
development projects undertaken under the QMS.

## 2. Github Issues

- GitHub issues are used to track work within the CSC QMS. They can be created for change requests, user complaints,
  reporting incidents, requesting additional features etc.
- For each item of work that is required in a particular GitHub project, an issue should be created to track that item
  from beginning to completion.
- Each issue in a project in GitHub is given an identifier in the form "#<num>" which is unique to the project.
  This can be referenced anywhere in the project on GitHub.

## 3. Branches and commits

- To resolve an issue, a branch is created from the repo and stored locally on the developer's computer, where this
  piece of work is completed.
- Incremental changes should be saved via commits to this local branch.
- the title of the commit must be in the active case, no more than 50 characters, lower case with words separated
  by underscores.
- The format of the comment should adhere to the following guidelines
  - https://cbea.ms/git-commit/

## 4. Pull requests (PRs)

- Once the branch is in a state that requires review, a PR should be made to push the changes to the online repository.
  - The title of the PR should relate to the issue it resolves e.g. "#1 Create new doc" where issue #1 requires a
    document to be made.
  - In the PR title or the comment, quote the issue id eg "#5 resolved". (Note: there is a space between the id and
    the "resolved")

## 5. Reviewing PRs
<!-- [13485:4.1.4a,4.1.4b] -->

The PR must be reviewed by the reviewer nominated by the PR author in a timely manner.

- The Reviewer of the pull request should never be the staff member who submitted it.
- The review should be completed within a time frame agreed with the Developer.
- Multiple reviewers can be assigned to a PR.

The review should:

- consider the impact of the change on the QMS and on medical devices produced under this QMS.
- provide comments on any errors in the work.
- provide useful, actionable feedback
- check for typos, including in comments
- ensure format follows coding best practices
- address the developer's id handle in the comments to bring the review to their attention.
- ensure document versions have been iterated appropriately
- identify and review any risks introduced by the documentation/code changes, with respect to patient safety,
data security, and compliance with standards and regs. 
