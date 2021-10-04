---
title: Project Structure
has_children: false
nav_order: 3
---

{% include table-of-contents.md %}

## Overview

The MDI codebase is organized into modular GitHub repositories
that provide ease and flexibility for end users and developers.
They separate functions from each other
to allow users to access, and developers to work on, the tools 
that are the most relevant to them.

The following diagrams illustrate the overall project structure.
See below for a description of each component.

![Repository Structure]({{ "/assets/images/repo_structure_1.jpg" | relative_url }})

## Manager Utility

The MDI Manager utility is an R package that provides a few simple
commands that allow users to _install()_ the pipelines and apps 
and _run()_ the web interface. The concept is similar 
to the BiocManager utility of the 
[Bioconductor project](https://www.bioconductor.org/). 

The manager is required to properly run the R Shiny-based Stage 2 Apps.
It is not required to run the Stage 1 Pipelines if a user
manually clones the needed repositories, but the manager will manage
all repository cloning and management for you and is recommended. 

## Command Line Utility

Once a user has called the manager utility's _install()_ function,
they will run Stage 1 Pipelines using the 'mdi' command line utility
that was installed by the manager as part of the pipelines framework.
This single wrapper utility provides a unified method of executing and 
monitoring all pipelines, plus some additional functions.
It is one of the many advantages of adding your pipeline to a pipelines suite.

In certain usage modes, Stage 1 Pipelines can also
be run in the web interface, which calls 'mdi' on your behalf. 

## Frameworks

The MDI framework repositories provide the code that helps you
run the Stage 1 Pipelines and Stage 2 Apps, and also to develop
new pipelines and apps, by providing code and functions that are common and 
useful across many or most tools. For example, the 'mdi' command line utility
is part of the pipelines framework. As illustrated above, there are
two separate frameworks, one for pipelines and one for apps. 

The pipelines and apps frameworks are maintained by the MDI, but are open source
projects that you are invited to help build and improve.

## Suites

The code that does the main work in a pipeline or app
is found in Stage 1 and Stage 2 'suite' repositories. 
Similar to the frameworks, and in keeping with the MDI's overall design,
pipelines and apps are managed in separate suite repositories.

Pipelines and apps suites are developed by anyone, such as a core facility,
research laboratory or funded project. We encourage you to make your suite
repositories public as open source code, which makes it very easy to publish
work you did using those tools. However, you can develop and use private suites
as long as you provide a token to allow you to access those repositories. 

A suite, i.e., repository, could hold only one pipeline or app,
but we encourage you to combine multiple related tools into a single suite
as makes sense for your activities. As one example, a research laboratory
might combine its machine learning tools into a single pipelines suite
to make it easy for user's to access them all in a unified manner.
Creating pipelines and apps suites also makes it easy for you to share
modular code across many tools in your suite. 

When you develop a tool suite, the MDI provides a mechanisms for you 
to register your suite with the MDI, who will engage in a basic level
of code review to ensure that it is well constructed, appropriate, and
not nefarious. Such audited suites will be advertised within the frameworks.
You can also share your suites within a smaller group as you wish.
