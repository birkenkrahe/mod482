
# Table of Contents

-   [What will you learn?](#org131e5be)
-   [What's a process?](#org942cba3)
-   [Process modeling](#orgc5fb317)
    -   [Shared world view](#org602fb36)
        -   [Situation](#orga18a9d0)
        -   [Complication & Question](#orga2b512e)
        -   [Answer](#org6534ecc)
    -   [Process standardization](#org9c14f5b)
    -   [Process optimization](#orgbdd1a76)
-   [EPCs](#org2e2584a)
    -   [What are "Event-driven Process Chains"?](#orgd80b64b)
    -   [EPC elements](#orgedd06b1)
        -   [Events and functions](#org03e90d1)
        -   [Event and function rules](#org491e3e1)
        -   [Flow](#orgcf4706b)
        -   [Operators and tokens](#orgbbcc1c1)
        -   [Operator rules](#org06dfc1e)
        -   [Process interfaces](#orgabb385d)
        -   [Organizational units](#org83788b6)
    -   [Extended Event-driven Process Chain (eEPC)](#orgaf9d647)
    -   [EPC rules summary](#orgbafe70b)
-   [Practice - EPC Lab](#orga637a34)
    -   [Signavio demo](#orgd6975b3)
    -   [Find the mistakes](#org6634b64)
    -   [Fill in a process model](#org8c29c48)
    -   [A puzzling question](#org0850f3c)
    -   [Model a whole process](#org4c326ca)
    -   [Graded test (October 26)](#orgff650ed)
-   [References](#orgd9fd8e3)



<a id="org131e5be"></a>

# What will you learn?

-   What is a process?
-   What is process modeling\*
-   Example: Event-controlled Process Chains (EPC)
-   Practice in the Signavio Process Editor
    
    ![img](./img/pm.png)


<a id="org942cba3"></a>

# What's a process?

![img](./img/process.png)

-   What are the elements of any process?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   What's special (if anything) about "business processes"?<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>
-   What's special (if anything) about "IT processes"?<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>
-   Does data play any special role?


<a id="orgc5fb317"></a>

# Process modeling

The three-fold purpose of process modeling:

-   Shared world view (key)
-   Process standardization (means)
-   Process optimization (end)


<a id="org602fb36"></a>

## Shared world view


<a id="orga18a9d0"></a>

### Situation

![img](./img/hiring.gif)


<a id="orga2b512e"></a>

### Complication & Question

![img](./img/hr_vs_it.jpg)

**Example: hiring process.**

What does an IT person see and talk about?

What does an HR person see and talk about?

-   IT view

    *Image: computer parts - the IT world-view*
    
    ![img](./img/computer.gif)
    
    *Image source: [EngWorkSheets.com 2020](#org381105f)*

-   HR view

    *Image: HR and people operations - HR world-view*
    
    ![img](./img/hr.png)
    
    *Image source: [Sturgess, 2019](#org8f2d0a8)*


<a id="org6534ecc"></a>

### Answer

![img](./img/hiring.jpg)

New problem: process model is not **standardized**.

*Image source: [CVO-Europe](#orgc3a736f)*


<a id="org9c14f5b"></a>

## Process standardization

ARIS = Meta model for process modeling ("model of models")

![img](./img/aris.png)

*Image: Architecture of Information Systems (ARIS) [Software AG
2016](#org3e5941e)*


<a id="orgbdd1a76"></a>

## Process optimization

![img](./img/camunda.png)

*Image: Own image, modified after Camunda, BPM governance cycle,
2019*

PDF: <https://github.com/birkenkrahe/mod482/blob/main/9_modeling/img/camunda.pdf>


<a id="org2e2584a"></a>

# EPCs


<a id="orgd80b64b"></a>

## What are "Event-driven Process Chains"?

> The event-driven Process Chain (EPC) is a flow chart for business
> process modeling introduced by [August-Wilhelm Scheer](https://en.wikipedia.org/wiki/August-Wilhelm_Scheer) in the early
> 1990s. It illustrates the business process workflows. It uses
> graphical symbols to show the control-flow structure of a business
> process as a chain of events and functions. ([Visual Paradigm, 2021](#org82085a5))


<a id="orgedd06b1"></a>

## EPC elements

![img](./img/epc.png)

*Image source: [Dechow et al, 2007](#org651bf37)*


<a id="org03e90d1"></a>

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

Image source: [Software AG](#org3e5941e)


<a id="org491e3e1"></a>

### Event and function rules

-   Every EPC starts and ends with an event
-   Events and functions alternate


<a id="orgcf4706b"></a>

### Flow

-   Flow represents the flow of time, and is itself represented by a
    solid arrow with a solid tip.
-   All process elements must be connected by flow (arrows)

![img](./img/flowrules.png)

-   Loops are allowed (but careful: maintain model readability)

![img](./img/loops.png)


<a id="orgbbcc1c1"></a>

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


<a id="org06dfc1e"></a>

### Operator rules

-   Must use operator (only) when flow splits or merges
-   Token rule: Splitting operator = joining operator
-   Only the AND operator can split the flow after an event

![img](./img/operators.png)


<a id="orgabb385d"></a>

### Process interfaces

-   Process interfaces are used to link independent processes
-   Trigger following process or signal preceding process
-   Can only be at the start or at the end of a process diagram

![img](./img/interface.png)


<a id="org83788b6"></a>

### Organizational units

-   Organizational units are only connected to functions
-   They are RACI - Responsible, Accountable, Consulted and Informed
    
    ![img](./img/raci.png)


<a id="orgaf9d647"></a>

## Extended Event-driven Process Chain (eEPC)

eEPCs integrate the other views of the ARIS house:

-   Roles/organization
-   Products/services
-   Data input/output
    
    ![img](./img/eepc.png)


<a id="orgbafe70b"></a>

## EPC rules summary

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

![img](./img/summary.gif)

Here is a complete EPC "cheat sheet" (Source: Software AG)

![img](./img/cheatsheet.png)


<a id="orga637a34"></a>

# Practice - EPC Lab

![img](./img/practice.gif)

Tip: [This platform allows you to play around in their online editor.](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#)


<a id="orgd6975b3"></a>

## Signavio demo

![img](./img/signavio.png)

-   Fire up the [Signavio process editor](https://academic.signavio.com)
-   Let's draw some EPC diagrams
-   Create your models in your own folder


<a id="org6634b64"></a>

## Find the mistakes

-   Find all mistakes in the EPC diagram!
-   Do not fix mistakes as you go along
-   There are 11 mistakes in total
    
    ![img](./img/diagram.png)


<a id="org8c29c48"></a>

## Fill in a process model

The following process ("Invoice Check") has already been modeled
for you.

> "The invoice is checked by accounts payable when 1) the receipt for
> incoming goods, 2) the invoice, and 3) the sales order, have all
> been received. If the invoice is correct, it will be paid. If it is
> not correct, an inquiry process is triggered. The process is linked
> to four process interfaces: incoming -(1) incoming goods, (2)
> sales, and outgoing - (3) payment, (4) inquiry."

1.  Draw the diagram in Signavio (in your folder)
2.  Read the process description carefully
3.  Name all elements including the operators
4.  Name and save your diagram
    
    ![img](./img/invoice_problem.png)

*The diagram contains rule violations. Why?*


<a id="org0850f3c"></a>

## A puzzling question

![img](./img/puzzle.gif)

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


<a id="org4c326ca"></a>

## Model a whole process

Consider the following process description:

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


<a id="orgff650ed"></a>

## Graded test (October 26)

-   Process elements
-   Process modeling
-   Event-driven Process Chains
-   Multiple choice and open questions


<a id="orgd9fd8e3"></a>

# References

<a id="orgc3a736f"></a> CVO-Europe (n.d.). Our Hiring Process [website]. [Online:
cvo-europe.com](https://www.cvo-europe.com/en/careers/our-hiring-process).

<a id="org651bf37"></a> Dechow et al (2007). Interactions between modern
information technology and management control [article]. [Online:
researchgate.net.](https://www.researchgate.net/publication/274260317_Interactions_between_modern_information_technology_and_management_control)

<a id="org381105f"></a> EngWorkSheets (2020). Computer Parts ESL Vocabulary Matching
Exercise Worksheet For Kids - PDF Preview [website]. [Online:
engworksheets.com](https://www.engworksheets.com/vocabulary-pdf-preview/Computer-Parts/4/computer-parts-esl-vocabulary-matching-exercise-worksheet-for-kids.html).

<a id="org137e2ab"></a> Maya G (Jun 29,2021). ITIL Processes [blog]. [Online:
itil-docs.com.](https://www.itil-docs.com/blogs/itil-concepts/itil-processes-functions)

<a id="orgde61abb"></a> SAP (n.d.). What is ERP? [website]. [Online:
insights.sap.com.](https://insights.sap.com/what-is-erp/?sred=glo-products-whatiserp)

<a id="org3e5941e"></a> Software AG University Relations (2016). BPM with ARIS
[presentation]. [Online: ariscommunity.com.](http://cdn.ariscommunity.com/community2/documents/urelation/BPM-ARIS_Part2.pdf)

<a id="org8f2d0a8"></a> Sturgess G (June 20, 2019). What's the Difference
between HR and People Operations? [website]. [Online:
talentalign.com.](https://www.talentalign.com/whats-the-difference-between-hr-and-people-operations/)

<a id="org82085a5"></a> Visual Paradigm (2021). What is Event-Driven
Process Chain (EPC)? [Website]. [Online: visual-paradigm.com](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#).

<a id="orgcce08d5"></a> Wikipedia (1 Oct 2021). ITIL [website]. [Online:
en.wikipedia.org](https://en.wikipedia.org/wiki/ITIL).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Different languages use different terms:(1)
\*Functions\*/tasks/actions/activities; (2) \*events\*/status/trigger; (3)
\*flow\*/path/sequence/connectors; (4) \*operators\*/gateways/decisions.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> Business processes generate added value.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> Cp. ITIL library of IT processes, especially with regards
to IT services. More: [Wikipedia](#orgcce08d5) (2021).

![img](./img/itil.jpg)
*Image source: ITIL docs, 2021*

<sup><a id="fn.4" href="#fnr.4">4</a></sup> Any productive ERP system contains many more transactions than
that. In practice, these are often modeled as BPMN diagrams, or as ER
Diagrams, if customer-facing or database operations are being
modeled. For more about ERP systems, see this tutorial ([SAP](#orgde61abb)).
