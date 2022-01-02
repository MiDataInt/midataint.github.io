---
title: Project Structure
has_children: false
nav_order: 3
---

{% include table-of-contents.md %}

## Overview

The MDI codebase is organized into modular GitHub repositories
that provide ease and flexibility for end users and developers.
They separate functions from each other to allow users to access 
&ndash; and developers to work on &ndash; 
the tools most relevant to them.

The following diagram illustrates the overall project structure.

![Repository Structure]({{ "/assets/images/repo_structure_tool_suites_cropped.jpg" | relative_url }})

## Installation and Management Utilities

The MDI Manager is an R package that provides a few simple commands to 
_install()_ pipelines and apps and _run()_ the web interface. 
The concept is similar to the BiocManager utility of the 
[Bioconductor project](https://www.bioconductor.org/). 

The MDI Installer is a distinct wrapper utility that makes it
incrementally easier to run the manager utility. It also provides
a streamlined, non-R installation alternative for people who will only 
use Stage 1 pipelines, skipping the slower installation of Stage 2 
R Shiny apps when they aren't needed. 

Another alternative for simplifying MDI installation and management is the 
[MDI script generator site](https://wilsonte-umich.shinyapps.io/mdi-script-generator)
which helps users create customized batch scripts for their local computer 
to install, control, and use the MDI in both local and remote installations.

These are the repositories for the MDI installation and management utilities:  

- <https://github.com/MiDataInt/mdi>
- <https://github.com/MiDataInt/mdi-manager>
- <https://github.com/MiDataInt/mdi-script-generator.git>

## Frameworks

The MDI framework repositories help run Stage 1 Pipelines and Stage 2 Apps by 
providing code and functions that are common and useful across many tools. 
They are the foundational building blocks that make it much easier to quickly 
develop new tools. As illustrated above, there are two separate frameworks, 
one for Stage 1 pipelines and one for Stage 2 apps. 

The pipelines and apps frameworks are maintained by the MDI as open source
projects that you are invited to help build and improve. These are the
repositories for the pipelines and apps frameworks:

- <https://github.com/MiDataInt/mdi-pipelines-framework>
- <https://github.com/MiDataInt/mdi-apps-framework>

Most users will simply install the frameworks using the installer or manager and not 
think about them further.

## Tool Suites

The code that does the specific work of a pipeline or app is found in an 
MDI tool suite repository. Tools suites are developed by anyone, such as a core 
facility, research laboratory, or funded project. We encourage you to make your 
suite repositories public as open source code, which makes it easy to publish
work performed with those tools. However, you can develop and use private 
suites if you provide a token that allows access to their repositories. 

A suite, i.e., repository, might hold only one pipeline or app,
but we encourage you to combine multiple related tools into a single suite
as makes sense for your activities. For example, a research laboratory
might combine its machine learning tools into a single suite
to make it easy for users to access them in a unified manner.
Creating suites also makes it easy to share modular code between tools. 

We provide mechanisms for you 
to register your suite with the MDI and will engage in a basic level
of review to ensure that your code is well constructed, appropriate, and
not nefarious. Such audited suites from trusted developers can be advertised to users.

It is easy to get started building your own tool
suites using the following template repository:

- <https://github.com/MiDataInt/mdi-suite-template>

## Command Line Utility

Once a user has called the manager's _install()_ function,
they can run Stage 1 Pipelines using the 'mdi' command line utility
that was installed as part of the pipelines framework.
This single wrapper utility provides a 
[unified method of executing and monitoring pipelines]({{ "/assets/images/screenshots/stage1-command-line.jpg" | relative_url }}). 
It is one of the many advantages of adding your pipeline to an MDI suite.

In remote usage modes, Stage 1 Pipelines can also be run in the 
[web interface's Pipeline Runner app]({{ "/assets/images/screenshots/pipeline-runner.jpg" | relative_url }}),
which calls 'mdi' on your behalf. 

## Documentation

The MDI helps developers maintain robust, standardized documentation for all 
project-associated code using GitHub features including README.md files and 
[GitHub Pages](https://pages.github.com/).
The following are the repositories for this documentation site,
our basic training tutorials, and the MDI 
[Jekyll](https://jekyllrb.com/)
documentation themes and templates. 
The latter are also built into the suite template, above.

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

