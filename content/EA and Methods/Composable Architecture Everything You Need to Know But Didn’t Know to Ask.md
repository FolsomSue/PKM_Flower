---
title: "Composable Architecture: Everything You Need to Know But Didn’t Know to Ask"
source: https://cloudinary.com/blog/composable-architecture-everything-you-need-to-know-but-didnt-know-to-ask
author:
  - "[[Cloudinary Blog]]"
published: 2022-08-08
created: 2024-12-02
description: Why composable architecture is quickly becoming one of the hottest trends in tech.
tags:
  - EA
  - EA_App
  - Design_Pattern
  - Patterns
  - Methods
  - Microservices
---
**In this article:**

- [What is Composable Architecture?](https://cloudinary.com/blog/#what_is_composable_architecture_)
- [Benefits of Composable Architecture](https://cloudinary.com/blog/#benefits_of_composable_architecture)
- [Cloudinary Composable Architecture](https://cloudinary.com/blog/#cloudinary_composable_architecture)
- [Cloudinary Features](https://cloudinary.com/blog/#cloudinary_features)
- [Programmable Media Powered by Intelligence and Automation](https://cloudinary.com/blog/#programmable_media_powered_by_intelligence_and_automation)
- [Headless DAM](https://cloudinary.com/blog/#headless_dam)
- [MACH-Certified](https://cloudinary.com/blog/#mach_certified)
- [Third-Party Integrations](https://cloudinary.com/blog/#third_party_integrations)
- [Developer First](https://cloudinary.com/blog/#developer_first)
- [Conclusion](https://cloudinary.com/blog/#conclusion)

Bringing new products to the web requires a lot of time and effort. Delivering content and experiences that fit all contexts is even more labor-intensive. You start by preparing each rich media asset for multi-channel delivery. It then needs to be adapted and manipulated to fit all modes in which that media will be delivered and consumed.

When working at scale, the amount of time invested into visual media manipulation is significant, consuming a considerable chunk of your limited development time.

Generally, when establishing a technology  ecosystem, organizations either lean on digital suites or develop a digital infrastructure in-house, meaning their architecture will be tailored to — and created in response to — their own challenges.

The problem with pursuing in-house digital ecosystems stems from financial costs and time sinks associated with developing architectures from the ground up. The larger your organization, the more time and money it takes to develop an architecture in house. You can outsource the work of creating an architecture and rich media manipulation solution to multiple vendors, but should you? You’ll need to consider such questions as:

- What products do you currently use in your development stack?
- What products are you hoping to use? Do they integrate with your current stack?
- Do the new vendors you hope to work with integrate with the *other new* vendors you’re working with? Are they compatible?

Enter composable architecture. 

Composable architecture, a design pattern that allows developers to create reusable components to build applications, is also known as TCA (The Composable Architecture). This approach is based on the microservices concept. This refers to loosely coupled services, applications, and features that act as independent building blocks. These building blocks communicate via APIs, ensuring flexibility and scalability in the development process.

With composable architecture, you can avoid these complex integration issues and vendor lock-in by using APIs and other flexible tooling that enable you to scale your entire development stack more easily. And, when working with imagery and video manipulation and delivery, a composable architecture makes it easy to work with all kinds of tools to handle — or at least assist with — tedious, complicated, or time-sensitive media tasks.

Let’s explore what composable architecture is, its benefits, and how it can make media creation and sharing easier.

Before diving into what composable architecture is and what it entails, let’s discuss why it’s important.

Let’s say you want to automate your image and video delivery process, so you use a workflow automation tool from Vendor A. You’ve been working with Vendor A for a while, so you’re comfortable and familiar with the tool. But as your organization’s goals expand, you’d like to introduce additional functionality into your workflow: using AI to transcribe your video content automatically. 

You want this to occur automatically within your current workflow, so you have to look for tools that are compatible with —and complement — the automation tool you have from Vendor A. Finding a transcription tool from Vendor B is challenging, as vendor lock-in with Vendor A limits the number of tools you could potentially integrate.

You’re stuck. Managing the interlinked dependencies among all the vendors is no easy trick. As your organization expands, integration challenges become even more complex. You could find yourself looking for tools that integrate *and* scale together, which might mean introducing new tools altogether. If you’re looking to scale up services and your Vendor A tool can’t keep up, you’ll need to investigate other options.

This happens when vendors’ products aren’t built on the foundations of compatibility. They don’t speak a common language and may not be compatible in other foundational, functional ways, which makes them hard (or impossible) to integrate.

Composable architecture to the rescue! With composable architecture, each component used during your development process is pluggable and can be replaced, scaled, and consistently improved to help you meet your business needs. When establishing composable architecture, each component of your development stack and microservices should be able to communicate with one another — regardless of differences in language or code. 

Composable architectures eliminate the dependency on web and enable you to avoid vendor lock-ins, freeing you up from costly investments in time and effort in integrating multiple services with each other.

The first step of implementing composable architecture is to understand the current state of systems. This includes understanding what capabilities, technologies, and processes have already been built within the organization. By having a clear understanding of the existing infrastructure, organizations can better determine how to integrate new components seamlessly.

Composable architectures are based on the foundational principle of [API-first](https://cloudinary.com/blog/why-take-an-api-first-approach). APIs ensure applications work and pair well with microservices and other APIs, which might operate on different code or with a different language. They provide open pathways and open communication lines between each application in the stack. 

Composable architecture offers developers significant benefits, including: 

- **Bring products and experiences to market faster.** Using a composable architecture with a microservices-based approach enables developers to bring products to market faster using agile development methodologies.

- **Speed up creation and delivery times.** Composable architectures support automation and orchestration**.** This means massive visual media collections can be managed and optimized using AI and SaaS automatization solutions.

- **Encourage reusability.** In the early days of the web, HTTP was the only player. App-to-app communication could only be done with highly custom direct TCP connections. There were no standards for app-to-app integrations, which meant you had to customize development for each app you wanted your app to talk to. By contrast, composable architectures’ components are highly reusable.

- **Reduce costs.** Given the high reusability of components built for composable architectures, costs are minimized to those at initial development.

- **Boost flexibility and avoid vendor lock-in.** Composable architectures are language agnostic. New tools can be easily integrated with our existing technology stack — and any evolutions of our stack — using widgets, APIs, SDKs, and prebuilt integrations.

- **Scale up quickly and easily to capitalize on growth opportunities.** Composable architectures are extremely flexible, allowing developers to expand services more easily and quickly and be more responsive to market changes.  And, because composable architectures are language agnostic, new APIs and tools to support growth can be added as needed.

An analogy to better understand composable architecture is the popular children’s toys by Meccano. Each piece of the toy is built from similar machine pieces of metal, which can be joined in different configurations to make anything from a crane to a helicopter. This flexibility and modularity are what composable architecture aims to achieve in the software world.

When it comes to managing rich media formats, development velocity gets eaten up easily when developers don’t have a single tool — or a cohesive, integrative suite of tools — that offers all the media preparation, modification, and sharing capabilities needed for imagery, video and emerging formats like 3D, AR and VR.

Companies need flexibility and efficiency to keep up with the competition and offer our customers the best content possible. Composable architectures enable companies to seek out the tools that best suit their use cases, publishing avenues, and aesthetic objectives without worrying whether tools play nicely with one another.

Forrester analyst Joe Cicman recently shared his thoughts during opening remarks at MACH One on why MACH vendors are poised to overtake the market. “Technology should enable brands to bring innovative digital experiences to life. It should not be what hinders companies from acting on great ideas.” The future, Cicman believes, is all about microservices. “The monoliths still provide value, but they cannot keep pace,” he explained. 

Cloudinary offers a media-centric [composable architecture](https://cloudinary.com/solutions/composable-architecture) that enables our customers to create, modify, and refine visual content more easily. It’s a headless, AI-powered platform that enables brands to easily create and deliver rich media content that’s ready to use and share across different channels and in different forms. And, since it uses an SaaS, API-first, and microservices-based approach to media development and production, many of the world’s largest and most successful brands, like Puma, River Island and Mattel, rely on Cloudinary to easily manage and optimize their media at scale.

Cloudinary offers AI-powered automation for the entire media asset lifecycle in its purpose-built and future-proof [Media Experience Cloud](https://cloudinary.com/products/image_video_technology_platform), enabling seamless integrations and promoting continuous innovation.

Cloudinary’s microservices and API-first approach to development means we offer many solutions, APIs, and tools that support our composable architecture. Let’s explore some of the features Cloudinary offers that make our media creation process more efficient and enjoyable.

Cloudinary [Programmable Media](https://cloudinary.com/products/programmable_media), an offering within the Media Experience Cloud, provides several tools that are backed by AI and automation, including background removal with the [Background Removal add-on](https://cloudinary.com/documentation/cloudinary_ai_background_removal_addon) and [object-aware cropping](https://cloudinary.com/documentation/cloudinary_ai_content_analysis_addon#object_aware_cropping), and [automatic image tagging](https://cloudinary.com/documentation/cloudinary_ai_content_analysis_addon#automatic_image_tagging) using their [Content Analysis add-on](https://cloudinary.com/documentation/cloudinary_ai_content_analysis_addon). With these tools, images can be prepared and exported in all necessary variants for any delivery channel, whether it’s for a thumbnail, social media, or email campaign. 

Furthermore, Cloudinary’s AI-powered add-ons also work with Google to perform [video transcription](https://cloudinary.com/documentation/google_ai_video_transcription_addon) and [video moderation](https://cloudinary.com/documentation/google_ai_video_moderation_addon) and provide [AI-based video preview features](https://cloudinary.com/product_updates/ai_based_video_preview). 

Cloudinary brings digital asset management capabilities to your fingertips. Our SaaS model and media APIs for search, administration, organization, collaboration, and more allow you to easily build your own UI or media programming into your workflows, whether they’re customer-facing or internal. 

The [MACH Alliance](https://machalliance.org/) is a group of companies that have joined forces to create a new standard for software development. The MACH Alliance is committed to building microservices-based, API-first, cloud-native, and headless software. This new standard allows software developers to create more scalable, reliable, and manageable applications.

As a member of the [MACH Alliance](https://cloudinary.com/blog/what-is-the-mach-alliance), Cloudinary’s base technology is certified as adhering to the cutting edge and future-proof approach of MACH technology. Cloudinary’s media APIs are flexible, expandable, and encourage cross-platform collaboration, making it easy to prepare your media for multi-channel publication.

Cloudinary’s Media Experience Cloud’s open architecture and API support make its digital ecosystem highly pluggable and friendly with other MACH members. This introduces agility and flexibility to digital media content operations. 

Cloudinary also provides [prebuilt widgets](https://cloudinary.com/documentation/embed_widgets_players), including the Upload widget, Media Library widget, and the Cloudinary Media Editor, among others, to help with various parts of the visual media creation and delivery process all in one place. However, you can also quickly leverage [certified integrations](https://cloudinary.com/documentation/cms_ecommerce_integrations) to extend the already powerful Cloudinary Media Experience Cloud, enabling efficient collaboration among existing content operations tools and services.

Cloudinary’s AI-powered solutions use a developer-first approach, meaning you have everything you need to manage and deliver all kinds of media—from images and videos to AR and the metaverse—quickly without a significant lift. Additionally, the developer-first approach helps brands avoid spending too much on developing solutions, ensures they scale easily, and allows developers to work in their language of choice, reducing  the learning curve and increasing productivity.

Composable architecture is a powerful foundation for building modular, scalable, and testable applications. It allows you to build complex applications by combining small, reusable components.

With a composable architecture, you can build systems that are flexible and adaptable to change. This is important because organizations are constantly changing and evolving, and they need to be able to adapt their systems to meet new challenges and opportunities.

Organizations relying on visual engagement with customers can particularly benefit from composable architecture. The ability to rapidly respond to changes in the market is essential for success. Additionally, easily integrating new technologies and services can give organizations a competitive edge.

Cloundary’s composable architecture provides a flexible visual media asset delivery platform. Cloudinary helps brands experiment with and deliver quality visual experiences without having to invest effort into manual tasks related to rich media. Cloudinary automates most repetitive tasks with pixel-perfect accuracy and global content availability.

To start delivering visual experiences faster and with greater flexibility and ease, check out [Cloudinary’s composable architecture solution](https://cloudinary.com/solutions/composable-architecture).

Interested in more from Cloudinary?

- [Check our Cloudinary Media Experience Cloud for composable architectures](https://cloudinary.com/solutions/composable-architecture)
- [What Is MACH Architecture?](https://cloudinary.com/blog/what-is-mach-architecture)
- [Progressive Web Apps: Architecture and Examples](https://cloudinary.com/blog/progressive_web_apps_architecture_and_examples)