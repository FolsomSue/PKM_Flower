This is the first article of a series about ArchiMate Interoperability, which includes:

1.  Potential issues illustrated with practical cases with Archi, EA, Modelio (this article)
2.  [From models to linked data using semantic web technologies?](https://www.linkedin.com/pulse/archimate-from-models-linked-data-using-semantic-web-dr-nicolas-figay/?published=t)
3.  [What do we learn from exchange format schemas study?](https://www.linkedin.com/pulse/archimate-interoperability-what-do-we-learn-from-exchange-figay/)

Don't hesitate sharing you comments, knowledge, viewpoints and experience/best practices on the topic. If you think this article creates value, don't hesitate to share it and like it. And don't hesitate reflecting my skills on my [LinkedIn profile](https://www.linkedin.com/in/nfigay/) if you think it is appropriate :)

## Introduction

With an open specification of a simple language delivered by a mature community, and an open format for interchange, some may think that interoperability between software products implementing ArchiMate and import/export based on this open format is something acquired.

But is it really the case?

Based on simple and concrete examples, this article will show that it is not so easy when considering different issues, such as:

1.  The physical breakdown (or organization) of an ArchiMate model,
2.  The strict compliance with the specifications (if not under specified),
3.  The strategies adopted by modeling solution providers supporting ArchiMate with several other languages, etc.
4.  Evolution of the ArchiMate language and associated specifications

It then proposes some improvement we should expect concerning the ArchiMate specifications or implementations in order to achieve the targeted operational interoperability between Enterprise Modeling applications based on ArchiMate.

Finally, it will propose a test data set and an approach for testing interoperability.

The different tools (extensible list- new versions of the article are produced over the time) used for assessing interoperability based on ArchiMate are Archi, SPARX' Enterprise Architect, Modelio, Visual Paradigm, Abacus, etc.

The different parts of the article are:

1.  How Open Group addresses interoperability
2.  Physical breakdowns of an ArchiMate models
3.  The Interoperability issues illustrated with Archi, Enterprise Architect, Modelio and Abacus
4.  Evolution of ArchiMate and associated specifications
5.  Analysis
6.  Proposal for addressing the identified issues
7.  A more systematic approach for testing

The conclusion opens perspective on strategy to adopt for Enterprise Architects: ensuring Interoperability isn't a long quiet river...

## Part 1- How Open Group addresses Interoperability

When considering that one motivation for ArchiMate was to provide a common simple language allowing different kind of architects and stakeholders to communicate together, reflecting their respective viewpoints in order to be aligned on the same business objectives, Open Group started to address the needs for interoperability at Business level first, by improving communication within the enterprise for better cooperation.

For this, providing a formal description of a simple language shared between concerned stakeholders (several kind of architects, operational managers, etc.) was the way to deal with interoperability at semantic and information level.

In addition, providing the [Open Group ArchiMate Model Exchange](https://www.opengroup.org/open-group-archimate-model-exchange-file-format) (I will call it Open Format for ArchiMate in the rest of the article), which relies on an XML and standardized XML schemas, should support model/information interchange between ArchiMate modeling applications and Enterprise Digital Assets Repositories (e.g. Business Management Systems, Product Management Systems, etc.) realized with heterogeneous products.

In addition, the Open Group proposes some certification of the tool implementing ArchiMate, as described [here](https://www.opengroup.org/certifications/archimate/tool). It proposes a process, a set of requirements for conformance, generic tools certification documents and a link to a test directory accessible only to members. Let's consider that some requirements are optional, in particular for customization of the language by mean of stereotypes. For each certified tools which are commercial ones, a set of documents are provided with test data set, and sometimes videos giving evidence that the tested tools supports compliance requirements. They are those in the following screen capture. Also, it is important to consider that tests are performed for given configurations, i.e. versioned software product with eventually versioned complementary modules (e.g for Modelio). But it is not always explicitely mentionned.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQGZJMnAd9F_9A/article-inline_image-shrink_1500_2232/0/1565692996017?e=1646870400&v=beta&t=kYB0lymZZhK05T5Ml8xXha3KD8zZdDCSJa2WfSCfEew)

The level of information provided for each tool is not exactly the same. Some PDF files, XML files related to tests (but without clear identification on how they were produced) and videos showing the usage of the tool for modeling or interchange which are most of the time missing, except for Modelio. I was surprised by Abacus certification, as I had to assess it and identified that this tool which is very good as ArchiMate modeler unfortunately doesn't support import/export based on the open format for ArchiMate model exchange. This doesn't clearly appear in the certification information. Archi tool, which is an open source and free implementation of ArchiMate, is not certified (but usually it is mandatory only for commercial products). Let's note that I always considered this tool to be an implementation of reference of ArchiMate, which is very useful for promoting it as a first an easy way to discover the language and Enterprise Modeling value creation. Enterprise Architect isn't certified. Modelio is certified and is proposing one of the most complete set of information providing evidence of its compliance.

Support of interchange by mean of the Open Format for ArchiMate model is included in the compliance statement, and should ensure interoperability between EA applications of different organisations having to collaborate.

However, when practicing and having to interchange models between different solutions, Archi, Abacus, EA or Modelio, some problems occurred when willing to interchange ArchiMate models, despite the availability of a common language, of an interchange specifications and of a certification process for compliance. The first I faced and described is related to physical breakdown of an ArchiMate model. It is the first interoperability issue I met, motivating the production of this article.

Indeed, as a solution architect working within an organization having to use ArchiMate with SPARX Enterprise Architect (SEA), the question arises concerning ability to produce ArchiMate models, in order to facilitate the collaborative production of model component by heterogeneous and independent organizational units having eventually different modeling platforms or EA repositories. Doing so, some requirements came concerning ability to integrate in SEA models produced by mean of Archi, or in the reverse to be able to export models within Archi in order to take advantage of useful Archi functionalities such as advanced visualisation or querying. Also, Archi is a convenient and accurate component when having to test interoperability, as it is considered as fully aligned with ArchiMate specifications and as it supports import/export based on the Open Format for ArchiMate. SEA also supports this exchange format by default, i.e. without additional module. Finally, very often, complex interfaces are created between modeling tools and Excel, as it is often considered that modeling is a too complicated exercise, constituting a real stopper for collaboration with non architect people.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQE_uEYecbaFHQ/article-inline_image-shrink_1000_1488/0/1572616334613?e=1646870400&v=beta&t=Idgy_wNKjQhJE-pQpF2QmOo_i4FIjPxvwGEOkA1-s_M)

This following ArchiMate view illustrates the situation where we could be willing to establish interoperability between EA modeling platforms, considering not only SEA and Archi, but also Modelio with the ArchiMate module.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQHM7MZowR3EOg/article-inline_image-shrink_1500_2232/0/1561406456725?e=1646870400&v=beta&t=hgdi5MDxjosgzTsWnSPVXO0_0LectA4msyRGlPJJbGo)

> _These tests were performed with EA14 and EA15 (out in September 2019) with the same results._

In order to support such collaboration, it is also needed to be able to partition physically ArchiMate models as set of artifacts (e.g. physical outputs from an activity). Such need implies ability by the tools to compose these artefacts, and consequently a physical breakdowns of archiMate models artefacts, being through import or export indication (like for the STEP language or some programming languages), or through containments (like for UML, based on packages and modules). It is what is detailed in the next chapter of the article.

## Part 2 - Physical breakdowns of an ArchiMate models

What is a physical breakdown of an ArchiMate models?

It is a structuration of these models relying on containers which are physically partitioning the constructs of the models.

Within Archi, it is realized by mean of folders which partition the construct according to their types: Strategy, Business, Application, Technology& Physical, Motivation or Implementation&Migration modeling elements, plus Other, Relations and Views.

This is what you will see when opening an Archi Model, on the model pane on the left.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQEaUyd8IKrVpw/article-inline_image-shrink_1000_1488/0/1554375330980?e=1646870400&v=beta&t=6yCwXPbD0QTi4qRDgGeNwU7hEHxOVbNZIHEsssAQrqI)

Any modeling element created with Archi will be automatically located on the appropriate folder, corresponding to the layer it belongs to (except relations which are all grouped in a single folder) and views, which are views on the model and are constituted of visual elements representing the model elements.

You can in addition create sub folders, in order to reflect complementary structure based on whatever you want, e.g. human organization, source of information, etc. The following figure shows a partitioning for model elements and views reflecting two organizations (Org 1 and Org 2), two sources of information from which the model elements will be collected and views which could be specific to an organization or shared between organizations. In order not to mix all the modeling elements, they were partitioned by the mean of folders as illustrated in the following figure.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQEN5JNRcX9hEA/article-inline_image-shrink_1000_1488/0/1554375705785?e=1646870400&v=beta&t=_PdcdH9UCza0By4SgJRBGaMnbhh22EhKXxOBka3YpOo)

Let's note that in terms of serialization, which Archi achieved by mean of XML(.archimate files), the structure is reflected exactly the same hierarchical way, and that the modeling elements are encapsulated between XML tags, which are constituting themselves a physical containment and partition of the XML elements describing the model elements.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQEFZL0iv6VS_Q/article-inline_image-shrink_1000_1488/0/1554376138554?e=1646870400&v=beta&t=6xY7Ktfat6BNOgqyd1FD2Aqm6zHn1ee70itXyTbuRKU)

Considering ArchiMate modeling with Enterprise Architect, it can be addressed similarly with Packages, as illustrated in the following figure.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQGc60AdyFRHaw/article-inline_image-shrink_1000_1488/0/1554376316548?e=1646870400&v=beta&t=YNXgxbUHxEshlCWdVJVWcEbXVxtfaWI0zEvN8KwaU8g)

As for Archi Folders, UML package used by Enterprise Architect are a way to partition physically the content of an Enterprise Architect Project or Model repository. It can be stereotyped as a model (<<model>>), allowing then to capture in a project a set of models which are physically distinct, each model constituting a container. With such a mechanism, it is also possible to split a project and contained packages in different files or blobs within a database, constituting what the solution providers in this domain call "modules". A project can be split in modules. But it can also be constituted aggregating modules provided in shared modules libraries. It can also be the way for aggregating modules providing from different organization and tools, relying on the XML Interchange Model format (XMI) which support model interchange. No similar modularization mechanism is provided by Archi.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQEsrvy7LH8VHQ/article-inline_image-shrink_1000_1488/0/1561301322418?e=1646870400&v=beta&t=RNTWkmOP3eLQvZ8hhSCqJvlkzjtEgLt0yIOyRXEDto0)

With Modelio, as illustrated above, with the ArchiMate Module, the approach is on between. The initial package structure is constrained, and very closed to what Archi proposes. An ArchiMate project with Modelio is managed apart from the other projects with UML or other languages, so we don't have as much freedom than with EA.

Let's note that such constructs are provided by the solution providers, but are not part of the ArchiMate specification. A "Visual group" construct is specified, used in diagrams (views), but being visual, it is not a partition of the model, only the visual element of a view. A "Grouping" construct is also specified since ArchiMate 3, which is logical, but doesn't split physically a model.

## Part 3 - The Interoperability issues illustrated with Archi, Enterprise Architect, Modelio and Abacus

### First Interoperability test - preservation of folders/packages

The principle of the first interoperability test is the following: let's realize a loop with transfer of a model with a physical breakdown structure and let's compare the starting model and the resulting model: is the model preserved, or do we loose information during this process?

Here is the realized test procedure, starting from Archi to SEA:

-   Creation of a default model with Archi
-   Structuration per organization and model by mean of Archi folders
-   Exportation from Archi based on the Open Format
-   Importation in Enterprise Architect/Modelio based on the Open Format
-   Export from Enterprise Architect/Modelio based on the Open Format
-   Import in Archi based on the Open Format

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQFe_--Rr_6dZg/article-inline_image-shrink_1000_1488/0/1554364008302?e=1646870400&v=beta&t=1nkNsfUfJ_qualyWdRFTR6Fpx72Gi0M-gQvwUdndgNU)

What were the next steps of the experimentation? I've been doing the same starting from Enterprise Architect:

1.  For that, I reused the model resulting from the import in SEA, as the physical breakdown described with folders was preserved with a package created for each folder. Performing the export from SEA based on the Open Format, it appears that export is possible only if having at least one model element in the exported package, and if at least one view (diagram) exists.
2.  So I created an ArchiMate Business Object, BO 1, for a given organisation and model in the location where it should be using Archi. I also created two views within given folders under the Views folder. I then realized an export from SEA based on Open Format, and imported it in Archi: all the packages created in SEA disappeared, with BO 1 located in the Business folder, and views placed in the Views folder
3.  Then, in the SEA model, I moved BO 1 in another package, located under the Physical 1 Technology folder. Let's note it is not an issue with SEA, while it is something impossible with Archi, as Archi constrains any created model element to be in the appropriate top folder structure, based on layers plus in addition Views and Relations folders. I then realized the same actions for exporting from SEA and importing in Archi. I obtained exactly the same result.
4.  I repeated the same actions, after moving the folder containing BO 1, Source S2, under the exported package, the package being not anymore under one of the package corresponding to the top folders imposed by Archi for the layers. I obtained exactly the same result.

This is illustrated in the following figure.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQFTP6fmOJIR5A/article-inline_image-shrink_1000_1488/0/1554364089913?e=1646870400&v=beta&t=I-YzY3L0d6gVchPETRluBLCSbWKslqe3klYd_FqA_o0)

In addition to confirm that a package structure is not preserved with the EA export based on Open Format (but it was already identified with the first test procedure), it also points out that the way Enterprise Architect deals with physical breakdown of an ArchiMate model is quite different than the one adopted by Archi with folders.

### Second interoperability test : Grouping

ArchiMate 3 came with a new construct, the "Grouping". If we consider the way it is implemented in Archi, it is a model element with a weak semantic, but which should allow to group heterogeneous elements of an ArchiMate model. If I don't like it due to the weak semantic, it provides some advantages and valuable usage when dealing with populations of heterogeneous elements which can 't be an aggregation or composition of an element typed with one of the modeling construct of ArchiMate. E.g. a fleet of devices of a given kind and with common properties. In such a case, Grouping is usefull and provides some flexibility. It could be considered in OWL as a DL query for which no Class is explicitely defined, at the condition we can captured through properties what characterize the elements of the Grouping.

The way Modelio supports grouping is quite similar.

If possible with Archi and Modelio, it is unfortunately not possible with the implementation of Grouping provided by EA, which doesn't correspond to a model element, but to a specialization of a boundary, which is a graphical element of a diagram. Archi proposes similar object, a Group, which is a visual element. Both Group and Grouping can have defined properties with Archi. This properties are not imported in SEA.

Test scenario:

1- creation of a model in Archi with interconnected groupings, one having a property

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQFpR6uDKSoL7A/article-inline_image-shrink_1000_1488/0/1555409285874?e=1646870400&v=beta&t=NLZ-G2bxTyCYPMtk2HXmQf0aFsjr0qvUit27wlAIa9A)

2- export using the open format

3- Import in SEA using the open format

4- Comparison

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQEyhb0zP33Wow/article-inline_image-shrink_1000_1488/0/1555409286119?e=1646870400&v=beta&t=0IvfywUIJ8W0ScT49B3x2164JduRPSlDXWlO6_CaJeM)

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQE71vRYNiURAA/article-inline_image-shrink_1000_1488/0/1555409286647?e=1646870400&v=beta&t=mYQa95-8wxuPN7kbEenr1kpZRXiqnTyfoevx9k8zxEQ)

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQH73IDVoeVo6Q/article-inline_image-shrink_1000_1488/0/1555409286639?e=1646870400&v=beta&t=uma4BFLRQqZJ2rDbEN_CXD-bol2jGVRumO_ISKkQqAQ)

We can see that the Grouping is a boundary, for which no properties exit after the import.

### Third interoperability test : relation between a model element and a relation

This feature is part of ArchiMate since version 3 of the language. It can be captured in models with SEA, Archi or Modelio.

However, when exporting from SEA using the open format, or when importing, such kind of relations are not considered.

Test scenarios:

Test 1:Creation of model with Archi, with a relation between a flow relation and a business object which is conveyed by the flow (the model is a representation of the high level functional view of ISA95)

1.  Export from Archi using the "Export model in open Exchange File Format" feature
2.  Research in the XML file of the relation
3.  Import in SEA using the "Import Model Exchange" File feature
4.  Checking on the model that the relation is present

Test 2: Creation of model with SEA, with a relation between a flow relation and a business object which is conveyed by the flow (same ISA95 model)

1.  Export from SEA using the "Generate Model Exchange File" feature
2.  Research in the XML file of the relation
3.  Import in Archi using the "Import Model from Model Exchange File" feature
4.  Checking on the model that the relation is present

Realising the text, we can see that SEA is not able to import such a construct from a standard exchange file, and can't generate it in a standard exchange file.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQEwzDfUPEuv1A/article-inline_image-shrink_1500_2232/0/1558342660178?e=1646870400&v=beta&t=_QoYI8-XS0N3MCwIhDw2B-BvPjExWzUh61m_gjzikCI)

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4E12AQFvgj2jpB-HOw/article-inline_image-shrink_1500_2232/0/1558342660790?e=1646870400&v=beta&t=BaiaSY3lBI4xwzI9WnP0qlnScQnTR0I-vomPg6R2m5Q)

_Assessment for the same tests with Modelio is ongoing when writing this version of the post and will be provided soon._

_At this stage, on a complex model exported from Archi, then reimported, some problems occurred with some relationships without source or target, and after suppressing them by hand, with some visual elements without references. Why the issues on these relationships particularly is under investigation._

### Fourth interoperability test : viewpoints

When working on a more systematic approach in the part 6 of this article, I created a test model with Modelio with a view for each viewpoint, and then tried to export it relying on the open format in order to make then an import in the last version of Archi. There were a blocking error when importing, due to some viewpoints definitions in the exported XML file. Removing it in a text editor, the import then worked quite well. Studying the XSD schemas of the open format, I discovered that such data in the exchange file is covered by the proposed schema for views and viewpoints. The issue comes from Archi. The two following images shows the error and the part of the XML data at the origin of the error.

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQFz4i0OikHz9Q/article-inline_image-shrink_1500_2232/0/1565692998664?e=1646870400&v=beta&t=sOKOQEJBfY9kBiqjNamBtkAgIQM609GEzcyBOXz7bZM)

![No alt text provided for this image](https://media-exp1.licdn.com/dms/image/C4D12AQGaZEflGs9Alg/article-inline_image-shrink_1500_2232/0/1565692998970?e=1646870400&v=beta&t=UL4UZKbvSptqio8zdnkFbGwhBmCGeey-1l8E0EMwQ5k)

It highlights that Archi is not necessarily 100% percent compliant (To be checked if support of views and viewpoints definition is optional or mandatory).

## Part 4 - Evolution of the ArchiMate language and associated spécifications

If you follow the news related to ArchiMate, the new minor version 3.1 is just out at the time of this article version, with the specification [C197](https://publications.opengroup.org/c197) the 5th of November, 2019. The main changes are summarized on the post "[ArchiMate® 3.1 Specification: The New Version of the Standard](https://blog.opengroup.org/2019/11/05/archimate-3-1-specification-the-new-version-of-the-standard/)" by Marc Lankhorst , whith as the main proposed improvments:

1.  The introduction of a directed notation for association
2.  Further formalization and refinement of the rules for deriving relationships
3.  The addition of a value stream element

The first point, the introduction of a directed notation for association, has no impact for data exchange and for interoperability. As visual representation is not exchanged at this level of details, you can exchange models even based on the previous version of ArchiMate without problems. In terms of communication involving people, as all ArchiMate relationships are oriented from a source to a target, providing the ability to visually indicate it is a plus, as it makes this information available on the model visible on the diagrams.

The second point is I think Something more related to a service that can be made available by an EA modeling tool, which is not necessarily related to the serialization of the model or its exchange. It is illustrated by previous versions of Archi which displayed the derived relationships on diagrams, without saving it in the model. If considering "derived" or "potential" relationships as something that can be serialized or exchanged, the question then arises concerning how to differentiate or indicating a relation is derived or potential. Let's consider it will not be the case, as it can lead to very huge file. Tools deriving or finding derieved and potential relationships will then probably not save them as it doesn't create value.

The third point creates an issue, between versionned tools supporting the previous versions, and those which don't. It also implies enriching the exchange schema, with the Value Stream Element but also with all the allowed relationships involving a value Stream and with the views allowing a Value Stream element or view dedicated to Value Stream. When the modeling constructs are hard coded, it will imply new software product version (or module version) and more heterogeneity for the application landscape, with potential import of ArchiMate 3.1 modeling tool to ArchiMate 30 modeling tool (no retro compatibility). This can eventually be solved if some mechanism are proposed for solving it, e.g. providing a tagged or stereotyped generic object (Business\_Object), with a formal concensus on the way to make it.

> With such a sample example, we can see the impact of change on Interoperability for digital continuity and interoperability

With such a simple example, we can see the potential impact of the evolution of a standardized language. Does it mean it should not change? I don't think so. May be what should be explored is provide modelers with a language that can be extended a standard way and then to address exchange from new version to older version with a transformation mechanism relying on it.

> Should modeling application integrate by design ability to manage language evolution?

A last impact: what about testing interoperability and about the test model to produce? It is not yet reflected in the article, but new testing models and update of the proposed approached will be provided very soon. Let's consider that an update of the exchange format is announced the 6th of November, 2019, but no date is indicated for the publication.

## Part 5- Naming conventions when coding imports/exports

For analysts and developers working on imports/exports between different tools relying on different programming or representation languages, one issue is that the adopted coding conventions may be quite different for the ArchiMate language constructs. E.g let's consider the Relationships matrix (part of the specification and made available in Archi), jArchi, ArchiMate-PlantUML and the Open Exchange Format.

You have to pay attention to the following points:

-   The used naming convention for names of elements or relationships is not the same than for Archi or Open Exchange Format for ArchiMate (coding issue as you have to deal with these differences for import/export functions)
-   ArchiMate-PlantUML distinquishes Business\_Location and Other\_Location, when only "Location" is specified for ArchiMate
-   If Grouping is an ArchiMate model element, it is not the case for Group which is only a visual element
-   Open Exchange Format or ArchiMate-PlantUML make explicit the difference between and\_Junction and or\_Junction, the Relationship Matrix combines both using only Junction

In addition to some identified non alignment with the specification (PlantUML), this implies tedious efforts for ensuring that not mistakes comes from the mapping between the various adopted naming conventions. The same should arise when dealing with production of object models or APIs derived from the ArchiMate language.

The following diagram reflects the naming convention used with the Open Exchange Format (Caps, neither "\_" or "-" used for the name.

![No alt text provided for this image](https://www.linkedin.com//:0)

![No alt text provided for this image](https://www.linkedin.com//:0)

![No alt text provided for this image](https://www.linkedin.com//:0)

## Part 6- Analysis

Through the performed tests and experimentation, what did we learn?

First we don't have full Interoperability between Archi, Modelio and SEA, as a full loop of exchange for a given model with a physical breakdown doesn't preserve this breakdown.

> We don't have full interoperability between Archi, Modelio and Enterprise Archictect

Should we consider that it is due to the solution providers?

Yes for Grouping, as it is indicated as a model element in the specifications. If we consider that Archi also provides an illustration of the concept as an implementation of reference, I think it is a misinterpretation of the EA team who implemented the support of ArchiMate.

Yes for the relation between a relation and another model element. It is definitively an issue with the implementation of export and import with the open Model Exchange Format of the Open Group. This could be a stopper for using EA as a tool being part of an Enterprise toolchain. However, it should be something easy to correct and to release for EA using the channel between EA and its clients. This shows that a tool can be ArchiMate compliant in terms of modeling, but not in terms of standardized import/export using the open Model Exchange Format. These is two different things to be considered, and which can impact each other as illustrated by Grouping construct.

No, for folders/package, as nothing is specified in ArchiMate 3.1 (or 2.1) concerning the way physical structuration should be achieved with ArchiMate. So **we are facing here an under specification**, which is at the origin of the issue.

> We are facing under specification but...

However, a question arises. It occurs that import and export based on the Open Format when using only Archi preserves the folder structure. How to explain that? The response stands on the Open Format specifications, which proposes an XML schema with some elements which should support the capture of physical breakdown elements such as folders.

It is also the reason why in Enterprise Architect from Archi also preserves the physical breakdown, creating a package for each folder with the appropriate hierarchy.

The problem should then stand on the Enterprise Architect export based on the open format. Can we consider that this export is not properly implemented by SEA?

It is not that simple. As SEA is not only an Enterprise Architecture modeling tool based on ArchiMate. It is a complete modeling platform relying on OMG standards for which ArchiMate is just one of the modeling language which can be supported using UML profiling. In addition, some unforced rules and features facilitates ArchiMate modeling with SEA, using the EA MDG Technology. Or such rules and features are usually not part of the specifications of a language, being ArchiMate, UML or any other standardized language.

> Solutions with advanced features may lead to incompatible physical organizations

If considering Modelio which is also based on UML/MDA technologies, the adopted approach is quite different than SEA, with clear separation of UML projects and ArchiMate projects. Mixing the languages is quite more restricted, only traceability or dependencies relations are allowed between the UML model elements and ArchiMate model elements. It facilitates ArchiMate model interchange, but limits ability to combine heterogeneous models and then ability for ensuring consistency between Design Models and SEA Models.

The different adopted strategies is what allows Solution Provider to differentiate their products on the market, by offering ways which will simplified the life of the users (Architects, Designers, System Engineers). For this, they may enforced some structural rules which are incompatible and then create interoperability issues. It is the case here:

-   Archi (and also Modelio with ArchiMate module) impose a top level structure based on ArchiMate for the layers, plus Views and Relations, and automatically put the modeling objects at the root of these folders by default, according to the layer they belong to. If possible to create other folders below them, it is quite difficult to create a complementary hierarchy which is reflected automatically in all the layers, and with the support of positioning the model elements in such a structure without having to make it manually. I.e. Archi doesn't support the ability to create a physical breakdown of models. Is it a weakness of Archi? Not exactly, it is more a weakness of ArchiMate which doesn't specify it. Archi being an open and free implementation of reference of ArchiMate, which doesn't rely on the Object Management Group modeling framework, it is quite difficult to blame the Archi team not to propose it, in particular because many consider that OMG modeling framework is too complicated. Being not based on OMG modeling framework, Archi implementation also lead to a set of quite excellent innovative ideas concerning visual modeling, correcting some drawbacks of traditional UML metamodeling platforms, in particular inheritance of traditional diagramming approach which prevents global views interrelating the content of traditional diagrams (fortunately, solution providers started to move and since few years, important innovations occurred correcting this drawback).
-   Enterprise Architect is a modeling platform based on the OMG modeling framework, including the Meta Object Facility, UML and many other languages as UML profiles. Doing so, it relies on OMG standardized specifications for implementing physical breakdowns of models. More precisely, the concerned specification is the one of UML, with as the main concerned modeling construct the package, which is a container allowing to partition the content of models produced with a UML modeler. For one modeling project, it is possible to capture several UML models, by stereotyping packages. So such UML models (not to be confused with model produced with a UML Modeling platform, which are more "projects") are also containers. So the model elements are contained in the model, which is a container due to the fact they are a specialization of a package. Because of that, EA will adopt a strategy which is quite different than the one adopted by Archi, strongly driven by the fact that SEA is first a modeling platform relying on the OMG modeling framework. If considering the practices of the concerned community, it is not very usual constraining some structural package reflecting layers. If considering how constraining it is when using Archi, it is also something we should not recommend to impose in order to facilitate collaborative and distributed production of heterogeneous models, which could be also required when dealing with Enterprise Modeling, in particular considering a digital business ecosystem concerning several independent organizations or enterprises.

Also, considering the Part 4 about evolution of the language, it reflects the important to consider the continuous evolution of a language by design. It is something that is most of the time not anticipated, considering that it will be included in new versions of software tools, without considering the impact on continuous digital interoperability within a business landscape.

This implies some rigor when producing libraries related to mappings between different environments relying on various languages, in particular for naming conventions and management of the little differences or compliance issues for the set of considered tools, as illustrated by the Part 5.

## Part 7- Proposal for addressing the identified issues

For addressing the issue, **one solution could be ArchiMate alignement with OMG modeling framework**. But ArchiMate is produced by the Open Group, and the two organizations can be considered as competitors. In addition, the OMG modeling framework is more complicated , and the community delivering modeling platforms based on these specifications is not so mature concerning delivery of compatible and interoperable platforms. Interchange of composite models with diagrams is still today very challenging within an industrial context. In particular, we will face exactly the same situation concerning differentiation between solutions leading to incompatible constraints with full respect of underspecified languages.

**Should we enforce the constraints coming from Archi in SEA, with top level packages reflecting the layers?** Not really a good idea, as it is not really convenient for architects, and requires a lot of work for ensuring the consistency, plus complex package/folder structure. Also, I consider that enforcing a physical structure of a model based on the categorization of model elements is a bad idea. I think the proper way to deal with that is to create taxonomies which will not enforce any structural constraint for the physical breakdown of the model. If still keeping this structuration rule for the ArchiMate files, this should be hidden for the users on the application front end, and new feature supporting package similar/compatible structuration should be made available. This approach works quite well, as it is the basis of ontology modeling with OWL. Unfortunately, Archi is an open source project with limited resources despite the important number of users and the high interest of the solution for the Open Group ArchiMate community (Here I encourage users to contribute to the funding of the project becoming through Patreon). So such a feature may not be prior on the roadmap of the project, considering that some other could provide more value and consequently will come before for those investing time and effort on the project.

So according to me, if willing to produce models which could be used both in SEA and Archi, ensuring an improved interoperability and interchangeability with shareable breakdown of models, the approach should be:

As Archi community member, to push the request for including an evolution:

1.  Changing structuration of the model based on layers, and add the ability to structure physically the model(s) in a way which is similar to what is supported by package based approach
2.  Eventually to build it without changing the serialization file structuration, in order to avoid incompatibility with legacy file structure. but it requires extra work for hiding it on the user front end, and makes the things a little bit more complex.

As ArchiMate/Open Group community member, to push a request for addressing the physical breakdown structuration of ArchiMate model within the specifications, in order to ensure the expected interoperability.

As EA user, to see if feasible using MDG technologies for ArchiMate to modify the export in order to ensure accurate folder/package mapping, after deciding the rules for structuring folders with Archi. Such rules, to be enforced manually, could be the subject for a little extension of Archi (Plugin? Script with jArchi? Other?). Also, should it be a specific extension for an organisation, or could it be shared with the Archi community also using EA or other similar solution products (Modelio, Magic Draw, etc.). It implies a good knowledge of the Open Format specification, and probably no change on the specifications (as folder exchange works with Archi - but some work is required to validate that the Open Format definitively addressed it correctly without any issue).

For Modelio, as assessment is on going, proposed solutions for not yet identified issues can be proposed yet ;)

Concerning the Part 4 related to language evolution, a solution could be to support by design the ability to support the language: considering extensibility which supports formalizing new modeling constructs with a legacy extended more generic one, some bidirectional transformation and exchange should be possible. Both should be provided with the extension of the language, for minimizing the impact of a language evolution.

For the Part 5, the community could propose shared naming conventions (bindings) which could make the work of developers and tests easier. Waiting for such an hypothetic effort, managing some shared knowledge about the existing differences and some libraries managing them could be useful, in particular when willing to push ArchiMate models to other technological environments, such as Semantic Web, APIs for micro services or graph databases.

## Part 8: a more systematic approach for testing ArchiMate interoperability?

### The needs

On the previous parts of the article, I mainly pointed out some kinds of issue, with some dedicated demonstration data sets I created on the run when encountering problems.

But many more issues can be identified, simply related to errors when implementing and insufficient tests during implementation. It is in particular the case for the constraints on modeling constructs which can be linked on the base of the ArchiMate relationships. It can be as well related to specifications which are not consistent or to under specifications.

In the article "Linked Enterprises: from ArchiMate language to ArchiMate Web Ontology?", I assessed the effort to be made for deriving an ontology from the ArchiMate langage. The effort is quite similar, even higher, when willing to deal with systematic testing and test data set creation.

1.  Fist we have to check that all the modeling constructs which are not relations can be interchange. So we need a model with one model element of each type.
2.  Then we need to check that all the allowed relationship can be interchanged.
3.  Also, we need to check that the non allowed relationships are properly managed by the tools.
4.  If not allowed relationships are described in an exchange file, does it lead to a software error or if it is managed in order to indicated that an issue is to be corrected in the model, or could it be properly managed as an extension/modification of the set of constraints to be applied?
5.  Can we exchange the diagrams without loosing the content?
6.  Can we exchange the diagrams without loosing the form?
7.  Are the information related to viewpoints typing the views correctly exchanged?
8.  Do constraints related to viewpoints create errors if not enforced by tools which are the source of exchange using the open format?
9.  Are the folders/packages structure (breakdowns) interchanged or lost?
10.  Are the properties for each model element preserved or not during interchange?
11.  Can stereotypes as proposed in ArchiMate 3 can be created and interchanged?

The open format for ArchiMate model interchanged being a realization of the specification, it should be assessed as well, with response to the question:

12\. Are ArchiMate specifications and XML Schema proposed for Open Exchange format aligned.

In addition, the question of the preservation of IDs occurs.

13\. Can the IDs being preserved occurs between the different applications?

14\. How do we manage Reference Data, or consistency between several reference data management system?

So what are then the test data sets to create in order to validate each of the 14 points identified?

1.  Here a first model with one element per construct is to be produced, without any view. It means 61 (including AndJunction and OrJunction) model elements. In order to anticipate the next test and to be able to create relationships between two model elements with the same type, we can double the number of model elements, 2 with the same kind in the model.
2.  Here, starting from the previous test data set, we should create a new test data set with a link per allowed relation, and shake that they are preserved by exchange loop. We can also start from the test file to be created for 3, with all the kind of relations created between all the kind of objects, without considering the restrictions, and then remove the relations which should not be allowed. The number of elements in the model is 10106. The created model is model002.
3.  Here, starting from the previous test data sets (1 or 2), we need to have a link per not allowed relation, and shake how interchange behave. Error for the import? Indication that some imported link are not allowed? As most of the tools are constraining the links that can be created, creation of such data set should be made without using a modeling tool (potential exception: EA). Creating an XML interchange file can be difficult using a text file editor. Creating it automatically with a program is probably the most efficient way, knowing that 61\*61\*11 links should be created in order covering all the cases. Considering that 2 instances of each entities is also created, the number of elements in the model is 41053. Creation using user interface of modeling tools, even for 2, is very long and error prone. So automation is highly recommended for creation of the test file. It can eventually be made manually, using some textual template which allow to make if fast, even manually, with a text editor. The produced model should respect the schemas provided by the Open Group with the Open Exchange Format for ArchiMate specification. So a validating parser should also be available if we want to ensure that the produced test files are valid. The created model is model003.
4.  Idem, we use model003 for this
5.  Here a first idea is to use the model created for 3, and create one view (layered) with all the model element displayed. It should then be possible to check automatically if one visual representation exists per model element in the created view. However, we are facing here issues with the robustness of tools when drawing huge models. With most of the tools, drawing diagrams with all the elements lead to memory issues and sometimes it is needed to stop the tool. So several views are to be created, and eventually we can envisage producing test models with less relationships. However keeping all the relationships is a good way testing tools robustness with huge models.
6.  Let's consider that the different kind of automated layout could lead to differences between diagrams. So it should be checked if the visual representation of model element is preserved. For entities, location and size. It is more complicated for links, which can be created using many layouts which are tools dependent.
7.  From the test data set of 2, we can create a set of views, one for each viewpoint, and display on it all the model elements which are allowed in such a viewpoint. Then by interchange, are the viewpoints preserved and indication on what can or can't be part of each viewpoint is the same for each tool? Could be done by program or by a person checking on a modeling tool.
8.  Here we should created a test data set similar to the initially proposed one, with as model elements those proposed for 7 and distribution in the packages in a way that could be checked automatically.
9.  Here we can created from the model with all allowed constructs a set of views, one per viewpoint, with all the model elements displayed in the view with Archi (which support it, and just apply ghosting to model elements which should not be displayed for the viewpoint.
10.  Here we can create from the model with all allowed constructs a new test data model with added properties, with names and values which could be tested by program.
11.  Let's create a stereotype with a modeling tool supporting this modeling future, and let's try interchange
12.  Let's check if the format can be mapped with each part of the specification studying the documents. Full interchange loop with the data set created in 7 should be another way to validate it, except for stereotypes, folders/packages or properties which are not necessarily 100% aligned between ArchiMate specification and interchange format.

### The first attempt for creating test data set

I started to work with following exactly what was described in the description of the needs (which were updated according to the lessons learnt from this first attempt).

Here some captures of test data sets I created by hand, first with Modelio, but it was very long. I then continued with Archi, which allowed to make it quicker. But still too long. It is why I think that automation should be the way, not only for creating testing data, but also for checking.

Let's note I didn't rely on test data sets available from the Open Group communities, as it doesn't seem they are containing all the data required for testing constraints on relationships, or behavior when data are provided which are not respecting the constraints.

Also, another goal is to consider some optional requirements or differences between actual implementations which are tool specific. The objective here is not to certify a solution, but to assess and to qualify a collaboration environment between organizational units or enterprises having their own EA repositories based on heterogeneous solutions, being certified by Open Group or not. I leant from my past experience in the PLM area (Product and Process data exchange, sharing and long term archiving in the manufacturing domain and within extended enterprise) that a global collaboration system is to be qualified and can't rely only on usage of certified components which are not qualified within the actual collaboration context and environment (containing system).

The views/diagrams on the next snapshots are quite ugly, and I received many comments about the fact that they are useless models for supporting decision making by Enterprise stakeholders. But it is absolutely not the intended usage of the produced models: the goal is to assess networks of applications which are EA modeling tools/ EA model repositories, which should be implied for building End to End collaboration for a network of organisations.

![No alt text provided for this image](https://www.linkedin.com//:0)

![No alt text provided for this image](https://www.linkedin.com//:0)

Because of the required time, I changed my way of producing test models, and updated the "needs" section consequently. I also started to draft an approach using ArchiMate which is described in the following sub section.

### A first draft model of a systematic approach

This model aims at qualifying digital continuity for a chain of heterogeneous tools. As a prerequisite, each tool is to be qualified standalone with export and import of test data sets and validation that no data are lost.

> Don't think that implicitly import and export for a given tool will preserve the models.

Performing such tests will allow identifying import or export which will also be used in a tool chain, so to save time when analyzing the tools.

![No alt text provided for this image](https://www.linkedin.com//:0)

The model contains first the set of goals from which test data and test processes are to be created. It should correspond to the 14 points in the previous "Needs" section (I didn't align it yet).

Then relying on a set up testing environment, derived from the environment depicted in the Part 1 of the article, a test plan is to be created, with testing tasks to be run, following testing procedure/protocols which can be made generic and applied systematically with all the solutions to be assessed. The content of the test files will be created in order to achieve the testing goals, relying on what is described on the "Needs" section for creating test data sets

Of course, proposing this approach was strongly related with starting to experiment, and some interesting results can already be shared.

A first interesting result: when creating a model with not allowed relationships between some kind of elements (constraints associated to relationships in the ArchiMate specification), I was able to import it in Archi without any problem: no error signaled and no stop of the import. It means that we can have invalide models in Archi when importing.

A second interesting result: when I imported some models with Modelio, I had some rejection of the import without any indication of the reason why the model was rejected. A problem I faced is that sometimes, the same model was accepted and sometimes, it was not. Without indication of the problem (here I've to investigate if some logs are indicating the problem), it is quite difficult to perform analysis. So one expectation for any tool providing import capabilities is to have indication of the reason why they are refusing to perform some import.

A third interesting result: as I created XML file manually, I was able to understand better the structure of the schemas associated to the Open Group's Open Exchange Format for ArchiMate, in particular the "Organisation" and "Viewpoints" sections. The first one is about how the model elements are physically decomposed. It is related to the Part 2 of the article, dealing with issue encountered with preservation of the physical breakdown when using EA. Such physical structure of a model is not part of the ArchiMate language (unlike UML which include modeling of packages or containment in the language specifications). So it means that for dealing with interoperability for ArchiMate, considering the language only is insufficient, we also need to consider the structuration of models as proposed by the interchange format. I think it is an underspecification of the language, as such organisation is always displayed on user interface with "Project" or "Model" pan indicating such organisation. Solution providers are free to call it "folder" or "package", so we have something "nebulous" here which may lead to interoperability issues, i.e. data loss in exchange loops.

A fourth interesting result: there is a section "viewpoint" in the exchange schema. For each viewpoint, it provides the list of supported modeling objects which can be used for a viewpoint. It is quite interesting if willing to be able to create you own viewpoints, knowing that proposed viewpoints by ArchiMate are not anymore part of the specifications. It is since ArchiMate 3 just a set of examples. The problem is that some tools are today structuring ArchiMate modeling on proposed viewpoints (e.g. Archi or EA) without proposing ways to create new viewpoints and to exchange what they can contain. Modelio do it, but when you try to exchange a model through the open format with tools like Archi, you have an error due to the presence for the viewpoint section. If accepting it, an issue will be how to manage viewpoints which are not those described in the specifications, if creation and management of viewpoints is not part of the capabilities of the modeling tools.

A fourth interesting result: there is a section "viewpoint" in the exchange schema. For each viewpoint, it provides the list of supported modeling objects which can be used for a viewpoint. It is quite interesting if willing to be able to create you own viewpoints, knowing that proposed viewpoints by ArchiMate are not anymore part of the specifications. It is since ArchiMate 3 just a set of examples. The problem is that some tools are today structuring ArchiMate modeling on proposed viewpoints (e.g. Archi or EA) without proposing ways to create new viewpoints and to exchange what they can contain. Modelio do it, but when you try to exchange a model through the open format with tools like Archi, you have an error due to the presence for the viewpoint section. If accepting it, an issue will be how to manage viewpoints which are not those described in the specifications, if creation and management of viewpoints is not part of the capabilities of the modeling tools.

Testing export then import of a model with folders with Archi, I had the surprise not to retrieve the folders. A fifth interesting result is that it implies that test procedure should include qualifying each tool standalone before to qualify tool chains with heterogeneous tools.

## Conclusion: Ensuring interoperability is not a long quiet rive

If considering that the ArchiMate community addressed the needs for interoperability through a common well formalized language and an Open Format for model interchange, it occurs that we face however some interoperability issues. Several were initially identified are reported here.

The first one is related to folder/package preservation: the physical breakdown of a model, based on folders (like Archi) or packages (like SEA), is not necessarily preserved, as we demonstrated it. The analysis shows that this come from a set of factors, making the issue not so easy to be resolved. Combination of two frameworks produced by different organizations, specifications not addressing the needs for composite distributed models, different strategies for improving the architect user experience which are differentiators for the product, but result in incompatible structural constraints, cost of reengineering of solutions if willing at the same time to add such functionality, but also preserve legacy format for the concerned solutions.

The second one is related to Grouping: SEA didn't implement it properly, as a model element. In place, they specialized a Boundary, which is a visual element only.

The third is related to missing import/export of relations between a relation and a model element for SEA.

The fourth is related to exchange of views and viewpoints definitions, which failed between Modelio and Archi.

Such issues are not specific to ArchiMate, and I faced the same for UML modeling solutions, or for PLM interoperability with Manufacturing Data standards (ISO 10303 STEP, ISA 95, etc.)

However, with growing importance of digitalization and usage of Enterprise Modeling solutions, it is important for the future to consider support of collaborative modeling within distributed and heterogeneous community. UML comes with features which should allow to address it, mainly relying on packages. It is today a limitation of the ArchiMate specifications not having a similar and compatible mechanism, being for supporting the emerging needs or for ensuring interoperability with preservation of physical breakdown of ArchiMate model(s).

Also, any optional requirement is always creating the opportunity for some non interoperability, as well as underspecification. I think that in the future, it should be addressed.

-   better support of stereotypes by the community and the market tools (even if I don't like the mechanism)
-   preservation of identifiers
-   physical breakdown of models
-   ability to be combine with other modeling languages in UML meta-modeling environments (preventing language silos between different kind of architects and testing of multi-languages models)

Finally, having more systematic processes for testing, enriching the current practices for solution certification, should help. It will allow identification of interoperability issues on all the tools, being certified or not, when willing to deal with digital continuity between networked organisations.

A first draft of a proposed approach was described here, and experimentation when defining and applying test protocols already allowed identifying some new issues.

If interchanging models is quite advanced within the ArchiMate Digital Business Ecosystem compared to some other communities, some issues nevertheless exist. An approach allowing to support it a more systematic way, adopting an holistic approach, should help a lot for ensuring end to end interoperability between organisations (internal to enterprise or between collaborating enterprises), leveraging the impact and increasing the value of ArchiMate (SEA should not be restricted to model a single enterprise in the current digitalisation context with the Impact of Internet).

Finally, the adopted approach, is quite experimental and "black box" approach.

1.  There is neither any deep study of the XML schemas proposed by the Open Group for the Open Format, nor tooling for analyzing the content of XML files, taking advantage of validating parsing that comes with XML technologies. Could we assess interoperability starting from models generated from the interchange XML schemas and using mainly XML technologies, not software products? And are we sure that some issues are not coming from the specification of the Open format itself, or from some inconsistency between ArchiMate language specification and open format specification?
2.  Also, we didn't explore if possible publishing EA models using Semantic Web technology, relying on [ontology derived from ArchiMate?](https://www.linkedin.com/pulse/from-archimate-language-web-ontology-dr-nicolas-figay/)

This will be the subject of my two next articles, "[ArchiMate Interoperability: from models to linked data using semantic web technologies?](https://www.linkedin.com/pulse/archimate-from-models-linked-data-using-semantic-web-dr-nicolas-figay/?published=t)" and "ArchiMate Interoperability: what do we learn from exchange format schemas study?"

Don't hesitate sharing you comments, knowledge, viewpoints and experience/best practices on the topic.

And if you think this article creates value, don't hesitate to share it and like it ;)