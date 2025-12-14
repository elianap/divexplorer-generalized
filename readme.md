# DivExplorer – A Generalized Approach to Exploring Subgroup Divergence




DivExplorer is a framework for identifying and interpreting subgroup behavior in data and models.
It applies to:

* Dataset statistics (e.g., attribute means, distributions)
* Classification (labels, predictions, FPR/FNR, accuracy)
* Regression (true/predicted values, error metrics)
* Ranking & scoring functions

It allows data auditing, exploratory slice analysis, model debugging, model inspection, fairness and bias discovery.
The method is **model-agnostic** and **target-agnostic**.


##  Notebooks Overview

This repository includes several Jupyter **notebooks** (D01–D07), each **demonstrating DivExplorer** on a different dataset or task and allowing results reproducibility.

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