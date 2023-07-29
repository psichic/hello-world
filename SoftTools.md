# Software Tools

[TOC]

Notes on some software tools I have used over time. All Free. See also:

- [Awesome Lists Topics](https://github.com/topics/awesome)
- [The Original Awesome List, I think](https://github.com/sindresorhus/awesome)

# Personal Databases

## Treeline

[Treeline](http://treeline.bellz.org/) is a free lighteweight Personal Database Software which allows one to store data in its treelike nodes and subnodes. It allows the creation of custom forms and reports. It is not difficult to use, but first time users might hit a stumbling block. This document only attempts to explain the underlying principles, for detailed insights please refer to the [online documentation](http://treeline.bellz.org/use.html). Three good features are:

    - Multi-line text is very well supported
    - Cloned Nodes
    - Simple report generation using normal (or html) text and field variables.

- Samples can be found here: `C:\Program Files (x86)\TreeLine-3\samples`  **Fig 1** shows a basic books database opened from samples. This database is used in the remaining article as an example. I would usually turn-off the `breadcrumb` and `child panes` from the view menu: These would turn off the large white panels (shown by default) at the top of the windows. 
  
  ![](https://i.imgur.com/wWD9Wg6.png)

- Any database like the one shown above has multiple "Data Types" associated with it. Data types are defined through the data menu: configure data types. Initially only the `DEFAULT` type is defined (Fig 2). It cannot be deleted, but it can be *renamed*.
  
  ![](https://i.imgur.com/JbTR2y6.png)
  
 - In the sample book database, three data types are defined: ROOT, AUTHOR and BOOK (**Fig 3**). They appear in alphabetical order in the first tab of the configuration dialog. Each node in the database can be associated with only *one* of the types defined in this dialog, e.g the toplevel node called `SF Books` is of the data-type ROOT.
    
    ![](https://i.imgur.com/TUck9zs.png)
  
  - The Root type has a default child type: Author. Any subnodes created under a Root node would automatically become an Author subnode (This can be overridden by pressing Ctrl+T while the node remains selected - also possible using the Set Node Type item in the Data menu)
  
  - To constrain the nature of a type, keep it selected in the first tab and change to the next tab. Here, we can declare a default child type (e.g ROOT ➡️Author), choose an icon for the node and select some options related to how the data associated with a node would appear in the output.
  
  - Each data type can be associated with several fields.  For the ROOT data type, there is only one field: NAME. Each Field is created by default to contain *text* data, but this can be changed in the next tab: **Figure 4** shows all possibilities.
    
    <img src="https://i.imgur.com/4R7LgwA.png" title="" alt="" data-align="center">
  
  - How the data associated with a node would appear in the output is formatted in the last tab. It uses a mix of ordinary text, line breaks and field variables which are referenced as `{*VarName*}` . 

- To summarize:   A `Database` (`.trln` file) consist of a set of user defined `Data Types`. Each `Node` is linked to one `Data Type`. Each Data Type is associated with one or more `Fields` which can hold data of various sorts. Output associated with a node (or a set of nodes at the same level) can be constructed out of  `{*FieldVarNames*}` and ordinary text.


