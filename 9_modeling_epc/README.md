
# Table of Contents

-   [What will you learn?](#orgce6072c)
-   [What's a process?](#org9d5ed57)
-   [Process modeling](#org956ecc5)
    -   [Shared world view](#orgc34a2e8)
        -   [Situation](#org4f0915f)
        -   [Complication & Question](#orgd53fcf0)
        -   [Answer](#orgf4eeab0)
    -   [Process standardization](#orgcfaded4)
    -   [Process optimization](#orgbb2d650)
-   [EPCs](#org123e49d)
    -   [What are "Event-driven Process Chains"?](#org2b209a1)
    -   [EPC elements](#org1bdb72c)
        -   [Events and functions](#org8503248)
        -   [Event and function rules](#orgaee93ae)
        -   [Flow](#orgc187a92)
        -   [Operators and tokens](#org1862250)
        -   [Operator rules](#org3b29cc8)
        -   [Process interfaces](#org3533690)
        -   [Organizational units](#org54518ff)
    -   [Extended Event-driven Process Chain (eEPC)](#org6f68c6b)
    -   [EPC rules summary](#orga6598ef)
-   [Practice - EPC Lab](#org4a0dc31)
    -   [Signavio demo](#orgb8a2b24)
    -   [Find the mistakes](#orgf33f356)
        -   [Problem](#orga01f4aa)
        -   [Solution](#orgd958d9b)
    -   [Fill in a process model](#orga0a16f3)
        -   [Problem](#org6a05b1a)
        -   [Solution](#orgb32e24a)
    -   [A puzzling question](#org7b75720)
        -   [Problem](#orge85b0cc)
        -   [Solution](#orgce7340e)
    -   [Model a whole process](#orgd8c67c9)
        -   [Problem](#org6bc511d)
        -   [Solution](#org5e2433a)
    -   [Next: graded test (October 26)](#org970ee11)
    -   [Modify an EPC model](#org3f70bac)
-   [References](#org7f7f2e2)



<a id="orgce6072c"></a>

# What will you learn?

-   What is a process?
-   What is process modeling
-   Example: Event-controlled Process Chains (EPC)
-   Practice in the Signavio Process Editor
-   EPC exercises
    
    ![img](./img/perspective.gif)
    
    *Image: [Eiffel Tower GIF by Tom@Circlelineartschool.com](https://giphy.com/gifs/circlelineartschool-eiffel-tower-drawing-perspective-trees-WCPIabjFw2SY25SSnb)*


<a id="org9d5ed57"></a>

# What's a process?

![img](./img/process.png)

-   What are the elements of any process?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   What's special (if anything) about "business processes"?<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>
-   What's special (if anything) about "IT processes"?<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>
-   Does data play any special role?


<a id="org956ecc5"></a>

# Process modeling

The three-fold purpose of process modeling:

-   Shared world view (key)
-   Process standardization (means)
-   Process optimization (end)


<a id="orgc34a2e8"></a>

## Shared world view


<a id="org4f0915f"></a>

### Situation

![img](./img/hiring.gif)


<a id="orgd53fcf0"></a>

### Complication & Question

![img](./img/hr_vs_it.jpg)

**Example: hiring process.**

What does an IT person see and talk about?

What does an HR person see and talk about?

-   IT view

    *Image: computer parts - the IT world-view*
    
    ![img](./img/computer.gif)
    
    *Image source: [EngWorkSheets.com 2020](#org326b157)*

-   HR view

    *Image: HR and people operations - HR world-view*
    
    ![img](./img/hr.png)
    
    *Image source: [Sturgess, 2019](#orgd1645cb)*


<a id="orgf4eeab0"></a>

### Answer

![img](./img/hiring.jpg)

New problem: process model is not **standardized**.

*Image source: [CVO-Europe](#org2ad0b01)*


<a id="orgcfaded4"></a>

## Process standardization

ARIS = Meta model for process modeling ("model of models")

![img](./img/aris.png)

*Image: Architecture of Information Systems (ARIS) [Software AG
2016](#org113ef65)*


<a id="orgbb2d650"></a>

## Process optimization

![img](./img/camunda.png)

*Image: Own image, modified after Camunda, BPM governance cycle,
2019*

PDF: <https://github.com/birkenkrahe/mod482/blob/main/9_modeling/img/camunda.pdf>


<a id="org123e49d"></a>

# EPCs


<a id="org2b209a1"></a>

## What are "Event-driven Process Chains"?

> The event-driven Process Chain (EPC) is a flow chart for business
> process modeling introduced by [August-Wilhelm Scheer](https://en.wikipedia.org/wiki/August-Wilhelm_Scheer) in the early
> 1990s. It illustrates the business process workflows. It uses
> graphical symbols to show the control-flow structure of a business
> process as a chain of events and functions. ([Visual Paradigm, 2021](#org6705dae))


<a id="org1bdb72c"></a>

## EPC elements

![img](./img/epc.png)

*Image source: [Dechow et al, 2007](#org0c45f16)*


<a id="org8503248"></a>

### Events and functions

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Function</td>
<td class="org-left">Activities carried out by a person</td>
</tr>


<tr>
<td class="org-left">Event</td>
<td class="org-left">Status triggered by a function</td>
</tr>


<tr>
<td class="org-left">Control flow</td>
<td class="org-left">Sequence of activities</td>
</tr>
</tbody>
</table>

![img](./img/event1.png)

Image source: [Software AG](#org113ef65)


<a id="orgaee93ae"></a>

### Event and function rules

-   Every EPC starts and ends with an event
-   Events and functions alternate


<a id="orgc187a92"></a>

### Flow

-   Flow represents the flow of time, and is itself represented by a
    solid arrow with a solid tip.
-   All process elements must be connected by flow (arrows)

![img](./img/flowrules.png)

-   Loops are allowed in principle (but careful: maintain model
    readability)

![img](./img/loops.png)

Unfortunately, this diagram violates a rule and uses the wrong
operator (XOR instead of OR). I've cleaned it up (also avoiding
the loop but retaining all the important information) in the
diagram below:

![img](./img/convert1.png)


<a id="org1862250"></a>

### Operators and tokens

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Operator</th>
<th scope="col" class="org-left">Meaning</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">AND</td>
<td class="org-left">All following flows are executed</td>
</tr>


<tr>
<td class="org-left">OR</td>
<td class="org-left">One or several following flows are executed</td>
</tr>


<tr>
<td class="org-left">XOR (exclusive OR)</td>
<td class="org-left">Only one of the following flows is executed</td>
</tr>
</tbody>
</table>

![img](./img/operator.png)


<a id="org3b29cc8"></a>

### Operator rules

-   Must use operator (only) when flow splits or merges
-   Token rule: Splitting operator = joining operator
-   Only the AND operator can split the flow after an event

![img](./img/operators.png)


<a id="org3533690"></a>

### Process interfaces

-   Process interfaces are used to link independent processes
-   Trigger following process or signal preceding process
-   Can only be at the start or at the end of a process diagram

![img](./img/interface.png)


<a id="org54518ff"></a>

### Organizational units

-   Organizational units are only connected to functions
-   They are RACI - Responsible, Accountable, Consulted and Informed
    
    ![img](./img/raci.png)


<a id="org6f68c6b"></a>

## Extended Event-driven Process Chain (eEPC)

eEPCs integrate the other views of the ARIS house:

-   Roles/organization
-   Products/services
-   Data input/output
    
    ![img](./img/eepc.png)


<a id="orga6598ef"></a>

## EPC rules summary

![img](./img/summary.gif)

This is the complete lists of rules and recommendations. Despite
the apparent simplicity of this modeling language, it is incredibly
expressive - so much so that for example all of the 80,000 basic
transaction of an SAP Enterprise Resource Planning system are
modeled using EPCs.<sup><a id="fnr.4" class="footref" href="#fn.4">4</a></sup>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">&#xa0;</th>
<th scope="col" class="org-left">Rule</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">1</td>
<td class="org-left">Every EPC starts and ends with an event</td>
</tr>


<tr>
<td class="org-right">2</td>
<td class="org-left">Events and functions alternate</td>
</tr>


<tr>
<td class="org-right">3</td>
<td class="org-left">Must use operator (only) when flow splits or merges</td>
</tr>


<tr>
<td class="org-right">4</td>
<td class="org-left">Splitting operator = joining operator</td>
</tr>


<tr>
<td class="org-right">5</td>
<td class="org-left">Only the AND operator can split the flow after an event</td>
</tr>


<tr>
<td class="org-right">6</td>
<td class="org-left">Interfaces only before or after a process</td>
</tr>


<tr>
<td class="org-right">7</td>
<td class="org-left">Organizational units are only connected to functions</td>
</tr>


<tr>
<td class="org-right">8</td>
<td class="org-left">All process elements must be connected by flow</td>
</tr>


<tr>
<td class="org-right">9</td>
<td class="org-left">Loops are allowed as long as they're finite</td>
</tr>


<tr>
<td class="org-right">10</td>
<td class="org-left">Trivial events can be omitted</td>
</tr>
</tbody>
</table>

Here is a complete EPC "cheat sheet" (Source: Software AG)

![img](./img/cheatsheet.png)


<a id="org4a0dc31"></a>

# Practice - EPC Lab

![img](./img/practice.gif)

Tip: [This platform allows you to play around in their online editor.](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#)


<a id="orgb8a2b24"></a>

## Signavio demo

![img](./img/signavio.png)

-   Fire up the [Signavio process editor](https://academic.signavio.com)
-   Let's draw some EPC diagrams
-   Create your models in your own folder


<a id="orgf33f356"></a>

## Find the mistakes


<a id="orga01f4aa"></a>

### Problem

-   Find all mistakes in the EPC diagram!
-   Do not fix mistakes as you go along
-   There are 11 mistakes in total
    
    ![img](./img/diagram.png)


<a id="orgd958d9b"></a>

### Solution

One could count the operator between Event 6 and 7 as a 12th
mistake - it's a double mistake: the operator shouldn't be here
and there ought to be a function instead.

![img](./img/diagram_solution.png)


<a id="orga0a16f3"></a>

## Fill in a process model


<a id="org6a05b1a"></a>

### Problem

The following process ("Invoice Check") has already been modeled
for you.

> "The invoice is checked by accounts payable when 1) the receipt
> for incoming goods, 2) the invoice, and 3) the sales order, have
> all been received. If the invoice is correct, it will be paid. If
> it is not correct, an inquiry process is triggered. The process is
> linked to four process interfaces: incoming -(1) incoming goods,
> (2) sales, and - outgoing - (3) payment, (4) inquiry."

1.  Draw the diagram in Signavio (in your folder)
2.  Read the process description carefully
3.  Name all elements including the operators
4.  Name and save your diagram
    
    ![img](./img/invoice_problem.png)

*The diagram contains rule violations. Why?*


<a id="orgb32e24a"></a>

### Solution

Things to consider:

-   Stick as close to the problem description as you can - don't
    make stuff up, change words or "improve" the process unless
    requested.
-   Don't change the standard size of process elements. If an event
    or a function don't seem to fit in the element, it is likely
    that you need to rethink your model (e.g. the activity may be
    too large and needs to be split up).
    
    ![img](./img/invoice_solution.png)


<a id="org7b75720"></a>

## A puzzling question

![img](./img/puzzle.gif)


<a id="orge85b0cc"></a>

### Problem

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Can all processes be modeled with languages like EPCs?</td>
</tr>
</tbody>
</table>


<a id="orgce7340e"></a>

### Solution

Yes and no&#x2026;it depends on the ability to measure what's going
on. Process models - at least in the area of business and
technology - can only express things or actions that are
quantifiable.


<a id="orgd8c67c9"></a>

## Model a whole process


<a id="org6bc511d"></a>

### Problem

Consider the following process description<sup><a id="fnr.5" class="footref" href="#fn.5">5</a></sup>:

> "When programming in a compiled language (like C), you have to
> create a source code file using an editor. (This can be quite
> tricky if you use Emacs and haven't used it much before.) The
> compiler compiles the file and links it to a library. Finally you
> run the program.

-   Consider first what type of process this is
-   Model this process as an EPC in Signavio
-   Name the process "Compilation"
-   Save it in your personal folder
-   EPC models are usually drawn vertically


<a id="org5e2433a"></a>

### Solution

This is a sample solution. Process modeling is not an exact
science, and there is always more than one answer.

-   Simple solution - happy path

    ![img](./img/compilation.png)

-   Complete solution - extended EPC


<a id="org970ee11"></a>

## Next: graded test (October 26)

*Image: stats from classroom test 5 on October 19*

![img](../img/test5.png)

-   Process elements
-   Process modeling
-   Event-driven Process Chains
-   Multiple choice and (mostly) open questions


<a id="org3f70bac"></a>

## Modify an EPC model

-   **Open** the diagram `Compilation (Copy) in the folder ~?Shared
         documents?LYON_DSC_482.02?Marcus_Birkenkrahe` ([direct link](https://academic.signavio.com/p/editor?id=6e495dda2041412e8841a261d0a376c6)).
-   **Copy** the diagram to your personal folder in the `Shared
         documents` folder.
-   In your folder, **modify** the diagram to accommodate the following
    changed description:

> "When programming in a compiled language (like C), you have to
> create a source code file using an editor. The compiler compiles
> the file and links it to a library. Finally you run the program.
> 
> If the program does not run, you need to fix bugs in the source
> file, before going through the compilation process again.

-   **Save** your solution to your personal folder.
-   In the folder explorer view, **share** your solution with me by
    choosing `Share?Invite anyone for feedback`, entering my Lyon
    email address `birkenkrahe@lyon.edu`. Check `"Send a copy to me"`
    to make sure that the invitation was sent (see image below).
    
    ![img](./img/share.png)


<a id="org7f7f2e2"></a>

# References

<a id="org2ad0b01"></a> CVO-Europe (n.d.). Our Hiring Process [website]. [Online:
cvo-europe.com](https://www.cvo-europe.com/en/careers/our-hiring-process).

<a id="org0c45f16"></a> Dechow et al (2007). Interactions between modern
information technology and management control [article]. [Online:
researchgate.net.](https://www.researchgate.net/publication/274260317_Interactions_between_modern_information_technology_and_management_control)

<a id="org326b157"></a> EngWorkSheets (2020). Computer Parts ESL Vocabulary Matching
Exercise Worksheet For Kids - PDF Preview [website]. [Online:
engworksheets.com](https://www.engworksheets.com/vocabulary-pdf-preview/Computer-Parts/4/computer-parts-esl-vocabulary-matching-exercise-worksheet-for-kids.html).

<a id="orgb4ad640"></a> Gookin D (2021). [Tiny C Projects. Manning](https://www.manning.com/books/tiny-c-projects).

<a id="org82eb948"></a> Maya G (Jun 29,2021). ITIL Processes [blog]. [Online:
itil-docs.com.](https://www.itil-docs.com/blogs/itil-concepts/itil-processes-functions)

<a id="org44ac016"></a> SAP (n.d.). What is ERP? [website]. [Online:
insights.sap.com.](https://insights.sap.com/what-is-erp/?sred=glo-products-whatiserp)

<a id="org113ef65"></a> Software AG University Relations (2016). BPM with ARIS
[presentation]. [Online: ariscommunity.com.](http://cdn.ariscommunity.com/community2/documents/urelation/BPM-ARIS_Part2.pdf)

<a id="orgd1645cb"></a> Sturgess G (June 20, 2019). What's the Difference
between HR and People Operations? [website]. [Online:
talentalign.com.](https://www.talentalign.com/whats-the-difference-between-hr-and-people-operations/)

<a id="org6705dae"></a> Visual Paradigm (2021). What is Event-Driven
Process Chain (EPC)? [Website]. [Online: visual-paradigm.com](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#).

<a id="org4cb0812"></a> Wikipedia (1 Oct 2021). ITIL [website]. [Online:
en.wikipedia.org](https://en.wikipedia.org/wiki/ITIL).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Different languages use different terms:(1)
\*Functions\*/tasks/actions/activities; (2) \*events\*/status/trigger; (3)
\*flow\*/path/sequence/connectors; (4) \*operators\*/gateways/decisions.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> Business processes generate added value.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> Cp. ITIL library of IT processes, especially with regards
to IT services. More: [Wikipedia](#org4cb0812) (2021).

![img](./img/itil.jpg)
*Image source: ITIL docs, 2021*

<sup><a id="fn.4" href="#fnr.4">4</a></sup> Any productive ERP system contains many more transactions than
that. In practice, these are often modeled as BPMN diagrams, or as ER
Diagrams, if customer-facing or database operations are being
modeled. For more about ERP systems, see this tutorial ([SAP](#org44ac016)).

<sup><a id="fn.5" href="#fnr.5">5</a></sup> The idea for this problem came from a figure in a book I'm
reading, "Tiny C Projects" ([Gookin, 2021](#orgb4ad640)):

![img](./img/cycle.png)
