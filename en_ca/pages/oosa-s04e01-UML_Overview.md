# Introduction to UML #

> UML is a general-purpose visual modeling language - it is not a methodology
> 

> UP is a methodology
> 

## References ##

[Course Textbooks](textbooks.md)

- Chapter &sect;1 of the UML 2 course textbook
- Additional references to external reading material as provided

## Learning Outcomes ##

- Section &sect;1.11 of the UML 2 course textbook (UMLUP)
- You will learn to:
	* Identify UML as a language and not a methodology
	* Describe the history of UML
	* Explain the concept of Model Driven Architecture (MDA)
	* Identify how UML supports MDA
	* Define UML structure and basic building blocks
	* Illustrate the hierarchy of UML diagrams and abstract categories
	* Identify and explain the four common mechanisms of UML
	* Illustrate and explain the 4+1 Architecture
	* Identify how UML supports the 4+1 Architecture

## What is UML? &sect;1.2 ##

- A general-purpose visual modeling language for systems
- An open industry standard approved by the [Object Management Group (OMG)][omg]
- Can be used with ALL existing methodologies
- It is very well suited to be used with UP
- 'Unified' because it unifies the previous attempts at visual modeling languages and software engineering processes (SEPs)

## The birth of UML &sect;1.3 ##

- Started in 1994 as an attempt to fix the existing OO methods mess
- Booch and Rumbaugh joined Rational in 1994 to work on UML
- Jacobson came on board with Rational in 1995 (and also worked on UML)
- UML 1.0 was approved in 1997 by OMG
- UML 2.0 was finalized in 2005
- See Figure 1.2 for a visual summary

> __READ MORE__: [The original publication by the inventors][uml-1-book]
> 

> __READ MORE__: [The updated version incorporating UML 2][uml-2-book]
> 

> __READ MORE__: [OMG Formal Versions Of UML&reg;][uml-spec] provides the latest information
> 

Year | Event | Significance
-----|-------|-------------
1994 | Booch | Joins Rational to work on UML
1994 | Rumbaugh | Joins Rational to work on UML
1995 | Jacobson | Joins Rational thru acquisition of Objectory AB
1997 | UML 1.0 | First approved version by OMG
2000 | UML 1.x | Significant improvements to the initial version
2005 | UML 2.0 | Introduced a lot of new visual syntax

## The future of UML &sect;1.4
- Defined by a recent OMG initiative called [Model Driven Architecture (MDA)][mda]
- Ultimately, MDA sees the model drive the production of - and generate - code directly.

## Why Unified? &sect;1.5
Unified also because it is unified across several domains:

- Development life cycle
- Application domains
- Implementation languages & platforms
- Development processes
- Its own internal concepts

## Objects and UML &sect;1.6
- Two aspects of UML models:
	- Static structure
	- Dynamic behaviour

## UML Structure &sect;1.7
- Building blocks
- Common mechanisms
- Architecture

## UML Building Blocks &sect;1.8

### Things &sect;1.8.1
- The modeling elements themselves
- Structural things (class, interface, use case, etc.) 
- Behavioural things (interactions, activities, etc.)
- Grouping things (packages)
- Diagrams 

### Relationships &sect;1.8.2
- They tie things together
- They show how 2 or more things relate to each other

### Diagrams &sect;1.8.3
- Views into UML models
- 13 different types of diagrams (see Figure 1.6)
- _White_: with _italics text_ are abstract categories
- __Green__: with __bold text__ are diagrams we study in this course
- Yellow: with plain text are diagrams we study in OO Systems Design course
- Grey: with plain text are diagrams we don't directly study

![UML Diagrams Types][uml-diags]

## Sample UML ##

### Class Diagram ###

[gimmick:yuml (type: 'class', style: 'scruffy')]([Student]-[IdCard])

- Students are associated to an IdCard

---

[gimmick:yuml (type: 'class', style: 'scruffy')]([Student]-[IdCard], [IdCard]-[Instructor])

- Instructors are also associated to an IdCard

---

[gimmick:yuml (type: 'class', style: 'scruffy')]([Student]-[StudentCard], [Instructor]-[StaffCard], [IdCard]^-[StudentCard], [IdCard]^-[StaffCard])

- Instructors are associated to a specialized version of IdCard called StaffCard
- Students are associated to a specialized version of IdCard called StudentCard

### Object Diagram ###

[gimmick:yuml (type: 'class', style: 'scruffy')]([joe:Student]-[123:IdCard], [mary:Student]-[456:IdCard])

- The Student joe (object) is linked to IdCard 123 (object)
- The Student mary (object) is linked to IdCard 456 (object)

### Activity Diagram ###

[gimmick:yuml (type: 'activity', style: 'plain') ](`start`->`Replace IdCard`->`end`)

- Have your IdCard replaced

## UML common Mechanisms &sect;1.9

### Specifications &sect;1.9.1
- Graphical dimension
- Textual dimension

### Adornments &sect;1.9.2
- They are added to make visible aspects of the element's specification - as needed. See fig. 1.11 (p.18).

### Common divisions &sect;1.9.3

#### Classifier and instance &sect;1.9.3.1
- There are 33 classifiers in UML.
- See Table 1.2 (p.19) for the 7 more common classifiers.

#### Interface and implementation &sect;1.9.3.2
- Need to separate WHAT something does from HOW it actually does it.
- Interfaces specify WHAT must be done.
- Implementation specifies HOW it will be done.

### Extensibility mechanisms &sect;1.9.4

#### Constraints &sect;1.9.4.1
-  A constraint specifies some condition or rule about the modeling element that MUST be maintained as true.

#### Stereotypes &sect;1.9.4.2
- Represents a variation of an existing element with the same form but a modified intent.
- Can be shown as an icon or as text enclosed in &laquo; &raquo;.

#### Tagged values &sect;1.9.4.3
- Allow to indicate properties of new modeling elements defined by the stereotype.

#### UML Profiles &sect;1.9.4.4
- Profiles are collections of constraints, stereotypes and tagged values. See Table 1.4 (p. 22)

## Architecture &sect;1.10
- Represented in the 4+1 Views (see figure 1.13)
	- Logical view - captures the vocabulary of the problem domain as a set of classes and objects.
	- Process view - models the executable threads and processes in system classes.
	- Implementation view - models the files and components that make up the physical code base of the system.
	- Deployment view - models the physical deployment of artifacts onto a set of physical, computational nodes such as computers and peripherals.
	- [+1] Use Case view - captures the basic requirements for the system as a set of use cases.

---

[omg]: http://www.omg.org
[uml-1-book]: http://www.amazon.ca/dp/020130998X
[uml-2-book]: http://www.amazon.ca/dp/0321245628
[uml-spec]: http://www.omg.org/spec/UML/
[mda]: http://www.omg.org/mda

[uml-diags]: https://s3-us-west-2.amazonaws.com/oosa-wiki/uploads/images/uml-diags.png