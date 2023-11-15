---
layout: page   # This is required
title: Document Classes   # This is required

order: 30    # Determines the order of units. Doesn't need to be consecutive though
            # or even start with zero, the pages will be displayed in their sort
            # order.

duration: 15 # A hint to how long it will take to cover this topic in mintues.

tutorial: true  # Set to true if you want this page displayed as a web page
instructors_notes: true  # Set to true if you want this displayed in instructors notes

# Provide a brief description of what the unit is about. You can use markdown
# notation for this.
description: |
  This section goes into more detail on document classes. Describing more about
  what they are, what the common ones are and options for them.

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

## Document Classes

Document classes, perhaps unsurprisingly, defines different kinds of documents. 
This isn't the full story, but you can pretty much think of Document Classes as
a bag of commands that can used for that class. They also define the options and 
default formatting for a document too.

The classes mentioned previously, `article`,  `book`, `report`, and `letter`, 
and`slides` are just the most common. Like anything else in LaTeX users can 
write their own classes, so there are many more. Most often you will 
encounter them using OverLeaf templates. Good templates will have good
documentation, but often its best to stick with the common ones noted above
as they will result in less errors.


## Packages

Like document classes, packages are essentially a bag of commands. The difference
is that while the commands from a document class only work for that document class,
commands from a package should work for any document class. You only can use one 
document class, you can load as many packages as you want. Probably the most
common package you will use is `graphicx` that we have already seen.

## Commands

Commands are what you use most. The commands you can use are defined by LaTeX,
the document class you use and any packages you load.

## Excercise

One of the best ways to learn about classes, packages and commands is to use
the various OverLeaf templates explore them. Take some time and create some
documents from different templates that might seem useful to you. See what
document classes they use and what packages they load. Also look through
the commands. Look at the PDF document and see what items would be of use to 
you.






