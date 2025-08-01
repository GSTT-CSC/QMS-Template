---
qms_version: 2.2.0
sop_version: 2.0.3
---

# Post-Deployment Surveillance SOP
<!-- [13485:7.5.1f]-->

## General 

|                            |                 |
|----------------------------|-----------------|
| **Document ID**            | CSC PR.005      |
| **Document Version**       | 2.0.1           |
| **Author**                 |      | 
| **Approval**               |     |
| **QMS Version**            | 2.2.0           |
| **Regulatory References**  | MDR Article 84  |


## Purpose
This document describes the actions required once an application developed under this QMS has been deployed into a clinical setting, so that the performance of the medical device is continuously monitored. It ensures that new information about safety and performance is proactively collected and can be used as input for the risk management, clinical evaluation and software development of our applications.

## Scope
The processes in this document must be followed for all computing projects where the solution is intended to be 
used within a clinical setting, directly or indirectly influences patient care, or uses patient data. It also 
covers projects that involve the use of machine learning algorithms.

## Definitions

| Acronym | Definition                                               |
|---------|----------------------------------------------------------|
| QMO     | **Quality Management Officer**                           |
| PMCF    | **Post-Deployment Clinical Follow-Up activities**        |
| MHRA    | **Medicines and Healthcare Products Regulatory Agency**  |                                                                                                  
| SOUP    | **Software of Unknown Provenance**                       |
| CAPA    | **Corrective and Preventive Action**                     |   

## Roles and Responsibilities
<!-- [13485:7.5.6b]-->
At the start of the project the following roles must be allocated. 

| Role                    | Responsibility                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Clinical Safety Officer | Provide expertise and leadership in all activities associated with the evaluation of clinical risk management for the applications. |
| Product/process owner   | Takes ultimate responsibility for deployed product                                                                                  |

## 1. General Considerations

This process is followed for each product separately, meaning that for each product, a Post-Deployment
Surveillance Plan and Report are created and continuously updated.

> Note: For class I devices, you could specify a longer update interval, e.g. once every two years.
> Note: Feel free to assign the responsibility to any other role. It typically makes sense to choose a role
> that is both close to product development as well as clinical issues.

| Responsibility  | Document Update Interval |
|-----------------|--------------------------|
| Product Manager | Once per year            |

> Please also note that according to the Transitional Provisions of Art. 120 MDR, you are required to comply
> with MDR requirements regarding post-deployment surveillance (Art. 83 ff.) starting May 2021 even if your
> product runs on a valid MDD certificate. This basically means to use the new format of a ‘Period Safety
> Update Report’ (PSUR).

## 2. Process Steps
<!-- [13485:7.5.6a]-->

### 2.1 Create Post-Deployment Surveillance Plan

Based on the clinical evaluation and technical documentation, a new Post-Deployment Surveillance Plan is created
for a product.

| Participants            |
|-------------------------|
| Clinical Safety Officer |
| Product Manager         |

| Input                  | Output                            |
|------------------------|-----------------------------------|
| Device Description     | Post-Deployment Surveillance Plan |
| Clinical Evaluation    |                                   |
| Risk Management Report |                                   |

### 2.2 Conduct Post-Deployment Surveillance

The Post-Deployment Surveillance is carried out as described in the Post-Deployment Surveillance Plan in the defined
interval.

Ideally, the responsible person continuously collects information of all the categories described below and
enters them into our report template.

At minimum, the following information categories have to be taken into consideration:

 * **Clinical evaluations and PMCF activities:**: Input from our Post-Deployment Clinical Follow-Up activities.
 * **New research and development in the market:** Information regarding similar medical devices and
   technologies on the market.
 * **Input from recalls and reportable events:** Recalls, incidents and unintended side effects reported by
   competitors, similar applications and procedures or reported for other devices of our company (e.g.  MHRA).
 * **New or updated norms and standards, directives, regulation and other laws:** Verification if the list of
   applicable regulations is up to date.
 * **SOUP:** Verification if SOUP list is up to date.
 * **Complaints directly reported by customers:** Information gathered through customer feedback and complaints and GitHub.
 * **Trend analysis** Results from trend analysis for automation bias (e.g. DICE scores for contouring automation trended over time, showing level of agreement/editing) and confirmation bias (e.g. false positive rates decreasing over time between initial prospective and 1 year audit) as well as any other trends captured. 
 * **Other feedback** collected or reported by other stakeholders.

For each part of information, it is assessed whether it is applicable to the application. Additionally,
its severity is rated on the following scale:

 * **Severe:** Serious injury or death
 * **Moderate:** Non-serious injury
 * **Marginal:** Everything else, less than moderate

Depending on the applicability, severity and observed trends of the new information, appropriate actions are
initiated. The QMO and Medical Device Safety Officer must be consulted in this step, other roles (e.g. medical
staff) should be involved if needed.

Actions may entail:

 * **Updating the application risk management file**, for example by adding new risks according to our risk
   management process, updating occurrence / severity assumptions made for risks we already documented or
   updating risk mitigation measures in place.
 * **Initiating a CAPA**, for example to update processes, training measures or resource allocation.
 * **Initiating incident reporting** to authorities or a application recall.
 * **Design changes** to the application following the change management process described in the Design and Development SOP.

| Participants            |
|-------------------------|
| Clinical Safety Officer |
| Product Manager         |

| Input                                    | Output                 |
|------------------------------------------|------------------------|
| Post-Deployment Surveillance Plan        | Evaluated Information  |
| Post-Deployment Surveillance Information |                        |

### 2.3 Compile Periodic Safety Update Report

The Product Manager finalizes the Periodic Safety Update Report (PSUR), which is at least reviewed by the
QMO. The report should contain at least the following information:

 * main findings of post-deployment surveillance activities throughout the surveillance interval
 * conclusion regarding implications for the risk management and clinical evaluation of the product, in
   particular the overall residual risk and benefit-risk determination
 * the usage metrics of the device, e.g. amount of users and, where practicable, the usage frequency of the
   device.

| Participants               |
|----------------------------|
| Quality Management Officer |
| Clinical Safety Officer    |
| Product Manager            |

| Input                               | Output                        |
|-------------------------------------|-------------------------------|
| Collected and evaluated information | Periodic Safety Update Report |

---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).


