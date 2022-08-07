---
title: "Michigan Data Interface"
has_children: false
nav_order: 0
---

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

Install the **MDI Desktop**, a program that helps you connect to a server as needed and run MDI tools from your Windows or Mac computer:

- [Install the MDI Desktop on your PC](/mdi-desktop-app/docs/installation)

Alternatively, follow these instructions to clone and run command-line 
scripts that will install the MDI on an **HPC server**:

- [Install the MDI CLI on an HPC server](/mdi/docs/installation)

Tool developers should start by copying our **repository suite template**
and following its [documentation](/mdi-suite-template):

- [Create a new tool suite from the template](https://github.com/MiDataInt/mdi-suite-template/generate)

### Guiding Principles

- effective use of modern development tools
- optimal use of scalable computation resources
- rapid collaboration and code sharing
- interactive data analysis
- standardized implementation frameworks
- maximum developer flexibility

Our goal is to help you develop and share robust
data analysis tools more easily, or to use tools developed by others,
without forcing too many requirements into the process. 

### Basic Training for Developers

Please see our 
[Basic Training](https://midataint.github.io/mdi-basic-training) tutorials 
in the link below if you need help getting started with Git, R,
Shiny, the command line, job schedulers, etc.

### Portability and Licensing

The MDI can 
be used by any laboratory or organization for any data analysis need
under the MIT license (a few instructions 
are specific to the University of Michigan environment but the codebase
is generic).

<!-- please do not alter the next line -->
{% include mdi-project-documentation.md %}
