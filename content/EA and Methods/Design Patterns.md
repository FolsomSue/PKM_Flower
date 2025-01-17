---
title: Design Patterns - DZone Refcardz
source: https://dzone.com/refcardz/design-patterns
author:
  - "[[dzone.com]]"
published: 
created: 2024-12-29
description: Learn design patterns with this tutorial on the original 23 Gang of Four design patterns, including diagrams, explanations, use cases, and examples.
tags:
  - EA
  - EA_App
  - SA
  - Design_Pattern
  - Patterns
  - GoF
  - Gang_of_Four
  - Methods
---
The GoF design patterns are divided into three categories: creational, structural, and behavioral.

### Creational Patterns 

This type of pattern abstracts the instantiation process of an object.

#### Abstract Factory 

The abstract factory pattern creates families or groups of objects without knowing their implementation.

**Figure 1**: Abstract factory pattern

![[17168132-design-patterns-figure-1.png]]

**Table 1**

| **Summary** | **Use Cases** |
| --- | --- |
| Abstracts the creation logic for a family of objects into an **abstract factory** interface with methods whose return values are also interfaces. **Concrete factories** then implement the factory interface and return concrete objects from the factory methods. | - Creating groups or families of objects while hiding their instantiation details - Constraining families of related objects to be used in conjunction with one another - Exposing a group of objects, but only by their interfaces |

**Example**: An abstract factory can be used when interacting with file systems, where one family of objects pertains to Windows, while another family of objects pertains to Linux. When a client requests the objects used to interact with the file system on a Windows system, the Windows factory is provided; likewise, the Linux factory is provided when interacting with a Linux system.

#### Builder 

The builder pattern abstracts the logic for creating an object into a set of steps.

**Figure 2**: Builder pattern

![[17168133-design-patterns-figure-2.png]]

**Table 2**

| **Summary** | **Use Cases** |
| --- | --- |
| Defines a **builder** interface that contains methods that assemble an object step by step and return a completely assembled object. The returned object can be abstracted behind an interface, allowing different builders to return different concrete objects. | - Creating a complex object requiring multiple steps - Creating different concrete objects depending on the creation parameters - Creating identical objects by using the same configured builder |

**Example**: The Apache [`HttpClient`](https://github.com/apache/httpcomponents-website/blob/master/src/site/markdown/httpcomponents-client-5.2.x/index.md) library provides the [`URIBuilder`](https://javadoc.io/doc/org.apache.httpcomponents/httpclient/latest/org/apache/http/client/utils/URIBuilder.html) class, which allows clients to instantiate a builder object, configure the `URI` components (e.g., protocol, host, port, and query parameters), and then generate a `URI` object using the `build()` method.

#### Factory Method 

The factory method abstracts the creation logic for an object in the superclass, allowing subclasses to define the concrete object that will be created.

**Figure 3**: Factory method pattern

![[17168134-design-patterns-figure-3.png]]

**Table 3**

| **Summary** | **Use Case** |
| --- | --- |
| Defines an algorithm in a superclass based on the creation of an object, which is represented by a **factory method** with an interface return value. Concrete classes then override the factory method and return a concrete object. | Delegating the creation logic to subclasses |

**Example**: Factory methods can be used when creating task objects, where a `Scheduler` used to schedule and execute the logic of the task can be abstracted into a factory method. Subclasses can then be created, such as `SingleThreadedTask`, where the factory method returns a `SingleThreadedScheduler` that is used to execute the task logic.

#### Prototype 

The prototype pattern clones an existing object without requiring a client to know the concrete type.

**Figure 4**: Prototype pattern

![[17168135-design-patterns-figure-4.png]]

**Table 4**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **clone** method in the interface for a class that returns an object of the same interface. Concrete classes then implement the interface and return a copy of the same object with the same state from the clone method. | - Deciding which classes to instantiate at runtime - Reducing the number of class hierarchies and factory classes - Knowing *a priori* that there are only a few possible states for an object, and cloning existing objects may be easier than executing complex creation logic |

**Example**: The Java [`Object`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/lang/Object.html) class includes a [`clone()`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/lang/Object.html#clone\(\)) method, which allows a client to clone any object that implements the [`Cloneable`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/lang/Cloneable.html) interface. There is nuance to the implementation of the `clone()` method that deviates from a strict prototype pattern implementation, but conceptually, any class that implements `Cloneable` can be cloned.

#### Singleton 

The singleton pattern ensures that a class has only one object created, which is accessed through a single entry point.

**Figure 5**: Singleton pattern

![[17168138-design-patterns-figure-5.png]]

**Table 5**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **single object** (*singleton*) of a class and defines a static method that returns this singular object. Constructors are hidden so that clients cannot create additional objects. | - Requiring only a single object be created across an application - Requiring a single entry point to an object - Managing global data |

**Example**: The Spring Inversion of Control (IoC) container allows clients to create [singleton beans](https://docs.spring.io/spring-framework/reference/core/beans/factory-scopes.html#beans-factory-scopes-singleton). If a bean is declared as a singleton, then only one instance of the bean will be created per IoC container, and the same object will be used when auto-wiring the bean into dependent objects. Note that Spring does not implement this bean creation using a static method, but it conceptually enforces the singleton pattern.

### Structural Patterns 

Structural patterns compose classes and objects to form larger structures.

#### Adapter 

The adapter pattern allows an object with one interface to be used where another interface is expected.

**Figure 6**: Adapter pattern

![[17168162-design-patterns-figure-6.png]]

**Table 6**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates an **adapter** class with the **target** interface and embeds the original object (*adaptee*) as either a subclass or an attribute. The adapter then implements its methods using logic from the original object or class.   Note: There are *class* and *object* **adapters**; class adapters use inheritance to achieve adaptation, while object adapters use aggregation. Object adapters are more common than class adapters for many modern applications. | - Reusing an existing class, but its interface does not match the desired interface - Adding an interface to an existing class is impractical |

**Example**: The Java [`InputStreamReader`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/io/InputStreamReader.html#%3Cinit%3E\(java.io.InputStream\)) adapter class contains constructors that accept an [`InputStream`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/io/InputStream.html) and implements the [`Reader`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/io/Reader.html) interface. By creating an `InputStreamReader` using this constructor, an `InputStream` can be adapted to a `Reader` and used wherever a `Reader` is required. Likewise, an [`OutputStream`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/io/OutputStream.html) can be adapted to a [`Writer`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/io/Writer.html) using the [`OutputStreamWriter`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/io/OutputStreamWriter.html) class.

#### Bridge 

The bridge pattern splits orthogonal concepts in a single class hierarchy into multiple hierarchies. 

**Figure 7**: Bridge pattern

![[17168170-design-patterns-figure-7.png]]

**Table 7**

| **Summary** | **Use Cases** |
| --- | --- |
| Avoids a combinatorial explosion of concrete classes by separating a single class hierarchy into two or more hierarchies. One of the hierarchies (the **abstraction**) is maintained, and the separated hierarchy (the **implementor**) is added as an attribute of the first hierarchy. | - Avoiding permanent relationship between an abstraction and its implementation - Reducing the proliferation of implementations as the number of class hierarchies grow - Sharing implementations among multiple objects |

**Example**: There may be multiple properties that define a vehicle, such as its type (sedan, truck, etc.), its color, and its trim (sport, premium, etc.). Creating a new class for each of these hierarchies, such as `RedSportSedan`, would introduce a combinatorial explosion as the number of possibilities for each hierarchy grows. Instead, we can create a `Sedan` implementation for a `Vehicle` interface that has two properties, `Color` and `Trim`, where `Red` implements the `Color` interface and `Sport` implements the `Trim` interface.

#### Composite 

The composite pattern creates a hierarchy of nested objects, where the client does not know if it is performing an operation on a single leaf object or an object representing a collection of sub-objects. 

**Figure 8:** Composite pattern

![[17168171-design-patterns-figure-8.png]]

**Table 8**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates an interface that defines a **component**, then creates two categories of concrete implementations: terminal nodes called *leaves* and *composites* that contain a collection of sub-objects of that interface called *children*. When a client calls an interface method, the composite calls the same method on all its children.   Note: The children of composites can be both leaves and other composites. | - Needing to create tree structures of arbitrary depth - Wanting clients to treat an entire structure uniformly without handling collections of objects and singular objects differently |

**Example**: If we want to move files on a file system, we can create a `File` interface with a `moveTo(Path)` method, and have two concrete implementations: a composite called `Directory` and a leaf called `TextFile`. When a client calls the `moveTo(Path)` method on an arbitrary `File` object, a `TextFile` object will move itself, while a `Directory` object will move itself as well as all its children (either `TextFile` or other `Directory` objects).

#### Decorator 

The decorator pattern wraps an existing object to add additional responsibility.

**Figure 9**: Decorator pattern

![[17168175-design-patterns-figure-9.png]]

**Table 9**

| **Summary** | **Use Cases** |
| --- | --- |
| Defines an interface for a **component**, then defines **decorators** that implement that interface, while also wrapping another **implementor** as an attribute. When a method is called on the decorator, the decorator performs some action in addition to calling the same method on the wrapped object. | - Adding responsibility to classes without changing the original class - Changing responsibility dynamically by applying or forgoing a decorator - Dividing logic into small, nested objects |

**Example**: In order to debug issues and track the operation of an application, it is important to log critical events, but logging statements can add clutter to a method definition. Instead of adding logging directly to the method, we can create a decorator that logs the start and completion of the method call, allowing us to supplement the logic contained in the wrapped object without changing the wrapped object itself.

#### Façade 

The façade pattern defines a unified interface for a more complex set of sub-interfaces and classes.

**Figure 10**: Façade pattern

![[17170848-design-patterns-figure-10.png]]

**Table 10**

| **Summary** | **Use Cases** |
| --- | --- |
| Limits the interface of a complex set of interfaces and classes to the client's most important features. Provides a single point (**façade**) for the client to interact with the sub-components. Removes the need to directly interact with numerous sub-components. | - Providing a simple interface to a complex system - Decoupling complex dependencies in a subsystem - Separating subsystems by introducing façades for each subsystem and communicating between the subsystems only through their façades |

**Example**: The Spring IoC container allows clients to programmatically create beans through the [`ApplicationContext`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/context/ApplicationContext.html) class. While the Spring IoC container is a complex and intricate system, the `ApplicationContext` class provides a single entry point that allows clients to focus on bean creation and retrieval, rather than the details of the IoC container.

#### Flyweight

The flyweight pattern reuses shared components rather than instantiating new objects each time a component is needed.

**Figure 11**: Flyweight pattern

![[17168186-design-patterns-figure-11.png]]

**Table 11**

| **Summary** | **Use Cases** |
| --- | --- |
| Extracts shared, constant state of a component into a class that represents the intrinsic state. The component then stores this **intrinsic state** as an attribute and adds properties for its state that vary (called *extrinsic state*). When new instances of the component are created, each instance has its own extrinsic state but shares its intrinsic state. | - Limiting memory used by an application - Reducing the total number of objects used in an application - Sharing state when identity is not important (conceptually distinct objects may be identical since they are shared) |

**Example**: The boxed types in Java each contain a `valueOf` method that creates a boxed object from its primitive counterpart — for example, `Integer.valueOf(1)`. The [`Integer#valueOf(int)`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/lang/Integer.html#valueOf\(int\)) method will always return the same `Integer` object for values between `-128` and `127`, while other values may also be cached (e.g., `Integer.valueOf(1) == Integer.valueOf(1)` will always be `true`, while `Integer.valueOf(1000) == Integer.valueOf(1000)` is not guaranteed to be `true`). Note: the implementation used by `Interger#valueOf(int)` may not exactly match the flyweight pattern, but it conceptually implements the pattern.

#### Proxy 

The proxy pattern wraps an existing object in order to control access to the wrapped object.

**Figure 12**: Proxy pattern

![[17168192-design-patterns-figure-12.png]]

**Table 12**

| **Summary** | **Use Cases** |
| --- | --- |
| Defines an interface for a **subject**, then creates concrete implementations of this interface. Creates a **proxy** implementation, where a concrete implementation (*real subject*) is stored in the proxy as an attribute. The proxy wraps this implementation and controls access to it. Note: Proxies are similar to decorators, but proxy controls access while decorators provide additional capability. | - Limiting access to a service - Altering the behavior of an existing service - Caching data |

**Example**: A cache that reduces the number of calls made to a database. If we are trying to access books in a database, we can create a `BookRepository` interface with a `findById(long)` method, and we can create a `MongoDbBookRepository` to find `Book` objects in our MongoDB database. We can then create a `CachedBookRepository` that caches `Book` objects in memory and has a reference to the `MongoDbBookRepository` to find `Book` objects that are not already in the cache. When a client calls `findById(long)`, if the `Book` object is already in the cache, it is immediately returned without querying the MongoDB database, thus limiting the number of queries to the MongoDB instance.

### Behavioral Patterns 

This category assigns responsibility and defines communication among groups of objects.

#### Chain of Responsibility 

The chain of responsibility pattern passes a request to a chain of handlers, where each handler is responsible for handling the request or passing it to the next handler.

**Figure 13**: Chain of responsibility pattern

![[17168193-design-patterns-figure-13.png]]

**Table 13**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates an interface for **handlers**, and each concrete handler stores a reference to the next handler (*successor*) in the chain. Each handler either handles the request or passes it onto the next handler. | - Handling errors when the exact error is not known beforehand - Handling arbitrary requests that may require different levels of granularity |

**Example**: Although the code is opaque to the application, the Java exception handling uses the chain of responsibility concept. When an exception is thrown, the Java Virtual Machine (JVM) looks to see if the current context on the stack can handle the exception. If it can, the exception handler — defined using a catch block — is called; otherwise, the stack is popped, and the next context is checked to see if it can handle the exception. This process continues until a suitable exception handler is found or the entire stack is popped.

#### Command 

The command pattern stores a request, along with all the information necessary to handle the request, in a single object that can be executed by any client or queued for execution at a later time.

**Figure 14**: Command pattern

![[17168194-design-patterns-figure-14.png]]

**Table 14**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **command** interface, which usually has a single method that takes no parameters. Concrete commands store a reference to a **receiver** object that knows how to execute the command with certain parameters as well as the parameters for the command. When a client calls the command method, the concrete command object calls the receiver method, passing the required parameters. | - Needing to store a command for execution at a later time - Needing to execute a command by a different component than the original handler |

**Example**: Undo operations can be implemented through the command pattern. Each time an action is taken, a command object can be created — with the logic and parameters necessary to undo the action — and pushed onto a stack. If the user presses the undo button, the command objects can be popped from the stack and executed, thus undoing the previous action.

#### Interpreter 

The interpreter creates an object-based representation of a grammar and interprets that representation.

**Figure 15**: Interpreter pattern

![[17168198-design-patterns-figure-15.png]]

**Table 15**

| **Summary** | **Use Case** |
| --- | --- |
| Creates an Abstract Syntax Tree (AST) of objects that all implement an **expression** interface, which contains methods to interpret expressions based on the AST. This pattern is not as commonly used as the others anymore, and it is usually seen in more niche applications (e.g.,parsers, compilers, regular expression interpreters). | Parsing well-defined expressions of a language |

**Example**: Many times, interpreters are used for resolving trees of expressions — mathematical expressions, regular expressions, simple natural language expressions, Boolean expressions, and programming language expressions — into an interpreted result. These sets of expressions are represented as ASTs and then iteratively interpreted until a result is resolved.

#### Iterator 

The iterator pattern abstracts the traversal of collections without exposing the details of the collection.

**Figure 16**: Iterator pattern

![[17168202-design-patterns-figure-16.png]]

**Table 16**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates an **iterator** interface that allows clients to find the next element in an **aggregate** and check if there is a next element. Each collection returns one or more concrete iterators that traverses the collection in the desired manner (depth-first, sequentially, etc.). | - Abstracting the iteration process for a collection of objects - Traversing the same collection using different logic depending on the chosen iterator - Supporting uniform traversal of different underlying collections (e.g., lists, stacks, and queues) |

**Example**: The Java [`Collection`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/util/Collection.html) interface includes an [`iterator()`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/util/Collection.html#iterator\(\)) method that returns a concrete implementation of the [`Iterator`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/util/Iterator.html) interface. This method is specified by the [`Iterable`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/lang/Iterable.html) interface that the `Collection` interface extends. In Java, any class that implements the `Iterable` interface can be used in a for-each loop (enhanced for loop), which is made possible by the iterator returned by each implementing class (see the [Java Language Specification, JLS, 14.14.2](https://docs.oracle.com/javase/specs/jls/se20/html/jls-14.html#jls-14.14.2)).

#### Mediator 

The mediator pattern encapsulates the communication between numerous objects into a single object.

**Figure 17**: Mediator pattern

![[17168206-design-patterns-figure-17.png]]

**Table 17**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **mediator** interface, where each concrete mediator stores the logic for how to react to given events. Each **colleague** in the system is provided a reference to a mediator object and notifies the mediator when an event occurs. The mediator reacts to each event, notifying the necessary colleagues rather than having each colleague store references to all other colleagues and storing the logic for how to react to all possible events. | - Decoupling a large number of interdependent objects - Reducing the number of dependencies a class has - Facilitating simple communication between a large number of objects |

**Example**: The mediator pattern can be used to create an event or message broker, where each component that sends and receives messages can register with the broker. And as messages are sent to the broker, the broker passes the message onto one or more receivers based on some attribute (e.g., the `to` field) of the message.

#### Memento

The memento pattern stores a snapshot of the state of an object that can be used to restore that state at a later time.

**Figure 18**: Memento pattern

![[17168208-design-patterns-figure-18.png]]

**Table 18**

| **Summary** | **Use Cases** |
| --- | --- |
| An **originator** creates a **memento** object that contains the state of the originator at the time the memento was instantiated. The memento is then passed to a **caretaker** object that stores the memento and can use it to restore the state of the originator at a later time. | - Snapshotting the state of an originator - Restoring the state of an object by a caretaker from a previously taken snapshot |

**Example**: Similar to the command pattern, a memento can also be used to undo an operation. When an action is taken, a memento is stored in a caretaker and can be used later to undo the action. To undo the operation, a reference to both the originator and the memento is required. The command pattern can be used to create a command object with a reference to both, thus creating a single, self-contained object that can perform the undo operation.

#### Observer 

The observer pattern allows clients to subscribe to events that are published when an observed object is changed.

**Figure 19**: Observer pattern

![[17168209-design-patterns-figure-19.png]]

**Table 19**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **subject** interface, which stores a collection of registered concrete **subscribers** that implement the subscriber interface. When an event occurs, the subject subsequently notifies all the registered subscribers that the event occurs. This mechanism allows for asynchronous event notifications without a subject or a subscriber knowing the implementation details of the other. | - Notifying objects of asynchronous changes - Notifying objects of changes in arbitrary publishers |

**Example**: The [Java Event Listener framework](https://docs.oracle.com/javase/tutorial/uiswing/events/intro.html) is an application of the observer pattern, where the listener takes the role of the subscriber, and the object generating the event assumes the role of the subject. Note that there are many **publish-subscribe** (pub/sub) frameworks — not just in Java, but all languages — but pub/sub is not synonymous with the observer pattern. In some cases, a message broker is used as a mediator to completely decouple the publisher from the subscriber. 

#### State 

The state pattern alters the behavior of an object when its internal state changes.

**Figure 20**: State pattern

![[17168211-design-patterns-figure-20.png]]

**Table 20**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **context** class and a **state** interface, where the context obtained contains a reference to a state object. The logic in the context class methods change based on the state, and the context class provides a method for a client to change its state. If the state of the context object changes, the behavior of its methods also changes accordingly. | - Changing the state of an object at runtime - Reducing the number of conditional statements that depend on an object's state |

**Example**: The state pattern can be used to lock the internal state of an object without checking a conditional statement, such as `isLocked()`, before each method call. Instead, the object can delegate its methods to a state object. When the `lock()` method is called on the context object, it can replace the state object with one that does nothing when the methods are called. When `unlock()` is called, the state object can be replaced with the original state object that performs the desired logic. 

#### Strategy

The strategy pattern encapsulates a set of algorithms as objects with a common interface. 

**Figure 21**: Strategy pattern

![[17168212-design-patterns-figure-21.png]]

**Table 21**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **context** class, which has a reference to a **strategy** object that implements a strategy interface. The method in the context class varies its behavior based on the results of the algorithm method, allowing the behavior of the context class to vary based on the specific strategy object used. | - Abstracting the algorithm an object executes at runtime - Sharing algorithmic implementation between different objects - Separating algorithms from their results - Reducing the number of conditional statements that depend on algorithm implementations |

**Example**: The Java [`Comparator`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/util/Comparator.html) interface represents a strategy interface, where a `Comparator` object can be passed to a method, such as [`Collections#sort(List, Comparator)`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/util/Collections.html#sort\(java.util.List,java.util.Comparator\)), to compare one object to another. In the case of `Collections#sort`, the order that a `List` is sorted depends on the `Comparator` strategy that is passed to the method.

#### Template Method 

The template method pattern provides a structure for an algorithm, while allowing subclasses to define the specific implementation for each step of the algorithm.

**Figure 22**: Template method pattern

![[17168213-design-patterns-figure-22.png]]

**Table 22**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates an **abstract class** that defines the general order and structure of an algorithm but keeps the **primitive operation** methods abstract. A **concrete class** is created, which implements the details of each step, varying the behavior of the algorithm defined in the abstract class. | - Separating general steps of an algorithm from their implementation - Reducing duplication by extracting the essence of an algorithm into a superclass and allowing subclasses to implement the details - Controlling the degree of extension of a subclass (allowing only certain parts of an algorithm to be overridden but making the general steps final) |

**Example**: The Jakarta EE [`HttpServlet`](https://jakarta.ee/specifications/platform/9/apidocs/jakarta/servlet/http/httpservlet) abstract class implements default behavior for the `doGet`, `doPost`, and other basic HTTP methods by returning an HTTP `405 Method Not Allowed` response. Clients are expected to override at least one of these methods to change how the servlet handles a request.

#### Visitor 

The visitor pattern separates an algorithm from the objects on which the algorithm is applied.

**Figure 23**: Visitor pattern

![[17168214-design-patterns-figure-23.png]]

**Table 23**

| **Summary** | **Use Cases** |
| --- | --- |
| Creates a **visitor** algorithm, which has a *visit* method for each concrete type that implements the **element** interface. The element interface then defines an *accept* method that consumes a visitor object and passes itself as the argument to the visit method. This pattern uses the concept of **double-dispatch**, where the runtime behavior of the call depends on both the concrete visitor object selected and the concrete element that it is visiting. | - Performing operations on a large number of objects based on the implementation type of those objects - Performing unrelated operations on an object structure - Parsing the same object structure in different ways |

**Example**: The Java [`FileVisitor`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/nio/file/FileVisitor.html) class is an interface that clients can implement to perform a desired action each time a file is visited. The `FileVisitor` class can be used in conjunction with the [`Files#walkFileTree`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/nio/file/Files.html#walkFileTree\(java.nio.file.Path,java.util.Set,int,java.nio.file.FileVisitor\)) to iterate through the files under a desired path and perform the action defined in a concrete `FileVisitor` object when each file is visited.