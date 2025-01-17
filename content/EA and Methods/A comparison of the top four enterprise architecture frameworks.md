---
title: A comparison of the top four enterprise architecture frameworks
source: https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/
author:
  - "[[Svyatoslav Kotusev]]"
published: 2021-07-01
created: 2024-11-05
description: For many people, the very notion of enterprise architecture (EA) is closely associated with EA frameworks, if not entirely synonymous to them, writes Svyatoslav Kotusev, Enterprise Architecture researcher.
tags:
  - EA
  - Framework
  - Methods
  - TOGAF
  - Zachman
  - DoDAF
  - FEAF
---
For many people, the very notion of enterprise architecture (EA) is closely associated with EA frameworks, if not entirely synonymous to them, writes Svyatoslav Kotusev, Enterprise Architecture researcher.

These frameworks allegedly offer the necessary guidance for practicing enterprise architecture and addressing the problem of business and IT alignment in organisations.

Existing EA frameworks are covered in many mainstream sources. These sources include, among others, a pretty well-known [article of Roger Sessions](https://web.archive.org/web/20170310132123/https:/msdn.microsoft.com/en-us/library/bb466232.aspx) presenting four leading EA frameworks, Zachman, TOGAF, FEA and Gartner, whose influence can be noticed even in the [latest industry publications](https://www.cio.com/article/222421/what-is-enterprise-architecture-a-framework-for-transformation.html), as well as a rather famous book ‘How to Survive in the Jungle of Enterprise Architecture Frameworks’ discussing 14 EA frameworks[<sup>1</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#1).

Furthermore, the very genre of musing on frameworks is extremely popular among various EA writers. For example, the academic literature offers tens of papers devoted to analysing, comparing and formulating selection criteria for EA frameworks[<sup>2</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#2). Gartner alone issued nearly a dozen of several hundred dollars-worth reports with its advice on how to analyse, choose and deal with EA frameworks properly[<sup>3</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#3). [Local consulting companies](https://www.terrafirma.com.au/our-thinking/top-10-enterprise-architecture-frameworks/) and [software tool vendors](https://www.avolutionsoftware.com/news/how-to-choose-an-enterprise-architecture-framework/) offer their own comparisons and framework selection guidelines as well.

At first glance, the current literature offers an exhaustive analysis of all existing EA frameworks from all imaginable perspectives. However, despite the abundance and variety of the available frameworks analyses, these analyses have one critically important feature in common: all these analyses are *perfectly speculative* in nature. Specifically, all of them assume that whatever is ‘promised’ by EA frameworks is true, i.e. represents genuine best practices and valid reference models that proved helpful in some organisations and can be beneficial to other companies willing to practice enterprise architecture. For this reason, all the extant analyses of EA frameworks essentially concentrate only on ample promises given by these frameworks and take their promises for granted, but never question them or analyse whether, or to what extent, these promises have actually been delivered.

So, what do we know about popular EA frameworks besides these speculations? While all the previous analyses compared only the claims and promises of EA frameworks (e.g. which frameworks propose more guidance on which aspects of an EA practice), this article compares their practical consequences and outcomes (e.g. whether EA frameworks in fact delivered on their promises and what their real value is). In particular, the article focuses on the four most widely known EA frameworks: the Zachman Framework, FEAF, DoDAF and TOGAF.

## Zachman Framework

The Zachman Framework initially emerged in the 1980s as a two-dimensional 30-cell taxonomy for architectural descriptions[<sup>4</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#4). Today, it is widely advertised as the fundamental structure or even [‘ontology’ for enterprise architecture](https://www.zachman.com/about-the-zachman-framework), whose role in the EA discipline is equivalent to the role of the periodic table of elements in chemistry.

The framework was proposed by John Zachman, at that time a marketing specialist at IBM, as part of his attempts ‘merely to improve on the planning methodologies to follow BSP’[<sup>5 (page xvi)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#5) (BSP was one of the earlier IBM’s information systems planning methodologies that he promoted since the 1970s). The framework resulted from Zachman’s observations of similarities allegedly existing between architectural representations utilised in the manufacturing and construction industries. Namely, Zachman speculated that ‘an analogous set of architectural representations is likely to be produced during the process of building any complex engineering product, including an information system’[<sup>4 (page 281)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#4). Although originally the framework was conceived for individual information systems, in the late 1990s it was readily ‘elevated’ to the enterprise level and repositioned as the framework for enterprise architecture, even without any noticeable modifications of its structure[<sup>6</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#6).

The fundamental flaw in the underlying analogy between engineering products and information systems exploited by Zachman was spotted long ago, besides many other people, even by his colleagues from IBM[<sup>7</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#7). Yet, Zachman continued to emphatically promote his framework and insistently inquired: ‘Why would anyone think that the descriptive representations for enterprises are going to be any different from the descriptive representations of anything else that has ever been created?’[<sup>8 (page 41)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#8) Moreover, he relentlessly argued for producing ‘excruciatingly’ detailed descriptions and even went further to guarantee that such formal, engineering-style drawings are necessary for organisations:

‘Some day, I guarantee you, you are going to wish you had every one of the models identified by the \[Zachman Framework\] made explicit, every one of them made explicit enterprise-wide, all the models integrated horizontally across every row, all the models integrated vertically down every column and all the models made explicit at excruciating levels of detail’[<sup>9 (page 9)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#9)

Of course, Zachman did not specify where his guarantees can be redeemed and did not risk his own dollars while disseminating these ideas. It is difficult to estimate now how many people have been perplexed by his prescriptions and how much money has been spent in vain in organisations globally in the attempts to develop ‘all the models made explicit at excruciating levels of detail’, as Zachman recommended. However, research reports from some organisations that acted in line with his advice indicate that their EA practices resulted in dramatic failures ‘with multimillion dollar consequences’[<sup>10 (page 85)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#10) and anecdotal evidence suggests that similar experiences were rather typical across the industry:

‘Most of us have heard John Zachman’s often-quoted remark: ‘Someday you are going to wish you had all these models made explicit, enterprise-wide, horizontally and vertically integrated, at an excruciating level of detail’. Taking this remark too literally has caused too many EA teams to lock themselves in their ivory towers, snowed under by hundreds of models that no one is able to keep up to date’[<sup>11 (page 10)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#11)

As a result of Zachman’s brilliant and persistent promotional efforts, what we have today is a purely symbolic taxonomy, which is claimed to be fundamental, but is apparently based on inappropriate and confusing assumptions, cannot classify real EA artifacts, has no demonstrated examples of its practical application, no use cases in organisations, no implications for EA practitioners and [does not add any theoretical or practical value to the EA discipline](https://www.bcs.org/content-hub/fake-and-real-tools-for-enterprise-architecture/), as discussed earlier. Besides that, contrary to the widespread beliefs, historically the Zachman Framework did not introduce the notion of architecture, was not the first architectural taxonomy and even [did not coin the term ‘enterprise architecture’](https://eapj.org/fake-and-real-tools-for-enterprise-architecture/), as also reported earlier.

At the present moment, it would arguably be fair to say that the broad interest in the Zachman Framework has already faded away and within the next few years it is likely to be forgotten by the EA community due to its inexplicable practical utility. However, some architects still like the Zachman Framework because, unlike other EA frameworks, it is easy to use – ‘using it’ does not require studying extensive materials and does not imply doing anything in particular.

## Federal Enterprise Architecture Framework (FEAF)

The Federal Enterprise Architecture Framework (FEAF) is a rather comprehensive EA guidance developed specifically for the U.S. Federal Government in the end of the 1990s[<sup>12</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#12). Rhetorically, FEAF was based on the pioneering ideas of John Zachman and Steven Spewak, who were regarded as ‘two of many recognised leaders in architecture conceptualisation and enterprise architecture planning’[<sup>12 (page 19)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#12).

In reality, however, FEAF descends directly from the ancient information systems planning methodologies of the 1960s-1970s. For instance, FEAF leverages Spewak’s Enterprise Architecture Planning (EAP) methodology, which in turn ‘has its roots in IBM’s BSP’, as explicitly acknowledged by its author[<sup>5 (page 53)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#5). Consequently, similarly to early architecture planning methodologies, FEAF is based on the naïve assumption that the long-term target state for the whole organisation can be defined by a dedicated group of planners, described in detail via numerous formal diagrams and relationship matrices and then implemented as planned.

> For you
> 
> Be part of something bigger, [join BCS, The Chartered Institute for IT](https://www.bcs.org/membership-and-registrations/become-a-member/ "Become a member").

BSP and similar mechanistic planning methodologies proved impractical long before the development of FEAF[<sup>13</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#13), [<sup>14</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#14), [<sup>15</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#15). Furthermore, even Steven Spewak himself admitted that ‘the vast majority of enterprises that undertake Enterprise Architecture Planning are not successful’[<sup>5 (page 19)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#5). Unsurprisingly, FEAF failed as well, and failed spectacularly:

‘Enterprise architecture within the Federal Government hasn’t been working, and far more often than not hasn’t delivered useful results. Moreover, significant parts of the federal EA program have been complete and utter failures’[<sup>16 (page 6)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#16)

The outright fiasco of FEAF can be fairly considered to be the single most expensive documented failure of an EA initiative in the history:

‘Literally more than a billion dollars have been spent so far on enterprise architecture by the Federal Government, and much, if not most of it has been wasted’[<sup>16 (page 52)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#16)

Even worse, the very emergence of FEAF also represents an evident failure of logic and common sense: the planning approach that consistently proved ineffective earlier in multiple companies has been ‘scaled up’ to the federal level only to fail again with much greater losses. In light of the abundant previous negative research findings regarding formal architecture methodologies[<sup>13</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#13), [<sup>14</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#14), [<sup>15</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#15), the failure of FEAF can be viewed as a natural, perfectly predictable and even the only possible outcome.

Today, FEAF arguably does not deserve any attention from the community of EA practitioners. It offers no reasonable guidance that can help anyone establish an EA practice, nothing of practical value, only some obscure pictures and a bunch of curious reference models the meaning of which was not really understood even by architects working for the U.S. Government[<sup>16</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#16).

## Department of Defense Architecture Framework (DoDAF)

The Department of Defense Architecture Framework (DoDAF) emerged in the mid-2000s as a common approach to architecture for the U.S. Department of Defense (DoD) and represents an evolution of the earlier C4ISR framework born in the 1990s[<sup>17</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#17). DoDAF defines the views that should be covered in architecture, specific products that should be created to describe them and the steps that should be followed to develop these deliverables.

Conceptually, DoDAF embodies essentially the same ideas and beliefs as FEAF inspired by early architecture planning methodologies, e.g. once you produce a comprehensive architecture depicting the desired future, it will naturally help you make better decisions (somehow). However, besides analogous findings regarding other architecture methodologies[<sup>13</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#13), [<sup>14</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#14), [<sup>15</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#15), the naivety of these beliefs was noticed previously even specifically in relation to the C4ISR framework, DoDAF’s direct predecessor:

‘The prevailing belief was that if one built the architecture, the owners and operators would come. History has shown, however, that few organisations actually ‘operationalised’ the architecture – and the owners and operators did not come. The inherent flaw from the beginning was the lack of a standard framework or methodology that allows the architecture to be inserted into the decision making process’[<sup>18 (page 2)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#18)

As in the case of FEAF discussed above, these earlier observations regarding the pitfalls of architecture methodologies did not stop DoD from repeating exactly the same mistakes again on a wider scale. In particular, DoD intended to create a comprehensive architecture for its business mission area consisting of almost the full set of 26 products prescribed by DoDAF[<sup>19 (pages 40-41)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#19) (this case, by the way, clearly demonstrates that EA frameworks were originally designed to be implemented literally ‘as is’, not merely as flexible toolkits for architecture, as many people would argue today). However, the official report to congressional committees concluded that the developed architecture deliverables turned out largely useless:

‘The products that it has produced do not provide sufficient content and utility to effectively guide and constrain ongoing and planned systems investments. As a result, despite spending almost 4 years and about $318 million, DoD does not have an effective architecture program’[<sup>19 (page ii)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#19)

Precisely the same conclusions have also been echoed several years later in another official report:

‘Even though DoD has spent more than 10 years and at least $379 million on its business enterprise architecture, its ability to use the architecture to guide and constrain investments has been limited’[<sup>20 (page ii)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#20)

Therefore, instead of establishing a successful EA program in DoD, DoDAF consumed nearly $400 million and generated only the heaps of arcane documents unsuitable for decision-making purposes, in a way similar to FEAF[<sup>16</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#16). As one of the DoD reports neatly summarised, ‘hundreds of millions of dollars had been spent on a business enterprise architecture (BEA) that had limited use’[<sup>21 (pages 1-2)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#21).

Currently, DoDAF can arguably be helpful, at best, as a loose catalogue of diverse models some of which occasionally might be found useful or inspiring by experienced architects, and predominantly in the realm of solution architecture. No sane human beings should ever consider the prescriptions of DoDAF seriously as an actionable guidance for their EA practice, as DoD did.

## The Open Group Architecture Framework (TOGAF)

The Open Group Architecture Framework (TOGAF) was created by The Open Group in the mid-1990s from the materials of the earlier TAFIM framework[<sup>22</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#22), which itself was based on some earlier models initiated in the mid-1980s. TOGAF provides an end-to-end, holistic guidance for an EA practice including the steps and sub-steps required to develop architecture (ADM), a comprehensive collection of artifacts and deliverables necessary to describe architecture (ACF), governance and maturity models, as well as many other diverse recommendations[<sup>22</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#22). Presently, TOGAF has achieved the status of the most popular EA framework and is regarded by many as a de facto industry standard in enterprise architecture.

Similarly to FEAF and DoDAF, TOGAF follows fundamentally the same mechanistic step-by-step logic as all the previous architecture planning methodologies (e.g. BSP, Method/1 and Information Engineering) that discredited themselves long ago and, therefore, offers essentially nothing new and simply cannot work successfully in practice[<sup>23</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#23). For instance, exactly the same well-known problems associated with all formal architecture methodologies had been reported earlier regarding TAFIM and ultimately led to its retirement (and thus to the emergence of TOGAF):

‘TAFIM most certainly required a large investment of both time and money. \[...\] The elapsed time required to produce the architecture makes it close to obsolete before completion. \[...\] The end result is normally incomprehensible to a business-oriented audience and is harder to trace to the business strategy. \[...\] Perhaps in part due to some of these flaws, the TAFIM was abruptly cancelled’[<sup>24 (page 79)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#24)

Those architects following ADM steps more or less closely and developing at least half of all the deliverables prescribed by ACF will inevitably face analogous problems, experience disappointment and eventually abandon TOGAF as a practical guidance:

‘After an intensive phase of familiarisation and an initial workshop, where TOGAF was presented to the involved stakeholders, we decided: Thanks, too complicated for us’[<sup>25 (page 14)</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#25)

However, as reported earlier[<sup>23</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#23), [<sup>26</sup>](https://www.bcs.org/articles-opinion-and-research/a-comparison-of-the-top-four-enterprise-architecture-frameworks/#26), currently the [absurdness of TOGAF is already widely acknowledged](https://www.bcs.org/content-hub/the-critical-scrutiny-of-togaf/) among seasoned EA practitioners. Now, in virtually all cases, TOGAF is viewed merely as a label and ‘used’ purely declaratively - [its prescriptions are simply ignored](https://www.bcs.org/content-hub/enterprise-architecture-is-not-togaf/) and other, [more reasonable planning approaches are followed instead](https://www.bcs.org/content-hub/togaf-version-92-whats-new/).

It is arguably impossible to assess with any precision how much money had been wasted in the past by organisations trying to adopt TOGAF’s ‘best practices’, but the stories of EA teams that aligned their activities with TOGAF, produced heaps of shelfware and have been eliminated or reorganised are plentiful in every corner of the planet. Taking into account that TOGAF is aggressively promoted worldwide with varying intensity for at least two decades as a proven EA standard and buttressed by the global infrastructure of consultancies, experts and other commercially motivated supporters, these expenditures can be truly daunting and vastly outnumber the aggregate toll of all other EA frameworks. Besides that, a standalone multimillion-dollar industry has also formed around TOGAF courses, training and certifications that yields nothing but symbolic badges.

Although the overall step-wise planning approach recommended by TOGAF is unfit for real organisations, it would be fair to say that some separate terms, notions, ideas and artifacts mentioned in the 500-pages-long TOGAF manual can certainly be found helpful in practice. However, to be able to ‘decipher’ this manual, distinguish a few good ideas from numerous not-so-​good ones and determine their applicability in concrete situations, architects should fully realise how EA practices actually work. From this perspective, TOGAF can be ironical viewed as a ‘trash can’ of random EA-related ideas, where something useful can occasionally be found, but only by mature EA practitioners who *already* know all of that, understand what to look for and how to interpret it properly.

The discussion above presented a realistic view and analysis of the four most prominent EA frameworks from a pragmatic, practical standpoint. A comparison of the top four EA frameworks is briefly summarised in Figure 1.

[![[comparison-of-frameworks.jpg|Table displaying the comparison of EA frameworks]]](https://www.bcs.org/media/7480/comparison-of-frameworks-lg.jpg)

Figure 1. A Comparison of the Top Four Enterprise Architecture Frameworks (click to view larger image)

So, which one of them is worse? As it is evident from the comparison provided in Figure 1, none of the top four EA frameworks is substantiated by anyone’s genuine best practices; all of them represent merely renovated replicas of some earlier architecture planning methodologies that were once advertised by consultancies but proved impractical and vanished, except for the Zachman Framework, which represents a superficial attempt to improve on one of those methodologies. All these frameworks also advocate simplistic ideas inspired by classic engineering-style thinking manifested in formalised documentation or step-by-step processes unsuitable for real organisations with their dynamism, social nature and enormous complexity. Each of the famous EA frameworks also caused noticeable damage to organisations trying to use them in the form of wasted money and efforts, even when these frameworks were tailored specifically for concrete organisations, as in the case of FEAF and DoDAF. Needless to say, each of them promised infinitely more than it has actually delivered, if anything at all. For this reason, it would be fair to conclude that these EA frameworks are *all worse*.

Even though none of the top four EA frameworks proved useful, each of them is still actively advertised as some form of ‘best practice’ by its salesmen: the [Zachman Framework](https://www.zachman.com/about-the-zachman-framework) has ‘profound significance in putting definition around enterprise architecture’, [FEAF and DoDAF](https://feacinstitute.org/feac-training/enterprise-architecture-training) have ‘proven to have immediate applicability’ and ‘are very powerful frameworks’, while [TOGAF](https://www.opengroup.org/togaf) is ‘a proven enterprise architecture methodology’ and ‘the most prominent and reliable enterprise architecture standard’. Generally, the entire stream of EA frameworks is driven by commercial interests, rather than common sense. Numerous consultancies, vendors and gurus tout EA frameworks for their own pecuniary purposes, regardless of their detrimental effects on the EA discipline.

Overall, the phenomenon of EA frameworks most certainly is a grand management fad that was shamefully swallowed by the EA community. Moreover, it arguably represents one of the most ridiculous fads in the history of management, or [‘the fad of the century’](https://www.bcs.org/content-hub/enterprise-architecture-frameworks-the-fad-of-the-century/), which proposed so few new ideas relative to the previously existing approaches, wasted so much money in organisations globally, brought so little value to practice and, taking all that into account, is still not unanimously acknowledged as a fad. Even worse, instead of being rejected outright as impractical and forgotten, EA frameworks slowly get institutionalised into the fabric of society in the form of university courses and prerequisite certifications for architects, perpetuating themselves and causing permanent cognitive dissonance between rhetoric and reality throughout the EA community.

As it requires a rich imagination, unshakeable faith or strong commercial motivation to find any resemblance between how successful EA practices actually work and what popular EA frameworks prescribe, these frameworks do not deserve to be discussed seriously, but only to be derided and thrown out. Do not try to implement EA frameworks and, please, beware of the next fads!

## References

<sup><span id="1">1</span></sup> Schekkerman, J. (2004) *How to Survive in the Jungle of Enterprise Architecture Frameworks: Creating or Choosing an Enterprise Architecture Framework (2nd Edition)*, Victoria, BC: Trafford Publishing.

<sup><span id="2">2</span></sup> Bui, Q. N. (2017) ‘Evaluating Enterprise Architecture Frameworks Using Essential Elements’, *Communications of the Association for Information Systems*, Vol. 41, No. 1, pp. 121-149.

<sup><span id="3">3</span></sup>Lapkin, A. and Weiss, D. (2008) ‘Ten Criteria for Selecting an Enterprise Architecture Framework’ (#G00163673), Stamford, CT: Gartner.

<sup><span id="4">4</span></sup> Zachman, J. A. (1987) ‘A Framework for Information Systems Architecture’, *IBM Systems Journal*, Vol. 26, No. 3, pp. 276-292.

<sup><span id="5">5</span></sup>Spewak, S. H. and Hill, S. C. (1992) *Enterprise Architecture Planning: Developing a Blueprint for Data, Applications and Technology*, New York, NY: Wiley.

<sup><span id="6">6</span></sup> Zachman, J. A. (1996) ‘Concepts of the Framework for Enterprise Architecture: Background, Description and Utility’, Monument, CO: Zachman International.

<sup><span id="7">7</span></sup>Stecher, P. (1993) ‘Building Business and Application Systems with the Retail Application Architecture’, *IBM Systems Journal*, Vol. 32, No. 2, pp. 278-306.

<sup><span id="8">8</span></sup>Zachman, J. A. (2010) ‘Architecture Is Architecture Is Architecture’, In: Kappelman, L. A. (ed.) *The SIM Guide to Enterprise Architecture*, Boca Raton, FL: CRC Press, pp. 37-45.

<sup><span id="9">9</span></sup>Zachman, J. A. (2001) ‘You Can't "Cost-Justify" Architecture’, Monument, CO: Zachman International.

<sup><span id="10">10</span></sup>Hobbs, G. (2012) ‘EAM Governance and Organisation’, In: Ahlemann, F., Stettiner, E., Messerschmidt, M. and Legner, C. (eds.) *Strategic Enterprise Architecture Management: Challenges, Best Practices, and Future Developments*, Berlin: Springer, pp. 81-110.

<sup><span id="11">11</span></sup> Konkol, S. and Kiepuszewski, B. (2006) ‘Enterprise Architecture Agility: Roadmapping with EARM’, *Cutter IT Journal*, Vol. 19, No. 3, pp. 10-15.

<sup><span id="12">12</span></sup>FEAF (1999) ‘Federal Enterprise Architecture Framework, Version 1.1’, Springfield, VA: Chief Information Officer Council.

<sup><span id="13">13</span></sup>Goodhue, D. L., Kirsch, L. J., Quillard, J. A. and Wybo, M. D. (1992) ‘Strategic Data Planning: Lessons from the Field’, *MIS Quarterly*, Vol. 16, No. 1, pp. 11-34.

<sup><span id="14">14</span></sup>Lederer, A. L. and Sethi, V. (1988) ‘The Implementation of Strategic Information Systems Planning Methodologies’, *MIS Quarterly*, Vol. 12, No. 3, pp. 445-461.

<sup><span id="15">15</span></sup>Periasamy, K. P. (1994) *Development and Usage of Information Architecture: A Management Perspective*, PhD Thesis: University of Oxford, UK.

<sup><span id="16">16</span></sup>Gaver, S. B. (2010) ‘Why Doesn't the Federal Enterprise Architecture Work?’, McLean, VA: Technology Matters.

<sup><span id="17">17</span></sup>DoDAF (2004) ‘DoD Architecture Framework, Version 1.0 (Volume I: Definitions and Guidelines)’, Arlington County, VA: Department of Defense (DoD).

<sup><span id="18">18</span></sup>Thomas, R., Beamer, R. A. and Sowell, P. K. (2000) ‘Civilian Application of the DOD C4ISR Architecture Framework: A Treasury Department Case Study’, In: Burns, D. (ed.) *Proceedings of the 5th International Command and Control Research and Technology Symposium*, Canberra: CCRP Press, pp. 1-21.

<sup><span id="19">19</span></sup>GAO (2005) ‘DOD Business Systems Modernization: Long-Standing Weaknesses in Enterprise Architecture Development Need to Be Addressed’ (#GAO-05-702), Washington, DC: Government Accountability Office.

<sup><span id="20">20</span></sup>GAO (2013) ‘DOD Business Systems Modernization: Further Actions Needed to Address Challenges and Improve Accountability’ (#GAO-13-557), Washington, DC: Government Accountability Office.

<sup><span id="21">21</span></sup>GAO (2007) ‘Business Systems Modernization: Strategy for Evolving DOD's Business Enterprise Architecture Offers a Conceptual Approach, but Execution Details Are Needed’ (#GAO-07-451), Washington, DC: Government Accountability Office.

<sup><span id="22">22</span></sup>TOGAF (2018) ‘TOGAF Version 9.2’ (#C182), Reading, UK: The Open Group.

<sup><span id="23">23</span></sup>Kotusev, S. (2018) ‘TOGAF: Just the Next Fad That Turned into a New Religion’, In: Smith, K. L. (ed.) *TOGAF Is Not an EA Framework: The Inconvenient Pragmatic Truth*, Great Notley, UK: Pragmatic EA Ltd, pp. 27-40.

<sup><span id="24">24</span></sup>Perks, C. and Beveridge, T. (2003) *Guide to Enterprise IT Architecture*, New York, NY: Springer.

<sup><span id="25">25</span></sup>Buckl, S., Ernst, A. M., Lankes, J., Matthes, F. and Schweda, C. M. (2009) ‘State of the Art in Enterprise Architecture Management’, Munich, Germany: Software Engineering for Business Information Systems (SEBIS), Technical University of Munich.

<sup><span id="26">26</span></sup>Kotusev, S. (2018) ‘TOGAF-Based Enterprise Architecture Practice: An Exploratory Case Study’, *Communications of the Association for Information Systems*, Vol. 43, No. 1, pp. 321-359.

## Related