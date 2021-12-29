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
[writing your own tool suites](https://midataint.github.io/docs/project-structure/#suites).

## Screenshots

The following static images provide a quick visual orientation to the MDI.

<div style="width: 30%; display: inline-block;">
      <a width="100%" href="{{ "/assets/images/stage1-command-line-screenshot.jpg" | relative_url }}"><img src="{{ "/assets/images/stage1-command-line-screenshot.jpg" | relative_url }}"</a>
      <p>Stage 1 pipelines via command line, YAML-based tool and job definitions</p>
</div>
<div style="width: 30%; display: inline-block;">
      <a width="100%" href="{{ "/assets/images/stage1-apps-screenshot.jpg" | relative_url }}"><img src="{{ "/assets/images/stage1-apps-screenshot.jpg" | relative_url }}"</a>
      <p>Stage 2 interactive apps via a public, limited access web server</p>
</div>

## Quick Start

Use the following web site to generate a friendly batch script
for your desktop computer, which you can use to install and run the MDI.

- <https://wilsonte-umich.shinyapps.io/mdi-script-generator>

Alternatively, follow these instructions to clone the 
MDI manager repository and install the pipeline and app frameworks.

- <https://github.com/MiDataInt/mdi-manager#install-the-server-manager-and-framework>

Developers should start by copying our repository templates.

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

Our goal is to help you develop and share
data analysis tools more easily, or to use tools developed by others,
without forcing too many requirements into the process. 

## Basic Training

This documentation assumes familiarity with open source
code development. Please see our Basic Training tutorials
in the link below if you need help getting started with Git, R,
Shiny, job schedulers, etc.

## Portability

As the name implies, the MDI was started to support researchers
at the University of Michigan; a few instructions will be specific 
to our environment. However, the MDI codebase is generic and can 
be used by any laboratory or organization under the MIT license.


<!-- please do not alter the next line -->
{% include mdi-project-documentation.md %}
