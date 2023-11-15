---
layout: page   # This is required
title: Working With Graphics and Tables   # This is required

order: 70    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Handling graphics using the graphicx packages.

instructors_note: |
  Demonstrate the parts live if possible.
  

  
# These should resolve to files in the supporting_files directory
# or if you specified a different one in _config.yml use that.
# The link_text can be anything you want.
supporting_files:
 - file:
   file_name: /sample_image.png
   link_text: A sample file to use.


---

## Graphics

You can add graphics into your document as shown here.

```latex

\begin{figure}[h]
\centering
\includegraphics[width=1\textwidth]{sample_image}
\caption{Here is my image}
\label{image-myimage}
\end{figure}

```

The first thing to notice is the `[h]` which specifies the placement. **h** 
means to put the figure roughly in this position. Other options include **t** 
for top of the page, **b** bottom of the page and **p** to put it on a 
separate figures page. LaTeX tries to find the "best" place for your figure,
so you can add an exclamation (**h!**) to force it to put the figure more 
exactly in that location.

By default, LaTeX puts a figure on the left, so `\centering` centers the image 
on the page. The include `includegraphics` command specifies the file and. you
can also give a scaling factor. In this case its 1, 0.5 would scale by half.

The figures are captioned in order, and the label allows you to refer to the image 
elsewhere in the document.


## Tables

Below is an example of a table.

```latex

\begin{tabular}{|l|l|}
Apples & Oranges \\
\cline{1-2}
Red & Orange \\
Pome & Citrus \\
\end{tabular}

```

By default, LaTeX doesn't add horizontal or vertical rules. The curly braces
`{|l|l|}` specify to have verticale lines and the contents to be aligned to the
left. You can align to left (l), right (r), center (c) while the vertical pipes
specify vertical rules. 

The next line gives the first row of data, the ampersands `&` delineate the columns. 
The next line `\cline{1-2}` specifies a horizontal line across columns one and two.
`\cline{1-1}` would just put a horizontal rule across the first column. 
Double back slashes `\\` denote new lines.

