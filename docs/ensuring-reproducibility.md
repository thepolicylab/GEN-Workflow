---
title: Why should anyone believe our work? 
date: 2020-01-30
slug: ensuring-reproducibility
---

The Policy Lab produces tools, reports, and services in which we aim to empower our governmental collaborators to improve their work and enhance the lives of the public. Given this goal, we strive to ensure that no product relies on any single person in order for use or interpretation.

# Making credible reports of data analyses

We here describe our basic process. We build on the processes of the [Office of Evaluation Sciences](https://oes.gsa.gov/methods/) and the following guides to good data analytic code practice [10 things to know about project workflow](https://egap.org/methods-guides/10-things-workflow) and [How to improve your relationship with your future self](http://www.jakebowers.org/PAPERS/11-BOWERS-RCP-363.pdf).

## No Cutting and Pasting, No step-by-step code execution

Interactivity enhances the process of code writing --- the process of making errors, or of fine tuning graphics or tables, or even of exploring different approaches to the same task. Yet, once the development phase of code creation is over, all scripts that go from raw data to a final table or figure or number must be able to run as a whole workflow from start to finish. In fact, we demand that this whole flow be executable on a fresh computer so that we can be sure that no output depends on idiosyncracies of a given machine or system.

For example, many of our data analysts either use R markdown files using the RStudio IDE or jupyter notebooks using various IDEs (like JupyterLab). Both of these approaches free our analysts to explore and write better code faster than they might have without the interactivity allowed by those tools. Yet, once the development is done both workflows lead to, in essence, one-click execution of sets of linked files. On OS X or Linux, this tends to be the execution from the unix command line of all of the code using the `make` system. But, it may also involve other tools as well.

## (fill in from the above adapting for a policy team oriented approach)

# Making useful and reliable predictive and/or descriptive tools

## How we protect ourselves and collaborators from algorithmic bias

A predictive model can only be trained on past data, often on data collected for purposes other than the ones driving any given current project. A decision-making dashboard or other descriptive tool can only represent categories and flows of work characteristic of the past (or at least categories and work that we can imagine). If tools like these are too change how government works, then we anticipate that this change will in turn change the kinds of data available or at least change the relationships among data elements. No single predictive model can maintain its predictive power let alone its utility over the long run. Thus, we work to build periodic checks into the use of our models --- say, at 6 months, and then every year thereafter. We also strive to build quality checks into the models themselves --- if the model predictions begin to diverge greatly from those using the training data, for example, our tools show alert the users to contact us.

# Code Review and Reanalysis

Every field experiment or observational study that we execute is *preceded by* a [pre-analysis plan](link) so that we and others who want to make decisions based on our work can interpret our results --- namely, we use those plans to clarify what we expected and what we think we have discovered as we explored the data at the end of a study.

Every field experiment or observational study that we execute is *followed by* a reanalysis process whereby experts in causal inference who do not know the outcomes of our study take our raw data and pre-analysis plan and re-analyze the data following that plan. We do this to ensure that any reports we make to decision makers does not contain errors and to ensure that our results do not inadvertently reflect the many decisions made by data analysts when they work from raw data to causal inferences.
