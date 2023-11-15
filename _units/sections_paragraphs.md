---
layout: page   # This is required
title: Sections   # This is required

order: 50    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Learn how to create sections and heading. Learning how to make them numbered
  or unnumbered.

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

## Sections

This template starts us off with an introduction. Let's add the remaining
typical sections for an IMRaD article (Introduciton, Methods, Results, and
Discussion.)

```latex

...

\end{abstract}

\section{Introduction}

\section{Methods}

\section{Results}

\section{Discussion}

\end{document}

```

By default, your section titles will be numbered. You may not want this, but
its easy to remove the numbers.

```latex


...

\end{abstract}

\section*{Introduction}

\section*{Methods}

\section*{Results}

\section*{Discussion}

\end{document}

```

The adding of the asterisk, `\section*`, removes the numbers. You can even 
mix them. There are few, if any, instances where you would want to do this,
but if you mix numbered and unnumbered sections, LaTeX only counts the numbered
, un-asterisked, sections. Asterisked sections don't get counted.

## Subsections

You can add subsections into your document, up to seven levels. As you can see
from below that subsections can also be numbered or unnumbered and follow the
same counting rules.

```latex

...

\end{abstract}

\section{Introduction}

\subsection{Fancy Subsection}

\subsection*{An Unnumbered Subsection}

\subsection{Fancy Subsection Number Two}

\subsection*{An Unnumbered Subsection Two}



\section*{Methods}

\subsection*{Foo}

\subsubsection*{Getting}

\subsubsection*{Deeper}

\subsection*{Bar}

\section{Results}

\section*{Discussion}

\section{Gratuitous}

\end{document}

```

## Paragraphs

There are three ways to make paragraphs as shown below.

```latex

\section{Introduction}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
incididunt ut labore et dolore magna aliqua. Feugiat nisl pretium fusce id 
velit ut tortor pretium. Iaculis urna id volutpat lacus laoreet non curabitur 
gravida. Eu facilisis sed odio morbi quis commodo odio aenean. 
                                                        % Two returns makes 
                                                        % a paragraph
At imperdiet dui accumsan sit amet nulla facilisi morbi tempus. Venenatis lectus 
magna fringilla urna porttitor rhoncus dolor purus non. Auctor eu augue ut lectus 
arcu bibendum at. Non pulvinar neque laoreet suspendisse interdum consectetur 
libero id faucibus. Sem viverra aliquet eget sit. 

Tempor id eu nisl nunc mi ipsum faucibus. Viverra adipiscing at in tellus 
integer feugiat. Auctor augue mauris augue neque gravida. Donec enim diam vulputate 
ut pharetra sit amet aliquam id. Ultricies integer quis auctor elit sed vulputate 
mi sit amet. Fames ac turpis egestas integer eget aliquet. 
diam donec adipiscing tristique risus. Fermentum odio eu 
feugiat pretium nibh. \par                              % \par creates a paragraph
Eu volutpat odio facilisis mauris sit amet massa vitae. Sed velit dignissim 
sodales ut eu sem integer vitae justo. Praesent semper feugiat nibh sed. Nisi 
lacus sed viverra tellus in hac. Id interdum velit laoreet id donec ultrices 
tincidunt arcu. Ac turpis egestas integer eget aliquet nibh praesent tristique 
magna. Enim neque volutpat ac tincidunt vitae semper quis lectus nulla. Odio 
aenean sed adipiscing diam donec adipiscing. Adipiscing elit duis tristique 
sollicitudin. Dignissim diam quis enim lobortis scelerisque fermentum.

\paragraph{Heading}             % \paragraph gives you a heading and more options
Id aliquet risus feugiat in ante metus dictum at tempor. Pulvinar elementum 
integer enim neque volutpat ac tincidunt vitae semper. In nisl nisi scelerisque 
eu ultrices. Libero enim sed faucibus turpis in eu mi bibendum. Enim neque 
volutpat ac tincidunt. Pharetra vel turpis nunc eget lorem. Faucibus turpis 
in eu mi bibendum. Porta nibh venenatis cras sed felis eget velit aliquet. 
Egestas purus viverra accumsan in.

\subparagraph{Sub Paraheading}. % can sub, and subsub (etc) as paragraphs
A diam maecenas sed enim ut sem viverra aliquet eget. Rutrum quisque non tellus 
orci ac. Felis eget velit aliquet sagittis id consectetur purus ut. Faucibus 
ornare suspendisse sed nisi lacus sed viverra tellus in. Ut consequat semper 
viverra nam. Ante in nibh mauris cursus mattis molestie a iaculis at. Aliquam 
id diam maecenas ultricies mi eget mauris pharetra. 

\paragraph{Another Heading}
Ut consequat semper viverra nam libero justo laoreet sit. Scelerisque felis 
imperdiet proin fermentum leo vel orci porta non. Egestas sed tempus urna et 
pharetra pharetra massa massa. Ipsum nunc aliquet bibendum enim. Interdum 
varius sit amet mattis vulputate enim nulla aliquet. Pretium nibh ipsum 
consequat nisl vel pretium lectus quam id. Auctor urna nunc id cursus.

```

The first and easiest way is to just do two returns. This is probably the 
most common way. You can also use `\par` although this is heard to see, so 
its probably not the best way. Using the `\paragraph{}` command gives you 
a paragraph heading and also other options.

## Formatting Paragraphs

### Paragraph Indent

You can alter the in the following ways.

```latex


\setlength{\parindent}{50pt}. % this can really go anywhere, not just before
                              % the document
\begin{document}


...


\noindent At imperdiet dui accumsan sit amet nulla facilisi morbi tempus. 
Venenatis lectus magna fringilla urna porttitor rhoncus dolor purus non. 
Auctor eu augue ut lectus arcu bibendum at.


...


Adipiscing elit duis tristique sollicitudin. Dignissim diam quis enim lobortis 
scelerisque fermentum.

\setlength{\parindent}{0pt}

\paragraph{Heading}
Id aliquet risus feugiat in ante metus dictum at tempor. Pulvinar elementum 
integer enim neque volutpat ac


...


```

### Paragraph Justification

LaTeX justifies both sides by default. The following can change how this 
is handled.

```latex
A diam maecenas sed enim ut sem viverra aliquet eget. Rutrum quisque non tellus 
orci ac. Felis eget velit aliquet sagittis id consectetur purus ut. Faucibus 
ornare suspendisse sed nisi lacus sed viverra tellus in. Ut consequat semper 
viverra nam. Ante in nibh mauris cursus mattis molestie a iaculis at. Aliquam 
id diam maecenas ultricies mi eget mauris pharetra. 

\raggedright
A diam maecenas sed enim ut sem viverra aliquet eget. Rutrum quisque non tellus 
orci ac. Felis eget velit aliquet sagittis id consectetur purus ut. Faucibus 
ornare suspendisse sed nisi lacus sed viverra tellus in. Ut consequat semper 
viverra nam. Ante in nibh mauris cursus mattis molestie a iaculis at. Aliquam 
id diam maecenas ultricies mi eget mauris pharetra. 

\raggedleft
A diam maecenas sed enim ut sem viverra aliquet eget. Rutrum quisque non tellus 
orci ac. Felis eget velit aliquet sagittis id consectetur purus ut. Faucibus 
ornare suspendisse sed nisi lacus sed viverra tellus in. Ut consequat semper 
viverra nam. Ante in nibh mauris cursus mattis molestie a iaculis at. Aliquam 
id diam maecenas ultricies mi eget mauris pharetra. 

\centering
A diam maecenas sed enim ut sem viverra aliquet eget. Rutrum quisque non tellus 
orci ac. Felis eget velit aliquet sagittis id consectetur purus ut. Faucibus 
ornare suspendisse sed nisi lacus sed viverra tellus in. Ut consequat semper 
viverra nam. Ante in nibh mauris cursus mattis molestie a iaculis at. Aliquam 
id diam maecenas ultricies mi eget mauris pharetra. 


```

Unfortunately, you can set the justification but you can't clear it easily.
Most times an entire document will be the same. If you need more control, 
there are packages such as `ragged2e` that provide more flexibility.


## Table of Contents and Page Numbers

You can insert a table of contents and change how numbering occurs as 
follows.

```latex
\maketitle

\pagenumbering{roman}               % roman numeral pages numbers for TOC
\tableofcontents
\newpage                        % Force a new page after the TOC
\pagenumbering{arabic}         % araabic page numbers for the rest

```

Unnumbered sections aren't included by default. You can add them manually 
with this.

```latex

\addcontentsline{toc}{section}{Unnumbered Section}
\section*{Unnumbered Section}

```


