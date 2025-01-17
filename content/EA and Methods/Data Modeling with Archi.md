---
title: Data Modeling with Archi
source: https://eaprincipals.com/data-modeling-with-archi/
author:
  - "[[EA Principals]]"
published: 2023-08-17
created: 2025-01-09
description: Are you an ArchiMate modeler who also creates entity-relationship diagram (ERDs), UML class diagrams or other styles of data models? Have you ever wished that…
tags:
  - EA
  - EA_Data
  - Modelling
  - Data_Modelling
  - ArchiMate
  - Archi
---
Are you an ArchiMate modeler who also creates entity-relationship diagram (ERDs), UML class diagrams or other styles of data models?  Have you ever wished that you could use one free tool for enterprise architecture modeling as well as data modeling?  If so, here is some good news:  data modeling with ArchiMate is now very practical due to recent enhancements in the Archi free and open source tool for ArchiMate modeling \[1\], the introduction of the Archi plugin for Archi scripting \[2\], and the longstanding support of custom profiles by both the ArchiMate language \[3\] and Archi. 

**The Question**

I often have the privilege of assisting EA Principals CEO and Chief Architect Dr. Steve Else in his classes on enterprise architecture modeling with the ArchiMate language.   Recently, a student who is an enterprise data architect for a cruise line asked about the feasibility using of Archi for data modeling. 

**The Model**  
After giving the student’s question some thought and doing some investigation, configuration and scripting, I built following one-view model:

![[Article-Image-5-1024x838.png]]

The model view portrays some elementary relationships that involve Cruise Ships.  Cruise Ships are kinds of Oceangoing Vessels.  Each Oceangoing Vessel has one National Registration. Cruise Ships are composed of Decks, and they are scheduled for Cruises. Some Decks are composed of Cabins.  Passengers (not included in this simple demonstration model) make Reservations for particular Cabins on Cruises.      

Each relationship connector in the model, except for the Specialization connector, has a label with several components.  Moving from top to bottom, first we see a stereotype \[4\] called ERD, between double angle brackets. This serves to specialize the ArchiMate relationship.   Then, we see the name of the relationship, e.g. Cruise Ship-Deck. Finally, we see two cardinality (number of elements) range indicators in standard ERD or UML form separated by a vertical line or pipe character (|).  These indicators refer, respectively, to the source and target of the ArchiMate relationship. For Cruise Ship-Deck, the source cardinality is 1…1, which indicates exactly one Cruise Ship.  The target cardinality is 1…\*, which indicates one to many Decks.  In other words, each Cruise Ship has one or more Decks, and each Deck is part of exactly one Cruise Ship.

**The Label Expression**

Archi 4.7 enables users to compose labels from a mixture of text literals and model data \[5\]. Below is the definition of the label that I used for the view, followed by an example of the properties it references:

![[Article-Image-6-1024x431.png]]

![[Article-Image-7-1024x430.png]]

The first line of the label references the Stereotype property and places it in double angle brackets.  The second line references the name of the relationship. The third line, which is broken up into four lines due to the width of the Label Expression text box, references the four cardinality properties.   Note that I have named the properties using nested namespaces, e.g. Data:Card:Source:Min, following the style of the Jasper reports template provided with Archi.  This is completely optional and has no bearing on appearance of the view or the functionality of the model.  

In order to create the view, I had to add the Label expression into each of the six relationships that require it, since the jArchi plugin for Archi scripting does not yet support label management, although Phil Beauvoir, the primary Archi developer, has written that this feature is in progress\[6\]. However, I was able to select all six relationships, and enter the expression once.  This is convenient, since the script that adds the necessary properties, which I describe in the next section, requires the user to first select the relationships to which properties can be added.

**The Scripts**

![[Article-Image-8-1024x540.png]]

The script begins by initializing a counter and two literal constants.  The LABEL constant is not used; it is there in anticipation of support for label management in a future version of jArchi.  Then, the script iterates through the selected relationships (filtering out and thus ignoring anything selected that is not a relationship), ensures that each of their labels are visible, and adds five properties to each of them. The script adds default cardinality values to each relationship, which can be updated after the script completes.  The jArchi syntax for adding properties requires giving them values, so I chose to default to a common relationship scenario:  exactly one to one to many. 

The script ends with a dialog box that announces the number of relationships updated.

![[Article-Image-9-1024x443.png]]

Like the first script, it iterates through all selected relationships and provides a count of updated relationships when it is done. Since jArchi does not provide a single method for stripping all properties from a concept, I had to first generate a list of all properties for each selected relationship, and then iterate through that list to remove the properties one-by-one.

**Opportunities for Future Work**  
There are many opportunities to improve the first script.  For example, as it iterates through selected relationships, the script could ignore relationships such as specialization that are incompatible with cardinality, and prompt the user for cardinality values instead of just filling in defaults.  It could enforce valid syntax for cardinality values.  It could also discover relationships that could benefit from cardinality specification in selected views or entire models, and take the user through the process of specifying them.  

Additional scripts could add analysis of data model connectivity as well as statistics based on additional concept attributes.  Through the Archi command-line interface \[7\], jArchi processing can be combined freely with that of other languages, libraries and packages.  As models and their tooling become more complex and involve multiple collaborators, robust version control is necessary.  Robust collaboration with version control for Archi modeling is available with the coArchi plugin \[8\].  

In addition, modelers can transition models from Archi into multi-language architectural modeling tools that, like Archi, support the Open Group ArchiMate Model Exchange File Format \[9\], and explore how those tools meet their needs.  An example of such a tool is MID Innovator \[10\], which the Swiss government users for all of its architectural modeling. 

**Conclusion**

Archi and its jArchi plugin can support full-featured data modeling through the implementation and management of data modeling profiles for the ArchiMate language.   These rich capabilities are limited only by the creativity and industry of ArchiMate modelers and tool builders.

**References**

1. Archi – Open Source ArchiMate Modeling. [https://www.archimatetool.com/](https://www.archimatetool.com/)
2. jArchi – Scripting for Archi. [https://www.archimatetool.com/plugins/#jArchi](https://www.archimatetool.com/plugins/#jArchi)
3. ArchiMate Standard – Adding Attributes to ArchiMate Elements and Relationships. [https://pubs.opengroup.org/architecture/archimate3-doc/chap15.html#\_Toc10045465](https://pubs.opengroup.org/architecture/archimate3-doc/chap15.html#_Toc10045465)
4. ArchiMate Standard – Specialization of Elements and Relationships. [https://pubs.opengroup.org/architecture/archimate3-doc/chap15.html#\_Toc10045466](https://pubs.opengroup.org/architecture/archimate3-doc/chap15.html#_Toc10045466)
5. Archi Label Expressions Wiki. [https://github.com/archimatetool/archi/wiki/Label-Expressions](https://github.com/archimatetool/archi/wiki/Label-Expressions)
6. Archi Forum – jArchi Label Expression processing with jArchi. [https://forum.archimatetool.com/index.php?topic=926.msg5061#msg5061](https://forum.archimatetool.com/index.php?topic=926.msg5061#msg5061)
7. Archi Command Line Interface. [https://github.com/archimatetool/archi/wiki/Archi-Command-Line-Interface](https://github.com/archimatetool/archi/wiki/Archi-Command-Line-Interface)
8. coArchi – Model Collaboration for Archi. [https://www.archimatetool.com/plugins/#coArchi](https://www.archimatetool.com/plugins/#coArchi)
9. The Open Group ArchiMate Model Exchange File Format. [https://www.opengroup.org/open-group-archimate-model-exchange-file-format](https://www.opengroup.org/open-group-archimate-model-exchange-file-format)
10. Innovator Enterprise Modeling Suite. [https://www.mid.de/en/business-activities/tools/innovator](https://www.mid.de/en/business-activities/tools/innovator)

Authored by Iver Band, Senior Trainer and ArchiMate Expert