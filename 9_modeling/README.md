
# Table of Contents

-   [What will you learn?](#org62d71c8)
-   [What's a process?](#org8a36a89)
-   [Process modeling](#orge0038aa)
    -   [Shared world view](#orgdd96af7)
        -   [Situation](#org45e3dc1)
        -   [Complication & Question](#org76ed456)
        -   [Answer](#orgbf4f97e)
    -   [Process standardization](#org5642d8e)
    -   [Process optimization](#orgf996c70)
-   [EPCs](#org20f998e)
    -   [What are "Event-driven Process Chains"?](#org3fcd476)
    -   [EPC elements](#org86a5fa6)
        -   [Events and functions](#org300a0fd)
        -   [Operators and tokens](#orgecf074f)
        -   [Process interfaces](#org5a8194e)
        -   [Organizational units](#orgb44b2ff)
    -   [Extended Event-driven Process Chain (eEPC)](#org96141d5)
    -   [EPC rules summary](#orgd42b19c)
-   [Practice](#orgdd15fe5)
    -   [Signavio demo](#orgb37bb2b)
    -   [Find the mistakes](#org70353a0)
    -   [Fill in a process model](#orga626f54)
    -   [Model a whole process](#orgae92503)
    -   [Test (October 26)](#org13196f0)
-   [References](#org0c2c7bb)



<a id="org62d71c8"></a>

# What will you learn?

-   What is a process?
-   What is process modeling\*
-   Example: Event-controlled Process Chains (EPC)
-   Practice in the Signavio Process Editor


<a id="org8a36a89"></a>

# What's a process?

![img](./img/process.png)

-   What are the elements of any process?
-   What's special (if anything) about "business processes"?
-   What's special (if anything) about "IT processes"?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   Does data play any special role?


<a id="orge0038aa"></a>

# Process modeling

The three-fold purpose of process modeling:

-   Shared world view (key)
-   Process standardization (means)
-   Process optimization (end)


<a id="orgdd96af7"></a>

## Shared world view


<a id="org45e3dc1"></a>

### Situation

![img](./img/hiring.gif)


<a id="org76ed456"></a>

### Complication & Question

![img](./img/hr_vs_it.jpg)

**Example: hiring process.**

What does an IT person see and talk about?

What does an HR person see and talk about?

-   IT view

    *Image: computer parts - the IT world-view*
    
    ![img](./img/computer.gif)
    
    *Image source: [EngWorkSheets.com 2020](#orgfded392)*

-   HR view

    *Image: HR and people operations - HR world-view*
    
    ![img](./img/hr.png)
    
    *Image source: [Sturgess, 2019](#orgb04cd19)*


<a id="orgbf4f97e"></a>

### Answer

![img](./img/hiring.jpg)

New problem: process model is not **standardized**.

*Image source: [CVO-Europe](#org37af66c)*


<a id="org5642d8e"></a>

## Process standardization

ARIS = Meta model for process modeling ("model of models")

![img](./img/aris.png)

*Image: Architecture of Information Systems (ARIS) [Software AG
2016](#org234b1ee)*


<a id="orgf996c70"></a>

## Process optimization

![img](./img/camunda.png)

*Image: Own image, modified after Camunda, BPM governance cycle,
2019*

PDF: <https://github.com/birkenkrahe/mod482/blob/main/9_modeling/img/camunda.pdf>


<a id="org20f998e"></a>

# EPCs


<a id="org3fcd476"></a>

## What are "Event-driven Process Chains"?

> The event-driven Process Chain (EPC) is a flow chart for business
> process modeling introduced by [August-Wilhelm Scheer](https://en.wikipedia.org/wiki/August-Wilhelm_Scheer) in the early
> 1990s. It illustrates the business process workflows. It uses
> graphical symbols to show the control-flow structure of a business
> process as a chain of events and functions. ([Visual Paradigm, 2021](#org235c6d4))


<a id="org86a5fa6"></a>

## EPC elements

![img](./img/epc.png)

*Image source: [Dechow et al, 2007](#org8e0b54e)*


<a id="org300a0fd"></a>

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

Image source: [Software AG](#org234b1ee)

-   Event and function rules

    -   Every EPC starts and ends with an event
    -   Events and functions alternate


<a id="orgecf074f"></a>

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


<a id="org5a8194e"></a>

### Process interfaces

-   Process interfaces are used to link independent processes
-   Trigger following process or signal preceding process
-   Can only be at the start or at the end of a process diagram

![img](./img/interface.png)


<a id="orgb44b2ff"></a>

### Organizational units

-   Organizational units are only connected to functions
-   They are RACI - responsible, accountable, consulted and informed
    
    ![img](./img/raci.png)


<a id="org96141d5"></a>

## Extended Event-driven Process Chain (eEPC)

eEPCs integrate the other views of the ARIS house:

-   Roles/organization
-   Products/services
-   Data input/output
    
    ![img](./img/eepc.png)


<a id="orgd42b19c"></a>

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


<a id="orgdd15fe5"></a>

# Practice

![img](./img/practice.gif)

Tip: [This platform allows you to play around in their online editor.](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#)


<a id="orgb37bb2b"></a>

## Signavio demo

-   Fire up the Signavio process editor
-   Let's draw some EPC diagrams
-   Create your models in your own folder


<a id="org70353a0"></a>

## Find the mistakes

Find all mistakes in the EPC diagram!


<a id="orga626f54"></a>

## Fill in a process model

(Classroom exercise)


<a id="orgae92503"></a>

## Model a whole process

(Graded homework)


<a id="org13196f0"></a>

## Test (October 26)


<a id="org0c2c7bb"></a>

# References

<a id="org37af66c"></a> CVO-Europe (n.d.). Our Hiring Process [website]. [Online:
cvo-europe.com](https://www.cvo-europe.com/en/careers/our-hiring-process).

<a id="org8e0b54e"></a> Dechow et al (2007). Interactions between modern
information technology and management control [article]. [Online:
researchgate.net.](https://www.researchgate.net/publication/274260317_Interactions_between_modern_information_technology_and_management_control)

<a id="orgfded392"></a> EngWorkSheets (2020). Computer Parts ESL Vocabulary Matching
Exercise Worksheet For Kids - PDF Preview [website]. [Online:
engworksheets.com](https://www.engworksheets.com/vocabulary-pdf-preview/Computer-Parts/4/computer-parts-esl-vocabulary-matching-exercise-worksheet-for-kids.html).

<a id="org332ffe8"></a> Maya G (Jun 29,2021). ITIL Processes [blog]. [Online:
itil-docs.com.](https://www.itil-docs.com/blogs/itil-concepts/itil-processes-functions)

<a id="org234b1ee"></a> Software AG University Relations (2016). BPM with ARIS
[presentation]. [Online: ariscommunity.com.](http://cdn.ariscommunity.com/community2/documents/urelation/BPM-ARIS_Part2.pdf)

<a id="orgb04cd19"></a> Sturgess G (June 20, 2019). What's the Difference
between HR and People Operations? [website]. [Online:
talentalign.com.](https://www.talentalign.com/whats-the-difference-between-hr-and-people-operations/)

<a id="org235c6d4"></a> Visual Paradigm (2021). What is Event-Driven
Process Chain (EPC)? [Website]. [Online: visual-paradigm.com](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#).

<a id="org2c81f92"></a> Wikipedia (1 Oct 2021). ITIL [website]. [Online:
en.wikipedia.org](https://en.wikipedia.org/wiki/ITIL).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Cp. ITIL library of IT processes, especially with regards
to IT services. More: [Wikipedia](#org2c81f92) (2021).

![img](./img/itil.jpg)
*Image source: ITIL docs, 2021*
