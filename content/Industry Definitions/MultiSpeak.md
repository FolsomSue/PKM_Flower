---
tags:
  - Industry_Definitions
  - ITOT
  - ADMS
  - Standards
  - Protocols
---
# MultiSpeak
## References
- [MultiSpeak site](https://www.multispeak.org/)
## Overview
MultiSpeak is ideally suited to supporting a strategic, SOA-based integration architecture or it can be realized in a tactical point-to-point approach with simple transport layer security. A bus architecture makes it easier for a single application uniformly to support services for a number of other software packages in place at a utility. Structuring the web services in this manner also helps to support a service oriented architecture (SOA). Figure 1 illustrates the MultiSpeak service bus architecture.
![[Pasted image 20230907155659.png]]
As shown in the Figure, MultiSpeak supports a number of functions (represented by the single boxes, for example, CD: Connect/Disconnect). Software vendors offer products that will contain one or more functions combined into applications. This functional decomposition permits applications to flexibly support only those functions that are important for that vendor’s desired integration and also supports the reusability of interface functionality.

The Notification (NOT) endpoint enables any application to subscribe to any number of publish-type messages provided by a wide variety of publishers.

The following table provides a comparison of selected capabilities by of MultiSpeak as contained in the most recent releases of Versions 3.0 (build ac), 4.1.6, and Version 5.0, including endpoint coverage and specification attributes.

## Deployment Questions
- Network zone location
- Firewall implications
- SOA vs. transactional approaches
- Updates, vendor support, etc.
- Bigger question: where will the OMS be deployed? Especially as systems (like FME, Maximo, etc.) will integrate via REST, files
## Tasks
- Using MultiSpeak will likely require an Architectural Decision Record
	- Using it in IT / Corporate Zones instead of OIC + SOA


