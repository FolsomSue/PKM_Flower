---
title: "Gang of Four: Fundamental Design Patterns"
source: https://medium.com/@liams_o/gang-of-four-fundamental-design-patterns-41a85a562954
author:
  - "[[Williams O]]"
published: 2022-07-15
created: 2024-12-29
description: Have you ever heard the concept “Gang of Four”? It would be a good name for a Rock band from the 70’s but it is actually a collection of Design Patterns created way back in 1994 in the book “Design…
tags:
  - EA
  - EA_App
  - SA
  - Design_Pattern
  - Patterns
  - Gang_of_Four
  - GoF
  - UML
  - Methods
---
[

![[1*1DvBSKNBoBFcGO1RyULA0g.jpeg|Williams O]]

](https://medium.com/@liams_o?source=post_page---byline--41a85a562954--------------------------------)

![[1*mcqLN2gbkNVqoE3PxdMP9A.png]]

Have you ever heard the concept “Gang of Four”? It would be a good name for a Rock band from the 70’s but it is actually a collection of Design Patterns created way back in 1994 in the book “Design Patterns: Elements of Reusable Object-Oriented Software”, which adopts the nickname Gang of Four for being the creation of 4 authors. Its application is still as valid as it was then, so I propose in this post to review these patterns, and better yet, to implement a JS code example for each case in order to better illuminate each idea. Bear in mind that these patterns, as the name of the original book details, are applicable in the world of object-oriented programming, which, although it is the fundamental paradigm in most applications, does not fully cover the spectrum of options.

In [my previous post](https://medium.com/@liams_o/fundamental-software-architectural-patterns-663440c5f9a5), focused on Architecture patterns, I commented on the difference between those and Design patterns, which are the ones we will dig into next. Let me then recap that Design patterns differ from Architectural Patterns in their scope, they are more a solution to a localized problem and usually impact a specific section of the code base. We can consider Design patterns a medium-scale tactic that flesh out some of the structure and behavior of entities and their relationships.

GoF Design Patterns are divided into three categories:

1. **Creational**: The design patterns that deal with the creation of an object.
2. **Structural**: The design patterns in this category deals with the class structure such as Inheritance and Composition.
3. **Behavioral**: This type of design patterns provide solution for the better interaction between objects, how to provide loose coupling, and flexibility to extend easily in future.

## Creational Design Patterns

## Singleton

Ensure a class has only one instance, and provide a global point of access to it. A good usage for this pattern is for example when creating a database connection; we want to ensure that connection is not created multiple times but the same instance reused multiple times.

![[1*0tINZIjOkOaPp8Mo7Gk-rw.png]]

Singleton Class Diagram

## Factory method:

The Factory defines an interface for creating a single object, but let subclasses decide which class to instantiate. El siguiente snippet muestra el ejemplo de una fabrica de vehículos donde estos pueden ser o bien autos o bien camiones. Respecto al diagrama de clases, el snippet omite el concrete creator, los productos son creados directamente a traves de la factory.

![[1*Ss9Sl-LZJ4Q_aJT-Xc2ERg.png]]

Factory Class Diagram

## Abstract factory

This pattern provides an interface for creating families of related or dependent objects without specifying their concrete classes. Takes out the responsibility of instantiating an object from the class to a Factory class. The example below shows how to use this pattern by creating employees and vendors through a Factory of those, hiding the creation of the concrete members.

![[1*Rkc-z6F4IhSnHutoOGIEwA.png]]

Abstract Factory Class Diagram

## Prototype

Prototype pattern allows creating a new object instance from another similar instance and then modify according to our requirements. This helps to boost performance and keeping memory footprints to a minimum. We commonly see this pattern in Javascript programs. The example below shows how to create multiple servers at different ports from the same prototype instance.

![[1*HiRGjcptOnHM8Kxp_luUKQ.png]]

Prototype Class Diagram

## Builder

This pattern separates the construction of a complex object from its representation. The most common motivation for using Builder is to simplify client code that creates these complex objects. The example below shows how to create a Car Shop by using specific builders that take care of the details.

![[1*B881_2C1ccdlL5K7y_nCoQ.png]]

Builder Class Diagram

## Structural Patterns

## Decorator

Decorator pattern dynamically adds/overrides behaviour in an existing method of an object. The functionality of an object is modified at runtime.We can see this pattern being a fundamental piece on frameworks such as Angular or NestJS. The next example shows how to add extra logging when creating a new class.

![[1*zv1ULGPaReJb1toFgyFrhA.png]]

Decorator Class Diagram

## Proxy

The Proxy pattern provides functionality as a middle-man for another object to control access, reduce cost, and reduce complexity. The example below shows a simple implementation of a Geo Coder where a Proxy acts as an intermediate interface that stores coordinates in a cache to speed up queries that already happened. The consumer client of this isn’t really aware, or cares about, when things are returned from the proxy or the original source.

![[1*kaKnWEVW-9gqwU1vO0wL0g.png]]

Proxy Class Diagram

## *Façade*

*Façade* provides a wrapper simplified interface to a large portion of code. It is often present in systems that are built around a multi-layer architecture. The next example shows how 3 subsystems are used to validate an insurance request.

![[1*3vQYxPU2v22rl95fnKd-9A.png]]

Facade Class Diagram

## Composite

Used when we have to create a partitioned hierarchy. Composes zero-or-more similar objects so that they can be manipulated as one object. A perfect example for this pattern is a *tree* structure, where nodes or leaf objects are use to build up more complex results.

![[1*0Uh4zsZvFtyuqKuJHmoNjw.png]]

Composite Class Diagram

## Adapter

Provides an interface between two unrelated entities so that they can work together. This is done by wrapping an interface around an already existing class. The example shows how an implementation of a Shipping Cart is re-implemented but interface for consumers is kept through the usage of a Shipping Adapter.

![[1*KNHiYY2_5YDv230zmVzZGQ.png]]

Adapter Class Diagram

## Bridge

This pattern helps to decouple or hide an abstraction from its implementation so that the two can vary independently. This example shows how input devices are managed through a Bridge interface that hides the hardware complexity. With the Bridge pattern input and output devices can vary independently (without changes to the code). Gestures (finger movements) and the Mouse are very different input devices, but their actions map to a common set of output instructions: click, move, drag, etc. Screen and Audio are very different output devices, but they respond to the same set of instructions

![[1*cR3FYZN9I8ek5jcfsR9N4Q.png]]

Bridge Class Diagram

## Flyweight

Helps to cache and reuse object instances, is commonly used with immutable objects. This reduces the cost of creating and manipulating a large number of similar objects. In the example, the FlyweightFactory maintains a pool of Flyweight objects. The factory will check if one already exists; if not a new one will be created and stored for future reference. Several different cars are added to a CarsCollection. At the end we have a list of 7 Cars objects that share only 2 Flyweights. With large datasets the memory savings can be significant.

![[1*Bg2GBHSkniGf8wq3rg4QMg.png]]

Flyweight Class Diagram

## Behavioral Patterns

## Observer

Is a publish/subscribe pattern which allows a number of observer objects to see an event. In the example, we wish to suscribe when an Alarm is fired without checking the alarm continuously. The *Alarm* object represents the Subject. The *alarmHandler* function is the subscribing Observer.

![[1*Z8erWmZnEv8UccrSongFwQ.png]]

Observer Class Diagram

## Iterator

Accesses the elements of an object sequentially without exposing its underlying representation. A trivial example below shows an Iterator class that provides methods to move through an array of elements.

![[1*vHTkb3M_hRoFWkhhrvKkBQ.png]]

Iterator Pattern Class Diagram

## State

Allows an object to alter its behavior when its internal state changes. We can typically find this pattern in shopping cart applications where we need to represent the life cycle of objects. The simple example below shows the map of the state for a traffic light which transitions between its 3 state colors. The `currentState` var keeps the light state.

![[1*vrwIcT3ONdJrK8LehrryQA.png]]

State Pattern Class Diagram

## Strategy

Allows one of a family of algorithms to be selected on-the-fly at runtime without the consumer client realize in it. The following example illustrates how we can use this pattern in a Shipping situation where we can deliver a package into 3 different strategies: air, sea or land.

![[1*EZhw-cnGcuukf5xzkQ42gQ.png]]

Strategy Pattern Class Diagram

## Chain of responsibility

Delegates commands to a chain of processing objects. The Chain of Responsibility pattern is related to the Chaining Pattern which is frequently used in JavaScript. The following example demonstrates the money dispense for an ATM where multiple amounts are resolved through a chain of requests.

![[1*_W0_uMaBGG9zplYcm7OEFg.png]]

Chain of Responsibility Pattern Class Diagram

## Command

Creates objects which encapsulate actions and parameters. These command objects allow you to centralize the processing of the actions. The brief example below shows a program that supports the Cut, Copy, and Paste clipboard actions. Think that these actions can potentially be triggered in different ways throughout the app: by a menu system, a context menu or by a keyboard shortcut.

![[1*1OH6DmDPxBf4l-ZehUEwow.png]]

Command Pattern Class Diagram

## Interpreter

Implements a specialized language. Allows the end-user to manipulate your application through simpler instructions for example using a scripting language. In the following example the interpreter program translates decimal input into its roman representation.

<diaram>

## Mediator

The *Mediator* pattern provides central authority over a group of objects by encapsulating how these objects interact. Allows loose coupling between classes by being the only class that has detailed knowledge of their methods. In the next example we represent an Auction event where the Auctioneer acts as the *mediator* between bidders informing the auction.

![[1*Lvvxl_giggu4BF4R5JtaKg.png]]

Mediator Pattern Class Diagram

## Memento

Provides the ability to restore an object to its previous state (undo). The example shows a Contact manager that provides the ability to restore a person’s original identity through hydrate/dehydrate methods.

![[1*gl5lud4dxDsgSomc7aeslQ.png]]

Memento Pattern Class Diagram

## Template

The template method defines the skeleton of an algorithm as an abstract class, allowing its subclasses to provide concrete behavior. An example is an object that fires a sequence of events in response to an action, for instance a process request. The next concrete example the `datastore` function represents the AbstractClass and `postgres` represents the ConcreteClass. `postgres` overrides the 3 template methods with specific implementations.

![[1*Z0nlp4ui2rEmvNZ6KZAyhA.png]]

Template Method Pattern Class Diagram

## Visitor

This pattern defines a new operation to a collection of objects without changing the objects themselves. The new logic resides in a separate object called the *Visitor*. Below example shows employees getting a salary raise and 2 more vacation days. Two visitor objects, `AddSalary` and `AddVacation`, make the changes to the employee objects.

![[1*8EMtgkpwCEMUWSuW8Fmogw.png]]

Visitor Pattern Class Diagram

And that would be the full list. This was a long one so congratulations if you made it this far. It is very likely that you don’t have to apply all of the patterns but just a few of them, nonetheless it is reasonable to know their existence. Besides, you can always come back to this post to refresh your memory when needed.

That’s pretty much it. Thanks for reading! 📖

You can [follow me on Twitter](https://twitter.com/liams_o) for more posts and cool stuff.

Cheers! 🤘