
# Table of Contents

-   [What will you learn?](#org594c965)
-   [What's a process?](#org1f0f3aa)
-   [Process modeling](#org50915ec)
    -   [Shared world view](#orga143abf)
        -   [Situation](#orga8dd968)
        -   [Complication & Question](#orgc62ce89)
        -   [Answer](#org0fd012c)
    -   [Process standardization](#org8ea6fb9)
    -   [Process optimization](#orgf899252)
-   [EPCs](#org04d00c8)
    -   [What are "Event-driven Process Chains"?](#orgcdd2e9d)
    -   [EPC elements](#orgd65bbb8)
        -   [Events and functions](#org0218013)
        -   [Operators and tokens](#org0b2fc79)
        -   [Process interfaces](#org3f75344)
        -   [Organizational units](#orgd5b6e06)
    -   [Extended Event-driven Process Chain (eEPC)](#orge967e19)
    -   [EPC rules summary](#orgfd236ed)
-   [Practice](#orgf5d914d)
    -   [Signavio demo](#org955d0b9)
    -   [Find the mistakes](#org5e7ebfb)
    -   [Fill in a process model](#org518b83f)
    -   [Model a whole process](#orge865a0e)
    -   [Test (October 26)](#org940b5af)
-   [References](#org874ac6e)



<a id="org594c965"></a>

# What will you learn?

-   What is a process?
-   What is process modeling\*
-   Example: Event-controlled Process Chains (EPC)
-   Practice in the Signavio Process Editor
    
    ![img](./img/pm.png)


<a id="org1f0f3aa"></a>

# What's a process?

![img](./img/process.png)

-   What are the elements of any process?
-   What's special (if anything) about "business processes"?
-   What's special (if anything) about "IT processes"?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   Does data play any special role?


<a id="org50915ec"></a>

# Process modeling

The three-fold purpose of process modeling:

-   Shared world view (key)
-   Process standardization (means)
-   Process optimization (end)


<a id="orga143abf"></a>

## Shared world view


<a id="orga8dd968"></a>

### Situation

![img](./img/hiring.gif)


<a id="orgc62ce89"></a>

### Complication & Question

![img](./img/hr_vs_it.jpg)

**Example: hiring process.**

What does an IT person see and talk about?

What does an HR person see and talk about?

-   IT view

    *Image: computer parts - the IT world-view*
    
    ![img](./img/computer.gif)
    
    *Image source: [EngWorkSheets.com 2020](#orgc06f08b)*

-   HR view

    *Image: HR and people operations - HR world-view*
    
    ![img](./img/hr.png)
    
    *Image source: [Sturgess, 2019](#org6ee9f4a)*


<a id="org0fd012c"></a>

### Answer

![img](./img/hiring.jpg)

New problem: process model is not **standardized**.

*Image source: [CVO-Europe](#org6a7757e)*


<a id="org8ea6fb9"></a>

## Process standardization

ARIS = Meta model for process modeling ("model of models")

![img](./img/aris.png)

*Image: Architecture of Information Systems (ARIS) [Software AG
2016](#org1b4892b)*


<a id="orgf899252"></a>

## Process optimization

![img](./img/camunda.png)

*Image: Own image, modified after Camunda, BPM governance cycle,
2019*

PDF: <https://github.com/birkenkrahe/mod482/blob/main/9_modeling/img/camunda.pdf>


<a id="org04d00c8"></a>

# EPCs


<a id="orgcdd2e9d"></a>

## What are "Event-driven Process Chains"?

> The event-driven Process Chain (EPC) is a flow chart for business
> process modeling introduced by [August-Wilhelm Scheer](https://en.wikipedia.org/wiki/August-Wilhelm_Scheer) in the early
> 1990s. It illustrates the business process workflows. It uses
> graphical symbols to show the control-flow structure of a business
> process as a chain of events and functions. ([Visual Paradigm, 2021](#orgc4917b9))


<a id="orgd65bbb8"></a>

## EPC elements

![img](./img/epc.png)

*Image source: [Dechow et al, 2007](#orgf76313c)*


<a id="org0218013"></a>

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

Image source: [Software AG](#org1b4892b)

-   Event and function rules

    -   Every EPC starts and ends with an event
    -   Events and functions alternate


<a id="org0b2fc79"></a>

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


<a id="org3f75344"></a>

### Process interfaces

-   Process interfaces are used to link independent processes
-   Trigger following process or signal preceding process
-   Can only be at the start or at the end of a process diagram

![img](./img/interface.png)


<a id="orgd5b6e06"></a>

### Organizational units

-   Organizational units are only connected to functions
-   They are RACI - responsible, accountable, consulted and informed
    
    ![img](./img/raci.png)


<a id="orge967e19"></a>

## Extended Event-driven Process Chain (eEPC)

eEPCs integrate the other views of the ARIS house:

-   Roles/organization
-   Products/services
-   Data input/output
    
    ![img](./img/eepc.png)


<a id="orgfd236ed"></a>

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


<a id="orgf5d914d"></a>

# Practice

![img](./img/practice.gif)

Tip: [This platform allows you to play around in their online editor.](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#)


<a id="org955d0b9"></a>

## Signavio demo

-   Fire up the Signavio process editor
-   Let's draw some EPC diagrams
-   Create your models in your own folder


<a id="org5e7ebfb"></a>

## Find the mistakes

Find all mistakes in the EPC diagram!


<a id="org518b83f"></a>

## Fill in a process model

(Classroom exercise)


<a id="orge865a0e"></a>

## Model a whole process

(Graded homework)


<a id="org940b5af"></a>

## Test (October 26)


<a id="org874ac6e"></a>

# References

<a id="org6a7757e"></a> CVO-Europe (n.d.). Our Hiring Process [website]. [Online:
cvo-europe.com](https://www.cvo-europe.com/en/careers/our-hiring-process).

<a id="orgf76313c"></a> Dechow et al (2007). Interactions between modern
information technology and management control [article]. [Online:
researchgate.net.](https://www.researchgate.net/publication/274260317_Interactions_between_modern_information_technology_and_management_control)

<a id="orgc06f08b"></a> EngWorkSheets (2020). Computer Parts ESL Vocabulary Matching
Exercise Worksheet For Kids - PDF Preview [website]. [Online:
engworksheets.com](https://www.engworksheets.com/vocabulary-pdf-preview/Computer-Parts/4/computer-parts-esl-vocabulary-matching-exercise-worksheet-for-kids.html).

<a id="org0404e8f"></a> Maya G (Jun 29,2021). ITIL Processes [blog]. [Online:
itil-docs.com.](https://www.itil-docs.com/blogs/itil-concepts/itil-processes-functions)

<a id="org1b4892b"></a> Software AG University Relations (2016). BPM with ARIS
[presentation]. [Online: ariscommunity.com.](http://cdn.ariscommunity.com/community2/documents/urelation/BPM-ARIS_Part2.pdf)

<a id="org6ee9f4a"></a> Sturgess G (June 20, 2019). What's the Difference
between HR and People Operations? [website]. [Online:
talentalign.com.](https://www.talentalign.com/whats-the-difference-between-hr-and-people-operations/)

<a id="orgc4917b9"></a> Visual Paradigm (2021). What is Event-Driven
Process Chain (EPC)? [Website]. [Online: visual-paradigm.com](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#).

<a id="org4c5e122"></a> Wikipedia (1 Oct 2021). ITIL [website]. [Online:
en.wikipedia.org](https://en.wikipedia.org/wiki/ITIL).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Cp. ITIL library of IT processes, especially with regards
to IT services. More: [Wikipedia](#org4c5e122) (2021).

![img](./img/itil.jpg)
*Image source: ITIL docs, 2021*
