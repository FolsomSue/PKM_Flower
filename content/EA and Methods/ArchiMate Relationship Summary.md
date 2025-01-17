#Technology #EA #Methods #ArchiMate 
# ArchiMate Relationship Summary

## Relationship Classifications

• _Structural_ relationships, which model the static construction or composition of concepts of the same or different types

• _Dependency_ relationships, which model how elements are used to support other elements
	• The _serving_ relationship represents a _control_ dependency, denoted by a solid line
	• The _access_ relationship represents a _data_ dependency, denoted by a dotted line
	• The _influence_ relationship represents an _impact_ dependency, denoted by a dashed line
	• The _association_ relationship represents a dependency not covered by any of the other relationships
	
• _Dynamic_ relationships, which are used to model behavioral dependencies between elements

• _Other_ relationships, which do not fall into one of the above categories

## Relationship Direction(s)
### Structural -- Composition, Aggregation, Assignment
Structural relationships represent the “static” coherence within an architecture. The uniting (composing, aggregating, assigned, or realizing) concept (the “from” side of the relationship) is always an element; for assignment and realization it can be an element or a relationships connector. The united (being composed, aggregated, assigned to, or realized) concept (the “to” side of the relationship) may in some cases also be another relationship or relationship connector.
### Structural -- Realizations
The interpretation of a realization relationship is that the _whole or part_ of the source element realizes the _whole of_ the target element. 
### Dependency Relationships
Arrows that represent such supporting, influencing, serving, or realizing dependencies point “upwards” towards the client/user/business (unlike [[UML]]).
### Dynamic Relationships
Traditional flow or triggering direction.
### Other -- Specialization / Generalization
The specialization relationship represents that an element is a particular kind of another element. The arrow points from the "kind" to the element, i.e. The Specialized Element points up to the Generalized Element (same as [[UML]]).

## Table: Relationships

| **Structural Relationships**     | **Notation**                                                     | **Role Names**                                                   |                                                   |
| ---------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------- |
| Composition                  | Represents that an element consists of one or more other concepts. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image063.png) | ← composed of → composed in                       |
| Aggregation                  | Represents that an element combines one or more other concepts. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image064.png) | ← aggregates → aggregated in                      |
| Assignment                   | Represents the allocation of responsibility, performance of behavior, storage, or execution. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image065.png) | ← assigned to → has assigned                      |
| Realization                  | Represents that an entity plays a critical role in the creation, achievement, sustenance, or operation of a more abstract entity. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image066.png) | ← realizes → realized by                          |
| **Dependency Relationships** | **Notation**                                                 | **Role Names**                                               |                                                   |
| Serving                      | Represents that an element provides its functionality to another element. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image067.png) | ← serves → served by                              |
| Access                       | Represents the ability of behavior and active structure elements to observe or act upon passive structure elements. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image068.png) | ← accesses → accessed by                          |
| Influence                    | Represents that an element affects the implementation or achievement of some motivation element. | ![fig26](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image049.png) | ← influences → influenced by                      |
| Association                  | Represents an unspecified relationship, or one that is not represented by another ArchiMate relationship. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image069.png) | associated with ← associated to → associated from |
| **Dynamic Relationships**    | **Notation**                                                 | **Role Names**                                               |                                                   |
| Triggering                   | Represents a temporal or causal relationship between elements. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image070.png) | ← triggers → triggered by                         |
| Flow                         | Represents transfer from one element to another.             | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image071.png) | ← flows to → flows from                           |
| **Other Relationships**      | **Notation**                                                 | **Role Names**                                               |                                                   |
| Specialization               | Represents that an element is a particular kind of another element. | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image072.jpg) | ← specializes → specialized by                    |
| **Relationship Connectors**  | **Notation**                                                 | **Role Names**                                               |                                                   |
| Junction                     | Used to connect relationships of the same type.              | ![img](https://pubs.opengroup.org/architecture/archimate3-doc/ts_archimate_3.1-final_files/image073.png) |                                                   |