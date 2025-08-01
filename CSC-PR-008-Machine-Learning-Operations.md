---
qms_version:2.2.0
sop_version:2.0.2
---

# Machine Learning Operations (MLOps)

## General

|                                  |                  |
|----------------------------------|------------------|
| **Document ID**                  | CSC PR.008       |
| **Document Version**             | 2.0.2            |
| **Author**                       |     |
| **Approval**                     |       |
| **QMS Version**                  | 2.2.0            |
| **Regulatory References**        |                  |

## Purpose
This document describes the design and development processes required for ML computing projects undertaken by the Clinical Scientific Computing Team in Medical Physics at Guys and st Thomas' NHS foundation Trust.

This document described the addition requirements to SOP-0002 (Design and Development SOP) for cases where the application under development uses Machine Learning methods.  

## Scope
The processes in this document must be followed for all ML computing projects where the solution is intended to be used is within a clinical setting, directly or indirectly influences patient care, or uses patient data. 

## Definitions
| Acronym  | Definition                                                                                        |
|----------|---------------------------------------------------------------------------------------------------|
| SOUP     | **Software of Unknown Provenance** - Software used in the project that is not approved by the QMS |
| XNAT     | **eXtensible Neuroimaging Archive Toolkit** (imaging informatics platform)                        |
| ML       | **Machine Learning**                                                                              |
| AI       | **Artificial Intelligence**                                                                       |
| MLOps    | **Machine Learning Operations** (related to DevOps)                                               |
| MLFlow   | **Machine Learning lifecycle management software**                                                |
| MAP      | **MONAI application package**                                                                     |
| MONAI    | **Medical Open Network for Artificial Intelligence**                                              |

## Roles and Responsibilities

At the start of the project the following roles must be allocated. The persons filling each role must have adequate training to perform the role.

| Role                    | Description | Responsibility                                                                                                  |
|-------------------------|-------------|-----------------------------------------------------------------------------------------------------------------|
| Clinical Safety Officer | Clinician   | Appointed to oversee the clinical risk management of the product                                                |
| Development lead        | Developer   | Leads the application development process, including data collection, training, validation and deployment tasks |


## 1. Application Development with MLOps
MLOps is a set of tools and processes that are used to support the development of machine learning algorithms. This includes data management, training, deployment, and testing.

### 1.1 Starting a project
All ML projects should be based on the [project template](https://github.com/GSTT-CSC/Project_template). This template should be flexible enough for all ML applications. By conforming to the template it is possible to automate certain requirements and ensures that the project is structured in a way that is easy to follow and can be supported by CSC.

The project template is structured as below:

```
├── Dockerfile
├── README.md
├── config
│   └── config.cfg
├── project
│   ├── DataModule.py
│   ├── Network.py
│   ├── __init__.py
│   └── transforms
│       └── __init__.py
├── requirements.txt
├── run_project.py
├── tests
│   ├── __init__.py
│   ├── test_DataModule.py
│   └── test_Network.py
└── train.py
```

| Location | type |  Content |
|-----------|-------|-------|
| config  | directory | The config directory should contain configuration information for the project.  | 
| project  | directory| This directory should contain all the functional code for the project, at a minimum it should contain a DataModule and Network classes that are used to define the data and network architecture. It should also contain a separate directory for custom data transforms where necessary.  | 
| requirements.txt  | text file| Should define the required python packages that will be installed through pip; compatible versions of SOUP should be specified.   | 
| run_project.py  | python file| run_project.py runs the ML application. The entry point can be defined at runtime.  | 
| tests  | directory| A directory to store test functions and test data  | 
| train.py  | python file| train.py is an example entry point, other entry points can be defined as required (e.g. tune.py) and should be defined in the config file and accessed using the `-e` flag when executing run_project.py  | 

### 1.2 Data
Each version of a project's data should be stored on shared CSC hardware and the data version logged to MLFlow or git so that any model can be retrained retrospectively with the same data.

Image data is collected, anonymized and archived through XNAT. Likewise, non-image data relevant to the project should be stored and archived on XNAT. Developers should perform high level data exploration using an appropriate tool.

Validation data are kept separate from training data and are used to monitor the performance of the model.

### 1.3 Training
When training a model, each training run will be logged to MLFlow with all appropriate parameters, metrics, and artifacts logged using the MLFlow API. Much of this is handled by the MLOps project template, but developers are encouraged to log everything they deem relevant to the project. Training instructions can be found in the MLOps repository [wiki](https://github.com/GSTT-CSC/MLOps/wiki).

After a promising model architecture has been identified and tested, developers should run a tuning algorithm to further optimize model performance, this is facilitated by tools such as ray tune.


### 1.4 Validation and Testing
The MLFlow UI can be used to view and compare the performance characteristics of all trained models. Any production model must been tracked in MLFlow. 

All production models must meet or exceed the performance requirements defined by the user requirements in the design plan.

### 1.5 Deployment
Any production model must have been tracked in MLFlow. When a model is in the 'staging', 'production' or 'archived' states, this must be noted registered the matching MLFlow run.

Applications should be packaged using the MONAI deploy SDK as MAPs.

Production models must be regularly audited for performance and stability.

## 2. Maintenance of MLOps
The MLOps tools and processes used for projects within the CSC team are purpose built and maintained by the team. It is important that these tools can be improved and kept up to date where necessary. Therefore relevant useful guides are kept within the [wiki](https://github.com/GSTT-CSC/MLOps/wiki) within the MLOps repository.
