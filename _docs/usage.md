---
title: Usage
has_children: false
nav_order: 40
---

{% include table-of-contents.md %}

Now that you have successfully installed the MDI, 
you will likely want to do two things, in order:

1. run a Stage 1 Pipeline on an HPC server
2. load and visualize the output from step 1 in a Stage 2 App

Developers will also want to write their own pipelines and apps.

## Stage 1 Pipelines

You run MDI data analysis pipelines using the 'mdi' 
command line utility. Its usage is described in detail
at the link below, including how to write effective
job configuration files. 

- <{{ "/mdi" | absolute_url }}>

{% include figure.html file="command-line/mdi.png" %}

Alternatively, the Pipeline Runner app provides a graphical interface 
to construct, run, and monitor the status of pipelines jobs. 
The best way to use it is via the MDI Desktop via an SSH connection:

- <{{ "/mdi-desktop-app" | absolute_url }}>

{% include figure.html file="screenshots/pipeline-runner.jpg" %}

## Stage 2 Apps

Once you have successfully loaded the MDI apps interface
in a web browser, you simply load the data
package created by an appropriate Stage 1 Pipeline, which 
always ends in **mdi.package.zip**. 

Our demo app provides a simple working example - the
access key is 'mdi-demo'.

- <https://mdi-demo.wilsonte-umich.io>

It is difficult to provide more details here
since every app will be different.  However, here are a few
patterns to understand.

### App analysis steps

MDI apps are designed to have a stepwise execution according
to the tabs on the left of the screen. You usually want
to work through them in order (but can always go back).

{% include figure.html file="app-features/step-tabs.png" border=true width="600px" %}

### Settings (gear) and other useful icons

Apps often have many features "hiding" behind various icons, like the 
settings gear icon seen above.
Click away, you can't really break anything. The point of Stage 2 Apps
is to be interactive, so ... interact!

### Save bookmark files!!

A critical feature of the MDI is that you can save the state
of the app to reload later.  While the initial incoming 
data files are called 'packages', the work within an app
is saved as a 'bookmark' file using the link on the left of page 
(see screenshot above).

Bookmark files end with '.mdi'. After saving one, you simply load it
at the starting page instead of a data package. You will pick up
where you left off when you saved the file.

Bookmarks are extremely useful for preserving the state of
an app that generated a figure for a manuscript, etc. You
can also reload an old bookmark to add new data to it, etc.

### Multiple parallel analyses

Many MDI apps are designed to allow you to load multiple data
packages at once using the launcher interface:

{% include figure.html file="app-features/data-sources.png" %}

and to use the sample assignment grid and other tools
to create comparisons within and between data sets 
for maximum versatility in data analysis: 

{% include figure.html file="app-features/selection-grid.png" %}

## Tool suite development

The following links provide detailed descriptions of how
to use our tool suite repository template 
and frameworks to create your own tools:

- <{{ "/mdi-suite-template" | absolute_url  }}>
- <{{ "/mdi-pipelines-framework" | absolute_url  }}>
- <{{ "/mdi-apps-framework" | absolute_url  }}>
