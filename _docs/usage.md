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

- https://midataint.github.io/mdi

## Stage 2 Apps

Once you have successfully loaded the MDI apps interface
in your web browser, you simply need to load the data
package created by an appropriate Stage 1 Pipeline, which 
always ends in **mdi.package.zip**. 

Our demo app provides a simple working example - the
access key is 'mdi-demo'.

- <https://mdi-demo.wilsonte-umich.io>

It is difficult to provide a lot of details beyond that
since every app will be different.  However, here are a few
patterns to understand.

### App analysis steps

MDI apps are designed to have a stepwise execution according
to the tabs on the left of the screen. You usually want
to work through them in order (but can always go back).

### Multiple parallel analyses

Many MDI apps are designed to allow you to load multiple data
packages at once and to use our sample assignment grid 
to create comparisons within and between data sets. 

### Settings (gear) and other useful icons

Apps often have many features "hiding" behind various icons.
Click away, you can't really break anything. The point of Stage 2 Apps
is to be interactive, so ... interact!

### Save bookmark files!!

A critical feature of the MDI is that you can save the state
of the app to reload later.  While the initial incoming 
data files are called 'packages', the work within an app
is saved as a 'bookmark' file using the link on the left of page.

Bookmark files end with '.mdi'. After saving one, you simply load it
at the starting page instead of a data package. You will pick up
where you left off when you saved the file.

Bookmarks are an extremely useful way to preserve the stage of
and app that generated a figure for a manuscript, etc. You
can also reload an old bookmark to add new data to it, etc.

## Tool suite development

The following link provides a detailed description of how
to use our tool suite repository template to create your own tools:

- < {{ "/mdi-suite-template" | relative_url }} >
- {{ "/mdi-suite-template" | relative_url }}
- <{{ "/mdi-suite-template" | absolute_url  }}>
- {{ "/mdi-suite-template" | absolute_url }}
