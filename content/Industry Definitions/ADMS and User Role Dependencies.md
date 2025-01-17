 #ADMS #Electric #ITOT  #OT
Implementing an Advanced Distribution Management System (ADMS) can be game changing for a utility. For power utilities implementing them, they are often faced with multiple challenges including effective business process development and managing change in existing business processes. Replacing an outdated, decentralized, and redundant electric distribution legacy system with a highly integrated ADMS can be a huge undertaking. Legacy systems typically have a very different concept and simpler architecture than a modern ADMS, which features a re-distributed model of the solution as shown in the figure to the right.

[](https://wwwpowerengcom.cdn.prismic.io/wwwpowerengcom/bd4f5a14-456f-47ee-8b88-ae5053107ee7_ADMS+Environment+graphic.pdf)

[![Click to see larger image](https://images.prismic.io/wwwpowerengcom/c2986fb0-7a10-45f0-a63f-f3d6c9811f63_ADMS+Environment+graphic.jpg?auto=compress,format)

Click to see larger image



](https://wwwpowerengcom.cdn.prismic.io/wwwpowerengcom/bd4f5a14-456f-47ee-8b88-ae5053107ee7_ADMS+Environment+graphic.pdf)

ADMS merges supervisory control and data acquisition (SCADA), distribution management (DMS), outage management (OMS), and distributed energy resources (DERMS) systems into one unified solution.

While having one integrated system instead of a decentralized collection of systems can be advantageous for a power utility, an additional layer of complexity is introduced. Different stakeholders must be ready to accommodate the changes and added responsibilities that come with implementing a unified solution. Internal consolidation between different business streams becomes vital. The example shown in the figure below demonstrates a correlation between different ADMS user roles, systems, and processes.

[](https://wwwpowerengcom.cdn.prismic.io/wwwpowerengcom/94dce76c-c404-44e2-8b25-2fcb852be061_ADMS+_GIS+graphic.pdf)

[![Click to see larger image](https://images.prismic.io/wwwpowerengcom/773b76d9-e37d-453c-81dc-ec63ffdabfd5_ADMS+_GIS+graphic_rev.jpg?auto=compress,format)

Click to see larger image



](https://wwwpowerengcom.cdn.prismic.io/wwwpowerengcom/94dce76c-c404-44e2-8b25-2fcb852be061_ADMS+_GIS+graphic.pdf)

At a utility, the GIS is traditionally the single source of the truth for medium voltage (MV) and low voltage (LV) equipment. While all grid alterations are initiated within the GIS, changes introduced must be reflected on the ADMS side as well. Only consolidated data from both the ADMS and GIS can result in efficient grid monitoring, control, and equipment commissioning. Therefore, once the Feeder file is sent to the ADMS, it creates deltas (called a changeset) comprising of feeder-related electrical modifications. The user role of network model manager has an obligation to validate these changesets. Most commonly, this is performed in the QA zone if one exists. If any violations are identified, these must be resolved in the source data, which is typically within the GIS. Once electrical data is successfully imported, some utilities instantly generate a new schematic view (before promoting the changeset to the Production zone). When this step occurs and who performs this step is open for discussion since it’s dependent upon the utility's business processes.

The user role of SCADA engineer accomplishes the following dependent activity once SCADA configuration (telemetry changeset) is introduced in the QA zone. Below are two related key points:

1.  Electrical equipment on the feeder can be in a 'Planned' state (to be installed or uninstalled, for example). This does not prevent SCADA engineers from confining SCADA or performing signal mapping processes. Planned equipment that will be (de)commissioned in the future is present in both ADMS and the GIS systems. In ADMS, this is frequently represented as passive, grayed-out equipment that is not considered by topology services, and it is primarily shown for observation and commissioning purposes. The model manager is responsible for its (de)commissioning in the ADMS. SCADA engineers must sometimes perform SCADA configuration on the planned equipment in the ADMS. Although planned equipment is passive, SCADA configuration can be performed on this equipment - a feature of the ADMS system. In this way, the SCADA engineer is independent of the model manager.
2.  Since the remote terminal units (RTUs) have validation possibilities from the QA zone, Point to Point (P2P) testing can be performed there, but this phase is non-compulsory. Tangible P2P testing is accomplished in the production zone, using its Front-End Processor (FEP).

This is the initial point where harmonization between the model manager and SCADA engineer can be identified. However, the process gets progressively more complex once equipment needs to be commissioned. At this point, other ADMS roles must be established. Business processes often involve switching plan utilization for equipment commissioning which initiates a third role – the switching planner (distribution operator). This role writes, dispatches, and executes switching steps. Finally, once the field crew takes over the plan and performs physical installation and energization, the process is finished. 

This is just one of the many examples where ADMS user role dependencies are significant. To successfully utilize a highly integrated ADMS, it is essential to develop comprehensive business processes followed by the facilitation of all ADMS stakeholders. These processes must prepare teams to respond to changes ahead of time and use existing resources by collaborating as much as possible.

Feel free to reach out to me with any questions related to the user role dependencies in ADMS, and please do not hesitate to contact us at POWER for any help or additional information.