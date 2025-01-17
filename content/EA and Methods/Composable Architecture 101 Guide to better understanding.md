---
title: "Composable Architecture 101: Guide to better understanding"
source: https://dev.to/momciloo/composable-architecture-101-guide-to-better-understanding-2kn5
author:
  - "[[Momcilo]]"
published: 2024-04-24
created: 2024-12-02
description: Choosing composable architecture for your website makes building and updating it easier. This method...
tags:
  - EA
  - EA_App
  - Design_Pattern
  - Patterns
  - Methods
  - Microservices
---
Choosing composable architecture for your website makes building and updating it easier. This method divides the site into smaller, reusable pieces that are easier to manage and update. Whether you’re a developer looking to make changes faster or a content manager wanting easier and faster content updates, this article will show you the advantages of composable architecture. Let’s dive in.

## What is Composable architecture?

Composable architecture is based on an unopinionated, headless methodology that enables developers to use APIs and create advanced websites faster.

So, a composable platform typically uses a headless CMS, because it provides APIs that the front-end code can call to fetch data.

As a headless CMS, composable architecture separates the presentation layer from the back-end system, leading to faster development, increased scalability, and agile cross-functional organization.

Even though these two approaches follow the same logic, there are some differences. ( They will be explained later in the text.) For now, let’s focus on composable architecture structure.

## Composable architecture structure

The composable architecture consists of a set of **modular components** that can be easily assembled and configured to the specific needs of each website, app, or project needs.

All modular components are independent of each other, but when assembled, they can form different website features, designs, or possibilities.

For better understanding: Think of Lego blocks. You can use one Lego block to build a tower, but if you mix different types of blocks you can build a castle, a lighthouse, or even a whole city. The same logic applies to modular components and that's why they are crucial in composable building.

![Image description](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F44gk7orj0y664rvngtp2.gif)

## Key components of composable architecture

Besides modularity and APIs, the key components include:

- CDN (Content Delivery Network): A modular solution for content delivery, scaling horizontally based on demand, improving speed, and enhancing UX.
- Hosting: Empowers organizations to compose or recompose infrastructure, ensuring scalability.
- Headless CMS: Manages and delivers content and data flexibly and modularly, serving as a central hub for content creation, storage, and management.
- Integration: Integrates third-party SaaS applications into the architecture, enhancing flexibility, scalability, and functionality.

## Composable architecture comparison

In this section, I will deal with the comparison of composable architecture with other ways of building websites and applications. Therefore, I will start with an analysis of the differences between composable and monolithic architectures.

### Composable vs monolithic architecture

Composable and monolithic architecture represent two fundamentally different approaches to designing software systems. Here's a comparison between the two:

[![Image description](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Ft9064b3ukvw4xd73ikyy.jpg)](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Ft9064b3ukvw4xd73ikyy.jpg)

**Monolithic architecture:**

1. **Single unit**: Monolithic architecture involves building the entire website or application as a single, indivisible unit. All components, including the user interface, business logic, and data access layer, are tightly integrated and deployed together.
2. **Tight coupling**: Components are tightly coupled, meaning they depend heavily on each other's implementations. Changes to one part of the application often require modifications to other parts, making the system less flexible and harder to maintain.
3. **Non-scalable**: Scaling a monolithic application can be challenging, as the entire application must be replicated to handle increased load. This can lead to inefficient resource usage and difficulty optimizing performance.
4. **Limited technology stack:** A monolithic environment often restricts technology choices, as all components must use the same programming language, frameworks, and libraries. This can limit flexibility.
5. **Deployment complexity**: Deploying updates to a monolithic application can be complex and risky, as changes to one component may impact the entire system. Deployments may require downtime and careful coordination to minimize disruptions.

**Composable architecture:**

1. **Modular design**: Composable architecture involves breaking down the application into smaller, independent components that can be developed, deployed, and scaled separately. Each component performs a specific function and can be easily combined and reconfigured.
2. **Loose coupling**: Components are loosely coupled, meaning they have minimal dependencies on each other's implementations. This promotes flexibility, allowing components to be replaced or updated without affecting the entire system.
3. **Scalability**: Enables greater scalability and flexibility by allowing components to be scaled independently based on demand. This allows for more efficient resource usage and better performance optimization.
4. **Tech-stack diversity**: Encourages the use of diverse technologies, as components can be developed using different programming languages, frameworks, and libraries. This promotes innovation and allows developers to choose the best tools for each component.
5. **Simplified deployment**: Deployments are typically simpler and less risky, as updates can be applied to individual components without impacting the entire system. This enables faster release cycles and easier rollback in case of issues.

For easier recognition of the differences, the comparison table would look like this:

|  | Composable | Monolithic |
| --- | --- | --- |
| Architecture | Independent components able to be replaced or updated | Single architecture where all components are tightly coupled |
| Scalability | Designed to be scalable | Non-scalable |
| Integration | Tech-agnostic | Limited tech-support |

### Composable architecture vs Microsevices

These two architectural paradigms promote flexibility, scalability, and agility in software development, but they differ in their approach to achieving these goals. Here's a comparison between the two:

[![Image description](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fjwdny1o60ik8klvy1460.jpg)](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fjwdny1o60ik8klvy1460.jpg)

**Modular VS Service-Oriented Design**: Composable architecture focuses on the composition of modular components within a single system, while microservices focus on breaking down the system into independent services.

**Data management:** Composable architecture typically relies on a centralized data store, while microservices emphasize decentralized data management with each service having its own database.

**Autonomy and independence**: Composable architecture emphasizes the composition of components to create complex systems. Components can be combined in various ways to create different configurations or compositions. Microservices place a strong emphasis on autonomy and independence of services, allowing for greater flexibility and agility in development and deployment.

**Granularity vs Fault Isolation**: Components in a composable architecture can vary in granularity, ranging from fine-grained microservices to larger, coarser-grained modules. Microservices promote fault isolation, as failures in one service are less likely to impact other services. As a result, failures within affected services are isolated and do not affect the entire system, which improves resilience and availability.

|  | Composable | Microservices |
| --- | --- | --- |
| Data Management | centralized data store | decentralized data store |
| Architecture | Modular design | Service-Oriented Design |
| Autonomy | Can be a mix of third-party vendors and in-house solutions | Operate on their own, interconnected via APIs |

### Composable vs headless

Composable and headless are similar concepts, but they aren’t the same. Both ensure that the frontend and backend are decoupled. However, **headless doesn’t necessarily imply a modular approach to architecture** – and that’s the main difference between these approaches.

Still, a headless CMS is one of the key components of composable architecture because it decouples content management from the presentation layer, allowing content to be managed independently and delivered via APIs to any platform or device.

[![Image description](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F31im9v4jdiiek8v41rhu.jpg)](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F31im9v4jdiiek8v41rhu.jpg)

When integrated into a composable infrastructure, a headless CMS serves as a foundational component that provides content services to the broader system. This integration enables developers to flexibly integrate content, reuse it across channels, scale with ease, and experiment with new technologies while maintaining a consistent user experience.

|  | Composable | Headless |
| --- | --- | --- |
| Scope | Composable architecture encompasses the entire system design | Focus on content management |
| Flexibility | Flexibility and customization across all aspects of the system | Flexibility for Frontend |
| Building blocks | Reuse of components and services across different projects | Reusability of content blocks different channels and applications. |

In summary, while both offer benefits in terms of flexibility, scalability, and customization, they serve different purposes within the software development lifecycle.

## How to go composable

To get closer to a composable approach, there are two primary directions to take:

- Hub-and-spoke’ approach
- Building from square one

### Going composable: Hub-and-spoke approach

The hub-and-spoke approach is often the simplest way to adopt composable architecture. It represents a method to go composable without replacing your current tech stack. All you need is an API-first platform that will enable you to tie together all the tech stack you are already using. If we go back to the Lego gif from the top of the article, in this method only thing you need is the grey Lego block:

[![Image description](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fovkfl85kr50i9ibol28e.png)](https://media2.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fovkfl85kr50i9ibol28e.png)

The gray Lego blocks represent the elimination of managing multiple base services and the elimination of any functionality gaps because it is possible to add a new tool or capability without altering the stack. You can use this approach to make legacy systems actually composable by switching to another service if your current one doesn't meet your requirements.

### Going composable: Building from square one

This approach involves building a website from scratch. It requires detailed preparation and requires more time, planning and an investment budget. In case, your choice is this approach, keep following these steps:

### 10 steps to build a website with a composable architecture

Building a website with a composable architecture involves breaking down the site's functionality into smaller components that can be easily combined and reconfigured. Here's a step-by-step guide:

1. **Define requirements**: Start by identifying the requirements and goals of your website. What features and functionality do you need? Who are your target users? Understanding these requirements will help guide your architectural decisions.
2. **Choose a headless CMS**: Select a [headless CMS](https://thebcms.com/blog/content-operations-headless-cms) that aligns with your content management needs. A headless CMS allows you to manage content separately from the presentation layer, providing flexibility and enabling integration with various frontend technologies.
3. **Design component architecture**: Break down the website's functionality into smaller components. Identify reusable components for common elements such as headers, footers, navigation menus, and content layouts. Define clear interfaces for communication between components.
4. **Select a frontend framework**: After choosing CMS, the next stack is a frontend framework or library for building the user interface. Popular options include Next CMS, NuxtCMS, or Gatsby CMS. These frameworks provide tools for creating reusable UI components and managing state.
5. **Implement components**: Develop the individual components based on the design architecture. Each component should be self-contained and independent, with well-defined inputs and outputs. Utilize component libraries or create your own reusable components to streamline development.
6. **Integrate with Headless CMS**: Connect your frontend components to the headless CMS to fetch and display content. Use the APIs provided by the CMS to retrieve data and render it dynamically within your components. This decoupled approach allows for easy content updates without affecting the frontend presentation.

Learn more: BCMS Widgets - [Reusable structured content - everything you need to know](https://thebcms.com/blog/bcms-widgets-reusable-structured-content-tutorial)
7. **Compose Pages**: Combine the components to build pages and layouts for your website. Use a flexible layout system that allows you to arrange components in different configurations. Leverage container components to manage the composition and layout of child components.
8. **Implement routing:** Set up routing to handle navigation on the website. Define routes for different pages and components using a routing library such as React Router or Vue Router. Ensure that URLs are user-friendly and SEO-friendly.
9. **Optimize performance**: Optimize the performance of your website by minimizing load times and optimizing resource usage. Implement lazy loading for components and images, optimize asset delivery, and leverage caching techniques to improve page speed.

Learn more:  [Why is your website slow?](https://thebcms.com/blog/why-is-your-website-slow-and-how-to-fix)
10. **Test and deploy**: Thoroughly test your website to ensure functionality, compatibility, and responsiveness across different devices and browsers. Deploy the website to a hosting platform or a content delivery network (CDN) to make it accessible to users.

## Go composable: How to implement composable architecture with headless CMS

Headless solutions can help you achieve composable architecture. In detail, by using an API system for content delivery you can integrate headless CMS into your platform (grey Lego block) seamlessly, and start taking advantage of composable architecture features in both ways: development and content management.

In one place you'll get composable features and building blocks for developers, marketers, and content creators.

All you need is to choose CMS with an API-first approach and start building websites and applications in a composable way. [BCMS headless CMS](https://thebcms.com/) is a tool that can help you achieve so, whatever method you choose: hub-and-spoke approach or building composable architecture from scratch.