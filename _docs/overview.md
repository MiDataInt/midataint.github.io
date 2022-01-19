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
   caption="Stage 2 interactive apps via a access-controlled public web server" %}

## Quick Start

To see 
[this](https://github.com/MiDataInt/demo-mdi-tools)
 **live demo** app server in action:

- go to: <https://mdi-demo.wilsonte-umich.io/>
- enter the access key: <code>mdi-demo</code>
- click <code>Load from Server</code> and select a data package or bookmark to load

Follow the instructions at this link to clone and run the helper script that 
will **install the MDI** frameworks and your tool suites of interest.

- <https://github.com/MiDataInt/mdi#install-the-mdi-frameworks>

Alternatively, use the following web site to generate a friendly, customized **batch script** for your desktop computer, e.g., to install and run the MDI remotely.

- <https://wilsonte-umich.shinyapps.io/mdi-script-generator>

Tool developers should start by copying our **repository suite template**.

- <https://github.com/MiDataInt/mdi-suite-template>

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
be used by any laboratory or organization for any data analysis need
under the MIT license.


<!-- please do not alter the next line -->
{% include mdi-project-documentation.md %}
