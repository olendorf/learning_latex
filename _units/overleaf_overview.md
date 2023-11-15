---
layout: page   # This is required
title: Using OverLeaf   # This is required

order: 0    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  A brief overview of OverLeaf with demonstrating a first blank document and 
  a templated document.

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

In this first unit, we'll learn the basic usage of OverLeaf and create some 
documents. We'll delve deeper into LaTeX later. In this unit, just try things 
out and get over your fear of making mistakes.

Go to [OverLeaf](https://www.overleaf.com/) and login. If you need to sign up 
for an account do that. You should be on your Home Page and see a **New Project**
button. Click on the **New Project** button and choose a blank project. You
can name it anything you like, but we'll be using *First Project*. Click 
**Create** and you should see something like this.

<figure>
  <img src="{{ site.baseurl }}/assets/img/first_document.png" alt="Just a sample image" style="width: 900px"/>
</figure>

On the left you see the project files over a project outline. In the middle 
is your LateX document with some auto-generated code. On the right is the 
PDF output. There is also a navigation bar on top, some of which we'll 
explore over the course of the tutorial.

Enter some text in your document, making it look as shown, then click the
**Recompile** button. The PDF document should now reflect your changes.

```latex

\title{First Project}
\author{rkolendo }
\date{October 2023}

\begin{document}

\maketitle

This is a line of text.  # Add this

\section{Introduction}

This is another line of text.  # Add this

\end{document}

```

### Exercise

Try adding some more text. Change the data in `\title`, `\author` and `\date`.

## Templates

This is the most basic way to make a document. OverLeaf also has a lot of 
templates you can try. Click on **New Project** again, but this time choose 
**_Templates/View All_**. Then search for *basic journal* and choose
**_Basic Academic Journal Article Template_** from the search results and then
choose **Open As Template**. We'll cover more on templates later, but notice 
there is a lot more text in this document. Most of it is filler text. You are
expected to change the data and text to fit your needs.

Formatting a LaTeX document can be a lot of work. Using templates is a great
time saver, and is also a really good way to learn LaTeX, so even if you don't 
use a given template, you may find it useful to look at them to learn some 
tips and tricks.

### Exercise

Spend some time editing this templated document. Don't worry if you break things.
That is normal, just undo your changes. Make small changes, recompile, then make
more changes.

