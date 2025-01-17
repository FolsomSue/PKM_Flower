#Electric #Industry_Definitions #OT #ITOT #AMI 
# Advanced Metering Infrastructure Architecture and Components
The advanced metering infrastructure (AMI) is typically structured into a bunch of networks and composed of a few major components. Figure 1 provides an overview of all components and most networks. It is made up of the Meter, the Collector and of the server systems at the distribution system operator ([[DSO]]) or metering company side.

The subsequent sections will briefly introduce the major components of the AMI.

![](https://blog.compass-security.com/wp-content/uploads/2013/02/advanced_metering_infrastrcuture1.png)

Figure 1: Advanced Metering Infrastructure Networks and Components

##  Conceptual AMI View
- [[AMI Conceptual Overview.PNG]]
## **Head-end System**  
The head-end system (HES), also known as **meter control system**, is located within a metering company network. In most cases the metering company is the responsible DSO. The HES is directly communicating with the meters. **Therefore, the HES is located in some demilitarized zone (DMZ) since services and functionality will be provided to the outside.**  
There is much more infrastructure at the DSO or metering company side. The collected data will be managed within a metering data management system (MDM) which also maps data to the relevant consumer. Depending on the automation level, the metering data will have influence on the DSO actions in order to balance the grid.  
Exposing the HES to consumers enables some significant threats to the DSO. For example, an adversary getting hold of the HES could read all consumer data. Moreover, one could control meters or could manipulate usage data or generate alerts in order to disturb the DSO operations or at least trigger the computer incident response team (CIRT) and maybe force the DSO to backup to some business continuity plan (BCP) while analysing and recovering the HES.

## **Collector**  
The collector, also known as concentrator or gateway serves as communication node for the HES. Depending on the infrastructure the collector could be a meter itself. Its primary function is to interface between the HES and the meters and/or other collectors within its neighbourhood – the neighbourhood area network (NAN).  
Not only the head-end but also the collector exposes threats. The collector is physically exposed to adversaries. Moreover, it has a trust binding to the HES and the NAN side and is thus privileged to communicate with either end. Adversaries might exploit the fact in order to attack the HES. Additionally, on the NAN side, adversaries might impersonate the collector to setup a man-in-the-middle scenario or to invoke arbitrary commands at the meters.

## **Meter**  
The meter is installed at consumer premises. When integrated with a collector, it directly communicates to the HES. As a meter it either communicates with the collector or may serve as a relay in order to route packets between nearby meters and the collector. Some meters provide an interface for appliances. With retail consumer that network is known as the home area network (HAN). Meters do also provide local diagnostic ports for manual readout, installation and maintenance tasks as shown in figure 2.  
From an attackers perspective the meter is the entry point to building automation, DER and usage data. But the meter is also a relevant part of the smart grid and under no circumstances should its manipulation allow critical influence or affect the availability of the grid or parts of it.

## **Communication**  
The infrastructure consist of several networks of which all could rely on absolutely different media and a multitude of protocols. In total, three networks are commonly described when referring to the AMI. The WAN, NAN and HAN.

### _**Wide Area Network**_  
The WAN does connect a meter or collector to the HES. The WAN is sometimes also referred to as the backhaul network. Communication on the WAN link is mostly Internet protocol (IP) based and does commonly rely on standard information technology (IT) media and technology stacks such as fibre optic cables (FOC), digital subscriber line (DSL), general packet radio service (GPRS), multi-protocol label switching (MPLS), power line carrier (PLC) or some sort of private network. A brief overview on PLC for WAN side communication is provided in \[1\]  
The CEN/CENELEC/ ETSI Smart Meter Co-ordination Group (SMCG) does not identify a specific protocol but proposes to rely on “secure and non proprietary protocols and communication platforms” \[2\] for bulk transmission from collectors that bundle a large number of meters.

### _**Neighbourhood Area Network**_  
The NAN connects meters and collectors. Typical [[NAN]] devices are electricity, gas, water or heat meters. organisations sometimes refer to the NAN as local metrological network (LMS) \[3\], field area network (FAN) \[4\] or the metering LAN \[5\].  
Although standards such as the IEEE 802.15.4 \[6\], \[7\] based ZigBee profiles are gaining momentum, the industry and regulators seam to struggle on a common standard. Utilities among the European union nations seem to prefer the meter bus standard for NAN communication \[3\] although the ENISA does not list \[4\] the meter bus as a NAN protocol.

### _**Home Area Network**_  
Depending on the consumer type the HAN could also be named as building area network (BAN) or industrial area network (IAN). Whatever its name is, the purpose of the HAN is to integrate additional gas, water or heat meters. The HAN could allow for intelligent building automation and does also allow the integration of DERs with the smart grid.

![](https://blog.compass-security.com/wp-content/uploads/2013/02/home_area_network.png)

Figure 2: Home Area Network and Local Bus Blueprint

To optimize consumption during peak hours a utility might for example decide not to entirely turn off but to throttle large heating, ventilation, and air conditioning (HVAC) appliances to balance the grid. For that purpose, consumers will be required to grant utilities or a third-party supplier access to their appliances. However, intelligent control does not necessarily require the intervention of an external part. Thus, an intelligent HVAC might decide to throttle automatically based on the real-time pricing information provided by the utility.  
Meters in the US largely focus on ZigBee for HAN communication \[8\]. Profiles for home automation and smart energy are specified in \[9\], \[10\]. The Europe based open metering system (OMS) group is pushing a specification that relies on M‑Bus whereby the wireless M‑Bus stack is compatible with the KNX specifications \[11\]. KNX is very popular in home automation.

## **Local Bus**  
Common interfaces for diagnostic purposes are provided as two or three-wire serial lines, current loop or as an optical interface \[12\], \[13\].

**References**  
\[1\] M. Rafiei and S. M. Eftekhari, A practical smart metering using combination of power line communication (PLC) and WiFi protocols, In Proceedings of 17th Conference on Electrical Power Distribution Networks (EPDC), 2012, pp. 1–5, May 2012  
\[2\] Smart Meters Co-Ordination Group. Standardization mandate to CEN, CENELEC and ETSI in the field of measuring instruments for the development of an open architecture for utility meters involving communication protocols enabling interoperability M/441: Final Report v0.7. Dec. 2009  
\[3\] Federal Office for Information Security (BSI) Germany. Technische Richtlinie BSI-TR-03109-1: Anforderungen an die Interoperabilität der Kommunikationseinheit eines intelligenten Messsystems, v0.5. 2012  
\[4\] ENISA. Smart Grid Security: Annex I. General Concepts and Dependencies with ICT. 2012  
\[5\] EN 13575-1:2002: Communication system for meters and remote reading of meters – Part 1: Data exchange  
\[6\] IEEE Std 802.15.4:2011. IEEE Standard for Local and metropolitan area networks – Part 15.4: Low-Rate Wireless Personal Area Networks (LR-WPANs)  
\[7\] C. Bennet and D. Highfill. Networking AMI Smart Meters. In Proceedings of Energy 2030 Conference, 2008. ENERGY 2008. IEEE. pp 1-8. Nov. 2008 (DOI 10.1109/ENERGY.2008.4781067)  
\[8\] V. Aravinthan, V. Namboodiri, S. Sunku and W. Jewell. Wireless AMI Application and Security for Controlled Home Area Networks. In Proceedings of Power and Energy Society General Meeting, 2011 IEEE. pp. 1-8. Jul. 2011 (DOI 10.1109/PES.2011.6038996)  
\[9\] ZigBee Alliance. Home Automation Public Application Profile. ZigBee Profile: 0x0104 Revision 26, Version 1.1, Feb. 2010  
\[10\] ZigBee Alliance. Smart Energy Profile Specification. ZigBee Profile: 0x0109, Revision 16, Version 1.1, Mar. 2011  
\[11\] EN50090-4-1:2004. Home and Building Electronic Systems (HBES) Part 4-1: Media independent layers – Application layer for HBES Class 1  
\[12\] EN 13575-6:2008: Communication system for meters and remote reading of meters – Part 6: Local Bus  
\[13\] EN 62056-21:2002, Electricity metering – Data exchange for meter reading, tariff and load control – Part 21: Direct local data exchange