---
title: Installation
has_children: true
nav_order: 30
---

As described under
[MDI project structure]({{ "/docs/project-structure" | relative_url }}), 
using the MDI requires access to both:
- the project frameworks
- the tool suites you'd like to use

## Multi-suite installation

We recommend the flexibility of an 'mdi-centric'
installation, which allows you to run many tool suites from one installation.
The installation sequence is:

1. install the MDI
2. load tools suites into your installation

Please see the corresponding tabs at the left for details.

## Single-suite installation

You can also run just one tool suite from
its own 'suite-centric' installation. Doing so is marginally easier 
since the MDI frameworks and tool suite are installed together, 
but you might end up with multiple parallel installations. 
Here, the installation sequence is:

1. clone the tool suite repository
2. run the suite's <code>install.sh</code> script

Details will be provided on the GitHub and/or documentation
page of the suite you wish to use.
