---
layout: page   # This is required
title: Paragraphs and Text Formatting   # This is required

order: 60    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Learn how to format paragraphs and format words and sections of text.

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

## Formatting Text

### Colored Text

You can implement colored text using the `color` or `xcolor` package as shown. 
The `xcolor` package supports more colors and flexibility so we'll use that. 
Including the package and using it is show below.

```latex

\documentclass{article}
\usepackage{graphicx} % Required for inserting images
\usepackage{xcolor}

% This adds even more colors and show how to load packages with options
% \usepackage[dvipsnames]{xcolor}.  
...

\begin{document}

...

This demonstrates using the \texttt{color} package. 

\begin{itemize}
\color{ForestGreen}
\item First item
\item Second item
\end{itemize}

\noindent
{\color{RubineRed} \rule{\linewidth}{0.5mm}}

The background colour of text can also be \textcolor{red}{easily} set. For 
instance, you can change use an \colorbox{BurntOrange}{orange background} and then continue typing.
\end{document}




```

### Type Face

Here is how to set the typeface for words.

```latex

\textit{words in italics} 
\textsl{words slanted} 
\textsc{words in smallcaps}
\textbf{words in bold}
\texttt{words in teletype}
\textsf{sans serif words}
\textrm{roman words}
\underline{underlined words}

{\textit Ut consequat semper viverra nam libero justo laoreet sit. Scelerisque 
felis imperdiet proin fermentum leo vel orci porta non. Egestas sed tempus 
urna et pharetra pharetra massa massa. Ipsum nunc aliquet bibendum enim. 
Interdum varius sit amet mattis vulputate enim nulla aliquet. Pretium nibh 
ipsum consequat nisl vel pretium lectus quam id. Auctor urna nunc id cursus.}

```



### Font Size

The default font size for most document classes is 10pts and supports 11pt and 
12pt. You can change the global setting when you define the document class.

```latex

\documentclass[12pt]{article}

 % If you need more than the default font sizes. It allows for the following 
 % font sizes: 8pt, 9pt, 10pt, 11pt, 12pt, 14pt, 17pt, 20pt.
\usepackage{extsizes}.  

```


Within the document you can change the font size relative to the global 
value using the following commands.

```latex

{\tiny tiny words}

{\scriptsize scriptsize words}

{\footnotesize footnotesize words}

{\small small words}

{\normalsize normalsize words}

{\large large words}

{\Large Large words}

{\LARGE LARGE words}

{\huge huge words}

```

## Lists

Numbered, or ordered lists are easy to implement.


```latex

...


\begin{enumerate}
\item First thing
\item Second thing
\begin{itemize}
\item A sub-thing
\item Another sub-thing
\end{itemize}
\item Third thing
\end{enumerate}


...

```

You can also change the bullet symbol as follows. Notice it doesn't have to 
be a symbol, it can be a letter or word.

```latex 

\begin{itemize}
\item[-] First thing
\item Second thing
\begin{itemize}
\item[Fish] A sub-thing
\item[Plants] Another sub-thing
\end{itemize}
\item[Q] Third thing
\end{itemize}

```