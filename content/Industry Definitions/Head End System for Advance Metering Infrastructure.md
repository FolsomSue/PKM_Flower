#Electric #Industry_Definitions #AMI
_This article is about Head End System for Advance Metering Infrastructure where we will discuss Head End System Architecture and  Head End System AMI in plants and industries. Now Question is ”What is a Head End System”  and Head End System Definition._

### **_What is a Head End System, Head End System Definition_**

> _A head-end system is hardware and software that receives the stream of meter data brought back to the utility through the AMI. Head-end systems may perform a limited amount of data validation before either making the data available for other systems to request or pushing the data out to other systems._

_This component operates within the NOC Application Layer, providing the primary interface between data extracted from / sent to the WAN and data used within back-office applications in the **NOC layer**, e.g., MDM, etc._

_Not many clear requirements exist for this element of the AMI. Typically, its properties will be defined by the choice of associated Smart Meters and DCUs deployed within the End-Customer and DCU Application Layers._

_However, the choice of Meter Data Management System (MDM) should be independent from the metering system choice, thus interoperability between HES and the MDM, and the use of open standards, is a key factor to consider._

### **_1\. Basic Technical Specifications_**

**_Interoperability_**

_The HES shall:_  
_● Support IEC 61968-9 to ensure interoperability between different metering systems and a single MDM._  
_● Offer easy integration with the Utility’s Enterprise Software (e.g., SAP) for functions such as CRM billing, etc._

### **_2\. Operational Requirements_**

#### **_2.1 Time-Synchronization_**

_The HES shall:_  
_● Possess an internal clock, synchronized with the AMI’s GPS-based, central timestamp._

#### **_2.2 Data Collection_**

_The HES shall:_  
_● Handle the registration of all DCUs (Solution A) or Smart Meters (Solution B) that that connect to its associated WAN._

_● Aggregate all metered data received from Smart Meters that connect to its associated NAN and which have registered with the DCU._

_● Store all metered data (received from registered Smart Meters) locally (as per §6.6.2.1:C), prior to sending the data to the NOC._

_● Facilitate data logging, via direct and secure access (as per §6.6.3 or alternative appropriate means) to locally stored meter data._

#### **_2.3 AMI Instructions_**

_The HES shall:_  
_● Be able to forward messages from the MDM to devices in the field (within both the End-Customer and DCU Application Layers)._

### **_3\. Interface with Wide Area Network (WAN)_**

#### **_3.1 Connectivity_**

_The HES shall:_  
_● Connect to other AMI components within the NOC Application Layer (as defined in this document) across a dedicated LAN or VLAN (i.e., not integrated with the corporate or PSA networks)_

_● Be equipped with a GSM/GPRS Interface to handle bi-directional communications to/from the WAN Communications Layer._

_● Be equipped with a RS-485 interface, furnished with at least 2× [RJ45](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjbhcOz9dTpAhW2AWMBHSR8DgwQFjAiegQIAxAB&url=https%3A%2F%2Fwww.anixter.com%2Fen_us%2Fresources%2Fliterature%2Ftechbriefs%2Fwhat-is-an-rj45-connector.html&usg=AOvVaw2zNEeSF5WEjUif0fIkIpG3) terminals._

_● Configure a data table for interactions with clients in the End-Customer and DCU Application Layers (Solution A) based on the Common Information Model (CIM)._

_● Be capable of processing complex pricing algorithms, including pre-pay customers, to apportion cost (according to tariff) to metered data profiles received._

_● Process the registration of each DCU connecting to the WAN (Solution A)_  
_or_  
_● Process the registration of each MECM connecting to the WAN (Solution B)_

**_3.2 The HES shall manage and monitor the health of communications within its associated WAN._**

## _Head End System Architecture_

_Picture shows the architecture of Head End System. For more information about architecture please search in our blog._

![Head End System for Advance Metering Infrastructure, Head End System Architecture, Head End System AMI, What is a Head End System, Head End System Definition](https://i0.wp.com/paktechpoint.com/wp-content/uploads/2020/05/img_5ece7f350f5a3.png?resize=722%2C468&ssl=1 "Head End System for Advance Metering Infrastructure, Head End System Architecture, Head End System AMI, What is a Head End System, Head End System Definition")

_Head End System for Advance Metering Infrastructure, Head End System Architecture, Head End System AMI, What is a Head End System, Head End System Definition_

**[Meter Data Management System & IEC 61968-9](https://paktechpoint.com/meter-data-management-system-iec-61968-9/)**

**[Wireless Communications Principles and Industrial Practice](https://paktechpoint.com/wireless-communications-principles-and-industrial-practice/)**