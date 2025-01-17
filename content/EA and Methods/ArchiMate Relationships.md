ArchiMate® 3.1 Specification  
[Copyright](https://pubs.opengroup.org/architecture/archimate3-doc/copyright.html) © 2012-2019 The Open Group

___

#Technology #EA #Methods #ArchiMate

# ArchiMate Relationships

The relationships are classified as follows (see Figure 21):

•               _Structural_ relationships, which model the static construction or composition of concepts of the same or different types

•               _Dependency_ relationships, which model how elements are used to support other elements

•               _Dynamic_ relationships, which are used to model behavioral dependencies between elements

•               _Other_ relationships, which do not fall into one of the above categories

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image035.png)

Figure 21: Overview of Relationships

Each relationship has exactly one “from” and one “to” concept (element, relationship, or relationship connector) as endpoints. The following restrictions apply:

•               No relationships are allowed between two relationships

•               All relationships connected with relationship connectors must be of the same type

•               A chain of relationships of the same type that connects two elements, and is in turn connected via relationship connectors, is valid only if a direct relationship of that same type between those two elements is valid

•               A relationship connecting an element with a second relationship can only be an aggregation, composition, or association; aggregation or composition are valid only from a composite element to that second relationship

It is good practice to explicitly name or label any relationship that would else be ambiguous or otherwise misunderstood.

For the sake of readability, the metamodel figures throughout this document do not show all possible relationships in the language. Section 5.7 describes a set of derivation rules to derive indirect relationships between elements in a model. Aggregation, composition, and specialization relationships are always permitted between two elements of the same type, and association is always allowed between any two elements, and between any element and relationship. The exact specification of permitted relationships is given in Appendix B.

## 5.1                 Structural Relationships

Structural relationships represent the “static” coherence within an architecture. The uniting (composing, aggregating, assigned, or realizing) concept (the “from” side of the relationship) is always an element; for assignment and realization it can be an element or a relationships connector. The united (being composed, aggregated, assigned to, or realized) concept (the “to” side of the relationship) may in some cases also be another relationship or relationship connector.

As an alternative to the graphical notations proposed in this section, structural relationships may also be expressed by nesting the united concept within the uniting element. Note, however, that this can lead to ambiguous views (although unambiguous in the model), in case multiple structural relationships are allowed between these elements.

### 5.1.1              Composition Relationship

The composition relationship represents that an element consists of one or more other concepts.

The composition relationship has been inspired by the composition relationship in UML class diagrams. Composition is a whole/part relationship that expresses an existence dependency: if a composite is deleted, its parts are (normally) deleted as well. When you model real-world elements – for example, an organization structure of departments and teams expressed as business actors – this dependency applies to these elements themselves. When you model exemplars or categories – as is common in Enterprise Architecture – this dependency may be interpreted as applying to their real-world instances. For example, a specific kind of server can be modeled as a node composed of a device and system software; this implies an existence dependency between individual servers of that kind and the individual devices and system software instances of which they consist.

A composition relationship is always allowed between two instances of the same element type.

In addition to this, the metamodel explicitly defines other source and target elements that may be connected by a composition relationship.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image036.png)

Figure 22: Composition Notation

The interpretation of a composition relationship is that the _whole or part_ of the source element is composed of the _whole of_ the target element. See also Section 5.1.5.

Example

Example 2 shows the two ways to express that the “Financial Processing” business function is composed of three sub-functions.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image037.png)

Example 2: Composition

### 5.1.2              Aggregation Relationship

The aggregation relationship represents that an element combines one or more other concepts.

The aggregation relationship has been inspired by the aggregation relationship in UML class diagrams. Unlike composition, aggregation does not imply an existence dependency between the aggregating and aggregated concepts.

An aggregation relationship is always allowed between two instances of the same element type.

In addition to this, the metamodel explicitly defines other source and target elements that may be connected by an aggregation relationship.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image038.png)

Figure 23: Aggregation Notation

The interpretation of an aggregation relationship is that the _whole or part_ of the source element aggregates the _whole of_ the target concept. See also Section 5.1.5.

Example

Example 3 shows two ways to express that the “Customer File” aggregates an “Insurance Policy” and “Insurance Claim”.

 ![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image039.png)

Example 3: Aggregation

### 5.1.3              Assignment Relationship

The assignment relationship represents the allocation of responsibility, performance of behavior, storage, or execution.

The assignment relationship links active structure elements with units of behavior that are performed by them, business actors with business roles that are fulfilled by them, and nodes with technology objects. It can, for example, relate an internal active structure element with an internal behavior element, an interface with a service, or a node, device, and system software with an artifact. The full set of permitted relationships is listed in Appendix B.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image040.png)

Figure 24: Assignment Notation

In the ArchiMate framework described in Section 3.4, it always points from active structure to behavior, from behavior to passive structure, and from active to passive structure. The non-directional notation from the ArchiMate 2.1 Specification and before, which shows the black ball at both ends of the relationship, is still allowed but deprecated.

As with all structural relationships, an assignment relationship can also be expressed by nesting the model elements. The direction mentioned above is also the direction of nesting; for example, a business role inside the business actor performing that role, an application function inside an application component executing that function, or an artifact inside a node that stores it.

The interpretation of an assignment relationship is that the _whole or part_ of the source element is assigned the _whole of_ the target element (see also Section 5.1.5). This means that if, for example, two active structure elements are assigned to the same behavior element, either of them can perform the complete behavior. If both active structure elements are needed to perform the behavior, the grouping element or a junction (see Section 5.5) can be used, and if the combination of these elements has a more substantive and independent character, a collaboration would be the right way to express this.

Example

Example 4 includes the two ways to express the assignment relationship. The “Finance” application component is assigned to the “Transaction Processing” application function, and the “Payment Interface” is assigned to the “Payment Service”.

 ![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image041.png)

Example 4: Assignment

### 5.1.4              Realization Relationship

The realization relationship represents that an entity plays a critical role in the creation, achievement, sustenance, or operation of a more abstract entity.

The realization relationship indicates that more abstract entities (“what” or “logical”) are realized by means of more tangible entities (“how” or “physical”). The realization relationship is used to model run-time realization; for example, that a business process realizes a business service, and that a data object realizes a business object, an artifact realizes an application component, or a core element realizes a motivation element.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image042.png)

Figure 25: Realization Notation

The interpretation of a realization relationship is that the _whole or part_ of the source element realizes the _whole of_ the target element (see also Section 5.1.5). This means that if, for example, two internal behavior elements have a realization relationship to the same service, either of them can realize the complete service. If both internal behavior elements are needed to realize, the grouping element or an _and_ junction (see Section 5.5.1) can be used. For weaker types of positive, neutral, or negative contribution to the realization of a motivation element, the influence relationship (see Section 5.2.3) should be used.

Example

Example 5 illustrates two ways to use the realization relationship. A “Transaction Processing” business function realizes a “Billing Service”; the “Billing Data” business object is realized by the representation “Paper Invoice”.

 ![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image043.png)

Example 5: Realization

### 5.1.5              Semantics of Structural Relationships

Structural relationships describe that the element on the source side contains, groups, performs, or realizes the concept on the target side of the relationship. Structural relationships can be transitively applied to (possibly unmodeled) parts of the source element. Below are some examples of how these semantics work:

•               Composition and aggregation relationships from parts also apply to the whole

For example, if a part of A aggregates B, A itself is also considered to aggregate B. Conversely, if A aggregates B, that can be interpreted as some part of A aggregating B.

•               Assignment relationships to behavior elements also apply to the active structure elements

For example, if business role A is assigned to business process B, some part of A may perform B. Conversely, if a part of A is assigned to B, A itself is also considered to be assigned to B.

•               Realization relationships to external behavior elements also apply to the internal behavior elements

For example, if a service B is realized by a process A, B may be realized by some part of A. Conversely, if a part of A realizes B, A itself is also considered to realize B.

Example

In the left-hand side of Example 6, the entire business actor B (possibly a department) is composed in business actor A (possibly a division), via some unmodeled element inside A. In the example on the right, business process A completely realizes business service B, via some unmodeled element inside A.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image044.png)

Example 6: Semantics of Structural Relationships

## 5.2                 Dependency Relationships

Dependency relationships describe how elements support or are used by other elements. Four types of dependency relationship are distinguished:

•               The _serving_ relationship represents a _control_ dependency, denoted by a solid line

•               The _access_ relationship represents a _data_ dependency, denoted by a dotted line

•               The _influence_ relationship represents an _impact_ dependency, denoted by a dashed line

•               The _association_ relationship represents a dependency not covered by any of the other relationships

Note that, although the notation of these relationships resembles the notation of the dependency relationship in UML, these relationships have distinct meanings in ArchiMate notation and (usually) point in the opposite direction. One advantage of this is that it yields models with directionality, where most of the arrows that represent such supporting, influencing, serving, or realizing dependencies point “upwards” towards the client/user/business, as you can see in the layered viewpoint example in Section C.1.5. Another reason for this direction, in particular for the serving relationship, is that it abstracts from the “caller” or “initiator”, since a service may be delivered proactively or reactively. The direction of delivery is always the same, but the starting point for the interaction can be on either end. UML’s dependency is often used to denote the latter, showing that the caller depends on some operation that is called. However, for modeling this type of initiative, the ArchiMate language provides the triggering relationship (Section 5.3.1), which can be interpreted as a dynamic (i.e., temporal) dependency. Similarly, the flow relationship is used to model how something (usually information) is transferred from one element to another, which is also a dynamic kind of dependency.

### 5.2.1              Serving Relationship

The serving relationship represents that an element provides its functionality to another element.

The serving relationship describes how the services or interfaces offered by a behavior or active structure element serve entities in their environment. This relationship is applied for both the behavior aspect and the active structure aspect.

Compared to the earlier versions of this standard, the name of this relationship has been changed from “used by” to “serving”, to better reflect its direction with an active verb: a service serves a user. The meaning of the relationship has not been altered. The “used by” designation is still allowed but deprecated, and will be removed in a future version of the standard.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image045.png)

Figure 26: Serving Notation

Example

Example 7 illustrates the serving relationship. The “Payment Interface” serves the “Customer”, while the “Payment Service” serves the “Pay Invoices” business process of that customer.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image046.png)

Example 7: Serving

### 5.2.2              Access Relationship

The access relationship represents the ability of behavior and active structure elements to observe or act upon passive structure elements.

The access relationship indicates that a process, function, interaction, service, or event “does something” with a passive structure element; e.g., create a new object, read data from the object, write or modify the object data, or delete the object. The relationship can also be used to indicate that the object is just associated with the behavior; e.g., it models the information that comes with an event, or the information that is made available as part of a service. The arrow head, if present, indicates the creation, change, or usage of passive structure elements. The access relationship should not be confused with the UML dependency relationship, which uses a similar notation.

Note that, at the metamodel level, the direction of the relationship is always from an active structure element or a behavior element to a passive structure element, although the notation may point in the other direction to denote “read” access, and in both directions to denote read-write access. Care must be taken when using access with derived relationships because the arrow on the relationship has no bearing to its directionality.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image047.png)

Figure 27: Access Notation

Alternatively, an access relationship can be expressed by nesting the passive structure element inside the behavior or active structure element that accesses it; for example, nesting a data object inside an application component.

Example

Example 8 illustrates the access relationship. The “Create Invoice” sub-process writes/creates the “Invoice” business object; the “Send Invoice” sub-process reads that object.

 ![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image048.png)

Example 8: Access

### 5.2.3              Influence Relationship

The influence relationship represents that an element affects the implementation or achievement of some motivation element.

The influence relationship is used to describe that some architectural element influences achievement or implementation of a motivation element, such as a goal or a principle. In general, a motivation element is realized to a certain degree. For example, consistently satisfying the principle “serve customers wherever they are” will help to make the goal “increase market share” come true. In other words, the principle contributes to the goal. In turn, to implement the principle “serve customers wherever they are”, it may be useful to impose a requirement of “24x7 web availability” on some customer-facing application component. This can be modeled as a requirement that has an influence on that principle, and as an application component that in turn influences the requirement. Consistently modeling these dependencies with an influence relationship yields a traceable motivational path that explains why, in this example, a certain application component contributes to the corporate goal to “increase market share”. This kind of traceability supports measuring the results of Enterprise Architecture, and provides valuable information to, for example, change impact assessments.

Additional to this “vertical” use of contribution, from core elements upwards to requirements and goals, the relationship can also be used to model “horizontal” contributions between motivation elements. The influence relationship in that case describes that some motivation element may influence (the achievement or implementation of) another motivation element. In general, a motivation element is achieved to a certain degree. An influence by some other element may affect this degree, depending on the degree in which this other element is satisfied itself. For example, the degree in which the goal to increase customer satisfaction is realized may be represented by the percentage of satisfied customers that participate in a market interview. This percentage may be influenced by, for example, the goal to improve the reputation of the company; i.e., a higher degree of improvement results in a higher increase in customer satisfaction. On the other hand, the goal to lay off employees may influence the company reputation negatively; i.e., more lay-offs could result in a lower increase (or even decrease) in the company reputation. And thus (indirectly), the goal to increase customer satisfaction may also be influenced negatively.

The realization relationship should be used to represent relationships that are critical to the existence or realization of the target, while the influence relationship should be used to represent relationships that are not critical to the target object’s existence or realization. For example, a business actor representing a construction crew might realize the goal of constructing a building, and a requirement to add additional skilled construction workers to an already adequate crew might influence the goal of constructing the building, but also realize an additional goal of opening the building by a particular date. Moreover, an influence relationship can be used to model either:

•               The fact that an element positively contributes to the achievement or implementation of some motivation element, or

•               The fact that an element negatively influences – i.e., prevents or counteracts – such achievement

Attributes can be used to indicate the sign and/or strength of the influence. The choice of possible attribute values is left to the modeler; e.g., {++, +, 0, -, --} or \[0..10\]. By default, the influence relationship models a contribution with unspecified sign and strength.

![fig26](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image049.png)

Figure 28: Influence Notation

Example

Example 9 illustrates the use of the influence relationship to model the different effects of the same requirement, “Assign Personal Assistant”. This has a strongly positive influence on “Reduce Workload Of Employees”, but a strongly negative influence on “Decrease Costs”.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image050.png)

Example 9: Influence

### 5.2.4              Association Relationship

An association relationship represents an unspecified relationship, or one that is not represented by another ArchiMate relationship.

An association relationship is always allowed between two elements, or between a relationship and an element.

The association relationship can be used when drawing a first high-level model where relationships are initially denoted in a generic way, and later refined to show more specific relationship types. In the metamodel pictures, some specific uses of the association relationship are explicitly shown. An association is undirected by default but may be directed. See also Section 5.2.5.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image051.png)

Figure 29: Association Notation

Example

Example 10 illustrates two directed association relationships between a contract and two business objects to which this contract refers. It also shows an association between a flow relationship and this contract, to indicate the kind of information that is communicated between the two functions.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image052.png)

Example 10: Association

### 5.2.5              Semantics of Dependency Relationships

Dependency relationships describe that a part of the target element has a dependency on a part of the source element. Although there is a dependency between the two elements, it does not necessarily mean this applies to all of the parts of the element as defined by any structural relationships.

This semantic allows you to model dependencies at a high level (with details removed) without implying specific dependencies at a more detailed level. This means, for example, that:

•               In serving relationships, some part of an internal behavior element is served by some part of an external behavior element; for example, if a business service A serves a business process B, some unmodeled sub-service of A may serve an unmodeled sub-process of B

•               In access relationships, some part of a behavior element accesses some part of a passive structure element; for example, if an application function A accesses a data object B, some unmodeled sub-function of A may access an unmodeled part of B

•               In influence relationships, some part of a core element influences some part of a motivational element; for example, if an application component A influences a requirement B, some unmodeled part of A may influence some unmodeled part of B

•               In association relationships, some part of an element is related to some part of another element; if it is directed, it can only be used in derivations in that direction (see Section 5.7)

Example

In the left-hand side of Example 11, a part of business process B is served by a part of application service A. In the right-hand example, a part of business process B accesses (reads) a part of business object A.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image053.png)

Example 11: Semantics of Dependency Relationships

## 5.3                 Dynamic Relationships

The dynamic relationships describe temporal dependencies between elements within the architecture. Two types of dynamic relationships are distinguished: _triggering_ and _flow_.

### 5.3.1              Triggering Relationship

The triggering relationship represents a temporal or causal relationship between elements.

The triggering relationship is used to model the temporal or causal precedence of behavior elements in a process. The interpretation of a triggering relationship is that some part of the source element should be completed before the target element can start (see also Section 5.3.3). Note that this does not necessarily represent that one behavior element actively starts another; a traffic light turning green also triggers the cars to go through the intersection.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image054.png)

Figure 30: Triggering Notation

Example

Example 12 illustrates that triggering relationships are used to model causal dependencies between (sub-)processes and/or events.

 ![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image055.png)

Example 12: Triggering

### 5.3.2              Flow Relationship

The flow relationship represents transfer from one element to another.

The flow relationship is used to model the flow of, for example, information, goods, or money between behavior elements. A flow relationship does not imply a causal relationship.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image056.png)

Figure 31: Flow Notation

Example

Example 13 shows a “Claim Assessment” business function, which forwards decisions about the claims to the “Claim Settlement” business function. In order to determine the order in which the claims should be assessed, “Claim Assessment” makes use of schedule information received from the “Scheduling” business function.

 ![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image057.png)

Example 13: Flow

### 5.3.3              Semantics of Dynamic Relationships

The semantics of triggering and flow relationships differ. The triggering relationship follows the same semantics as structural relationships (Section 5.1.5). A triggering relationship from A to B indicates that everything in B is preceded by a part of A. When A and B are business processes, for example, it means that all steps in business process B are performed after a part of A has occurred, but steps in A can occur after some or all steps in B have occurred. A stronger interpretation of triggering (everything in B is preceded by everything in A) could be imposed on the ArchiMate model by a modeling group wishing to do so.

The flow relationships follow the same semantics as dependency relationships (see Section 5.2.5). A flow relationship from A to B indicates that the whole or some part of A transfers something (e.g., information) to the whole or some part of B.

## 5.4                 Other Relationships

### 5.4.1              Specialization Relationship

The specialization relationship represents that an element is a particular kind of another element.

The specialization relationship has been inspired by the generalization relationship in UML class diagrams but is applicable to specialize a wider range of concepts.

A specialization relationship is always allowed between two instances of the same element type.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image058.jpg)

Figure 32: Specialization Notation

Alternatively, a specialization relationship can be expressed by nesting the specialized element inside the generic element.

Example

Example 14 illustrates the use of the specialization relationship for a process. In this case, the “Take Out Travel Insurance” and “Take Out Luggage Insurance” business processes are a specialization of a more generic “Take Out Insurance” business process.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image059.png)

Example 14: Specialization

### 5.4.2              Semantics of Other Relationships

The semantics of the specialization relationship are that the whole of the generic element is specialized by the specialized element.

## 5.5                 Relationship Connectors

### 5.5.1              Junction

A junction is not an actual relationship in the same sense as the other relationships described in this chapter, but rather a relationship connector.

A junction is used to connect relationships of the same type.

A junction is used in a number of situations to connect relationships of the same type. A path with junctions that connect relationships of this type is only allowed between two concepts, if a direct relationship of that type between these concepts is also permitted. Simply put, you cannot use junctions to create relationships between concepts that would otherwise not be allowed.

A junction may have multiple incoming relationships and one outgoing relationship, one incoming relationship and multiple outgoing relationships, or multiple incoming and outgoing relationships (the latter can be considered a shorthand of two contiguous junctions).

The relationships that can be used in combination with a junction are all the dynamic and dependency relationships, as well as assignment and realization. A junction is used to explicitly express that all elements together must participate in the relationship (_and_ junction) or that at least one of the elements participates in the relationship (_or_ junction). The _or_ junction can be used to express both inclusive and exclusive or conditions, which could be indicated by a modeler by naming the junction to reflect its type. It is allowed to omit arrowheads of relationships leading into a junction.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image060.png)

Figure 33: Junction Notation

Junctions used on triggering relationships are similar to gateways in BPMN and forks and joins in UML activity diagrams (without the associated semantics). They can be used to model high-level process flow. A label may be added to outgoing triggering relationships of a junction to indicate a choice, condition, or guard that applies to that relationship. Such a label is only an informal indication. No formal, operational semantics have been defined for these relationships, because implementation-level languages such as BPMN and UML differ in their execution semantics and the ArchiMate language does not want to unduly constrain mappings to such languages.

Examples

In Example 15, the _and_ junction in the model is used to denote that the “Sales” and “Finance” business functions together realize the “Invoicing” business service.

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image061.png)

Example 15: (And) Junction

In Example 16, the _or_ junction is used to denote a choice: business process “Assess Request” triggers either “Accept Request” or “Reject Request”. (The usual interpretation of two separate triggering relations, one from “Assess Request” to “Accept Request” and one from “Assess Request” to “Reject Request”, is that “Assess Request” triggers both of the other business processes.)

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image062.png)

Example 16: Or Junction

## 5.6                 Summary of Relationships

Table 3 gives an overview of the ArchiMate relationships with their definitions.

Table 3: Relationships

<table><tbody><tr><td colspan="2"><p><a name="_Hlk525906669"><span lang="EN-US">Structural Relationships</span></a></p></td><td><p><span lang="EN-US">Notation</span></p></td><td><p><span lang="EN-US">Role Names</span></p></td></tr><tr><td><p><span lang="EN-US">Composition</span></p></td><td><p><span lang="EN-US">Represents that an element consists of one or more other concepts.</span></p></td><td><p><img width="66" height="25" id="Picture 58" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image063.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> composed of<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> composed in</span></p></td></tr><tr><td><p><span lang="EN-US">Aggregation</span></p></td><td><p><span lang="EN-US">Represents that an element combines one or more other concepts.</span></p></td><td><p><img width="67" height="18" id="Picture 59" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image064.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> aggregates<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> aggregated in</span></p></td></tr><tr><td><p><span lang="EN-US">Assignment</span></p></td><td><p><span lang="EN-US">Represents the allocation of responsibility, performance of behavior, storage, or execution.</span></p></td><td><p><img width="64" height="8" id="Picture 60" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image065.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> assigned to<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> has assigned</span></p></td></tr><tr><td><p><span lang="EN-US">Realization</span></p></td><td><p><span lang="EN-US">Represents that an entity plays a critical role in the creation, achievement, sustenance, or operation of a more abstract entity.</span></p></td><td><p><img width="54" height="16" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image066.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> realizes<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> realized by</span></p></td></tr><tr><td colspan="2"><p><span lang="EN-US">Dependency Relationships</span></p></td><td><p><span lang="EN-US">Notation</span></p></td><td><p><span lang="EN-US">Role Names</span></p></td></tr><tr><td><p><span lang="EN-US">Serving</span></p></td><td><p><span lang="EN-US">Represents that an element provides its functionality to another element.</span></p></td><td><p><img width="76" height="31" id="Picture 62" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image067.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> serves<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> served by</span></p></td></tr><tr><td><p><span lang="EN-US">Access</span></p></td><td><p><span lang="EN-US">Represents the ability of behavior and active structure elements to observe or act upon passive structure elements.</span></p></td><td><p><img width="61" height="43" id="Picture 311" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image068.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> accesses<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> accessed by</span></p></td></tr><tr><td><p><span lang="EN-US">Influence</span></p></td><td><p><span lang="EN-US">Represents that an element affects the implementation or achievement of some motivation element.</span></p></td><td><p><img width="61" height="24" id="Picture 64" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image049.png" alt="fig26"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> influences<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> influenced by</span></p></td></tr><tr><td><p><span lang="EN-US">Association</span></p></td><td><p><span lang="EN-US">Represents an unspecified relationship, or one that is not represented by another ArchiMate relationship.</span></p></td><td><p><img width="61" height="31" id="Picture 271" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image069.png"></p></td><td><p><span lang="EN-US">associated with<br></span><span><span lang="EN-US">←</span></span><span lang="EN-US"> associated to<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> associated from</span></p></td></tr><tr><td colspan="2"><p><span lang="EN-US">Dynamic Relationships</span></p></td><td><p><span lang="EN-US">Notation</span></p></td><td><p><span lang="EN-US">Role Names</span></p></td></tr><tr><td><p><span lang="EN-US">Triggering</span></p></td><td><p><span lang="EN-US">Represents a temporal or causal relationship between elements.</span></p></td><td><p><img width="53" height="8" id="Picture 303" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image070.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> triggers<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> triggered by</span></p></td></tr><tr><td><p><span lang="EN-US">Flow</span></p></td><td><p><span lang="EN-US">Represents transfer from one element to another.</span></p></td><td><p><img width="53" height="8" id="Picture 307" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image071.png"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> flows to<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> flows from</span></p></td></tr><tr><td colspan="2"><p><span lang="EN-US">Other Relationships</span></p></td><td><p><span lang="EN-US">Notation</span></p></td><td><p><span lang="EN-US">Role Names</span></p></td></tr><tr><td><p><span lang="EN-US">Specialization</span></p></td><td><p><span lang="EN-US">Represents that an element is a particular kind of another element.</span></p></td><td><p><img width="55" height="15" id="Picture 67" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image072.jpg"></p></td><td><p><span><span lang="EN-US">←</span></span><span lang="EN-US"> specializes<br></span><span><span lang="EN-US">→</span></span><span lang="EN-US"> specialized by</span></p></td></tr><tr><td colspan="2"><p><span lang="EN-US">Relationship Connectors</span></p></td><td><p><span lang="EN-US">Notation</span></p></td><td><p><span lang="EN-US">Role Names</span></p></td></tr><tr><td><p><span lang="EN-US">Junction</span></p></td><td><p><span lang="EN-US">Used to connect relationships of the same type.</span></p></td><td><p><img width="64" height="58" id="Picture 230" src="https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image073.png"></p></td><td></td></tr></tbody></table>

## 5.7                 Derivation of Relationships

In the ArchiMate language, you can derive indirect relationships between elements in a model, based on the modeled relationships. This makes it possible to abstract from intermediary elements that are not relevant to show in a certain model or view of the architecture and supports impact analysis. The precise rules for making such derivations are specified in Appendix B.

Example

In Example 17, assume that the goal is to abstract from the application functions, sub-functions, and services in the model. In this case, an indirect serving relationship (thick red arrow on the right) can be derived from “Financial Application” to the “Invoicing and Collections” business process (from the chain assignment – composition – realization – serving).

![](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image074.png)

Example 17: Derivation from a Chain of Relationships

Derivation of relationships is intended as a way to create summaries of detailed models. It is a way to remove (to abstract from) details in a model, while still making valid “statements”. Hence, derivation is always meant to go from more detail to less detail. This mechanism is one of the unique properties of the ArchiMate language compared to other modeling languages.

The language allows the modeler directly to create relationships that are necessarily valid derived relationships without the constituents of the derivation being available in the model These relationships (for example, a realization relationship between an application component and an application service) assume that the required constituents (for example, an application function) needed for the derived relationship exist; however, these missing elements need not be modeled explicitly, and the derived relationships can be used as if they have not been derived. Thus, the modeler has full freedom in choosing the required level of detail.

Because the essence of derivation is to make simplifications or summaries, it cannot be used to infer more detail. For example, a realization relationship from an application component to an application service can be modeled, but from it no conclusions can be drawn about the exact source of this derivation (e.g., which functions realize which services).

This is information that should be added by a modeler during the design process: a higher-level, more abstract model can be refined by elaborating the derived relationships (in the previous example by adding an application function that realizes the application service and to which the application component is assigned).

It is important to note that all these derived relationships are also valid in the ArchiMate language. They are not shown in the metamodel diagrams included in the standard because this would reduce their legibility. However, the tables in Appendix B show all permitted relationships between two elements in the language.

[return to top of page](https://pubs.opengroup.org/architecture/archimate3-doc/chap05.html#top)

___

Downloads

Downloads of the ArchiMate documentation are available under license from the Download link within the [ArchiMate information web site](http://www.opengroup.org/archimate-forum). The license is free to any organization wishing to use ArchiMate documentation entirely for internal purposes. A book is also available from The Open Group Library as document [C197](http://www.opengroup.org/library/c197).

___

Copyright © 2012-2019 The Open Group, All Rights Reserved  
ArchiMate is a registered trademark of The Open Group.

___