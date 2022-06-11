---
title: "Michigan Data Interface"
has_children: false
nav_order: 0
---

{{ site.pages | inspect }}
{% for pg in site.pages %}

{{ pg | inspect }}

{% endfor %}


<!-- please do not alter the next line -->
{% include mdi-project-overview.md %} 


These pages describe the MDI project overall.
Links within lead you to documentation for 
specific components, e.g., how to get started
[writing your own tool suites]({{ "/docs/project-structure/#tool-suites" | relative_url }}).

### Screenshots

{% include screenshot.html 
   image="stage1-command-line.jpg" 
   caption="Stage 1 pipelines via command line, YAML-based tool and job definition" %}
{% include screenshot.html 
   image="pipeline-runner.jpg" 
   caption="Pipeline Runner web app running Stage 1 pipelines, remote HPC access" %}
{% include screenshot.html 
   image="stage2-apps.jpg" 
   caption="Stage 2 interactive apps via a access-controlled public web server" %}

### Live Demo

To try out 
[this repository's](https://github.com/MiDataInt/demo-mdi-tools)
 **live demo app server**:

- go to: <https://mdi-demo.wilsonte-umich.io/>
- enter the access key: <code>mdi-demo</code>
- click <code>Load from Server</code> and select a data package or bookmark to load

### Quick Start

Follow these instructions to clone and run the script that 
will **install the MDI** frameworks and your tool suites of interest
on an HPC server:

- <https://github.com/MiDataInt/mdi#install-the-mdi-frameworks> 
([documentation](/mdi/docs/installation.html))

Alternatively, use this web site to generate a custom **batch script** for your 
desktop computer, e.g., to control a remote MDI installation or run apps locally:

- <https://wilsonte-umich.shinyapps.io/mdi-script-generator>

Tool developers should start by copying our **repository suite template**
and following its [documentation](/mdi-suite-template).

- <https://github.com/MiDataInt/mdi-suite-template>

### Guiding Principles

- easy, standardized implementation
- simple, effective use of modern development tools
- efficient use of scalable computation resources
- maximum developer flexibility
- rapid collaboration and code sharing
- interactive data analysis

Our goal is to help you develop and share robust
data analysis tools more easily, or to use tools developed by others,
without forcing too many requirements into the process. 

### Basic Training for Developers

This documentation assumes familiarity with open source
code development. Please see our 
[Basic Training](https://midataint.github.io/mdi-basic-training) tutorials 
in the link below if you need help getting started with Git, R,
Shiny, job schedulers, etc.

### Portability and Licensing

The MDI was created to support researchers
at the University of Michigan and a few instructions are specific 
to our environment. However, the codebase is generic and can 
be used by any laboratory or organization for any data analysis need
under the MIT license.


<!-- please do not alter the next line -->
{% include mdi-project-documentation.md %}
