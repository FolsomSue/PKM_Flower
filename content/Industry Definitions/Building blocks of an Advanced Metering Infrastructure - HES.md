#Electric #Industry_Definitions #AMI

## **The Headend System**

A recent study of AMI professionals at leading DSOs revealed that regardless of the market set up or regulatory position, all utilities are currently investigating the business case for deploying modern smart meters to modernize the low voltage grid and integrate the last mile of the smart grid. Driving the rollout of next generation smart meters to improve customer service and support advanced analytics in the smart grid at minimal expenditure forms the backbone of Advanced Metering Infrastructure in today’s context. But what makes up this infrastructure? And which building blocks do utilities need to understand and consider?

As industry specialists in utility data integration and enterprise architecture, especially when it comes to Smart Metering, we advise and consult utilities globally and support application and system vendors implementing projects impacting millions of consumers. As a result of this experience, we see a variety of approaches to central architectural decisions that utilities are taking. In this article we explore key factors and provide our perspectives related to infrastructure cornerstones in the advanced smart metering value chain, namely the headend system. So what are the different types of headend systems on the market today and what constitutes a good and future-oriented integration architecture to support these systems?

## **The role of a Headend System**

The role of the headend system or systems (HES) in the Smart Metering architecture is typically two-fold. The main objective of HES is to acquire meter data automatically, avoiding any human intervention, and to monitor parameters acquired from meters. In this case HES is managing the connectivity and scheduling the collection of data from the metering infrastructure including both the meter devices and communication. However, HES also enables secure access to meters for configuration, software updates and ad-hoc requests.

![](https://content.greenbird.com/AMI-blog-post-HES1.png)

Figure 1: The traditional Smart Metering architecture

To avoid working in multiple operational systems, you would ideally want a HES that is able to expose most of its services through an application programming interface (API), meaning that most functions can be executed from a central system like Meter Data Management (MDM) or Customer Information System (CIS). As an example, an authorized operator should in theory be able to remotely disconnect a Smart Meter through the user interface of the HES. However, in most cases this disconnection use case would be initiated by the system that manages all customer information and interactions (CIS).

## **Traditional vs. universal HES**

Headend systems come in different shapes and formats. The most common form is one delivered by the meter manufacturer itself. Understandably, meter manufacturers offer a HES to operate their meter functionality as they would not be able to deliver smart meters without having an interface to operate their devices (i.e. HES).

Next to meter manufacturers providing their HES, a number of “universal” HES providers have entered the market over the last fifteen years. They originated from a market supporting Automated Meter Reading (AMR) for larger commercial and industrial customers (C&I customers) since the 90’s. AMR use cases were typically limited to reading out meter registers, hence, universal data collection solutions offered adapters or connectors to vendor-specific protocols of the various meters.

While this was common practice for C&I metering, a universal HES business case for Smart Metering, with its bi-directional communication and advanced functionality requirements, seems less clear. From a technical point of view, there are key challenges that need to be overcome:

-   Multiple communication technologies (radio, PLC, GSM) and patterns (mesh networks, concentrator-based networks or point-to-point communications) require different solutions and management capabilities from a HES. In addition to functional use cases, a HES is also expected to handle communication management and monitoring. Furthermore, performant and scalable data collection engines need to take into account the communication pattern in a given meter network:  
    A large proportion of point-to-point connections require strong multi-threaded collection capabilities with the ability to open, process and close many communication channels simultaneously. In opposition to that, concentrator-based solutions need to focus on the transfer and process of large amounts of data at speed.
-   Missing standardization: Even if some progress has been made during the last 15 years with respect to standardization of the meter protocols, there are still many different protocols and so-called standards. While that was one of the initial triggers for universal HES, it is also one of its biggest challenges:  
    keeping track of development changes in a multitude of meter protocol adapters (and making that commercially viable).
-   Meters now come with a great variation of functionalities. While requirements vary from country to country, most utilities tend to request a long list of functionalities, anticipating what may be needed during the lifetime of a smart meter which in most cases is longer than 10 years. Implementing these large number of functionalities for an equally large variety of different meter types within one solution posts challenges for universal headend solution suppliers.

There are also a number of key legal and commercial criteria that should be considered.

-   When investing in smart meters, you want them to work. The responsibility for that lies with the meter vendor. To prove and warrant a functioning infrastructure, the meter vendor will always need to utilize a HES, most likely the meter vendor will want to use their own HES for that purpose. In other words, if a customer wants to utilize a universal HES, the burden of proof for the functioning of the smart meters will most likely change, making it harder for the customer to prove non-compliance or performance of functionality within the delivery.
-   Most meter protocols consist of a public part and a private part, in general terms. While daily meter reads or even meter disconnection is relatively easy to implement for universal HES, more proprietary functions such as meter configuration, firmware management and functions supporting failure analytics are a challenge, and are in most cases close to impossible to implement, due to both complexity and IPR-related issues.

## **HES Southbound Integration**

From an architectural perspective, the universal headend looks promising at first. Instead of one integration between MDMS and each of the potentially many HES, only a single integration needs to be created and managed.

![](https://content.greenbird.com/AMI-blog-post-HES2.png)

Figure 2: Smart Metering architecture with universal HES

However, the complexity in the architecture described above is moved from the Northbound side of the HES, to the Southbound side, where a universal HES needs to manage multiple complex integrations with often non-standardized protocols and communication technologies. Furthermore, the HES itself is transformed from a straightforward protocol converter & configuration/collection engine for a single technology towards a complex monolithic application with potentially significant operational and maintenance cost.

## **HES Northbound integration**

On the Northbound integration side of the HES, the landscape has been changing in recent years. Integration between MDMS and HES was traditionally handled as point-to-point (p2p) integration between MDM and HES (See picture above). Many of the larger MDM suppliers developed “out-of-the-box” available connectors to specific HES from various vendors to support this need.

Similar to the issue of operation and maintenance costs that come with universal HES, the Northbound p2p integration also has the potential to inflict large operational and maintenance costs. The fact that the selected MDM vendor needs to accommodate all changes in its p2p integrations towards one or more HES can lead to the following issues:

-   Vendor lock / dependency on MDM vendor;
-   MDM vendors potentially lacking competence on enterprise integration;
-   Introducing tight coupling between systems where loose coupling would be logical and achievable; and
-   Non-compliance with regards to Smart Grid use cases that require additional flexibility

A manifestation of the problem caused by p2p integrations comes with new use cases in the Smart Grid area that require close-to-real-time data transfer from meters to solutions in the operational technology (OT) area. For example, “last gasp” messages that should be passed on to an ADMS solution as fast as possible to support fast power restoration, may need to be routed on a prioritized data flow and not go through the MDM first. This again causes the need for additional integrations towards the OT area that cannot be handled by the MDM vendor.

![](https://content.greenbird.com/AMI-blog-post-HES3.png)

Figure 3: Growing complexity with p2p integrations and new use cases

## **Changing paradigm on HES northbound**

During the last years, our customer projects, ongoing tenders and talks with partners supporting both HES and MDM solutions around the world have indicated that the market is currently undergoing a paradigm shift with regards to HES Northbound integration. This paradigm shift is mainly based on two developments:

1.  The growing acceptance of IEC 61698-9 (CIM) as de-facto standard and data model for all integration between HES and MDM solutions;
2.  Increased competence of customers around enterprise integration, introducing concepts of loose coupling and event-driven architecture (EDA), even in the smart metering value chain.

The growing acceptance and implementation of CIM empowers customers to be less dependent on the software suppliers’ services and makes it easier for third-party tools to take over the responsibility for MDM-HES integrations.

In addition, growing competence and experience in the area of enterprise integration makes customers realize that p2p integrations in general are not sustainable and that the concept of loose coupling and event-driven architecture is significantly cheaper and more effective in the long run.

Another important factor is based on many lessons learned from earlier AMI roll-outs where p2p integrations effectively prevented quick and reliable error analysis and resolution, based on the simple fact that no over-arching monitoring of all involved integration flows was available, leading to an endless “finger-pointing” game between involved vendors.  

## **How to make the right architectural choices regarding headend systems (HES)**

All these factors have led to us recommending utilities (and software vendors) implement a data integration layer, even on the HES Northbound side, between HES and MDM. Ideally, this integration layer supports CIM, loose coupling and event-driven architecture out-of-the-box. It should also support real-time streaming of data and be highly resilient.

When it comes to the role and integration of HES within the Smart Metering value chain, the following overall highly effective and resilient architecture is recommended for utilities:

![](https://content.greenbird.com/AMI-blog-post-HES4.png)

Figure 4: Resilient and effective HES architecture

In this article we were only focusing on HES and its integration into the Smart Meter value chain. We demonstrated that universal HES may not be as promising as they seem, and we explained why we think that Northbound HES integration should go via an adequate integration bus.

In our next article we will describe the role of the Meter Data Management System (MDM) and its integration into the Smart Meter value chain. We will also give an outlook on the future of MDM solutions as the core element of the Smart Meter value chain based on different likely scenarios.