---
qms_version: 2.2.0
sop_id: CSC PR.002
sop_version: 2.0.1
template_id: CSC F.013
template_version: 2.0.1
record_version: 
record_id: HZ-001
title: Hazard Log
---

# Hazard Log

## General

|                           |               |
|---------------------------|---------------|
| **Template ID**           | CSC F.013     | 
| **Template Version**      | 2.0.1         |
| **QMS Version**           | 2.2.0         |
| **SOP ID**                | CSC PR.002    |
| **SOP Version**           | 2.0.1         |
| **Regulatory References** |               |


|              |              |
|--------------|--------------|
| **Author**   |              |
| **Approval** |              |

## Scope

This document applies to {{device.name}} {{device.version}}.

## Purpose

This document contains the outputs of the risk assessment conducted in accordance with the Clinical Risk Management Plan.

This document is meant to be read and agreed-upon by the project owners, the CSC team, and the Clinical Safety
Officer (CSO) during design and development. It provides traceability for risk controls throughout the project.

## Related documents

| Document Title                   | ID       |
|----------------------------------|----------|
| Clinical Risk Management Plan    | CRMP-001 |
| Clinical Safety Case Report      | CSCR-001 |
| Verification and Validation Plan | V&V-001  |


## Hazard log 

| Hazard ID | Hazard | Possible causes  | Effect  | Harm | Severity | Likelihood | Initial risk  | Risk Controls | Final Likelihood  | Final Risk  | Comment  |
|-----------|--------|----------------|------------------|------|----------|------------|---------------------|---------------|-----------------|-------------------|-------------|
{%- for risk in risk.risks %}
| {{ risk.hazard_id }} | {{ risk.hazard }} | {{ risk.causes }} |{{ risk.effects }} |  {{ risk.harm }} |{{ risk.severity }} |{{ risk.likelihood }} |{{ risk.risk }} | - {{ risk.risk_control }} | {{ risk.residual_likelihood }} |{{ risk.residual_risk }} |{{ risk.comment }} |
{%- endfor %}


## Hazard log - Verbose 

{% for risk in risk.risks%}

{% if risk.hazard != None %}
---
### ID : {{risk.hazard_id}}
### Hazard: {{risk.hazard}}
### Harm :  {{ risk.harm }}

<b>Cause</b> : {{risk.causes}}        
<b>Effect</b> :  {{risk.effects}}
<br> <b>Initial Severity</b> : {{risk.severity}}
<br> <b>Initial Likelihood</b> : {{risk.likelihood}}
<br> <b>Initial Risk</b> : {{risk.risk}}
<br> <b>Control Measures</b> : {{risk.risk_control}}
<br> <b>Residual Probability</b> : {{risk.residual_likelihood}}
<br> <b>Residual Risk</b> : {{risk.residual_risk}}
<br> <b>Comment</b> : {{risk.comment}}
<br><br>
{% else %}
<b> ID : {{risk.hazard_id}}</b>
<br><b>Cause</b> : {{risk.causes}}        
<br><b>Effect</b> :  {{risk.effects}}
<br> <b>Initial Severity</b> : {{risk.severity}}
<br> <b>Initial Likelihood</b> : {{risk.likelihood}}
<br> <b>Initial Risk</b> : {{risk.risk}}
<br> <b>Control Measures</b> : {{risk.risk_control}}
<br> <b>Residual Probability</b> : {{risk.residual_likelihood}}
<br> <b>Residual Risk</b> : {{risk.residual_risk}}
<br> <b>Comment</b> : {{risk.comment}}
<br><br>
{% endif %}
{% endfor %}
