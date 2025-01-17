#EA #TOGAF #Technology 

# Application Platform - Taxonomy

This section describes the Application Platform taxonomy, including basic principles and a summary of services and qualities.

## Basic Principles

The [[TOGAF]] [[TRM]] has two main components:

1.  A **taxonomy**, which defines terminology, and provides a coherent description of the components and conceptual structure of an information system
2.  An associated **TRM graphic**, which provides a visual representation of the taxonomy, as an aid to understanding![[Pasted image 20210713114610.png]]

This section describes in detail the taxonomy of the TOGAF TRM. The aim is to provide a core taxonomy that provides a useful, consistent, structured definition of the Application Platform entity and is widely acceptable.

No claims are made that the chosen categorization is the only one possible, or that it represents the optimal choice.

Indeed, it is important to emphasize that the use of TOGAF, and in particular the TOGAF ADM, is in no way dependent on use of the TOGAF TRM taxonomy. Other taxonomies are perfectly possible, and may be preferable for some organizations.

For example, a different taxonomy may be embodied in the legacy of previous architectural work by an organization, and the organization may prefer to perpetuate use of that taxonomy. Alternatively, an organization may decide that it can derive a more suitable, organization-specific taxonomy by extending or adapting the TOGAF TRM taxonomy.

In the same way, an organization may prefer to depict the TOGAF taxonomy (or its own taxonomy) using a different form of TRM graphic, which better captures legacy concepts and proves easier for internal communication purposes.

However, a consideration to bear in mind in deciding which taxonomy to use, is that the taxonomy of the TOGAF TRM is used in structuring the TOGAF [[SIB]], the database of all industry standards endorsed by [[The Open Group]] which is available for populating an architecture. Any differences from the TOGAF TRM taxonomy would need to be catered for when using the TOGAF SIB. (This typically represents an additional overhead, but not a major obstacle.)

## Application Platform Service Categories

The major categories of services defined for the Application Platform are listed below.

Note that "Object Services" does not appear as a category in the TRM taxonomy. This is because all the individual object services are incorporated into the relevant main service categories. However, the various descriptions are also collected into a single subsection ([Object-Oriented Provision of Services](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap19.html#tag_20_04_02_01)) in order to provide a single point of reference which shows how object services relate to the main service categories.

-   Data Interchange Services ([_Data Interchange Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_01)):
    -   Document generic data typing and conversion services
    -   Graphics data interchange services
    -   Specialized data interchange services
    -   Electronic data interchange services
    -   Fax services
    -   Raw graphics interface functions
    -   Text processing functions
    -   Document processing functions
    -   Publishing functions
    -   Video processing functions
    -   Audio processing functions
    -   Multimedia processing functions
    -   Media synchronization functions
    -   Information presentation and distribution functions
    -   Hypertext functions
-   Data Management Services ([_Data Management Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_02)):
    -   Data dictionary/repository services
    -   Database Management System (DBMS) services
    -   Object-Oriented Database Management System (OODBMS) services
    -   File management services
    -   Query processing functions
    -   Screen generation functions
    -   Report generation functions
    -   Networking/concurrent access functions
    -   Warehousing functions
-   Graphics and Imaging Services ([_Graphics and Imaging Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_03)):
    -   Graphical object management services
    -   Drawing services
    -   Imaging functions
-   International Operation Services ([_International Operation Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_04)):
    -   Character sets and data representation services
    -   Cultural convention services
    -   Local language support services
-   Location and Directory Services ([_Location and Directory Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_05)):
    -   Directory services
    -   Special-purpose naming services
    -   Service location services
    -   Registration services
    -   Filtering services
    -   Accounting services
-   Network Services ([_Network Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_06)):
    -   Data communications services
    -   Electronic mail services
    -   Distributed data services
    -   Distributed file services
    -   Distributed name services
    -   Distributed time services
    -   Remote process (access) services
    -   Remote print spooling and output distribution services
    -   Enhanced telephony functions
    -   Shared screen functions
    -   Video conferencing functions
    -   Broadcast functions
    -   Mailing list functions
-   Operating System Services ([_Operating System Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_07)):
    -   Kernel operations services
    -   Command interpreter and utility services
    -   Batch processing services
    -   File and directory synchronization services
-   Software Engineering Services ([_Software Engineering Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_08)):
    -   Programming language services
    -   Object code linking services
    -   Computer-aided software engineering (CASE) environment and tools services
    -   Graphical user interface (GUI) building services
    -   Scripting language services
    -   Language binding services
    -   Run-time environment services
    -   Application binary interface services
-   Transaction Processing Services ([_Transaction Processing Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_09)):
    -   Transaction manager services
-   User Interface Services ([_User Interface Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_10)):
    -   Graphical client/server services
    -   Display objects services
    -   Window management services
    -   Dialogue support services
    -   Printing services
    -   Computer-based training and online help services
    -   Character-based services
-   Security Services ([_Security Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_11)):
    -   Identification and authentication services
    -   System entry control services
    -   Audit services
    -   Access control services
    -   Non-repudiation services
    -   Security management services
    -   Trusted recovery services
    -   Encryption services
    -   Trusted communication services
-   System and Network Management Services ([_System and Network Management Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_12)):
    -   User management services
    -   Configuration management (CM) services
    -   Performance management services
    -   Availability and fault management services
    -   Accounting management services
    -   Security management services
    -   Print management services
    -   Network management services
    -   Backup and restore services
    -   Online disk management services
    -   License management services
    -   Capacity management services
    -   Software installation services
    -   Trouble ticketing services

## Object-Oriented Provision of Services

A detailed description of each of these service categories is given in [_Object-Oriented Provision of Services_](https://pubs.opengroup.org/architecture/togaf8-doc/arch/chap20.html#tag_21_13) .

-   Object Request Broker (ORB) Services:
    -   Implementation repository services
    -   Installation and activation services
    -   Interface repository services
    -   Replication services
-   Common Object Services:
    -   Change management services
    -   Collections services
    -   Concurrency control services
    -   Data interchange services
    -   Event management services
    -   Externalization services
    -   Licensing services
    -   Lifecycle services
    -   Naming services
    -   Persistent object services
    -   Properties services
    -   Query services
    -   Relationship services
    -   Security services
    -   Start-up services
    -   Time services
    -   Trading services
    -   Transaction services

## Application Platform Service Qualities

### Principles

Besides the platform service categories delineated by functional category, service qualities affect Information Systems Architectures. A service quality describes a behavior such as adaptability or manageability. Service qualities have a pervasive effect on the operation of most or all of the functional service categories.

In general a requirement for a given level of a particular service quality requires one or more functional service categories to co-operate in achieving the objective. Usually this means that the software building blocks that implement the functional services contain software which contributes to the implementation of the quality.

For the quality to be provided properly, all relevant functional services must have been designed to support it. Service qualities may also require support from software in the Application Software entity and the External Environment as well as the Application Platform.

In some cases, a service quality affects each of the service categories in a similar fashion, while in other cases, the service quality has a unique influence on one particular service category. For instance, international operation depends on most of the service categories in the same way, both providing facilities and needing their co-operation for localization of messages, fonts, and other features of a locale, but it may have a more profound effect on the software engineering services, where facilities for producing internationalized software may be required.

During the process of architecture development, the architect must be aware of the existence of qualities and the extent of their influence on the choice of software building blocks used in implementing the architecture. The best way of making sure that qualities are not forgotten is to create a quality matrix, describing the relationships between each functional service and the qualities that influence it.

### [[Taxonomy of Service Qualities]]

- RFP Tech Questions / Observations
	- Make clear the distinction between cloud and on-prem
		- If cloud then we don't care about minutia re server size, frameworks, programming languages, databases, etc.
		- We *do* care about interfaces with existing on-prem and hosted services
		- We **do** care about authentication options (SSO) and authorization options (RBAC)
		- We **do** care about service levels, multiple environments, update cycles (opt-in, forced, etc.)
			- And related, if cloud then are we in a multi-tenant situation, dedicated instance, etc.)
		- Data repatriation (if cloud)
		- Security aspects (SSL, encryption, etc.)