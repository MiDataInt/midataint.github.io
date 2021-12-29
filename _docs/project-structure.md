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
most relevant to them.

The following diagram illustrates the overall project structure.
See below for a description of each component.

![Repository Structure]({{ "/assets/images/repo_structure_1.jpg" | relative_url }})

## Manager Utility

The MDI Manager is an R package that provides a few simple
commands to _install()_ the pipelines and apps 
and _run()_ the web interface. The concept is similar 
to the BiocManager utility of the 
[Bioconductor project](https://www.bioconductor.org/). 

The manager is required to run the R Shiny-based Stage 2 Apps.
It is not strictly required to run the Stage 1 Pipelines if a user
manually clones all needed repositories, but greatly assists
repository management and is strongly recommended. 

This is the repository for the MDI manager utility:  

- <https://github.com/MiDataInt/mdi-manager>

## Command Line Utility

Once a user has called the manager's _install()_ function,
they will run Stage 1 Pipelines using the 'mdi' command line utility
that was installed by the manager as part of the pipelines framework.
This single wrapper utility provides a unified method of executing and 
monitoring all pipelines. It is one of the many advantages of adding 
your pipeline to an MDI suite.

In certain usage modes, Stage 1 Pipelines can also be run in the 
web interface's Pipeline Runner app, which calls 'mdi' on your behalf. 

## Frameworks

The MDI framework repositories provide the code that helps you
run the Stage 1 Pipelines and Stage 2 Apps, and also to develop
new pipelines and apps, by providing code and functions that are common and 
useful across many tools. For example, the 'mdi' command line utility
is part of the pipelines framework. As illustrated above, there are
two separate frameworks, one for pipelines and one for apps. 

The pipelines and apps frameworks are maintained by the MDI as open source
projects that you are invited to help build and improve. These are the
repositories for the pipelines and apps framework repositories:

- <https://github.com/MiDataInt/mdi-pipelines-framework>
- <https://github.com/MiDataInt/mdi-apps-framework>

Most users will simply install the frameworks using the manager and not 
think about them further.

## Suites

The code that does the main work of a pipeline or app
is found in Stage 1 and Stage 2 'suite' repositories. 
Similar to the frameworks, and in keeping with the MDI's project design,
pipelines and apps are managed in separate suite repositories.

Pipelines and apps suites are developed by anyone, such as a core facility,
research laboratory, or funded project. We encourage you to make your suite
repositories public as open source code, which makes it easy to publish
work you performed with those tools. However, you can develop and use private 
suites if you provide a token to allow you to access those repositories. 

A suite, i.e., repository, might hold only one pipeline or app,
but we encourage you to combine multiple related tools into a single suite
as makes sense for your activities. For example, a research laboratory
might combine its machine learning tools into a single pipelines suite
to make it easy for users to access them in a unified manner.
Creating pipelines and apps suites also makes it easy to share
modular code between many tools. 

We provide mechanisms for you 
to register your suite with the MDI and will engage in a basic level
of review to ensure that your code is well constructed, appropriate, and
not nefarious. Such audited suites will be advertised to users.
You can also share your suites within a smaller user group as you wish.

It is easy to get started building your own pipelines and apps
suites using the following repository suite templates:

- <https://github.com/MiDataInt/mdi-pipelines-suite-template>
- <https://github.com/MiDataInt/mdi-apps-suite-template>

## Documentation

The MDI helps developers maintain
robust, standardized documentation for all project-associated code.
The following are the repositories for this documentation site,
our basic training tutorials, and the MDI documentation themes and templates. 
The latter are also built into the suite templates above.

- <https://github.com/MiDataInt/midataint.github.io.git>
- <https://github.com/MiDataInt/mdi-basic-training.git>
- <https://github.com/MiDataInt/mdi-documentation-template.git>
- <https://github.com/MiDataInt/just-the-docs-mdi.git>

## Public Server Support

The MDI runs equally well on many computer infrastructures.
The following repositories help you quickly create a publicly addressable 
MDI server installation using 
[Amazon Web Services](https://aws.amazon.com/). 

- <https://github.com/MiDataInt/mdi-web-server.git>
- <https://github.com/MiDataInt/mdi-aws-ami.git>
- <https://github.com/MiDataInt/mdi-script-generator.git>
