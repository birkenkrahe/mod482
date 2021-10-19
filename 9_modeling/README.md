
# Table of Contents

-   [What will you learn?](#orgcf76f99)
-   [What's a process?](#orgda4095b)
-   [Process modeling](#org26e915d)
    -   [Shared world view](#orgf00e24b)
        -   [Situation](#orgb1d8c4f)
        -   [Complication & Question](#orgb57cddb)
        -   [Answer](#org0797294)
    -   [Process standardization](#org747366b)
    -   [Process optimization](#org1913197)
-   [EPCs](#org50496d4)
    -   [What are "Event-driven Process Chains"?](#org9eba30c)
    -   [EPC elements](#org80428ea)
        -   [Events and functions](#orga8e5540)
        -   [Operators and tokens](#orgf6143d0)
        -   [Process interfaces](#orgaa46655)
        -   [Organizational units](#orgb029b9d)
    -   [Extended Event-driven Process Chain (eEPC)](#orga1d8e20)
    -   [EPC rules summary](#org2ce4aba)
-   [Practice](#orgff52d23)
    -   [Signavio demo](#orgce5536f)
    -   [Find the mistakes](#orgbdc3aa6)
    -   [Fill in a process model](#org0dd13db)
    -   [Model a whole process](#orgc723a1e)
    -   [Test (October 26)](#orgca46fa5)
-   [References](#org1eeb556)



<a id="orgcf76f99"></a>

# What will you learn?

-   What is a process?
-   What is process modeling\*
-   Example: Event-controlled Process Chains (EPC)
-   Practice in the Signavio Process Editor


<a id="orgda4095b"></a>

# What's a process?

![img](./img/process.png)

-   What are the elements of any process?
-   What's special (if anything) about "business processes"?
-   What's special (if anything) about "IT processes"?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   Does data play any special role?


<a id="org26e915d"></a>

# Process modeling

The three-fold purpose of process modeling:

-   Shared world view (key)
-   Process standardization (means)
-   Process optimization (end)


<a id="orgf00e24b"></a>

## Shared world view


<a id="orgb1d8c4f"></a>

### Situation

![img](./img/hiring.gif)


<a id="orgb57cddb"></a>

### Complication & Question

![img](./img/hr_vs_it.jpg)

**Example: hiring process.**

What does an IT person see and talk about?

What does an HR person see and talk about?

-   IT view

    *Image: computer parts - the IT world-view*
    
    ![img](./img/computer.gif)
    
    *Image source: [EngWorkSheets.com 2020](#org1afcb16)*

-   HR view

    *Image: HR and people operations - HR world-view*
    
    ![img](./img/hr.png)
    
    *Image source: [Sturgess, 2019](#orga0c5b8b)*


<a id="org0797294"></a>

### Answer

![img](./img/hiring.jpg)

New problem: process model is not **standardized**.

*Image source: [CVO-Europe](#org3d176e3)*


<a id="org747366b"></a>

## Process standardization

ARIS = Meta model for process modeling ("model of models")

![img](./img/aris.png)

*Image: Architecture of Information Systems (ARIS) [Software AG
2016](#org0b51cf1)*


<a id="org1913197"></a>

## Process optimization

![img](./img/camunda.png)

*Image: Own image, modified after Camunda, BPM governance cycle,
2019*

PDF: <./img/camunda.pdf>


<a id="org50496d4"></a>

# EPCs


<a id="org9eba30c"></a>

## What are "Event-driven Process Chains"?

> The event-driven Process Chain (EPC) is a flow chart for business
> process modeling introduced by [August-Wilhelm Scheer](https://en.wikipedia.org/wiki/August-Wilhelm_Scheer) in the early
> 1990s. It illustrates the business process workflows. It uses
> graphical symbols to show the control-flow structure of a business
> process as a chain of events and functions. ([Visual Paradigm, 2021](#orgfbe1403))


<a id="org80428ea"></a>

## EPC elements

![img](./img/epc.png)

*Image source: [Dechow et al, 2007](#org6b40c68)*


<a id="orga8e5540"></a>

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

![img](./img/event.png)

Image source: [Software AG](#org0b51cf1)

-   Event and function rules

    -   Every EPC starts and ends with an event
    -   Events and functions alternate


<a id="orgf6143d0"></a>

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

-   Operator rules

    -   Must use operator (only) when flow splits or merges
    -   Token rule: Splitting operator = joining operator
    -   Only the AND operator can split the flow after an event
    
    ![img](./img/loops.png)


<a id="orgaa46655"></a>

### Process interfaces

-   Process interfaces are used to link independent processes
-   Trigger following process or signal preceding process
-   Can only be at the start or at the end of a process diagram

![img](./img/interface.png)


<a id="orgb029b9d"></a>

### Organizational units

-   Organizational units are only connected to functions
-   They are RACI - responsible, accountable, consulted and informed
    
    ![img](./img/raci.png)


<a id="orga1d8e20"></a>

## Extended Event-driven Process Chain (eEPC)

eEPCs integrate the other views of the ARIS house:

-   Roles/organization
-   Products/services
-   Data input/output
    
    ![img](./img/eepc.png)


<a id="org2ce4aba"></a>

## EPC rules summary

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-left" />
</colgroup>
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
</tbody>
</table>

![img](./img/summary.gif)


<a id="orgff52d23"></a>

# Practice

![img](./img/practice.gif)

Tip: [This platform allows you to play around in their online editor.](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#)


<a id="orgce5536f"></a>

## Signavio demo

-   Fire up the Signavio process editor
-   Let's draw some EPC diagrams
-   Create your models in your own folder


<a id="orgbdc3aa6"></a>

## Find the mistakes

Find all mistakes in the EPC diagram!


<a id="org0dd13db"></a>

## Fill in a process model

(Classroom exercise)


<a id="orgc723a1e"></a>

## Model a whole process

(Graded homework)


<a id="orgca46fa5"></a>

## Test (October 26)


<a id="org1eeb556"></a>

# References

<a id="org3d176e3"></a> CVO-Europe (n.d.). Our Hiring Process [website]. [Online:
cvo-europe.com](https://www.cvo-europe.com/en/careers/our-hiring-process).

<a id="org6b40c68"></a> Dechow et al (2007). Interactions between modern
information technology and management control [article]. [Online:
researchgate.net.](https://www.researchgate.net/publication/274260317_Interactions_between_modern_information_technology_and_management_control)

<a id="org1afcb16"></a> EngWorkSheets (2020). Computer Parts ESL Vocabulary Matching
Exercise Worksheet For Kids - PDF Preview [website]. [Online:
engworksheets.com](https://www.engworksheets.com/vocabulary-pdf-preview/Computer-Parts/4/computer-parts-esl-vocabulary-matching-exercise-worksheet-for-kids.html).

<a id="org46f8935"></a> Maya G (Jun 29,2021). ITIL Processes [blog]. [Online:
itil-docs.com.](https://www.itil-docs.com/blogs/itil-concepts/itil-processes-functions)

<a id="org0b51cf1"></a> Software AG University Relations (2016). BPM with ARIS
[presentation]. [Online: ariscommunity.com.](http://cdn.ariscommunity.com/community2/documents/urelation/BPM-ARIS_Part2.pdf)

<a id="orga0c5b8b"></a> Sturgess G (June 20, 2019). What's the Difference
between HR and People Operations? [website]. [Online:
talentalign.com.](https://www.talentalign.com/whats-the-difference-between-hr-and-people-operations/)

<a id="orgfbe1403"></a> Visual Paradigm (2021). What is Event-Driven
Process Chain (EPC)? [Website]. [Online: visual-paradigm.com](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#).

<a id="org1e51bee"></a> Wikipedia (1 Oct 2021). ITIL [website]. [Online:
en.wikipedia.org](https://en.wikipedia.org/wiki/ITIL).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Cp. ITIL library of IT processes, especially with regards
to IT services. More: [Wikipedia](#org1e51bee) (2021).

![img](./img/itil.jpg)
*Image source: ITIL docs, 2021*
