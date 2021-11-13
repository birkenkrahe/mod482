
# Table of Contents

-   [What will you learn?](#orgf48eaee)
-   [What is UML?](#org434dcc3)
    -   [UML vs. Flowcharts vs. EPC vs. BPMN](#orgc52dee8)
    -   [How UML came about](#org67fbbbe)
    -   [How do you use UML?](#orga3ef013)
        -   [Software engineering views](#org637fd3e)
    -   [UML diagram overview](#org184d3b6)
        -   [Structure diagrams](#org8f22153)
        -   [Behavior diagrams](#orgf3e009b)
    -   [Case study: airport](#org649d21c)
        -   [Use case diagrams: issuing a boarding pass](#org2be84e8)
        -   [Activity diagrams: checking in](#orged33dde)
        -   [Sequence diagrams: check in and boarding](#org9fc2fa1)
        -   [Package diagram: organisational units](#orge7896de)
        -   [Class diagram: Passenger services](#orgf4bae7e)
-   [Discussion - whaddayathink?](#orge339c65)
-   [Use case diagrams](#orgdf05bbb)
-   [Use case elements](#orgcb9b059)
    -   [Situation](#org30fb038)
    -   [Requirements](#org218f85d)
    -   [System](#orgfd32472)
    -   [Actors](#orgb38420c)
        -   [Tricky actors](#orgf97bf93)
        -   [Generalization](#org2f742cd)
    -   [Use cases](#orgcd38fcc)
    -   [Communication lines](#orge750666)
    -   [System boundaries](#org3d4638c)
    -   [Descriptions](#orga89de1b)
    -   [Reusing use cases with `<<include>>`](#orgb3f8215)
    -   [Special cases](#org5fb7ed2)
    -   [Optional reuse with `<<extend>>`](#org61c454e)
    -   [Process optimization with use cases](#org5b8ca76)
    -   [Overview diagrams](#orgb21e72c)
    -   [Use case practice](#orge1c6d92)
        -   [Find mistakes in a use case diagram](#orgbd2036d)
        -   [Create a use case from simple requirements](#org9464a7c)
        -   [Create a use case for the term project](#org1fed644)
        -   [Transfer a EPC/BPMN into an UML use case diagram](#org2f2b713)
        -   ["Hello world" as use case diagram](#org3de70e3)
-   [References](#orgabab24c)



<a id="orgf48eaee"></a>

# What will you learn?

-   What is UML?
-   How do you use UML in practice?
-   What are the main UML diagrams?
-   What are use case diagrams?
-   UML case study (airport systems)
-   Use case diagrams (requirements analysis/outside view)
-   UML practice (use case only)


<a id="org434dcc3"></a>

# What is UML?


<a id="orgc52dee8"></a>

## UML vs. Flowcharts vs. EPC vs. BPMN

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Diagram</th>
<th scope="col" class="org-left">Purpose</th>
<th scope="col" class="org-left">Example</th>
<th scope="col" class="org-left">Where</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Flowcharts</td>
<td class="org-left">Model flow</td>
<td class="org-left">Programming loop</td>
<td class="org-left">Programming</td>
</tr>


<tr>
<td class="org-left">EPC</td>
<td class="org-left">Model transactions</td>
<td class="org-left">Credit card check</td>
<td class="org-left">Bank</td>
</tr>


<tr>
<td class="org-left">BPMN</td>
<td class="org-left">Model process with communication</td>
<td class="org-left">IT support communication</td>
<td class="org-left">IT Service</td>
</tr>


<tr>
<td class="org-left">UML</td>
<td class="org-left">Model systems and processes</td>
<td class="org-left">Infrastructure and services</td>
<td class="org-left">Airport</td>
</tr>
</tbody>
</table>

In UML, one can also model static systems (without flow).


<a id="org67fbbbe"></a>

## How UML came about

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Time frame</th>
<th scope="col" class="org-left">Paradigm</th>
<th scope="col" class="org-left">Problem</th>
<th scope="col" class="org-left">Solution</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Until 1970s</td>
<td class="org-left">Software creation is an art</td>
<td class="org-left">Complexity crisis</td>
<td class="org-left">Engineering</td>
</tr>


<tr>
<td class="org-left">Until 1980s</td>
<td class="org-left">Split data and procedures</td>
<td class="org-left">Fragmentation</td>
<td class="org-left">ERD / Petri Nets</td>
</tr>


<tr>
<td class="org-left">Until 1990s</td>
<td class="org-left">Object orientation</td>
<td class="org-left">Reusability</td>
<td class="org-left">UML 0.9<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup></td>
</tr>


<tr>
<td class="org-left">Since 2005</td>
<td class="org-left">Integrated modeling</td>
<td class="org-left">Standardisation</td>
<td class="org-left">UML 2.0 (OMG)<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup></td>
</tr>
</tbody>
</table>


<a id="orga3ef013"></a>

## How do you use UML?

![img](./img/use.gif)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">UML as a sketch</td>
<td class="org-left">Convey key points, then throw away</td>
</tr>


<tr>
<td class="org-left">UML as a blueprint</td>
<td class="org-left">Detailed system specification. Use UML tool. Reverse and forward engineering to keep model in line with system. Turn portions of model into code.</td>
</tr>


<tr>
<td class="org-left">UML as a programming language</td>
<td class="org-left">Go from UML model to executable code: every aspect of the system is modeled. Model enables deployment to different environments.</td>
</tr>
</tbody>
</table>


<a id="org637fd3e"></a>

### Software engineering views

*Image: [Phillippe Kruchten's 4+1 view software engineering model](https://en.wikipedia.org/wiki/4%2B1_architectural_view_model)*

![img](./img/kruchten.png)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">VIEW</th>
<th scope="col" class="org-left">WHAT IS IT</th>
<th scope="col" class="org-left">UML Diagrams</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Logical view</td>
<td class="org-left">Abstract description of system's parts and their interactions (logic)</td>
<td class="org-left">class, object, state machine, interaction</td>
</tr>


<tr>
<td class="org-left">Process view</td>
<td class="org-left">Describes processes within the system and what might happen (simulation)</td>
<td class="org-left">activity</td>
</tr>


<tr>
<td class="org-left">Development view</td>
<td class="org-left">Describes how system's parts are organized into modules and components, and how they are layered (architecture)</td>
<td class="org-left">package, component</td>
</tr>


<tr>
<td class="org-left">Physical view</td>
<td class="org-left">Describes how system is transferred to the real world (deployment)</td>
<td class="org-left">deployment</td>
</tr>


<tr>
<td class="org-left">Use case view</td>
<td class="org-left">Describes the system functionality from an outside perspective - what the system is supposed to do. Guides all other views (requirements)</td>
<td class="org-left">use case, interaction overview</td>
</tr>
</tbody>
</table>


<a id="org184d3b6"></a>

## UML diagram overview

-   Watch the video: [UML Diagrams Full Course](https://youtu.be/WnMQ8HlmeXc) ([freeCodeCamp.org,
    2021](#org314d663)) - especially the overview (first 10 minutes)

![img](./img/uml.png)


<a id="org8f22153"></a>

### Structure diagrams

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">STRUCTURE DIAGRAMS</th>
<th scope="col" class="org-left">WHAT IS IT</th>
<th scope="col" class="org-left">EXAMPLE</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Class diagram</td>
<td class="org-left">Classes, types, interfaces, and the relationships between them</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/class.png">Order processing system</a></td>
</tr>


<tr>
<td class="org-left">Component diagram</td>
<td class="org-left">Structural relationship of important components within your system</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/component.png">Automatic Teller Machine (ATM)</a></td>
</tr>


<tr>
<td class="org-left">Deployment diagram</td>
<td class="org-left">Hardware and software across multiple machines in a realworld situation</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/deployment.png">Web application</a></td>
</tr>


<tr>
<td class="org-left">Object (instance) diagram</td>
<td class="org-left">Object instances of the classes defined in class diagrams in configurations that are important to your system</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/object.jpg">Order processing system (with data)</a></td>
</tr>


<tr>
<td class="org-left">Package diagram</td>
<td class="org-left">Dependencies between software packages and the hierarchical organization of groups of classes and components</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/package.png">Web application</a></td>
</tr>


<tr>
<td class="org-left">Profile diagram</td>
<td class="org-left">Customize UML to your case using <code>&lt;&lt;stereotype&gt;&gt;</code></td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/profile.png">Server classes</a></td>
</tr>


<tr>
<td class="org-left">Composite structure diagram</td>
<td class="org-left">The internals of a class or component, and class relationships within a given context</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/composite.jpg">School class</a></td>
</tr>
</tbody>
</table>


<a id="orgf3e009b"></a>

### Behavior diagrams

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">BEHAVIOR DIAGRAMS</th>
<th scope="col" class="org-left">WHAT IS IT</th>
<th scope="col" class="org-left">EXAMPLE</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Use case diagram</td>
<td class="org-left">Interactions between your system and users or other external systems. Helpful to map requirements.</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/usecase.png">Broadcasting System</a></td>
</tr>


<tr>
<td class="org-left">Activity diagram</td>
<td class="org-left">Sequential and parallel activities within your system (functions)</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/activity.jpg">Enter PIN</a></td>
</tr>


<tr>
<td class="org-left">State machine diagram</td>
<td class="org-left">The state of an object throughout its lifetime and the events that can change that state</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/state.png">Game states</a></td>
</tr>


<tr>
<td class="org-left">Sequence diagram</td>
<td class="org-left">Interactions between objects where the order of the interactions is important</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/sequence.png">ATM scenario</a></td>
</tr>


<tr>
<td class="org-left">Communication (collaboration) diagram</td>
<td class="org-left">The ways in which objects interact and the connections that are needed to support that interaction</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/communication.png">Bank transaction</a></td>
</tr>


<tr>
<td class="org-left">Timing diagram</td>
<td class="org-left">Interactions between objects where timing is an important concern</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/timing.png">Car park</a></td>
</tr>


<tr>
<td class="org-left">Interaction overview diagram</td>
<td class="org-left">Used to collect sequence, communication, and timing diagrams to capture an important interaction that occurs within your system</td>
<td class="org-left"><a href="https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/interaction.png">Online shopping</a></td>
</tr>
</tbody>
</table>


<a id="org649d21c"></a>

## Case study: airport

Airports are complicated. Though it does not always go like this:
watch the [video](https://youtu.be/gWYTnc7m9mE) of a 21st century public project scandal. ([DW 2020](#org5d8e973))

Some services in an airport:

![img](./img/airport.png)

Three relevant models:

1.  Business system model (passenger services)
2.  IT systems model (enabling passenger services)
3.  System integration model (interacting IT systems)

![img](./img/airport1.png)

8 diagram types used to model the whole airport ([PDF](https://github.com/birkenkrahe/mod482/blob/main/11_uml/img/airport.pdf)):

![img](./img/airport2.png)


<a id="org2be84e8"></a>

### Use case diagrams: issuing a boarding pass

First draft of the use case:

![img](./img/airport_usecase1.png)

Extended use case diagram:

![img](./img/airport_usecase.png)


<a id="orged33dde"></a>

### Activity diagrams: checking in

`Passenger services` overview (low level of detail):

![img](./img/airport_activity1.png)

More detail: `Passenter checks in`:

![img](./img/airport_activity2.png)

The same diagram but without explanations:

![img](./img/airport_activity3.png)


<a id="org9fc2fa1"></a>

### Sequence diagrams: check in and boarding

Constructing sequence of actions:

![img](./img/airport_sequence1.png)

The entire sequence spans the business use cases `check-in` and
`boarding`:

>    ![img](./img/airport_sequence2.png)


<a id="orge7896de"></a>

### Package diagram: organisational units

Constructing a package diagram by collecting organizational
units/roles:

![img](./img/airport_package1.png)

Package diagram for the organization unit `Passenger service`:

![img](./img/airport_package1.png)


<a id="orgf4bae7e"></a>

### Class diagram: Passenger services

Illustration of class "generalization". In OOP terms, `List of
    checked in passengers` and `List of passengers not yet on board`
inherits attributes and methods from `Passenger List`.

![img](./img/airport_class1.png)

Classes of the internal view of the business system:

![img](./img/airport_class3.png)

Class diagram of `Passenger services` including associations
between them. This way of drawing class diagrams focuses on the
relationships, not on the methods/functions or abilities of the
classes.

![img](./img/airport_class2.png)


<a id="orge339c65"></a>

# Discussion - whaddayathink?

![img](./img/learn.gif)

-   What do you like best? EPC, BPMN, UML? Why?
-   If Germans are so fond of modeling, why can't they seem to build
    an international airport? ([DW, 2020](#org5d8e973)).


<a id="orgdf05bbb"></a>

# Use case diagrams

![img](./img/food.png)

-   Overview: [freeCodeCamp.org](https://www.youtube.com/watch?v=WnMQ8HlmeXc&t=3427s) (video, 7 min)<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>
-   Tutorial: [Lucidchart](https://youtu.be/zid-MVo7M-E) (video, 14 min)<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">PURPOSE</th>
<th scope="col" class="org-left">CASE EXAMPLE</th>
<th scope="col" class="org-left">VIEW</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Specify the context of a system</td>
<td class="org-left">Weblog CMS</td>
<td class="org-left">Logical</td>
</tr>


<tr>
<td class="org-left">Capture requirements of a system</td>
<td class="org-left">Create new blog account</td>
<td class="org-left">Process</td>
</tr>


<tr>
<td class="org-left">Validate system architecture</td>
<td class="org-left">Specify successful/failed end condition</td>
<td class="org-left">Development</td>
</tr>


<tr>
<td class="org-left">Drive implementation and generate test cases</td>
<td class="org-left">Program and debug use cases with test data</td>
<td class="org-left">Physical</td>
</tr>
</tbody>
</table>


<a id="orgcb9b059"></a>

# Use case elements


<a id="org30fb038"></a>

## Situation

The problem: "Chinese whispers"

![img](./img/projects.png)

The solution: Use case modeling

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Focus</td>
<td class="org-left">System <b>requirements</b> strictly from the outside looking in</td>
</tr>


<tr>
<td class="org-left">Task</td>
<td class="org-left">Specify the <b>value</b> that the system delivers to <b>users</b>.</td>
</tr>


<tr>
<td class="org-left">Tools</td>
<td class="org-left">User <b>stories</b>, project canvas, <b>agile</b> workflow (Scrum)</td>
</tr>


<tr>
<td class="org-left">Excluded</td>
<td class="org-left">Nonfunctional requirements (e.g. performance targets)</td>
</tr>
</tbody>
</table>


<a id="org218f85d"></a>

## Requirements

Requirement A.1:

> A content management system (CMS) shall allow an **administrator** to
> **create a new blog account**, provided the personal details of the new
> blogger are **verified** using the **author credentials database**.


<a id="orgfd32472"></a>

## System

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">A system is defined by its boundaries.</td>
</tr>
</tbody>
</table>

![img](./img/cms.png)


<a id="orgb38420c"></a>

## Actors

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Actors are outside our system (CMS)</td>
</tr>


<tr>
<td class="org-left">Actors don't have to be actual people</td>
</tr>


<tr>
<td class="org-left">Actors must interact with the system</td>
</tr>


<tr>
<td class="org-left">Actors cannot be changed by system design</td>
</tr>
</tbody>
</table>

![img](./img/actor.png)


<a id="orgf97bf93"></a>

### Tricky actors

Some actors are tricky: is the `system clock` an actor?

Decision process:

![img](./img/actorprocess.png)

The `system clock` is not a person and it cannot change with the
system's design (it's part of the given computing
infrastructure), so it's not an `actor`.


<a id="org2f742cd"></a>

### Generalization

![img](./img/generalization.png)


<a id="orgcd38fcc"></a>

## Use cases

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Use cases must have clear pass/fail criteria</td>
</tr>


<tr>
<td class="org-left">All actors must know if the system fulfils the use case</td>
</tr>


<tr>
<td class="org-left">Complete use cases have system interaction and output</td>
</tr>


<tr>
<td class="org-left">Use cases provide measurable results to users</td>
</tr>
</tbody>
</table>

A use case is drawn as an oval with a name that describes the
interaction that it represents. E.g. for requirement A.1:

![img](./img/blog.png)


<a id="orge750666"></a>

## Communication lines

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Communication lines are not flow lines</td>
</tr>


<tr>
<td class="org-left">Communication means purposeful interaction</td>
</tr>
</tbody>
</table>

![img](./img/comm1.png)

![img](./img/comm2.png)


<a id="org3d4638c"></a>

## System boundaries

![img](./img/boundary.png)


<a id="orga89de1b"></a>

## Descriptions

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Use cases are too simple to be self-explanatory</td>
</tr>


<tr>
<td class="org-left">A use case should be accompanied by description</td>
</tr>


<tr>
<td class="org-left">Writing/understanding the description requires domain knowledge</td>
</tr>
</tbody>
</table>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">DESCRIPTION DETAIL</th>
<th scope="col" class="org-left">EXAMPLE</th>
<th scope="col" class="org-left">MEANING</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Related requirements</td>
<td class="org-left">Requirement A.1</td>
<td class="org-left">Which requirements this use case fulfils</td>
</tr>


<tr>
<td class="org-left">Goal in context</td>
<td class="org-left">New or existing author requests a new blog account from the <code>Administrator</code></td>
<td class="org-left">The use case's place within the system and why this use case is important</td>
</tr>


<tr>
<td class="org-left">Preconditions</td>
<td class="org-left">Author needs to have appropriate proof of identity</td>
<td class="org-left">What needs to happen before the use case can be executed</td>
</tr>


<tr>
<td class="org-left">Successful end condition</td>
<td class="org-left">A new blog account is created for the author</td>
<td class="org-left">What the system's condition should be if the use case executes successfully</td>
</tr>


<tr>
<td class="org-left">Failed end condition</td>
<td class="org-left">The application for a new blog account is rejected</td>
<td class="org-left">What the system's condition should be if the use case fails to execute successfully</td>
</tr>


<tr>
<td class="org-left">Primary actors</td>
<td class="org-left"><code>Administrator</code></td>
<td class="org-left">The main actors that participate in the use case (and triggering or benefiting actors)</td>
</tr>


<tr>
<td class="org-left">Secondary actors</td>
<td class="org-left">Author Credentials Database</td>
<td class="org-left">Actors that participate but are not the main players in a use case's execution</td>
</tr>


<tr>
<td class="org-left">Trigger</td>
<td class="org-left"><code>Administrator</code> asks CMS to <code>create a new blog account</code></td>
<td class="org-left">The event triggered by an actor that causes the use case to execute</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Main flow</td>
<td class="org-left">1. Admin asks CMS to create new account</td>
<td class="org-left">The place to describe each of the important steps in a use case's normal execution</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">2. Admin selects an account type</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">3. Admin enters author's details</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">4. Author's details are verified using the Author Credentials Database</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">5. The new blog account is created</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">6. A summary of the new blog account's details are emailed to the author</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Extensions</td>
<td class="org-left">4.1 Author Credentials Database does not verify the author's details</td>
<td class="org-left">A description of any alternative steps from the ones described in the <code>main flow</code></td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">4.2 The author's new blog account application is rejected</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>

Improved use case diagram after reviewing the description:

![img](./img/boundary2.png)


<a id="orgb3f8215"></a>

## Reusing use cases with `<<include>>`

What if we add another similar requirement Requirement A.2:

> The content management system shall allow an **administrator** to
> create a **new personal wiki**, provided the personal details of
> the applying **author** are verified using the **Author Credentials
> Database**.

The requirement is easily added as a new use case:

![img](./img/include.png)

To indicate that the step `check identity` can be reused (without
changes to the code) it is added as a separate use case with an
`<<include>>` relationship. The `administrator` has no part in
this.

![img](./img/include1.png)

All use case descriptions need to be updated to include a
`Included cases` category, and the `main flow` must contain
`include::Check Identity`:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Main flow</td>
<td class="org-left">&#x2026;</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">4. The author's details are checked</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left"><b>include::Check Identity</b></td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#x2026;</td>
</tr>
</tbody>
</table>

The use case itself get its own description:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">DESCRIPTION DETAIL</th>
<th scope="col" class="org-left">DESCRIPTION</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Related requirements</td>
<td class="org-left">Requirement A.1, Requirement A.2</td>
</tr>


<tr>
<td class="org-left">Goal in context</td>
<td class="org-left">An author's details need to be checked and verified as accurate</td>
</tr>


<tr>
<td class="org-left">Preconditions</td>
<td class="org-left">The author being checked has appopriate proof of identity</td>
</tr>


<tr>
<td class="org-left">Successful end condition</td>
<td class="org-left">The details are verified</td>
</tr>


<tr>
<td class="org-left">Failed end condition</td>
<td class="org-left">The details are not verified</td>
</tr>


<tr>
<td class="org-left">Primary actors</td>
<td class="org-left">Authors Credentials Database</td>
</tr>


<tr>
<td class="org-left">Trigger</td>
<td class="org-left">Author's credentials are provided to the system for verification</td>
</tr>


<tr>
<td class="org-left">Main flow</td>
<td class="org-left">1. The details are provided to the system</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">2. The Author Credentials Database verifies the details</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">3. Details are returned as verified by the Author Credentials Database</td>
</tr>


<tr>
<td class="org-left">Extensions</td>
<td class="org-left">4.1 AUthor Credentials Database does not verify the author's details</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">4.2 The author's new blog account application is rejected</td>
</tr>
</tbody>
</table>

The main flow can be shown as an activity diagram:

![img](./img/check_identity.png)


<a id="org5fb7ed2"></a>

## Special cases

If there are different blog account types (e.g. with different
rights), the use cases will differ little. Different types can be
implemented as special cases, with the original use case as their
generalization:

![img](./img/general.png)

The description gets a `Base Use Case` field:


<a id="org61c454e"></a>

## Optional reuse with `<<extend>>`


<a id="org5b8ca76"></a>

## Process optimization with use cases

Remember "process optimization" in the context of process modeling?
It also applies to requirements analysis with use case diagrams.

As-is diagram:

![img](./img/asis.png)

To-be diagram:

![img](./img/tobe.png)

(Source: [Monteleone, 2021](#orgc119d46)).


<a id="orgb21e72c"></a>

## TODO Overview diagrams

![img](./img/underconstruction.gif)


<a id="orge1c6d92"></a>

## Use case practice

![img](./img/standards.png)

([Image: xkcd](https://xkcd.com/927)).

-   Find mistakes in a use case diagram
-   Create a use case from simple requirements
-   Create a use case for the term project
-   Transfer a EPC/BPMN into an UML use case diagram
-   "Hello World" as UML ([Akehurst, 2014](#orgfbee3e3))


<a id="orgbd2036d"></a>

### Find mistakes in a use case diagram

To solve these problems, return to the rules for actors, systems
and use cases.

-   Simple diagrams (actors, systems, use cases)

    -   Problem: Is this a system?
    
        ![img](./img/error5.png)
        
        ![img](./img/error6.png)
    
    -   Solution
    
        -   "Global Climate": no, because the system's boundaries are not
            well-defined.
        
        ![img](./img/error1.png)
        
        ![img](./img/error2.png)
        
        ![img](./img/error3.png)
        
        ![img](./img/error4.png)

-   TODO Diagrams with relationships


<a id="org9464a7c"></a>

### Create a use case from simple requirements

1.  Fire up Signavio Process Manager
2.  Go to your personal folder in `Shared Documents`
3.  Create a new `UML use case diagram`
4.  Sketch a use case description
    
    > A user logs into a computer.


<a id="org1fed644"></a>

### Create a use case for the term project


<a id="org2f2b713"></a>

### Transfer a EPC/BPMN into an UML use case diagram


<a id="org3de70e3"></a>

### "Hello world" as use case diagram

-   Problem

    -   Turn the C program below into UML
    -   Consider more than one
    
        #include <stdio.h>
        
        int main (void)
        {
          printf("Hello, world!\n");
          return 0;
        }

-   Further reading

    -   It doesn't have to be this complicated: [Akehurst, 2014](#orgfbee3e3)
    -   UML for the C programming language:
        
        > "Unified Modeling Language (UML) has been highly successful in
        > the modeling of software-intensive systems, including
        > systems-oriented models and realtime and embedded designs. The
        > most common implementation for these models has been C++, with
        > the C language in second place. On one hand, this is surprising
        > because the most common implementation language for realtime and
        > embedded systems overall by far is the language C. On the other
        > hand, UML is used almost exclusively for object-oriented systems
        > development, and most realtime and embedded designs are
        > functionally oriented."  ([Douglass, 2009](#org71055d4))


<a id="orgabab24c"></a>

# References

<a id="org803322f"></a> Miles/Hamilton: Learning UML 2.0. O'Reilly (2006). ISBN:

1.  URL: [URL: oreilly.com.](https://www.oreilly.com/library/view/learning-uml-20/0596009828/)

<a id="org4a42d72"></a> Graessle/Baumann/Baumann: UML 2.0 in Action - a
Project-based Tutorial. Packt Publishing
(2005). ISBN: 9781904811558. URL: [URL: packtpub.com](https://www.packtpub.com/product/uml-2-0-in-action-a-project-based-tutorial/9781904811558).

<a id="org1d55c8a"></a> Object Management Group: Unified Modeling Language
Specifications [website]. [URL: omg.org.](https://www.omg.org/spec/UML/2.5.1/About-UML/)

<a id="org314d663"></a> freeCodeCamp.org (21 Apr 2021). UML Diagrams Full Course
(Unified Modeling Language) [video]. [URL: youtu.be/WnMQ8HlmeXc.](https://youtu.be/WnMQ8HlmeXc)

<a id="orgb8067c0"></a> Creately.com (10 Sept 2021). UML Diagram Types Guide:
Learn about All Types of UML Diagrams with Examples [blog]. [URL:
creately.com](https://creately.com/blog/diagrams/uml-diagram-types-examples).

<a id="orgfbee3e3"></a> Akehurst (17 Aug 2014). Examples: UML: Simple Hello
World. [URL: dhakehurst.blogspot.com.](http://dhakehurst.blogspot.com/2014/08/examples-uml-hello-world-part-1.html)

<a id="org5d8e973"></a> DW (31 Oct 2020). Berlin's new airport finally opens: A story
of failure and embarrassment [blog]. URL: [URL: www.dw.com.](https://www.dw.com/en/berlins-new-airport-finally-opens-a-story-of-failure-and-embarrassment/a-55446329)

<a id="orgc119d46"></a> Monteleone (2021). Generalization/Specialization Use
Case Diagrams and Scenarios [blog]. URL: [URL: modernanalyst.com.](https://modernanalyst.com/Resources/Articles/tabid/115/ID/5465/Generalization-Specialization-Use-Case-Diagrams-and-Scenarios.aspx)

<a id="org71055d4"></a> Douglass/IBM (2009). UML for the C programming language
[white paper]. URL: [URL: www.techonline.com.](https://www.techonline.com/tech-papers/uml-for-the-c-programming-language/)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> UML 0.9 =
    + Booch Method (Grady Booch)
    + Object Modeling Technique (James Rumbaugh)
    + Object-Oriented Software Engineering (Ivar Jacobsen)
    + Others

<sup><a id="fn.2" href="#fnr.2">2</a></sup> Since 2017: UML 2.5.1 ([OMG](#org1d55c8a))

<sup><a id="fn.3" href="#fnr.3">3</a></sup> While the general UML overview is quite good, the Use Case
diagram explanation is not great and even contains (in the last
diagram) a few mistakes. The Lucidchart video is way better.

<sup><a id="fn.4" href="#fnr.4">4</a></sup> I had to smile at this comment.
![img](./img/youtube.png)
