---
qms_version: 2.2.0
sop_id: 
sop_version: 
template_id: CSC F.022
template_version: 2.0.1
record_version: 
record_id: UA-001
title: Unresolved Anomalies
---

# Unresolved Anomalies

## General

|                           |               |
|---------------------------|---------------|
| **Template ID**           | CSC F.022     |
| **Template Version**      | 2.0.1         |
| **QMS Version**           | 2.2.0         |
| **SOP ID**                |               |
| **SOP Version**           | 2.0.1         |
| **Regulatory References** |               |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |
## Purpose and Scope

This document describes any unresolved anomalies identified during the development process. 

This document applies to {{device.name}}, and includes changes made in release {{device.version}}.

## Known Anomalies

This section includes a list of outstanding problem reports (i.e., known anomalies). Each problem report includes a description of the problem, its impact on device performance, and any plans or timeframes for correcting the problem (where appropriate).

{% for cr in history.change_requests|selectattr('is_problem_report')|rejectattr('change_ids') %}
## {{cr.title}}

**Identifier:** {% if cr.url is defined %}[{{cr.id}}]({{cr.url}}){% else %}{{cr.id}}{% endif %}

**Description:**

{{cr.content}}
{% endfor %}