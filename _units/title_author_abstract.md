---
layout: page   # This is required
title: Titles Pages, Abstracts   # This is required

order: 40    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Shows how abstracts and keywords are added to the article class.

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

## Abstract and Keywords

We'll primarily work with a single blank template for this tutorial. Make a new
blank project. You should get a document that looks something like below.

```latex

\documentclass{article}
\usepackage{graphicx} % Required for inserting images

\title{New Project}
\author{rkolendo }
\date{November 2023}

\begin{document}

\maketitle

\section{Introduction}

\end{document}


```

Overleaf probably already converted your document into a PDF, if not click
the **Recompile** button. Edit the document to reflect the title, author, and 
date of your choice and recompile. Below is our tutorial document.


```latex

\documentclass{article}
\usepackage{graphicx} % Required for inserting images

\title{My Impactful Research}
\author{Random Citizen}
\date{November 23, 2023}

\begin{document}

\maketitle

\section{Introduction}

\end{document}

```

The Author, Title and Date fields can be formatted as needed. For instance, if 
you have multiple authors and adding contact emails you can do the following.

```latex

\documentclass{article}
\usepackage{graphicx} % Required for inserting images

\title{My Impactful Research}
\author{
    Random Citizen\\                      % This is a comment.
    \texttt{rcitizen@example.com}\\  \\   % Try adding the \and command between
    Professor Chaos\\.                    % Authors, on a new line, rather than
    \texttt{drchaos@example.com}.         % the double line return. 
}
\date{November 23, 2023}

\begin{document}

\maketitle

\section{Introduction}

\end{document}

```
Similar formatting can be used for the title and date as well. Note that
the double backslash `\\` creates a linebreak. Also notice the documentation
using the percent character `%`. Everything on the line after the `%` is ignored.
In this case, its describing using the `\and` command to get a different 
formatting. This was discovered as we googled stuff for this tutorial! It's
a good idea to do a lot of internet searches.

We can also add an abstract to your article as follows.

```latex

\documentclass{article}
\usepackage{graphicx} % Required for inserting images

\title{My Impactful Research}
\author{
    Random Citizen\\                      % This is a comment
    \texttt{rcitizen@example.com} \\ \\
    Professor Chaos\\
    \texttt{drchaos@example.com}
}
\date{November 23 2023}

\begin{document}

\maketitle

\begin{abstract}
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis 
    nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu 
    fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in 
    culpa qui officia deserunt mollit anim id est laborum.
\end{abstract}

\section{Introduction}

\end{document}

```

We are off to a great start! Next we'll look into sections.



