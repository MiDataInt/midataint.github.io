---
title: "Michigan Data Interface"
has_children: false
nav_order: 0
---
<!--- edit the title above with the short name of your repository, 
      e.g, "My Pipelines", which will appear on the menu tab item -->

<!-- please do not alter the next line -->
{% include mdi-project-overview.md %} 


These pages describe the MDI project overall.
Links within lead you to documentation for 
specific components of the MDI, e.g., how to get started
[writing your own tool suites]({{ "/docs/project-structure/#suites" | relative_url }}).

## Screenshots

{% include screenshot.html 
   image="stage1-command-line.jpg" 
   caption="Stage 1 pipelines via command line, YAML-based tool and job definition" %}
{% include screenshot.html 
   image="pipeline-runner.jpg" 
   caption="Pipeline Runner web app running Stage 1 pipelines, remote HPC access" %}
{% include screenshot.html 
   image="stage2-apps.jpg" 
   caption="Stage 2 interactive apps via a controlled-access public web server" %}

## Quick Start

Use the following web site to generate a friendly batch script
for your desktop computer, to install and run the MDI ~anywhere.

- <https://wilsonte-umich.shinyapps.io/mdi-script-generator>

Alternatively, follow these instructions to clone the 
MDI manager repository and install the pipeline and app frameworks using R.

- <https://github.com/MiDataInt/mdi-manager#install-the-server-manager-and-framework>

Tool developers should start by copying our suite repository templates.

- <https://github.com/MiDataInt/mdi-pipelines-suite-template>
- <https://github.com/MiDataInt/mdi-apps-suite-template>

## Guiding Principles

Principles guiding development of the MDI are:

- easy, standardized implementation
- simple, effective use of modern development tools
- efficient use of scalable computation resources
- maximum developer flexibility
- rapid collaboration and code sharing
- interactive data analysis

Our goal is to help you develop and share robust
data analysis tools more easily, or to use tools developed by others,
without forcing too many requirements into the process. 

## Basic Training for Developers

This documentation assumes familiarity with open source
code development. Please see our 
[Basic Training](https://midataint.github.io/mdi-basic-training) tutorials 
in the link below if you need help getting started with Git, R,
Shiny, job schedulers, etc.

## Portability and Licensing

As the name implies, the MDI was created to support researchers
at the University of Michigan; a few instructions are specific 
to our environment. However, the MDI codebase is generic and can 
be used by any laboratory or organization under the MIT license.


<!-- please do not alter the next line -->
{% include mdi-project-documentation.md %}
