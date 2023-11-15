---
layout: page   # This is required
title: Parts of LaTeX and OverLeaf   # This is required

order: 20    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Gives an overview of the main parts of a LaTeX System and Document. Also 
  describes the layout and parts of OverLeaf.

instructors_note: |
  Demonstrate the parts live if possible.
  

  
# These should resolve to files in the supporting_files directory
# or if you specified a different one in _config.yml use that.
# The link_text can be anything you want.
# supporting_files:
#   - file:
#     file_name: first_example_file.txt
#     link_text: Example file  for this unit.
#   - file:
#     file_name: another_example_file.png
#     link_text: Example image for this unit.

---

## LaTeX Document

The part you will interact most often with is the LaTeX Document. These are 
normal text documents with a `.tex` rather than `.txt` extension. You can
read and edit them fine with the `.txt` extension but the LaTeX compilers
won't know what to do with it.

A typical LaTeX Document can have lots of parts or sections. Many of which 
we will cover in later units. All LaTeX documents require three parts, or 
two parts, depending how you think of things. A `documentclass` a 
`begin{document}` and an `end{document}`. If you want to be a stickler, there
is a fourth part...the text content.

To get started, click the **New Project** button on the upper left, then
choose **Blank Project**. Oddly enough, in OverLeaf, this is not blank. Delete
everything and type in the text below. Click the **Complile** or **Recomplile**
button on the left side, and you should see a very simple PDF file displayed.

Everything between the `\documentclass` and the `\begin{}` is called the 
**preamble**. This contains various global formatting commands and also 
metadata about the document such as the title, authors and date.

```latex


    \documentclass{article}
    \usepackage{graphicx} % Required for inserting images
    
    \title{My Document}
    \author{Random Citizen }
    \date{October 31, 2023}
    
    \begin{document}
    
    \maketitle
    
    \section{Introduction}
    
    \end{document}

```

## The Compiler

The thing that converts the LaTeX document into a PDF is called a compiler. We
used it in the last step to create our first document. There are, in fact, many
compilers. If you click the **Menu** button on the top left, you will get the
various settings for OverLeaf. The first setting is the compiler. You can choose
between a few. Normally you can just ignore this option and the default is fine.
Sometimes, switching the compiler you use can make a failing document into one
that successfully compiles. Try switching compilers and see if anything changes.


## LaTeX Classes

In our first document, we defined the `Document Class` as an `article`, which 
means that it intended to be formatted like a research article. This is probably
the most commonly used class but LaTeX also defines `book`, `report`, and `letter`,
by default. These are fairly self explanatory. You will often see `slides`, which 
are great for creating presentation slides. There are some other rarely used classes,
if you find yourself needing one of these, just take some time to read about it first.

Sometimes you will see a class file included in a project. These are for when 
none of the available classes suit your needs. You (or more likely someone else)
can write a class file that modifies an existing class or creates an entirely 
new one.

To use a class you add the file to your directory structure, then call the class
`\documentclass{my_class}`.

## LaTeX Packages

If you go back and create a new blank project, which isn't actually blank, and 
don't delete anything you will see a few more things. The first are packages. 
Packages are a little like classes. However, while classes generally create 
or modify classes, packages add functionality to the document. You will
use packages a lot more than classes. In the sample document we invoke the 
**graphicx** class using `\usepackage{graphicx}`. This is a very commonly used
package. 

## LaTeX Commands

We have been using commands all along, although we have avoided referring to them
as such. In LaTeX commands are used to format and structure your document. 
Everything that starts with a backslash, '\\' is a command. The typical structure
for a command is `command_name[optional, arguments]{required, arguments}` for 
instance...

``` latex

    \documentclass[a4paper,11pt]{book} // optional and required arguments
    \begin{document}                   // required arguments
    \maketitle                         // no arguments
    
```

## Content

The final and easiest part of LaTeX is the content. This is just the stuff
you write that will be displayed.


