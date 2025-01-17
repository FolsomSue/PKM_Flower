---
Aliases: [Outage Management System, OMS]
---
#Industry_Definitions #Technology 

An **outage management system** (OMS) is a computer system used by operators of [electric distribution systems](https://en.wikipedia.org/wiki/Electric_distribution_systems "Electric distribution systems") to assist in restoration of power.

## Major functions of an OMS\[[edit](https://en.wikipedia.org/w/index.php?title=Outage_management_system&action=edit&section=1 "Edit section: Major functions of an OMS")\]

Major functions usually found in an OMS include:

-   Prediction of location of transformer, fused, recloser or breaker that opened upon failure.
-   Prioritizing restoration efforts and managing resources based upon criteria such as locations of emergency facilities, size of outages, and duration of outages.
-   Providing information on extent of outages and number of customers impacted to management, media and regulators.
-   Calculation of estimation of restoration times.
-   Management of crews assisting in restoration.
-   Calculation of crews required for restoration.

## OMS principles and integration requirements\[[edit](https://en.wikipedia.org/w/index.php?title=Outage_management_system&action=edit&section=2 "Edit section: OMS principles and integration requirements")\]

At the core of a modern outage management system is a detailed network model of the distribution system. The utility's [geographic information system](https://en.wikipedia.org/wiki/Geographic_information_system "Geographic information system") (GIS) is usually the source of this network model. By combining the locations of outage calls from customers, a rules engine is used to predict the locations of outages. For instance, since the distribution system is primarily tree-like or radial in design, all calls in particular area downstream of a fuse could be inferred to be caused by a single fuse or circuit breaker upstream of the calls.

The outage calls are usually taken by call takers in a call center utilizing a customer information system (CIS). Another common way for outage calls to enter into the CIS (and thus the OMS) is by integration with an [interactive voice response](https://en.wikipedia.org/wiki/Interactive_voice_response "Interactive voice response") (IVR) system. The CIS is also the source for all the customer records which are linked to the network model. Customers are typically linked to the [transformer](https://en.wikipedia.org/wiki/Transformer "Transformer") serving their residence or business. It is important that every customer be linked to a device in the model so that accurate statistics are derived on each outage. Customers not linked to a device in the model are referred to as "fuzzies".

More advanced [automatic meter reading](https://en.wikipedia.org/wiki/Automatic_meter_reading "Automatic meter reading") (AMR) systems can provide outage detection and restoration capability and thus serve as virtual calls indicating customers who are without power. However, unique characteristics of AMR systems such as the additional system loading and the potential for false positives requires that additional rules and filter logic must be added to the OMS to support this integration.[\[1\]](https://en.wikipedia.org/wiki/Outage_management_system#cite_note-1)

Outage management systems are also commonly integrated with [SCADA](https://en.wikipedia.org/wiki/SCADA "SCADA") systems which can automatically report the operation of monitored circuit breakers and other intelligent devices such as SCADA reclosers.

Another system that is commonly integrated with an outage management system is a [mobile data system](https://en.wikipedia.org/w/index.php?title=Mobile_data_system&action=edit&redlink=1 "Mobile data system (page does not exist)"). This integration provides the ability for outage predictions to automatically be sent to crews in the field and for the crews to be able to update the OMS with information such as estimated restoration times without requiring radio communication with the control center. Crews also transmit details about what they did during outage restoration.

It is important that the outage management system electrical model be kept up to current so that it can accurately make outage predictions and also accurately keep track of which customers are out and which are restored. By using this model and by tracking which switches, breakers and fuses are open and which are closed, network tracing functions can be used to identify every customer who is out, when they were first out and when they were restored. Tracking this information is the key to accurately reporting outage statistics. [(P.-C. Chen, et al., 2014)](http://www.pochenchen.com/uploads/3/3/7/6/3376872/2014_cired_final.pdf)

## OMS benefits\[[edit](https://en.wikipedia.org/w/index.php?title=Outage_management_system&action=edit&section=3 "Edit section: OMS benefits")\]

OMS benefits include:

-   Reduced outage durations due to faster restoration based upon outage location predictions.
-   Reduced outage duration averages due to prioritizing
-   Improved customer satisfaction due to increase awareness of outage restoration progress and providing estimated restoration times.
-   Improved media relations by providing accurate outage and restoration information.
-   Fewer complaints to regulators due to ability to prioritize restoration of emergency facilities and other critical customers.
-   Reduced outage frequency due to use of outage statistics for making targeted reliability improvements.

## OMS based distribution reliability improvements\[[edit](https://en.wikipedia.org/w/index.php?title=Outage_management_system&action=edit&section=4 "Edit section: OMS based distribution reliability improvements")\]

An OMS supports distribution system planning activities related to improving reliability by providing important outage statistics. In this role, an OMS provides the data needed for the calculation of measurements of the system reliability. Reliability is commonly measured by performance indices defined by the IEEE P1366-2003 standard. The most frequently used performance indices are [SAIDI](https://en.wikipedia.org/wiki/SAIDI "SAIDI"), [CAIDI](https://en.wikipedia.org/wiki/CAIDI "CAIDI"), [SAIFI](https://en.wikipedia.org/wiki/SAIFI "SAIFI") and [MAIFI](https://en.wikipedia.org/wiki/MAIFI "MAIFI").

An OMS also support the improvement of distribution reliability by providing historical data that can be mined to find common causes, failures and damages. By understanding the most common modes of failure, improvement programs can be prioritized with those that provide the largest improvement on reliability for the lowest cost.

While deploying an OMS improves the accuracy of the measured reliability indices, it often results an apparent degradation of reliability due to improvements over manual methods that almost always underestimate the frequency of outages, the size of outage and the duration of outages. To compare reliability in years before an OMS deployment to the years after requires adjustments to be made to the pre-deployment years measurements to be meaningful.

## References\[[edit](https://en.wikipedia.org/w/index.php?title=Outage_management_system&action=edit&section=5 "Edit section: References")\]

1.  **[^](https://en.wikipedia.org/wiki/Outage_management_system#cite_ref-1 "Jump up")** ([Sridharan & Shulz 2001](https://en.wikipedia.org/wiki/Outage_management_system#CITEREFSridharanShulz2001))

-   Sastry, M.K.S. (2007), "[Integrated Outage Management System: an effective solution for power utilities to address customer grievances](http://www.inderscience.com/search/index.php?action=record&rec_id=14424&prevQuery=&ps=10&m=or)", _International Journal of Electronic Customer Relationship Management_, vol. **1**, no. 1, pages: 30-40
-   Burke, J. (2000), "Using outage data to improve reliability", _Computer Applications in Power_, IEEE volume **13**, issue 2, April 2000 Page(s):57 - 60
-   Frost, Keith (2007), "Utilizing Real-Time Outage Data for External and Internal Reporting", _Power Engineering Society General Meeting, 2007_. IEEE 24–28 June 2007 pages 1 – 2
-   Hall, D.F. (2001), "Outage management systems as integrated elements of the distribution enterprise", _Transmission and Distribution Conference and Exposition_, 2001 IEEE/PES volume **2**, 28 October - 2 November 2001, pages 1175 - 1177
-   Kearney, S. (1998), "How outage management systems can improve customer service", _Transmission & Distribution Construction, Operation & Live-Line Maintenance Proceedings_, 1998. ESMO '98. 1998 IEEE 8th International Conference on 26–30 April 1998, pages 172 – 178
-   Nielsen, T.D. (2002), "Improving outage restoration efforts using rule-based prediction and advanced analysis", _IEEE Power Engineering Society Winter Meeting_, 2002, volume **2**, 27–31 January 2002, pages 866 - 869
-   Nielsen, T. D. (2007), "Outage Management Systems Real-Time Dashboard Assessment Study", _Power Engineering Society General Meeting, 2007_. IEEE, 24–28 June 2007, pages 1 – 3
-   Robinson, R.L.; Hall, D.F.; Warren, C.A.; Werner, V.G. (2006), "Collecting and categorizing information related to electric power distribution interruption events: customer interruption data collection within the electric power distribution industry", _Power Engineering Society General Meeting_, 2006. IEEE 18–22 June 2006, page 5.
-   P.C. Chen, T. Dokic, and M. Kezunovic, "[The Use of Big Data for Outage Management in Distribution Systems](http://www.pochenchen.com/uploads/3/3/7/6/3376872/2014_cired_final.pdf)," International Conference on Electricity Distribution (CIRED) Workshop, 2014.
-   Sridharan, K.; Shulz, N.N. (2001), "Outage management through AMR systems using an intelligent data filter", _IEEE Transactions on Power Delivery_, **16** (4): 669–675, [doi](https://en.wikipedia.org/wiki/Doi_(identifier) "Doi (identifier)"):[10.1109/61.956755](https://doi.org/10.1109%2F61.956755)