# DivExplorer – A Generalized Approach to Exploring Subgroup Divergence


##

*DivExplorer discovers and explains anomalous subgroup behavior in data and models*


## Overview

DivExplorer is a framework for identifying and interpreting **data subgroups whose behavior significantly diverges** from the overall dataset.
It applies to:

* Dataset statistics (e.g., attribute means, distributions)
* Classification (labels, predictions, FPR/FNR, accuracy)
* Regression (true/predicted values, error metrics)
* Ranking & scoring functions

It allows data auditing, exploratory slice analysis, model debuggin, model inspection, fairness and bias discovery.

The method is **model-agnostic** and **target-agnostic**: any definable outcome function can be analyzed.

---

## Key Features

The **divergence** quantifies how much a subgroup differs from the full dataset. It support real-valued and boolean metrics
and statistical significance via Welch’s t-test (continuous) or Bayesian t-test (boolean).

The automatic subgroup discovery uses **frequent pattern mining** to efficiently enumerate all subgroups above a minimum support threshold.

The approach also supports a simple ε-threshold heuristic removes near-duplicate subgroups and produces a compact summary of results.

Our approach provides interpretable quantification of each attribute's contribution via
* **Local Shapley values** → explain divergence of *one specific subgroup*
* **Global Shapley values** → aggregated at dataset level to identify the most influential factors overall

---

##  Notebooks Overview

The repository includes several Jupyter notebooks (D01–D07), each demonstrating DivExplorer on a different dataset or task:

* D01a – Airbnb Dataset
Divergence analysis on the Airbnb NY dataset.

* D01b – Airbnb Preprocessing
Full preprocessing pipeline: cleaning, feature engineering, discretization. We document the Airbnb NY preprocessing in a technical report (processign_airbnb_technical_report.pdf).  

* D02 – Synthetic Dataset
Controlled example showing individual vs. global divergence behavior.

* D03 – Bike Sharing Regression
Divergence analysis on true/predicted rental counts and regression errors.

* D04 – COMPAS Classification
Subgroup divergence for FPR, FNR, accuracy, and label distributions.

* D05 – Folktables (Census)
Attribute and income divergence across demographic subgroups.

* D06 – Law School Rankings
Score and ranking divergence with local/global Shapley explanations.

* D07 – Comparison with the related work
Comparison with the related work, supplementary tests and extended evaluations.

Each notebook is self-contained and illustrates how to load data, define an outcome function, run DivExplorer, and interpret subgroup divergence results.

