---
created: 2023-11-21T10:48:23 (UTC -07:00)
tags:
  - cloud
  - transformation
  - application
  - migration
  - strategy
  - architecture
  - management
  - platform
  - hybrid
  - solution
  - portfolio
  - EA
  - Methods
source: https://txture.io/en/blog/6-Rs-cloud-migration-strategies
author:
---

# All you need to know: The 6 R’s of Cloud Migration - txture.io

> ## Excerpt
> Rehost, Replatform, Repurchase, Re-architect, Retire or Retain? 6 Application Migration Strategies: A fundamental guideline for almost any Cloud Transformation.

---
Welcome to our Cloud Essentials blog post series! In this series we provide you with insights about important concepts and practical tips for Cloud transformations. Whether you are currently going through a Cloud transformation or are preparing for it, be sure to check back frequently for more articles. This part of our Cloud Essentials series is dedicated to one of the most widely used key concepts in application transformation planning – the 6R’s of Cloud transformation. The 6R's are your essential tool to structure and communicate your application transformation roadmap. It helps to determine, for each and every application, what is the best strategy to move this application to the Cloud. So read on to find out what is inside the 6R's, how you can apply each transformation strategy and the benefits to expect.

## How the 6R’s help you define your Cloud Migration Strategy

Inadequately migrating applications from on-premises to the Cloud can completely waste the financial and practical benefits of Cloud offerings – both in the short and long run. That is why every Cloud migration roadmap needs to define a clear migration strategy for every application, based on a holistic **[application assessment](https://txture.io/en/product/cloud-readiness-assessment)**. This assessment should not only take into account technical aspects but also business, organization, security and compliance. The selected strategy fundamentally affects the expected migration effort, the potential amount of benefit of using Cloud and possible long term cost savings of the new operations model. This is where the 6Rs come into play. Essentially, you can think of each “R” as a possible migration strategy for your applications. Each strategy refers to a specific method to move an application to the Cloud, and the outcomes of this method. It is an overall framework, which does not provide detailed migration steps.

## Where do the 6Rs of Cloud Migration come from?

The concept was first mentioned by the Gartner analyst Richard Watson in 2011. The 5 original strategies – namely the Rehost, Refactor, Revise, Rebuild and Replace – were revived and adapted in a widely cited blog post by Steven Orban of AWS in 2016. Orban kept some of Gartner’s strategies, renamed some and added a new one. Via the AWS Cloud Enterprise Strategy Blog the approach has been made public and became popular. Thus, the 5R’s became the 6R’s. Today, the 6R’s are used as a fundamental guideline for almost any Cloud transformation. There are still disputes whether further strategies should be added. A 7th R, **[“Relocate”](https://txture.io/en/blog/7rs-of-cloud-migration-strategy)**, was introduced by AWS a few years ago. However, we at Txture still rely on the 6 key strategies of Orban’s article: Rehosting, Replatforming, Repurchasing, Re-architecting, Retire and Retain. Let’s get into the details of the strategies and discuss some examples for each of them.

## A closer look at each of the 6Rs Cloud Migration strategies

In the following, we dive deeper into each migration strategy. Here is an infographic to give you a first overview of the different Rs:

![6Rs of cloud migration infographic](https://txture.io/asset/blog/post_pics/6R-cloud-migration-strategies-infographic.png)6Rs of cloud migration infographic

### Rehosting

This strategy, commonly known as **[lift-and-shift](https://txture.io/en/blog/lift-and-shift-6R-cloud-migration)**, is a widely chosen strategy due to the relatively low migration effort. The virtual machine and the application that runs in are simply copied as-is to a cloud provider. The most important benefit of this strategy is migration speed because no architectural refactoring needs to be done. Moreover, the migration can often be done automatically using a variety of lift-and-shift or so-called workload mobility tools.  
However, the Rehosting strategy has a major drawback. Using this approach it is not possible to exploit the cloud's entire potential since the applications are not built in a cloud-native fashion. Simply rehosted applications are, compared to cloud-native applications, not decoupled from the operating system[\[2\]](https://txture.io/en/blog/6-Rs-cloud-migration-strategies#litRef-2) and are usually much more difficult to scale. Experience shows that from a cost perspective Rehosting usually does not lead to any major advantage.

#### Example

A VM currently running on your local ESX cluster is copied to your vSphere instance running on AWS or is started as an equivalent AWS EC2 instance, GCP VM instance or a compute instance of some other cloud provider.

We recommend using the Rehosting strategy only if speed is the most important factor. For example, if you are forced out of your data center due to the end of lease or a carve-out. If you want to make use of the Cloud’s full potential with regards to agility, scalability and long-term cost reduction you should choose a different strategy – so read on!

![Rehosting](https://txture.io/asset/blog/cloud_essentials/part1/rehosting.png)

### Replatforming

In contrast to Rehosting, **[Replatforming](https://txture.io/en/blog/replatforming-strategy-cloud-migration)** leads to cloud optimization due to some cloud platform adoption, while keeping the application core architecture the same. Replatforming requires **[deeper insights](https://docs.aws.amazon.com/prescriptive-guidance/latest/migration-replatforming-cots-applications/welcome.html)** into the application or the virtual machines to be migrated than Rehosting but does not lead to the complexity and effort typically associated with Rearchitecting[\[3\]](https://txture.io/en/blog/6-Rs-cloud-migration-strategies#litRef-3). Replatformed applications show some cloud-native characteristics like horizontal scaling and portability. Often, Replatforming is used when replacing database backends of applications with a corresponding PaaS database solution of a cloud provider.  

#### Example

An application currently runs on a VM and uses a NoSQL database running on a different VM. When re-platforming to e.g. AWS, AWS DynamoDB may constitute a proper replacement for your on-premises database. This way you do not have to manage the underlying compute resources of the database yourself anymore. Similarly, this can be discussed for the application software itself too, given that its runtime environment is supported by a cloud providers' application platform. Otherwise, a plain Rehosting strategy can be applied.

We recommend using the Replatforming strategy if you want to take advantage of cloud with improved scalability, elasticity, cost and performance, but cannot invest the required resources and effort to re-architect the application. But be aware of potential vendor lock-in, particularly for databases and middleware technologies (Txture helps you to identify these lock-in potentials 😉).

![replatforming](https://txture.io/asset/blog/cloud_essentials/part1/replatforming.png)

### Re-architecting / Refactoring

For highly critical applications that require cloud-native characteristics or applications that need thorough modernization due to outdatedness or performance issues a higher migration effort is typically profitable and hence should be part of cloud considerations[\[4\]](https://txture.io/en/blog/6-Rs-cloud-migration-strategies#litRef-4). Re-architecting (also called Refactoring or Rebuild) is the strategy that usually leads to the highest transformation cost. However, it allows optimized use of the cloud, leading to cloud-native benefits and making the application future proof. In doing so, the affected application is refactored using an alternative application architecture. Typically this involves breaking down the application’s components into smaller building blocks, microservices and wrapping them into (Docker) containers for a deployment on a container platform.  
**[Re-architecting](https://txture.io/en/blog/rearchitecting-6R-strategy)** an application often comes along with the opportunity to even break down the supported business processes into fragments, which greatly improves simplicity and makes a business process more agile[\[5\]](https://txture.io/en/blog/6-Rs-cloud-migration-strategies#litRef-5).

#### Example

You target a cloud solution for your inhouse developed “Production Planning Manager”. Your application is hosted on your physical server. Since you are operating in a highly specialized business area, an off-the-shelf application is not readily available for you. As this application provides some of your crucial business capabilities you commission the development of a new version of the application based on a cloud-native architecture. During the development of your solution blueprint you identify e.g. common data domains, shared service functions as well as expected capacity and load demands. Accordingly, you implement a microservice landscape and service facade (typically a proper web-based GUI) which you can pack into containers and deploy in a Kubernetes cluster.

![Re-architecting or Refactoring](https://txture.io/asset/blog/cloud_essentials/part1/rearchitecting.png)

### Retire

The Retire strategy means that an application is explicitly phased out. This makes sense when the business capabilities this application provides are not needed anymore or are offered in a redundant way (this is then sometimes called Reconcile to express the consolidating effect when leveraging the existing application portfolio for replacements). We see this often in those cases where organizations recently went through mergers and acquisitions. You should take the Cloud transformation project as a welcome opportunity to screen your application portfolio and reduce obsolete applications on the go.

#### Example

While reviewing your application portfolio you discover an application that only has a handful of users but incurs significant license cost. The capabilities that this application offers are provided by a more modern application that was implemented recently and with great user acceptance. This is why you retire the old application as soon as possible and advise remaining users to switch to the new standard application.

![Retire](https://txture.io/asset/blog/cloud_essentials/part1/Retire.png)

### Retain

Retain (or Revisit) means that you do not migrate the application at this point since you are lacking important information or are hindered by other factors. For some applications, a move to the cloud just does not make any sense. For example, due to latency requirements, compliance reasons or simply because the benefits of a migration won't outweigh the cost and effort to be invested. You should, however, always set yourself a reminder to “Revisit” the application because the technical or compliance landscape might have changed.

#### Example

The application in scope has real-time latency requirements as it is essentially running your production line. Also, it involves secret information to be stored and hence the use of filesystem encryption, demanding the sole control of yours. It is unlikely (still not impossible) that a public cloud data center is the right candidate for your application. This is why you decide to keep the application as-is for now or for longer.

![Retain](https://txture.io/asset/blog/cloud_essentials/part1/Retain.png)

### Repurchasing

Repurchasing (also called Replacing) is the strategy where the legacy application is fully replaced by a SaaS-solution that provides the same or similar capabilities.  
The migration effort heavily depends on the requirements and options of migrating (live) data. Some SaaS-replacements for on-premise products from the same vendor offer an option to quickly migrate data with little effort or even automatically. Some providers offer analysis tools to assess the to-be-expected migration effort. However, this might not be the case when switching to a product of a different vendor or if the migration path has been interrupted due to neglected maintenance of the on-premise application.

#### Example

A typical example of Repurchasing is replacing the outdated on-premise CRM software with a SaaS-solution like SalesForce or HubSpot. Another important example that is currently shaking up many organizations, is the migration from on-premises SAP deployments to the cloud.

![Repurchase](https://txture.io/asset/blog/cloud_essentials/part1/Repurchase.png)

## How to define what is the best migration strategy for your application?

The 6R’s of Cloud transformation are an essential tool for categorizing the Cloud migration strategy of your applications and bringing structure into your decision processes. But how to determine which migration strategy is the most accurate for a specific application? To help you get started, Txture listed 9 important questions to answer regarding your application’s specificities (technical dependencies, application lifecycle, business value, etc.). More information?

  

![6R Cloud Migration Decision Guide](https://txture.io/_next/image?url=%2Fasset%2Fresources%2F6R-migration-decision-guide-preview.png&w=3840&q=75)

### 6R Cloud Migration Decision Guide

Of course, to conduct a thorough Cloud readiness application assessment, you need to collect all relevant information to define the characteristics of your application. But fear not! Txture helps you to significantly reduce the time and effort to collect the data and automatically suggests the appropriate migration strategy for your applications.
