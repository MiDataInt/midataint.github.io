---
title: Analysis Stages
has_children: false
nav_order: 1
---

{% include table-of-contents.md %}

## Overview

The MDI manages data analysis flow in two stages with different handling, as depicted below. 

![Analysis Flow]({{ "/assets/images/analysis-flow.png" | relative_url }})

The critical distinctions between Stage 1 Pipelines and Stage 2
Apps are enumerated below. Users and developers may be interested in 
working with either or both stages depending on their needs.

## Stage 1: HPC Pipelines

We use 'pipeline' synonymously with 'workflow' to refer to a series of analysis 
actions coordinated by scripts. Stage 1 pipelines are generally:

- sample autonomous, i.e., they are executed "per sample"
- executed once on an input data set, not iteratively
- executed the same way on every sample, regardless of the experiment
- hands-off, i.e., not interactive
- resource intensive, in storage and/or CPU needs
- executed on a high-performance computing (HPC) cluster
- dependent on large input data files
- capable of producing smaller output data files

The above properties make Stage 1 pipelines well suited to being run by a core facility 
or data producer according to agreed upon best practices. They are also ideal for a 
cluster server, which the 'mdi' command line utility helps manage.

Examples of Stage 1 pipeline actions are bulk image processing, 
training of machine learning algorithms, and read alignment to a genome.

The pipelines framework does not encode data analysis pipelines themselves, 
which are found in other code repositories called 'tool suites'. 
Instead, the framework encodes script utilities that:

- allow YAML configuration files to be used to define a pipeline
- wrap pipelines in a common command-line executable function
- coordinate pipeline job submission to HPC schedulers

## Stage 2: Visualization Apps

Once data are processed by pipelines, Stage 2 applications, or "apps",
support interactive, graphical data visualization characterized by:

- lower resource needs
- execution by end users via a web interface
- iterative execution, with adjustments for hypothesis testing, etc.
- execution per sample set, project, etc. (i.e., multiple samples)
- a need for the user’s detailed knowledge of the project
- common analytical approaches applied to variable study designs
- smaller processed data files as input
- publication-ready images and other files as output

Examples of Stage 2 apps are R Shiny web tools that make
interactive graphs and tables. Once again, the MDI framework does not
carry the tools themselves, it provides a common web interface
where all MDI apps can be easily loaded. Developers provide apps 
within their tool suites.
