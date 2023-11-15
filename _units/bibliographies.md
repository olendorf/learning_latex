---
layout: page   # This is required
title: Bibliographies   # This is required

order: 80    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  Creating Bibliographies using BibTeX

instructors_note: |
  Demonstrate the parts live if possible.
  

  
# These should resolve to files in the supporting_files directory
# or if you specified a different one in _config.yml use that.
# The link_text can be anything you want.
supporting_files:
  - file:
    file_name: sample_bib.bib
    link_text: Sample BibTeX file.
  - file:
    file_name: nature.zip
    link_text: Nature Template and Bibliography Style

---

## Bibliographies

### BibTeX

The first step in creating a bibliography is to create a BibTeX data base.
There is a small sample file is provide in the supporting_files. If you open
 it with any text editor, you will see that it is just a formatted text file, 
 where the entries look something like this.
 
 ```
 @article{2151372020110601,     % <- this is the citation id
   abstract = {Previous behavioral studies have shown that individuals with 
               autism are less hindered by interference from global processing 
               during the performance of lower-level perceptual tasks, such as 
               finding embedded figures. The primary goal of this study was to 
               examine the brain manifestation of such atypicality in 
               high-functioning autism using fMRI. Fifteen participants with 
               high-functioning autism and fifteen age- and IQ-matched typical 
               controls were asked to perform a lower-level perceptual 
               line-counting task in the presence of a distracting depiction 
               of a 3-D object, in which participants counted whether there were 
               more red or more green contours (In a contrasting 3-D task, 
               participants judged whether the same 3-D stimulus objects 
               (but without color in any contours) depicted a possible or 
               impossible 3-D object). We hypothesized that individuals with 
               autism would be less likely than controls to process the global 
               3-D information (and would hence show fewer neural signs of
               such interfering 3},
   author = {Yanni Liu and Vladimir L Cherkassky and Nancy J Minshew and 
             Marcel Adam Just},
   issn = {1873-3514},
   issue = {7},
   journal = {Neuropsychologia},
   keywords = {Adult,Autistic Disorder/*physiopathology,Autistic 
               Disorder/*psychology,Brain/*physiopathology,Color,
               Executive Function/physiology,Female,Humans,Judgment/physiology,
               Magnetic Resonance Imaging,Male,Neural Pathways/*physiopathology,
               Neuropsychological Tests,Perception/*physiology,Psychomotor 
               Performance/physiology,Sex Characteristics,Space 
               Perception/physiology,Visual Perception/physiology,Young Adult},
   pages = {2105-2111},
   title = {Autonomy of lower-level perception from global processing in autism: 
            evidence from brain activation and functional connectivity.},
   volume = {49},
   url = {https://proxying.lib.ncsu.edu/index.php?url=https://search.ebscohost.com/login.aspx?direct=true&db=cmedm&AN=21513720&site=ehost-live&scope=site},
   year = {2011},
 
 ```
 
 No one writes these themselves. The best way to create your BibTeX database
 is to use a reference manager such as Zotero, Mendeley or EndNote. They all
 have the option for exporting your chosen references in this format. The best
 strategy is to export all the citations you may need. You don't need to use
 everything, so it is usually most efficient to add what you could possibly use.
 
### Creating a Bibliography
 
 Creating a bibliography requires adding three lines of code. Also make sure
 you have uploaded your BibTeX file into overleaf.
 
 
 ```latex
 
 \documentclass{article}
 
 ...
 
 
\usepackage{natbib}    % This package works well for bibliographies

\bibliographystyle{unsrtnat}.  % One of the built in styles

...

\begin{document}

...


\bibliography{sample}  % You typically put them at the end of your document.
\end{document}

```

There are a few packages for creating bibliographies, `natbib` is pretty reliable.
The commands to include your bibliography package and the style go in the head matter
before `\begin{document}`. You place the command to create the document anywhere,
but typically that will be the end of the document.

If you recompile now, you will get an error! Go ahead and do that. Try using
a web search to find the solution before moving on.

### Adding Citations

If you did find the solution to the error above, then you know you need to 
add citations. You do this by putting `\cite{citation_id}` where you want
the inline citations to be, where *citation_id* is the first item inside the 
curly braces. If we want to add the citation above it would be 
`\cite{2151372020110601}`. You can add this anywhere in your text, for 
example.

```latex

Id aliquet risus feugiat in ante metus dictum at tempor. Pulvinar elementum 
integer enim neque volutpat ac tincidunt vitae semper \cite{12461122020171001}. 
Inisl nisi scelerisque eu ultrices. Libero enim sed faucibus turpis in eu mi 
bibendum. 

```

Add one or more citations into your text and recompile again. It should work now.


### Bibliography Styles

There are other styles built into the *natbib* package shown 
[here](https://www.overleaf.com/learn/latex/Natbib_bibliography_styles). You can
also upload additional styles as .bst files.

## Exercises

1. Add more inline citations.
2. Change the bibliographic style to one of the built in styles.
3. Challenging. Use the provided Nature template and style
    1. Create a new document and use the template.
    2. Upload the .cls and .bst files
    3. Create a bibliography using this template and style
 
 

