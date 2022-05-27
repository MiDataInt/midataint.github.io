---
title: Install the MDI
parent: Installation
has_children: false
nav_order: 1
---

{% include table-of-contents.md %}

This section describes the paths to installing the MDI itself, 
i.e., the frameworks. It is easy, but there are many ways
to do it. The following are important decision points.

## Stage 1 Pipelines vs. Stage 2 Apps

Review the MDI's 
[conceptual analysis stages]({{ "/docs/analysis-flow" | relative_url }})
to decide what kind of tools you seek to run.

If you will run **Stage 1 Pipelines** on an HPC server
(and possibly Stage 2 Apps accessed remotely),
use our 'mdi' command line utility:

- repository: <https://github.com/MiDataInt/mdi>
- documentation: <https://midataint.github.io/mdi>

If you will run **Stage 2 Apps** on data generated elsewhere,
do that on your personal computer by generating a
batch script:

- batch scripts: <https://wilsonte-umich.shinyapps.io/mdi-script-generator>

or set up a public web server on [Amazon Web Services](https://aws.amazon.com/) (AWS)
using our Amazon Machine Images (AMIs):

- AWS AMIs: [mdi-empty machine images](https://us-east-2.console.aws.amazon.com/ec2/v2/home?region=us-east-2#Images:visibility=public-images;v=3;search=:mdi-empty)
- repository: <https://github.com/MiDataInt/mdi-aws-ami>
- documentation: pending

## Local, Remote, and Public Apps Servers

Stage 1 Pipelines nearly always run on an HPC server as linked above.
However, there are many ways to run a Stage 2 Apps server depending 
on your needs.

### Local mode

In local mode, you run the R Shiny server on your desktop or laptop computer,
which acts as both the web server and client (i.e., browser).

First, you must install R:

- R project: <https://www.r-project.org/>

Then, the best path is to generate a custom batch script
to install and run the server:

- batch scripts: <https://wilsonte-umich.shinyapps.io/mdi-script-generator>

Alternatively, install the MDI from within R as described here:

- mdi-manager: <https://github.com/MiDataInt/mdi-manager#installation>

### Remote modes

In local mode, PENDING.

### Public server mode

Finally, PENDING.
