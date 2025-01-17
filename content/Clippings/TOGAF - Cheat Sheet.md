---
title: TOGAF certification - Cheat Sheet
source: https://readwise.io/reader/shared/01jdqak25rw0ps33xsv6j32f6n/
author:
  - "[[Kedar Patil]]"
published: 2024-04-30
created: 2024-11-27
description: This concise guide encompasses all the essential topics you’ll need to master to pass this exam. I crafted this cheat sheet during my own…
tags:
  - TOGAF
  - Methods
  - EA
---
This concise guide encompasses all the essential topics you’ll need to master to pass this exam. I crafted this cheat sheet during my own certification preparation, and I believe it will be just what you need to succeed in your certification journey. Follow it diligently, and you’re on your way to success!

## Definitions

**Architecture** is structure of components, their inter-relationships and principles & guidelines governing their design and evolution over time is architecture

An **Enterprise** is Any group of Organization’s working towards a shared goal. It could be a business OR multiple businesses working together

**Enterprise Architecture** is a structured approach to organize and manage information technology assets and processes in alignment with overall Business Strategy

**Architecture Principles** are general rules and guidelines, intended to be enduring and seldom amended, that inform and support the way in which an organization sets about fulfilling its mission

**Architecture Requirements Specification** is a set of quantitative statements that outline what an implementation project must do in order to comply with the architecture.

**Request For Architecture Work** is a document that is sent from the sponsoring organization to the architecture organization to trigger the start of an architecture development cycle

**Statement of Architecture Work** is the scope and approach that will be used to complete an architecture development cycle

**Architecture Contract** is a joint agreement between development partner and sponsors on deliverable quality of an architecture

Individual with an interest in System is **Stakeholder**

**Architecture Repository** is structured way to store all important document, artifacts and information related to organization’s architecture

**Content Framework** is framework to be used to structure architecture description, which is also the document showing architecture and different models explaining architecture

**Architecture Capability** is ability to develop , use and sustain architecture of particular enterprise and use architecture to govern changes

**Risk Analysis** is effect of un-certainty on objectives. The effect of un-certainty is any deviation from what is expected

**GAP Analysis** is a technique to highlight shortfall between Baseline and Target Architectures

**ADM** (Architecture Development Method) is tested and repeatable process fir developing architectures. It’s a method for deriving organization specific enterprise architecture and is specially designed to address business requirements

Documents which are under development and have not yet undergone formal review and approval process is **Draft**

**Architecture View** is representation of system from perspective of related set of concerns

**Architecture Viewpoint** is specification of convention for constructing and using architecture Views

**ADM** (*Architecture Development Cycle*)

![](https://miro.medium.com/v2/resize:fit:361/1*_PSevdaBCjoJj4HqoWhiPg.gif)

Architecture Development Method cycle

## Purpose of ADM

*Preliminary Phase* :  
Initial steps and preparations needed to establish an Architecture Capability. It includes the customization of the TOGAF framework to suit specific organizational needs and the creation of Architecture Principles.

*Phase A: Architecture Vision*  
Early stage of an architecture development cycle, detailing the definition of scope, identification of stakeholders, creation of the Architecture Vision, and securing approval to advance with the architecture development.

*Phase B: Business Architecture  
Phase C: Information Systems Architectures(Data and Application)  
Phase D: Technology Architecture*  
Describes the development of four architectures, that are commonly accepted as subsets of an overall Enterprise Architecture, to support the agreed Architecture Vision:  
— Business  
— Information Systems — Data  
— Information Systems — Application  
— Technology

*Phase E: Opportunities and Solutions*  
Involves initial planning for implementation and identifying delivery mechanisms for the architecture defined in earlier phases.

*Phase F: Migration Planning*  
Focuses on transitioning from the Baseline to the Target Architectures by completing a detailed Implementation and Migration Plan.

*Phase G: Implementation Governance*  
Provides architectural oversight for the implementation.

*Phase H: Architecture Change Management*  
Establishes procedures for managing change to the new architecture.

*Requirements Management*  
Operates the process of managing architecture requirements throughout the ADM.  
This is a continuous phase which ensures that any changes to requirements are handled through appropriate governance processes and reflected in all other phases.

## ADM Phase-wise Objectives

*Preliminary Phase*  
• Determine the Architecture Capability desired by the organization.  
• Establish the Architecture Capability.

*Phase A: Architecture Vision*  
• Develop a high-level aspirational vision of the capabilities and business value to be delivered as a result of the proposed Enterprise Architecture  
• Obtain approval for a Statement of Architecture Work that defines a program of works to develop and deploy the architecture outlined in the Architecture Vision

*Phase B: Business Architecture*  
• Develop the Target Business Architecture that describes how the enterprise needs to operate to achieve the business goals, and respond to the strategic drivers set out in the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns  
• Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Business Architectures

*Phase C: Data Architecture*  
• Develop the Target Data Architecture that enables the Business Architecture and the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns  
• Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Data Architectures

*Phase C: Application Architecture*  
• Develop the Target Application Architecture that enables theBusiness Architecture and the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns  
• Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Application Architectures

*Phase D: Technology Architecture*  
• Develop the Target Technology Architecture that enables the Architecture Vision, target business, data, and application building blocks to be delivered through technology components and technology services, in a way that addresses the Statement of Architecture Work and stakeholder concerns  
• Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Technology Architectures

*Phase E: Opportunities & Solutions*  
• Generate the initial complete version of the Architecture Roadmap, based upon the gap analysis and candidate Architecture Roadmap components from Phases B, C and D  
• Determine whether an incremental approach is required, and if so identify Transition Architectures that will deliver continuous business value  
• Define the overall Solution Building Blocks (SBBs) to finalize the Target Architecture based on the ABBs

*Phase F: Migration Planning*  
• Finalize the Architecture Roadmap and the supporting Implementation and Migration Plan  
• Ensure that the Implementation and Migration Plan is coordinated with the enterprise’s approach to managing and implementing change in the enterprise’s overall change portfolio  
• Ensure that the business value and cost of work packages and Transition Architectures is understood by key stakeholders

*Phase G: Implementation Governance*  
• Ensure conformance with the Target Architecture by Implementation Projects  
• Perform appropriate Architecture Governance functions for the solution and any implementation-driven architecture Change Requests

*Phase H: Architecture Change Management*  
• Ensure that the architecture development cycle is maintained  
• Ensure that the Architecture Governance framework is executed  
• Ensure that the Enterprise Architecture Capability meets current requirements

> **It’s crucial to keep in mind**

- Ensuring compliance with internal, external standards and regulatory obligations is part of Architecture Governance.
- Architecture partitioning is technique of dividing an architecture into smaller and more manageable parts that can be developed, maintained and governed independently.  
Partitions are used to simplify management of Enterprise Architecture and to enable different teams work on different elements at the same time.
- Enterprise Architecture Capability is ability to develop and sustain architecture of particular enterprise using architecture to govern change
- Purpose of Enterprise Architecture is to guide effective change.
- Enterprise Continuum provides method for classifying architecture artifacts as they evolve from Generic to Organization specific architectures
- Architecture Landscape is divided into levels knows as Segment, Strategic and Capability architectures
- Purpose of Architecture Principles is to establish a common understanding of how to control business in pursuit of Strategic objectives.
- Architecture Principles that cover every situation perceived meets the recommended criteria of Completeness
- Content Metamodel is a formal structure that defines the types of entities and relationships that are used to store, filter architectural information in a way that supports consistency & completeness
- Purpose of Architecture Roadmap is to list packages on a timeline showing progress towards Target Architecture
- Business Scenarios describes Business & Technology environment in which problem occurs
- In phase E building block gaps become associated with work packages that will address gaps
- Business Principles, Business Goals and Business Drivers provides context for Architecture work by describing the needs and ways of working
- Architecture Contract is a deliverable that specifies the responsibilities and obligations of parties involved in the implementation and governance of an architecture.
- Best practice governance enables organization to control value realization.
- Rationale section of Architecture Principles should describe relationship to other principles.
- Responsibility of Architecture boards is to establish targets for re-use of components.
- Purpose of GAP analysis is to identify missing/ overlapping functions
- Purpose of GAP analysis is to identify items omitted from target architecture
- Enterprise Architecture involves establishing organizational structures, roles, responsibilities, skills, processes, tools and governance mechanisms to support development and use of enterprise architecture
- Actions arising from Business Transformation Readiness Assessment technique should be incorporated in Implementation & Migration plan
- Implementation & Migration plan is detailed plan to perform transition from Baseline to Target architecture
- ADM is iterative, over the whole process between phases and within phases
- Reference Library contains Guidelines & Templates used to create new architectures
- Architecture Landscape within Architecture Repository shows an Architectural view of building blocks that are in use within an organization & those are planned for future usage
- In Phase E of ADM building blocks become implementation specific
- Purpose of Business Scenarios is to identify & understand requirements
- Phase A focuses on defining problems to solved, identifying Stakeholders, their concerns and requirements
- Architecture Vision is high level description of desired outcomes & benefits of proposed architecture
- Objective of Preliminary phase is to select and implement!  
tools to support Architecture capability.
- Architect can present Architecture views & viewpoints to extract  
hidden agendas, principles and requirements to stakeholders
- Purpose at enterprise architecture is to guide effective change.
- Partitions an used to simplify the management at Enterprise Architecture
- Architecture Requirements Repository represents architecture requirements agreed with the Architecture Board
- Building block is described as a package of functionality defined to meet business needs across an organization.
- ADM recommends using Business Scenarios in developing Architecture Vision document
- Architecture Requirements Specification provides a set at statements that outlines what a project must do to comply win the architecture
- Architecture Contract- ensures adherence to the principles, standards & requirements of existing / developing architectures
- Planning horizon, depth & breadth at an architecture project along with contents a EA Repository are framed by all Strategy, Portfolio, Segment & End to End Architecture
- Segment refers to part at the organization addressed as Segment architecture
- End to end architecture encompasses the complete view at the planned architecture across entire org.
- Rationale section of architecture principle highlights business benefits at adhering to the principles & risks of not adhering to it
- Transformation readiness assessment can be performed in phase E (Opportunities & solutions) & actions resulting can be dealt in phase F (Migration planning)
- Achieving consistency between sub-architectures is responsibility & Architecture board.
- TOGAF standard aligns with agile development in Phase G, when a product is implemented.
- Four purposes that frame planning horizon, depth & breadth at an architecture project are Strategy, Portfolio, Project, Solution Delivery
- Ability to develop, use & sustain architectural particular enterprise casing architecture to govern change is an EA capability
- Architecture Principles are general rules and guidelines that relate to architecture work.  
*Architecture Principles* enable decision making  
*Architecture Principles* align the Enterprise — principles take subjectivity and bias out a equation and drive critical conversations  
*Architecture Principles* ensure Governance  
*Architecture Principles* provides better understanding al organizations culture values
- The initial assessment at Business Transformation Readiness in ADM is typically performed in phase A.
- Architecture abstraction is a technique for dividing problem into a smaller problem areas that are easier to model & solve.  
*Why* — why is this architecture needed  
*What* — What functionality & requirements need to be met by architecture  
*How* — How do we structure functionality  
*With What* — with what assets shall we implement this architecture
- Architecture abstraction levels are  
**Contextual**\- understanding the environment in which enterprise operates and context in which architecture work is planned & executed.  
**Conceptual** — Decomposing requirements to understand the problem, without focusing on how architecture will be realized.  
**Logical** — Identifying the kinds of Business, Data, Application and Technology components needed to achieve services identified in conceptual level.  
**Physical** — The allocation and implementation at physical components to meet the identified logical components.
- During phase D (Technology Architecture), Technical Reference Model (TRM) is considered in the development
- Work product that describes an aspect of the Architecture is Artifact
- Requirements Impact Assessment deliverable identifies, changes that should be made to the architecture and consider their implications.
- Every View has an associated as viccupbint that describes its
- Deliverable is contractually specified and formally reviewed, agreed architecture that address detailed needs & Business requirements are known as specific architectures
- During Phase F (Migration Planning), activity to in assess the dependencies, costs and benefits al migration project is considered
- Request for Architecture work document triggers start of ADM
- Initial implementation planning at Target Architecture is done during Phase E- Opportunities & Solutions
- Quality criteria of Architecture Principles are — Complete, consistent, robust, stable & understandable
- Governance repository includes parameters, structures and processes that supports overall governance
- During Phase G (Implementation Governance) an architecture contract is signed between the architecture and implementation org.
- Capability architecture level of Architecture Landscape describes abilities of an enterprise
- Business scenarios technique is recommended to define business needs and requirements in order to articulate architecture vision in Phase A
- Architecture governance manages and controls Enterprise Architecture at an enterprise-wide level
- In Phase E building blocks are associated with work packages that will address the gaps
- Architecture contracts are Joint agreement between development partners and sponsors on the deliverables, quality and fitness  
for purpose at an architecture.
- Architecture Definition document is the deliverable container for core architectural artifacts created during a project
- Architecture Definition Document spans all architecture domains (Business, Data, Application Technology) and also examines all relevant states of an architecture (Baseline, Transition & Target)
- Architecture Definition Document is first created in phase A where it is populated with artifacts created to support Architecture vision. Subsequently it is updated in phase B, C & D
- Architecture Definition Document is first created in Architecture Requirements Specification provides a set of quantitate statements that outlines what an implementation project must do in order to comply with architecture
- Architecture Definition Document is first created in Architecture Roadmap lists individual work packages that will realize Target architecture and lays them out on a timeline to show from Baseline to Target architecture
- Architecture Definition Document is first created in Architecture roadmap is incrementally developed throughout Phase E and Phase F and informed by roadmap components developed in Phase B, C &D
- Architecture Definition Document is first created in Architecture Vision is created in Phase A and provides high level of summary of the changes to enterprise that will follow from successful deployment of Target architecture
- Business Principles, Goals & Drivers are restated as an output a Preliminary phase and reviewed again in Phase A
- Capability assessment is first carried out in phase A and later reviewed in phase E
- Request for Architecture change (Change Request) is considered in Phase H (Architecture change management
- Communications plan is drafted in phase A
- Compliance assessment is done periodically in Phase G
- Implementation and migration plan is developed in phase E and F
- Architecture landscape is divided into 3 levels  
1) *Segment architecture* — address specific business unit, functions or processes within an enterprise  
2) *Strategic architecture* — provides high level view at organization vision, goals and direction  
3) *Capability architecture* — address specific business capabilities or services that span multiple segments or domains
- During Phase F (Migration planning) detailed plan to guide implementation at Target architecture to executed.
- Phase C (Information systems architecture) objective is to establish blueprint for individual application systems to be deployed, & interaction between application Systems
- Phase H is responsible for ongoing change management and enhancement of the architecture to ensure it remains relevant against original business objectives
- Architecture Governance is practice of monitoring and directing architectural activities to ensure alignment with business objectives
- Phase E primarily concentrates on formulating Implementation and Migration strategies & transition from Baseline to Target architecture
- During Phase F, emphasis is on identifying major implementation projects & initiatives required to transition from Current/ Baseline to Target architecture
- Draft architecture definition document is created during phase A
- Artifact describes an aspect of the architecture
- Phase G primarily emphasizes overseeing the implementation of architecture projects to ensure they an executed in alignment with defined architecture
- Business Scenarios technique is executed in phase A
- Architecture Vision document is description of how new Capability will address Stakeholder concerns
- Phase H (in case of re-architecting change) A change is driven by requirement to increase investment in order to create new value for exploitation
- In Phase F implementation & migration plan coordinated
- Catalog is is an artifact showing list of things
- Standards information Base is a specifications to which architecture must conform
- Architecture pattern is a way to identify combination of building blocks that have been proven to deliver solutions
- Architecture is description of system, detailed plan a system at component lead to guide its implementation
- During phase B, C and D final step is to create Architecture Definition Document
- Business Transformation Readiness Assessment is conducted during Implementation & migration plan
- Preliminary phase defines an enterprise
- First step in B, C, D is to select reference model, view points
- Architecture Governance Framework — approach to ensure effectiveness of organization architecture
- Matrix shows relationship between things
- Architecture Viewpoint is reusable artifact that is used to create architecture motels addressing stakeholder concerns
- Architecture Capability Framework provides set of reference materials for establishing as architecture function in organization
- Capability based planning — planning technique that focuses on Business outcomes
- Architecture Content Framework, describes typical architecture work deliverables
- Phase A: Define scope for the architecture development initiative & obtain approval to proceed with architecture development
- Phase A: earliest building black definition start as abstract entities
- Phase F Implementation & Migration Planning is carried out in co-operation with portfolio & project managers
- Purpose of Architecture Compliance Review — identify where standards may require modifications
- Requirement Management phase is responsible for managing flow of requirements
- Architecture Definition document is description to communicate intent of an architecture
- Information Reference Model (III-RM) is an example of applications reference model (Phase C)
- Architecture Capability is a tool for selling benefits of proposed capability to Stakeholders
- Objective of Preliminary phase is to define framework and methodologies to be used.
- In Phase E GAP Analysis results from output of earlier stages consolidated
- Business Transformation Readiness Assessment is initially done in Phase ABBs
- Viewpoints are used as templates to create views
- Phase G sets up architectural contract between Architecture Organization & Implementation Organization
- Statement Of Architecture Work defines scope and approach to complete Architecture project.
- In the ADM documents which are under development and have not undergone any formal review and approval process are called Draft
- Presenting different Architecture Views and Architecture Viewpoints to stakeholders helps architects to extract hidden agendas principles and requirements that could impact the final Target Architecture
- Best practice governance enables the organization to control value realization
- Enterprise Architecture Capability is the ability to develop use and sustain the architecture of a particular enterprise using architecture to govern change
- Implications section of the TOGAF template for Architecture Principles should highlight the requirements for carrying out the principle
- Rationale section of the TOGAF template for Architecture Principles should highlight the business benefits of adhering to the principle

> Important Timelines

![](https://miro.medium.com/v2/resize:fit:700/1*ulWR8c245tWVe706GsdW-w.png)

*I just want to emphasize that this article is intended as a last-minute refresher or a pocket guide. It’s important to take the exam only after a comprehensive review of the official TOGAF documentation. Wish you all the best !!!*

*References*

TOGAF official documentation

ADM Cycle images : [https://pubs.opengroup.org/architecture/togaf8-doc/arch/Figures/adm.gif](https://pubs.opengroup.org/architecture/togaf8-doc/arch/Figures/adm.gif)