---
qms_version: 2.2.0
sop_id: CSC PR.005
sop_version: 2.0.3
template_id: CSC F.011
template_version: 2.0.3
record_version: 
record_id: PMS-001
title: Post Market Surveillance Plan
---

# Post-Deployment Surveillance Plan

This plan describes product-specific post-deployment surveillance activities.

## General

|                           |               |
|---------------------------|---------------|
| **Template ID**           | CSC F.011     |
| **Template Version**      | 2.0.1         |
| **QMS Version**           | 2.2.0         |
| **SOP ID**                | CSC PR.005    |
| **SOP Version**           | 2.0.1         |
| **Regulatory References** |               |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |

---

## Product

| Product Name | Version     | Surveillance Period |
| ------------ | ----------- | ------------------- |
|              |             |                     |

## 1. General Considerations

According to Annex III section 1.1 (b) MDR, the post-market surveillance plan shall cover:

| MDR Requirement                                                                                                                                                                                                                                                                           | Activity                                                                                                                                                                                |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A proactive and systematic process to collect any information referred to in point (a). The process shall allow a correct characterisation of the performance of the devices and shall also allow a comparison to be made between the device and similar products available on the market | Monitor compliance with the Minimum Reporting Standards for in vivo Magnetic Resonance Spectroscopy (MRSinMRS) checklist for: Hardware, Acquisition, Data Analysis Methods and Outputs. |
| Effective and appropriate methods and processes to assess the collected data;                                                                                                                                                                                                             | Monitor compliance with the Minimum Reporting Standards for in vivo Magnetic Resonance Spectroscopy (MRSinMRS) checklist for: Data quality.                                             |
| Suitable indicators and threshold values that shall be used in the continuous reassessment of the benefit-risk analysis and of the risk management as referred to in Section 3 of Annex I;                                                                                                | Risk management is ensured via a risk analysis in compliance with Chapter 1-3 of Annex I.                                                                                               |
| Effective and appropriate methods and tools to investigate complaints and analyse market-related experience collected in the field;                                                                                                                                                       |                                                                                                                                                                                         |
| Methods and protocols to manage the events subject to the trend report as provided for in Article 88, including the methods and protocols to be used to establish any statistically significant increase in the frequency or severity of incidents as well as the observation period;     |                                                                                                                                                                                         |
| Methods and protocols to communicate effectively with competent authorities, notified bodies, economic operators and users;                                                                                                                                                               |                                                                                                                                                                                         |
| Reference to procedures to fulfil the manufacturers obligations laid down in Articles 83, 84 and 86;                                                                                                                                                                                      |                                                                                                                                                                                         |
| Systematic procedures to identify and initiate appropriate measures including corrective actions;                                                                                                                                                                                         |                                                                                                                                                                                         |
| Effective tools to trace and identify devices for which corrective actions might be necessary;                                                                                                                                                                                            |                                                                                                                                                                                         |
| A PMCF plan as referred to in Part B of Annex XIV, or a justification as to why a PMCF is not applicable.                                                                                                                                                                                 |                                                                                                                                                                                         |

## 2. Data Collection Activities

> Note: In the "Metric / Threshold" column there's a placeholder "(define)". Replace this with the metric and
> threshold you've decided upon.

| Activity                                                                                                     | Assigned To                  | Metric / Threshold | How Often?                    |
| ------------------------------------------------------------------------------------------------------------ | ---------------------------- | ------------------ | ----------------------------- |
| Incident documentation and analysis of undesirable side effects                                              | QMO                          | (define)           | 1/year on Jan 1st             |
| Assess feedback (customer complaints, sales feedback)                                                        | Head of Product              | (define)           | 1/year on Jan 1st             |
| Check SOUP for new published issues                                                                          | Head of Software Development | N/A                | 2/year on Jan 1st and Aug 1st |
| Research data about similar products in the market                                                           | QMO                          | (define)           | 1/year on Jan 1st             |
| Conduct post-market clinical follow-up activities as planned                                                 | Head of Medical Team         |                    |                               |
| Research scientific publications                                                                             | Head of Product              |                    |                               |
| Research updates of standards and legislation                                                                | QMO                          |                    |                               |
| Analyze trends, decide on necessary measures and implement them                                              | QMO                          |                    | 1 /year                       |
| Update risk management file                                                                                  | QMO                          |                    |                               |
| Compile post-market clinical follow-up report                                                                | Head of Medical Team         |                    |                               |
| Compile Periodic Safety Update Report                                                                        | Head of Product              |                    |                               |
| Upload PSUR to Eudamed database                                                                              |                              |                    |                               |
| Compile post-market surveillance plan and post-market clinical follow-up plan for next surveillance interval |                              |                    |                               |

## 3. Data Collection Categories

At minimum, the information required by the process for post-deployment surveillance is collected. For (enter
product name), the following categories of data will be collected specifically:

### Information about other devices\*

- [BfArM Field Corrective Actions][bfarm-fca]
  - Keywords:
  - Filter:
  - Time span:
- [BfArM Recommendations][bfarm-rec]
  - Keywords:
  - Time span:
- [MHRA][mhra]
  - Keywords:
  - Filter:
  - Time span:
- [Swissmedic: List of recalls and other field corrective actions][swissmedic]
  - Keywords:
  - Time span:
- [FDA Recalls: medical device recalls][fda-recalls]
  - Keywords:
  - Time span:
- [FDA Maude][fda-maude]
  - Keywords:
  - Time span:
- SOUP Incident Reports
  - Go through SOUP list
  - Research public incident reports of the last (enter time span) months

### Other information about similar devices

- Google News Search
  - Filter: (define)
  - Time span:
- (...)

### Specialist literature / technical databases

> Note: This chapter should analyze other publications applicable to our product which are not considered
> already (or typically) as part of the post-deployment clinical follow-up.

- Pubmed
  - Filter: (define)
  - Time span: last 12 months
- (...)

### Serious incidents of our medical device

- Incident documentation
  - None

### Non-serious incidents and undesirable side-effects of our own medical device

- Feedback and customer complaints
  - None

### Feedback we collect from our partners, users, distributors, importers

- Feedback and customer complaints
  - Filter: not hazard-related feedback, feedback to performance, safety or processes
  - Time span:

### Trends

- Compile list of trends as described in the section below.

## 4. Trend Analysis

Trend analysis is performed with a focus on undesirable side-effects and non-serious incidents. The trend analysis data sources may include Application audit and system logs, AI model inference time, AI confirmation bias, AI automation bias, GitHub issues, Complaints, feedback meetings with staff. These will be
monitored if they impact the benefit-risk ratio in a negative way.

Hazards in the risk table are compared to post-market surveillance results:

- If post-deployment surveillance leads to the finding that the estimated **probability** was too low (= event
  happened more often in post-market surveillance), actions are initiated as described in the SOP Post-Market
  Surveillance.
- If post-deployment surveillance leads to the finding that the estimated **severity** was too low (= event
  happened led to more serious harm in post-market surveillance), a CAPA is initiated.

<!-- Links -->

[bfarm-fca]: https://www.bfarm.de/SiteGlobals/Forms/Suche/EN/kundeninfo_Filtersuche_Formular_en.html?nn=4527724
[bfarm-rec]: https://www.bfarm.de/EN/MedicalDevices/RiskInformation/Recommendations/_functions/_node.html
[mhra]: https://www.gov.uk/drug-device-alerts
[swissmedic]: https://fsca.swissmedic.ch/mep/

<!-- This is a great link -->

[fda-recalls]: https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfRES/res.cfm?start_search=1&event_id=&productdescriptiontxt=&productcode=&IVDProducts=&rootCauseText=&recallstatus=&centerclassificationtypetext=&recallnumber=&postdatefrom=&postdateto=&productshortreasontxt=&firmlegalnam=&PMA_510K_Num=&pnumber=&knumber=&PAGENUM=100
[fda-maude]: https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfmaude/search.cfm

---

Template Copyright [openregulatory.com](https://openregulatory.com). See [template
license](https://openregulatory.com/template-license).

Please don't remove this notice even if you've modified contents of this template.
