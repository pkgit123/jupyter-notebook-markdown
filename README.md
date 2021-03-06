# jupyter-notebook-markdown
Playbook to add markdown to Jupyter Notebook

## Why do we add markdown to Python Jupyter Notebooks?
Python Jupyter Notebooks are often written with markdown cells at the top to describe background and context.  The top will have section header outline.  The notebook itself is divided into sections, each of which begin with markdown cells.  Goal is to add links to outine to jump straight to individual sections.  Another goal is to add links to individual sections to jump back to outline at top.

To simply the navigation code, below are examples of code for origin vs. destination.

### Markdown: Destination
In the destination markdown cell at the top, add an anchor tag (e.g. "Back to Top").  The unique ID for this anchor tag tells the notebook how to find this destination.

``` html
<a id='back_to_top'></a>
```

Side note: in certain versions of Jupyter Notebook, using `name` works better than `id`.
``` html
<a name='back_to_top'></a>
```

### Markdown: Origin
In the origin markdown cell, add two things.  
1. Square brackets to display [text] 
2. Parentheses with hashtag to point to destination anchor ID (#anchor_id)
``` html
[back to top](#back_to_top)
```

### Use cases:
* Navigate from outline at top to specific section
* Navigate from specific section back to outline at top
