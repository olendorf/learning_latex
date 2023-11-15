---
layout: page   # This is required
title: Formatting Mathematical Expressions   # This is required

order: 90    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Learn how to format mathematical expressions and code snippets.

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

## Mathematical Expressions.

Formatting mathematical expressions is one of the big reasons people use LaTeX.
It's a big subject, so we can only touch the surface here. As with most things 
in LaTeX, you will probably need to do some research for your specific needs.
Mathemetical expressions can be either inline or display mode. 

Inline expressions can be delimited in any of these ways.

```latex

\(...\)
$...$
\begin{math}...\end{math}


% example

This is one way to do it \(x^2 + y^2 = z^2\). Here are is another  
$x^2 + y^2 = z^2$ and a third way
\begin{math}
x^2 + y^2 = z^2
\end{math}
shown here.

```

Display mode puts the equation on another line. There are also three ways to
do it.

```latex

\[...\]
\begin{displaymath}...\end{displaymath}
\begin{equation}...\end{equation}

% example

This is one way to do it \[\sqrt{x^2+1}\]. Here are is another  
\begin{displaymath}
\sqrt{x^2+1}
\end{displaymath}
and a third way
\begin{equation}
\sqrt{x^2+1}
\end{equation}
shown here.

```


There are a lot of other characters too. Here is a sample. Note that they MUST
be inside a math expression block.

```latex


Greek Letters
\(\alpha \beta \gamma \rho \sigma \delta \epsilon\)

Binary Operators
\(\times \otimes \oplus \cup \cap\)

Relations
\(< > \subset \supset \subseteq \supseteq\)

Some others
\(\int \oint \sum \prod\)

```

