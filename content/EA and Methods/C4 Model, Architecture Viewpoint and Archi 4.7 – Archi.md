#EA #Methods #C4
# C4 Model and ArchiMate
### The C4 Model

The [C4 Model](https://c4model.com/) is a set of architecture viewpoints designed by [Simon Brown](https://simonbrown.je/) to address common needs in software architecture. I’ll let Simon describe it himself:

> The C4 model was created as a way to help software development teams describe and communicate software architecture, both during up-front design sessions and when retrospectively documenting an existing codebase. It’s a way to create maps of your code, at various levels of detail, in the same way you would use something like Google Maps to zoom in and out of an area you are interested in.
> 
> Although primarily aimed at software architects and developers, the C4 model provides a way for software development teams to efficiently and effectively communicate their software architecture, at different levels of detail, telling different stories to different types of audience, when doing up front design or retrospectively documenting an existing codebase.
> 
> The C4 model consists of a hierarchical set of software architecture diagrams for context, containers, components, and code.

The C4 Model is based on four key abstraction levels but is completed by additional diagrams.

[![C4 Model Overview](https://www.archimatetool.com/wp-content/uploads/2020/04/c4-overview-1024x768.png)](https://www.archimatetool.com/wp-content/uploads/2020/04/c4-overview.png)

### Architecture viewpoints?

The ArchiMate standard has been designed from the ground up to allow architects to communicate their work in a coherent and effective way. This is made possible not only by a good set of concepts, but also by the idea of architecture viewpoints, borrowed from the [ISO/IEC 42010](https://en.wikipedia.org/wiki/ISO/IEC_42010). In short, an architecture viewpoint is a set of conventions that can be used to produce an architecture view (a view could be a diagram, a catalog, a matrix or any useful way of describing a subset of your architecture) to answer a known concern from a known set of stakeholders.

#### Let’s take an example

If you and your team help projects to design their target architecture, you will, at some point, have to discuss this with the CISO (Chief Information Security Officer). Of course you’ll have to have your CISO validate your choices (i.e. you don’t just have to inform him). Now think about it, what are the key drivers of CISO: security as a whole of course, but what is important to them in your organization? For the sake of this example, let’s say your CISO mainly focuses on dataflow related to the internet (because the internet is not safe, while your intranet is). This will lead you to create some kind of document (part of the global design document) to address their concerns.

In addition to this, what level of detail do you need? Well, your CISO might not be too technical so you’ll have to provide an overview, not something too detailed.

Lets summarize what we have: for each project, you should provide a short document that allows the CISO to quickly understand project impacts on the internet dataflow. Nothing more is needed because you know that your CISO won’t care.

What we have done here is define an architecture viewpoint. Note that there’s no link with ArchiMate for the moment and that’s on purpose: ArchiMate is only one of the different ways to produce a view, but you could decide to use a drawing tool. Of course, using ArchiMate and a modelling tool will allow you to have a coherent set of views and will provide additional benefits (you can query your model and create some automated analysis).

Let’s assume that you’re going to use ArchiMate in your work. This means we can further describe our viewpoint.

What kind of “document” will you show to your CISO? You could decide to provide the catalog of network flows related to internet and impacted by the project. But as a picture is worth a thousand words, you decide to provide some diagrams using the ArchiMate standard. At this stage let’s ask this simple question: does your CISO know ArchiMate? Maybe just a little bit or even not at all, so you decide to use only a subset of ArchiMate (Node, Network…). In addition, because several network security experts often do it that way using Visio, you decide to draw network zones as big boxes inside which you put nodes (that you call “servers” for your CISO). Being trained in ArchiMate, you know that the right relationship to link (communication) networks and nodes (as servers) is association, but association is not meant to be shown as nested, but in this case you decide that nesting would really ease communication with your CISO and avoid them having to take time and learn something new, so you accept this non standard use of nesting. Of course, flows that are at risk are colored red because this is the de facto standard.

In addition, you know that the network team will reuse this document but some people are color blind, so you use labels as well as color so that the document is still usable for them.

Let’s wrap up. The full definition of your viewpoint is as follows:

-   **Viewpoint Name**: Internet Dataflow Viewpoint
-   **Key stakeholder**: CISO
-   **Key concerns**: Avoid any security breach related to internet dataflows
-   **Purpose**: Make a decision: obtain CISO’s agreement on target Architecture
-   **Level of detail**: Overview
-   **Type of representation**: Diagram
-   **Standard/metamodel**: ArchiMate
-   **Restriction on concepts**: Only “basic” concepts, mostly Node and Communication Network but other concepts allowed if used on purpose
-   **Modelling conventions**: Network zones will be modeled using Communication Network as big boxes inside which Nodes will be nested. Associations will be used to connect them. This is a non normative usage of nesting that is accepted in this viewpoint to ease communication. Flows (modeled using flow relationship) that are at risk will be colored red and label “risk” (to make it still readable for color blind people and/or when printed in black & white
-   **Other**: Limit yourself to a maximum of 20 concepts and should be printable in letter/A4.

### C4 Model and ArchiMate

If you read the C4 Model description (and I really encourage you to do so), you’ll note that each diagram type is in fact a metamodel and tool agnostic definition of an architecture viewpoint: you can use whatever solution you want to create such diagrams, including pen & paper and drawing tools. Of course, having an underlying model is important, and Simon Brown offers [Structurizr](https://structurizr.com/), a SaaS platform to create and maintain software architecture descriptions.

But what if you work in a context where some architects use ArchiMate? Well, in this case you can easily leverage ArchiMate to support the C4 Model. This simply requires a mapping between the [C4 Metamodel](https://c4model.com/#Metamodel) and [ArchiMate](https://pubs.opengroup.org/architecture/archimate3-doc/):

-   **Person** can be mapped to [Business Actor](https://pubs.opengroup.org/architecture/archimate3-doc/chap08.html#_Toc10045368)
-   **Software System** and **Container** can be mapped to [Application Component](https://pubs.opengroup.org/architecture/archimate3-doc/chap09.html#_Toc10045392)
-   **Component** can be mapped to [Application Function](https://pubs.opengroup.org/architecture/archimate3-doc/chap09.html#_Toc10045397)
-   **Code Element** is maybe too fine-grained to be useful in ArchiMate, but could be also mapped to [Application Function](https://pubs.opengroup.org/architecture/archimate3-doc/chap09.html#_Toc10045397)
-   **Relationship** can be mapped to [Triggering Relationship](https://pubs.opengroup.org/architecture/archimate3-doc/chap05.html#_Toc10045324) (convention is that the triggers goes from the caller to the callee)

Using this mapping it becomes easy to create an ArchiMate view which adheres to a C4 diagram. During my talk in Amsterdam I presented these examples:

[![System Landscape Diagram Example](https://www.archimatetool.com/wp-content/uploads/2020/04/System-Landscape-Diagram-1024x512.jpeg)](https://www.archimatetool.com/wp-content/uploads/2020/04/System-Landscape-Diagram.jpeg)

[![Container Diagram Example](https://www.archimatetool.com/wp-content/uploads/2020/04/Container-Diagram-1024x888.jpeg)](https://www.archimatetool.com/wp-content/uploads/2020/04/Container-Diagram.jpeg)

After my presentation, I was asked which tool was used to produce these diagrams. The answer was simple – I used Archi. However, I used several tricks:

-   The short description inside each Person, Software System or Container is created by nesting a visual note, which has the drawback of not being linked to the Business Actor or Application Component’s description.
-   The “user” or “people” icon is created using [FontAwesome](https://fontawesome.com/) [for desktop applications](https://fontawesome.com/how-to-use/on-the-desktop/setup/getting-started) and adding a visual note behind Business Actors.
-   In the last view, instead of  creating relationships from the container, I created them from the Software System. I did so because I didn’t want to maintain two relationships (one for each level of abstraction).

Of course, using these tricks makes sense only if you have a small number of diagrams to maintain. But with the upcoming new version (4.7) of Archi, you no longer need to use these tricks. And the great thing is that you can test this yourself now by using our [Early Access version](https://www.archimatetool.com/beta/).

### Archi 4.7 Label Expressions

Archi 4.7 will come with a new feature which allows you to dissociate the label shown on an element on a view from the element’s name in the model (which is still the default for obvious reasons). Instead of manually defining this alternative label, you can define it through an _expression_. You can regard _expressions_ as a simple yet powerful macro language which allows you to compose the new label with expressions such as _${name}_, _${documentation}_, _${property:propname}_ and [more](https://github.com/archimatetool/archi/wiki/Label-Expressions).

If this reminds you of something, that’s because this was first developed by [Hervé Jouin](https://www.linkedin.com/in/herv%C3%A9-jouin-9aa93761/) in his [specialization plugin](https://github.com/archi-contribs/specialization-plugin). Phil Beauvoir and I recently decided it was time to have a similar feature natively in Archi. We kept most of the original expressions defined by Hervé but added several others to cover more use-cases.

Thanks to this new feature, it becomes possible to set an expression such as:

![](https://www.archimatetool.com/wp-content/uploads/2020/04/Label-Definition.png)

Which will evaluate to something like the following for an Application Component named “Historical Incidents Application” having a “Stereotype” property set to “Software System”:

![Label Example](https://www.archimatetool.com/wp-content/uploads/2020/04/Label-Example.png)

Of course there’s a trade-off: it becomes really easier to maintain your model because you no longer have to add visual notes and duplicate documentation, but you can’t set two different fonts (one for the name and the other for the description).

Now, if you combine this new feature with a [Custom Toolbox](https://github.com/archimatetool/archi/wiki/Pattern-based-modelling-with-Archi), you will have the tools at your disposal to easily create and maintain C4 diagrams with Archi:

[![Archi configured for C4](https://www.archimatetool.com/wp-content/uploads/2020/04/Screenshot-from-2020-04-18-14-52-05-1024x542.png)](https://www.archimatetool.com/wp-content/uploads/2020/04/Screenshot-from-2020-04-18-14-52-05.png)
