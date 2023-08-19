---
title: Install the MDI
parent: Installation
has_children: false
nav_order: 1
---

{% include table-of-contents.md %}

This section describes the paths to installing the MDI itself, 
i.e., the frameworks. It is easy, but there are several ways
to do it. The following are important decision points.

## Stage 1 Pipelines vs. Stage 2 Apps

Review the MDI's 
[analysis stages]({{ "/docs/analysis-flow" | relative_url }})
to decide what kind of tools you seek to run.

If you will run **Stage 1 Pipelines** from the command line of
an HPC server, install and use our 'mdi' utility:

- repository: <https://github.com/MiDataInt/mdi>
- documentation: <{{ "/mdi" | absolute_url }}>

If you will run **Stage 2 Apps** on data generated elsewhere,
including the Pipeline Runner app,
do that on your personal computer using the MDI Desktop (recommended):

- repository: <https://github.com/MiDataInt/mdi-desktop-app>
- documentation: <{{ "/mdi-desktop-app" | absolute_url }}>

or directly within an R console (not recommended for most users):

- repository: <https://github.com/MiDataInt/mdi-manager> 
- documentation: <{{ "/mdi-manager" | absolute_url }}>

or set up a public web server on [Amazon Web Services](https://aws.amazon.com/) (AWS)
using our Amazon Machine Images (AMIs):

- AWS AMIs: [mdi-empty machine images](https://us-east-2.console.aws.amazon.com/ec2/v2/home?region=us-east-2#Images:visibility=public-images;v=3;search=:mdi-empty)
- AMI repository: <https://github.com/MiDataInt/mdi-aws-ami>
- web server repository: <https://github.com/MiDataInt/mdi-web-server>

## Local, Remote, and Public Apps Servers

Stage 1 Pipelines nearly always run on an HPC server as linked above.
However, there are many ways to run a Stage 2 Apps server depending 
on your needs.

### Local mode

In local mode, you run the R Shiny server on your desktop or laptop computer,
which acts as both the web server and client (i.e., browser).

{% include figure.html file="server-modes/local.png" %}

First, you must install R:

- R project via CRAN: <https://cran.r-project.org/>

Then, the best path is to use the MDI Desktop
to install and run the server (recommended):

- MDI Desktop: <https://github.com/MiDataInt/mdi-desktop-app>
- documentation: <{{ "/mdi-desktop-app" | absolute_url }}>

Alternatively, install the MDI from within R as described here (not recommended for most users):

- mdi-manager: <https://github.com/MiDataInt/mdi-manager#installation>
- documentation: <{{ "/mdi-manager" | absolute_url }}>

The advantages of this mode are security and speed.

### Remote modes

You can also use the MDI Desktop to install and run a MDI server
on a remote HPC server, or one of its nodes, with a connection 
over a secure, SSH port tunnel. 
- MDI Desktop: <https://github.com/MiDataInt/mdi-desktop-app>
- documentation: <{{ "/mdi-desktop-app" | absolute_url }}>

{% include figure.html file="server-modes/remote.png" %}  
{% include figure.html file="server-modes/node.png" %}

An advantage of this method is that your apps can have ready access
to the same disk drives as your pipelines.

### Public server mode

As noted above, advanced users can also set up a public Stage 2 web server
using our AWS AMIs:

{% include figure.html file="server-modes/public.png" %}

as described in the following repositories:

- AWS AMIs: [mdi-empty machine images](https://us-east-2.console.aws.amazon.com/ec2/v2/home?region=us-east-2#Images:visibility=public-images;v=3;search=:mdi-empty)
- AMI repository: <https://github.com/MiDataInt/mdi-aws-ami>
- web server repository: <https://github.com/MiDataInt/mdi-web-server>

Here, the main advantage is stable, shared access between many users.
