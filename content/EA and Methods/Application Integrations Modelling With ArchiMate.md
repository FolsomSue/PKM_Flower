---
title: Application Integrations Modelling With ArchiMate - Holistic Enterprise Development
source: https://www.hosiaisluoma.fi/blog/application-integrations-with-archimate/
author:
  - "[[Eero Hosiaisluoma]]"
published: 2016-12-03
created: 2024-12-20
description: "Several alternative approaches of modeling data switching between applications are shown in the examples (1 to 10) below. These alternative modelling approaches illustrate the situation as follows: “Application A” owns a “Data Object A-1”, which is requested by “Application B”. Data flows from “Application A” to “Application B”. “Application A” realizes a service “Application Service A-1” that is […]"
tags:
  - EA
  - Integration
  - Modelling
  - ArchiMate
---
Several alternative approaches of modeling data switching between applications are shown in the examples (1 to 10) below.

These alternative modelling approaches illustrate the situation as follows:

- “Application A” owns a “Data Object A-1”, which is requested by “Application B”.
- Data flows from “Application A” to “Application B”.
- “Application A” realizes a service “Application Service A-1” that is used by “Application B”. Accordingly, “Application Interface A-1” is the concrete structural implementation of the “Application Service A-1”.
- Practically, “Application B” requests the “Application A” and gets the “Data Object A-1” as a response – via the “Application Service A-1”, which behavior is exposed with the “Application Interface A-1”.

![[Application-Integration-View.jpg]]

Application Integration View.

### Summary

There are plenty of alternative ways to model application integrations with ArchiMate, some of which are shown above. In practice, it is necessary to agree which modeling patterns are to be used in an organization. This is crucial, so that the overall enterprise architecture modelling repository can be kept consistent and coherent.

Concerning application integrations modelling, I’d suggest to adapt and utilize approaches 1, 3 and 10 of those shown above. Those are the most informative and practical approaches (a.k.a “patterns”), as they are relatively simple and intuitively understandable.

---

For more ArchiMate examples & patterns see:

- **ArchiMate Cookbook**, [link](https://www.hosiaisluoma.fi/blog/archimate-cookbook/)
- **ArchiMate Examples**, [link](https://www.hosiaisluoma.fi/blog/archimate-examples/)
- ArchiMate & EA blog, [link](https://www.hosiaisluoma.fi/blog/)

---