---
date: 2023-08-19
tags:
- "OOP1"
- Folie
---
![[Martin - 2000 - Design Principles and Design Patterns.pdf]]

# Design Principles and Design Patterns
## Robert C. Martin
[www.objectmentor.com](http://www.objectmentor.com)

### Software Architecture
Software architecture is a multi-tiered concept. At its highest level, architecture patterns define the overarching shape and structure of software applications. As we move down the levels, we encounter architecture tied directly to the specific purpose of the software application. Further down, we delve into the architecture of individual modules, their interconnections, and the world of design patterns, packages, components, and classes. This chapter zooms in on this particular level of architecture.

### Scope of the Chapter
However, it's important to note that the scope of this chapter is intentionally limited. There's a wealth of additional information to explore about the principles and patterns discussed here. Readers who wish to delve deeper are encouraged to refer to [Martin99].

### Architecture and Its Dependencies
The text addresses the common issues that plague software over time. Initially, software designs are pristine and elegant, a reflection of the designers' vision. These designs exude a simple beauty that captivates designers and developers, motivating them to see it come to life. Yet, with time, a transformation occurs. The software begins to deteriorate. The process starts innocuously with minor imperfections, but gradually, these accumulate, leading to a dominance of significant problems. Ultimately, the program becomes an unwieldy mass of decaying code, posing challenges for the development team to maintain.

This underscores the criticality of upholding the quality of software architecture in order to thwart this gradual decline.

It's important to acknowledge that there's a vast landscape to explore concerning the principles and patterns outlined here. [Martin99] serves as a valuable resource for those seeking deeper insights.

---

# Symptoms of Rotting Design

There are four primary symptoms that indicate deteriorating software designs. These symptoms are interconnected and include:

1. **Rigidity:** Rigidity refers to the difficulty in making even simple changes to the software. A minor modification can lead to a cascade of changes across dependent modules. Initially small tasks can escalate into extensive modifications across the application, causing significant delays.

2. **Fragility:** Fragility is closely tied to rigidity. It's the tendency for the software to break in various places whenever changes are made. What's concerning is that these failures can occur in unrelated areas, causing apprehension for managers. With time, the probability of breakage increases, making the software progressively harder to maintain.

3. **Immobility:** Immobility arises when portions of the software become challenging to reuse or separate from the rest of the application. This can hinder developers from extracting and utilizing components elsewhere, leading to inefficiencies and code duplication.

4. **Viscosity:** Viscosity characterizes the situation when it's easier to follow a suboptimal or inefficient process rather than the intended correct process. There's a misalignment between the preferred architectural approach and the easier, albeit less effective, workaround.

These symptoms are interrelated, and their impact can escalate over time, making software maintenance increasingly difficult. Managers might become reluctant to authorize changes due to the unpredictability and potential for exacerbating the existing issues.

# Immobility, Viscosity, and Changing Requirements

## Immobility

**Immobility** refers to the inability to reuse software from other projects or even from different parts of the same project. There are instances where an engineer identifies the need for a module similar to one written by another engineer. However, it's common for that module to have excessive dependencies and complexities that make extracting the desirable parts challenging. The effort required to disentangle the useful components from the undesirable ones might be deemed impractical, leading to the decision to rewrite the software instead of reusing it.

## Viscosity

**Viscosity** manifests in two forms: viscosity of design and viscosity of the environment. In terms of design, when faced with changes, engineers often have multiple ways to implement them. Some methods maintain the design's integrity, while others are quick hacks that compromise the design. If the design-preserving methods are more difficult to execute than the quick hacks, the viscosity of design is high. It becomes easier to take shortcuts that aren't aligned with the intended design.

Viscosity of the environment arises when the development environment is inefficient. For instance, if compile times are long, engineers might opt for changes that avoid extensive recompilations, even if those changes aren't ideal from a design standpoint. Similarly, if the source code control system requires hours for a few file check-ins, engineers might prioritize minimal check-ins over design preservation.

## Changing Requirements

The degradation of the design can be attributed to **changing requirements**. As requirements evolve in ways unforeseen by the initial design, changes need to be implemented quickly. These modifications might be carried out by engineers who aren't well-versed in the original design philosophy. Consequently, while the design change fulfills the requirement, it might contradict the original design principles. Over time, these deviations accumulate, leading to a state of design malignancy.

However, it's important to recognize that blaming shifting requirements alone isn't sufficient. As software engineers, we understand that requirements naturally evolve. The requirements document tends to be the most fluid aspect of software development.

These four symptoms collectively indicate a poorly architected application that's deteriorating. Any software exhibiting these signs is essentially suffering from internal decay.

# Dependency Management

## Causes of Design Decay

What triggers the decay of designs? It's changes that introduce unforeseen and new dependencies. Each of the four symptoms previously mentioned is directly or indirectly linked to improper dependencies between software modules. The degradation primarily affects the dependency architecture, ultimately undermining the software's maintainability.

To prevent the erosion of the dependency architecture, it's essential to manage the dependencies between modules within an application. This management entails creating **dependency firewalls** that prevent dependencies from propagating beyond these barriers.

The realm of **Object-Oriented Design** provides an array of principles and techniques for establishing such firewalls and effectively managing module dependencies. The following sections will delve into these principles and techniques—design patterns—that aid in preserving an application's dependency architecture.

## Principles and Techniques

First, let's explore the **principles** that govern dependency management:

1. **Single Responsibility Principle:** Each module should have a single responsibility, minimizing its potential interactions with other modules and reducing the chances of excessive dependencies.

2. **Open-Closed Principle:** Software entities (modules, classes, etc.) should be open for extension but closed for modification. This discourages altering existing modules and risking the introduction of new dependencies.

3. **Dependency Inversion Principle:** High-level modules should not depend on low-level modules; both should depend on abstractions. This principle decouples modules and promotes more flexible dependency relationships.

With these principles as a foundation, **techniques** or **design patterns** come into play:

1. **Dependency Injection:** Modules receive their dependencies rather than creating them, reducing tight coupling and allowing for easier substitution of components.

2. **Inversion of Control Containers:** Frameworks that manage dependencies and control the flow of an application. They help enforce the Dependency Inversion Principle.

3. **Facade Pattern:** Provides a simplified interface to a complex system of modules, reducing direct dependencies between components.

4. **Adapter Pattern:** Converts the interface of a class into another interface that clients expect, avoiding direct dependencies between incompatible interfaces.

By adhering to these principles and utilizing appropriate techniques, software engineers can effectively manage dependencies and prevent the gradual decay of an application's design.

---

# Principles of Object-Oriented Class Design

## The Open Closed Principle (OCP)

**The Open Closed Principle (OCP)** states that a module should be open for extension but closed for modification. Among all the principles of object-oriented design, this is arguably the most crucial. Its origin traces back to Bertrand Meyer's work. Essentially, it suggests that modules should be designed in a way that they can be extended without necessitating modifications to their source code.

The OCP might sound paradoxical, but there are various techniques for achieving it on a larger scale, and these techniques are all rooted in **abstraction**. Abstraction is indeed the linchpin of the OCP. Some of these techniques are elucidated below.

### Dynamic Polymorphism

Consider the scenario in **Listing 2-1**. The `LogOn` function requires modification each time a new type of modem is introduced. Worse, due to the dependence of each modem type on the `Modem::Type` enumeration, every modem type must be recompiled upon the addition of a new kind of modem.

```java
struct Modem {
    enum Type {hayes, courrier, ernie) type;
};

struct Hayes {
    Modem::Type type;
    // Hayes related stuff
};

struct Courrier {
    Modem::Type type;
    // Courrier related stuff
};

struct Ernie {
    Modem::Type type;
    // Ernie related stuff
};

void LogOn(Modem& m, string& pno, string& user, string& pw) {
    if (m.type == Modem::hayes)
        DialHayes((Hayes&)m, pno);
    else if (m.type == Modem::courrier)
        DialCourrier((Courrier&)m, pno);
    else if (m.type == Modem::ernie)
        DialErnie((Ernie&)m, pno)
    // ...you get the idea
}
```

# Open Closed Principle (OCP) in Action

However, this is not the most detrimental aspect of such design approaches. Programs designed in this manner often become riddled with repetitive if/else or switch statements. Every time any action needs to be performed on the modem, a selection process through an if/else chain or switch statement becomes necessary. When new modem types are introduced or the modem's behavior changes, these code sections must be searched and adjusted accordingly.

To compound the issue, programmers might incorporate local optimizations that obfuscate the structure of these selection statements. For instance, it might turn out that the same function works for both Hayes and Courrier modems. Consequently, we may encounter code like this:

```java
if (modem.type == Modem::ernie)
    SendErnie((Ernie&)modem, c);
else
    SendHayes((Hayes&)modem, c);
```

![[Pasted image 20230819212156.png]]

**Figure 2-13**
**Listing 2-2**
```java
LogOn has been closed for modification
class Modem
{
public:
```

**Listing 2-2**
```java
LogOn has been closed for modification
virtual void Dial(const string& pno) = 0;
virtual void Send(char) = 0;
virtual char Recv() = 0;
virtual void Hangup() = 0;
};

void LogOn(Modem& m,
string& pno, string& user, string& pw)
{
m.Dial(pno);
// you get the idea.
}
```

# Static and Architectural Aspects of the Open Closed Principle (OCP)

## Static Polymorphism

An additional technique for adhering to the Open Closed Principle (OCP) involves the utilization of templates or generics. **Listing 2-3** demonstrates this approach. The `LogOn` function can be extended with various modem types without necessitating direct modifications.

```java 
Logon is closed for modification through static polymorphism
template <typename MODEM>
void LogOn(MODEM& m,
string& pno, string& user, string& pw)
{
m.Dial(pno);
// you get the idea.
}
```

# The Liskov Substitution Principle (LSP)

## The Principle Defined

**The Liskov Substitution Principle (LSP)** posits that subclasses should be capable of substituting their base classes. This principle was introduced by Barbara Liskov in her pioneering work on data abstraction and type theory. It also draws inspiration from the notion of Design by Contract (DBC) by Bertrand Meyer.

![[Pasted image 20230819212858.png]]

As the principle suggests, **Figure 2-14** illustrates the concept: derived classes should be interchangeable with their base classes. In essence, if a user interacts with a base class, that interaction should remain functional even when a derived class instance is passed to it.

```java
User, Based, Derived, example.
void User(Base& b);
Derived d;
User(d);
```

In other words, if a function `User` accepts an argument of type `Base`, then, as exemplified in **Listing 2-4**, it should be permissible to supply an instance of `Derived` to that function.

**The Circle/Ellipse Dilemma.** Most of us learn, in high school math, that a circle
is just a degenerate form of an ellipse. All circles are ellipses with coincident foci.
This is-a relationship tempts us to model circles and ellipses using inheritance as
shown in Figure 2-15.
![[Pasted image 20230819215950.png]]

**Figure 2-15**
Circle / Ellipse Dilemma

While this satisfies our conceptual model, there are certain difficulties. A closer look
at the declaration of Ellipse in Figure 2-16 begins to expose them. Notice that
Ellipse has three data elements. The first two are the foci, and the last is the length
of the major axis. If Circle inherits from Ellipse, then it will inherit these data
variables. This is unfortunate since Circle really only needs two data elements, a
center point and a radius
![[Pasted image 20230819220034.png]]

## Implementation Considerations

While this principle may appear self-evident, there are intricacies that require careful consideration. The classic illustration of this concept is the Circle/Ellipse predicament...

# The Liskov Substitution Principle (LSP) and The Dependency Inversion Principle (DIP)

## The Liskov Substitution Principle (LSP)

**The Liskov Substitution Principle (LSP)**, coined by Barbara Liskov, asserts that subclasses should be seamlessly interchangeable with their base classes. This principle is founded on the idea of Design by Contract (DBC) and holds that the contract of the base class should be adhered to by its derived classes.

However, even when conceptual models align with this principle, challenges can emerge. An illustrative example is the Circle/Ellipse scenario. Circles can be seen as a degenerate form of ellipses; therefore, modeling them with inheritance seems intuitive. But complexities arise—consider that the Ellipse class carries unnecessary data for a Circle.

## The Circle/Ellipse Dilemma

The Circle/Ellipse dilemma epitomizes LSP considerations. While Circle seems like a subtype of Ellipse, Circle's needs are more constrained, leading to improper data inheritance. Attempting to rectify this by overriding methods introduces its own set of problems, as it can lead to violation of implicit contracts.

## The Dependency Inversion Principle (DIP)

**The Dependency Inversion Principle (DIP)**, a pivotal concept in OO architecture, suggests that one should depend on abstractions rather than concretions. While procedural designs often involve dependencies pointing downwards, object-oriented architecture adopts an inverted dependency structure, emphasizing abstractions.

This inversion leads to a system where high-level modules, responsible for application policies, depend on abstractions. Detailed implementation modules, in contrast, depend on these abstractions, resulting in a more robust architecture. The Dependency Inversion Principle plays a significant role in driving component design and fostering modularity.

In essence, adhering to DIP results in loosely coupled, adaptable systems, where changes in high-level policies do not necessarily disrupt low-level implementations.

Please let me know if you require further adjustments or additional information.

# Depending upon Abstractions and Other Package Cohesion Principles

## Depending upon Abstractions

The core of the **Dependency Inversion Principle (DIP)** is to ensure that dependencies within a design target interfaces or abstract classes rather than concrete classes. This guideline is essential because abstract things tend to change less frequently compared to concrete elements, and abstractions serve as flexible points for extension without altering existing code. While there are exceptions for non-volatile concrete elements, the DIP emphasizes the stability and adaptability brought by depending on abstractions.

## The Interface Segregation Principle (ISP)

**The Interface Segregation Principle (ISP)** highlights that multiple client-specific interfaces are preferable to a single, general-purpose interface. This principle, supporting concepts like COM, advocates creating specific interfaces for each client category and multiple inheriting them into a class. This approach minimizes the impact of changes on clients, as each client only relies on the specific interface it requires.

## The Release Reuse Equivalency Principle (REP)

The **Release Reuse Equivalency Principle (REP)** underscores that the granularity of reuse aligns with that of releases. For a reusable element to be effective, it must be managed by a release system, as users are unwilling to constantly upgrade due to changes. This principle emphasizes the need to group reusable classes into packages, as packages serve as both the unit of release and the unit of reuse.

## The Common Closure Principle (CCP)

**The Common Closure Principle (CCP)** observes that classes that tend to change together should be grouped together. This principle is driven by the desire to minimize the impact of changes across packages within a development project. By grouping classes that often change together, architects can reduce the number of packages affected by each release cycle, streamlining the management and deployment process.

Please let me know if you require further adjustments or additional information.

# The Common Reuse Principle (CRP) and The Acyclic Dependencies Principle (ADP)

## The Common Reuse Principle (CRP)

**The Common Reuse Principle (CRP)** advises against grouping classes that are not reused together within the same package. This principle recognizes that a dependency on a package leads to a dependency on all its contents. When a package changes, even if only a small part is relevant to a client, the entire package must be revalidated. By adhering to CRP, architects strive to prevent unrelated classes from being grouped together, minimizing the impact of changes on clients.

## The Acyclic Dependencies Principle (ADP)

**The Acyclic Dependencies Principle (ADP)** underscores that package dependencies must not form cycles. Since packages serve as the unit of release and focus the work of engineers, creating cyclic dependencies can lead to cascading impacts during releases. An architecture with cycles can require engineers to compile and build multiple packages, increasing the workload exponentially. Architects and engineers should monitor the package dependency structure to identify and break cycles to ensure efficient development and release processes.

It's important to note that these principles often work in tension with one another and must be balanced based on the project's needs and goals.

Please let me know if you have any further questions or require additional information.

# Breaking a Cycle, The Stable Dependencies Principle (SDP), and The Stable Abstractions Principle (SAP)

## Breaking a Cycle

Cycles in package dependencies can be broken in two ways. One method involves creating a new package, while the other utilizes the Dependency Inversion Principle (DIP) and the Interface Segregation Principle (ISP).

## The Stable Dependencies Principle (SDP)

**The Stable Dependencies Principle (SDP)** suggests that dependencies between packages should be directed towards stable packages. Stability in this context refers to the resistance to change. A package with many incoming dependencies is considered stable, as it requires significant effort to adapt due to its widespread use. Packages that are less dependent upon are more flexible and can accommodate changes more easily.

## The Stable Abstractions Principle (SAP)

**The Stable Abstractions Principle (SAP)** states that stable packages should also be abstract, containing abstract classes. Stability and abstractness are related to the ease of change and extension, respectively. While stable packages are less likely to change, abstract packages are easier to extend. This principle aligns with the Dependency Inversion Principle (DIP), suggesting that packages heavily depended upon should also be the most abstract.

These principles guide the design of object-oriented architectures and contribute to the overall flexibility, maintainability, and extensibility of the software.

Please let me know if you have any further questions or require additional information.

# Design Patterns: Adapter, Observer, Bridge, and Abstract Factory

## Adapter

In situations where inserting an abstract interface is not feasible due to the server being third-party software or heavily depended upon, an **Adapter** can be used to bind the abstract interface to the server. The adapter is an object that implements the abstract interface and delegates the methods to the server. It translates and then delegates the calls.

## Observer

The **Observer** pattern addresses scenarios where one element in a design needs to take action when another element detects an event without the detector being aware of the actor. For instance, a meter displaying the status of a sensor should update its reading whenever the sensor changes. However, we don't want the sensor to be aware of the meter. The Observer pattern introduces a structure where the detecting element (Subject) informs the observing elements (Observers) of changes.

## Bridge

The **Bridge** pattern is employed when the implementation of an abstract class using inheritance becomes too tightly coupled. It separates the interface from the implementation, providing a more flexible design. A class hierarchy, such as a music synthesizer, can be decoupled by creating abstract functions in the base class that are implemented in a derived class, which delegates to another interface. This way, dependencies are reduced, and implementation details can be changed independently.

## Abstract Factory

The **Abstract Factory** pattern allows for the creation of instances of concrete classes without introducing the dependency on concrete classes everywhere. It recommends creating an interface (Factory) responsible for creating instances. Clients interact with the interface to create objects, reducing the direct dependency on concrete classes. This pattern ensures that the dependency on concrete classes exists only in the Factory implementation.

These design patterns contribute to the modularity, maintainability, and extensibility of object-oriented systems by addressing common design challenges. They enable the creation of more flexible and robust software architectures.

Please let me know if you have any further questions or need additional information.
