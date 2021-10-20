
# Table of Contents

-   [What will you learn?](#org4f78cb0)
-   [What's a process?](#org5f0b54d)
-   [Process modeling](#org824fcbb)
    -   [Shared world view](#org20854f6)
        -   [Situation](#orgea385d2)
        -   [Complication & Question](#org2ed1b96)
        -   [Answer](#org6cee774)
    -   [Process standardization](#org5723cfc)
    -   [Process optimization](#org37c272b)
-   [EPCs](#orga276eb9)
    -   [What are "Event-driven Process Chains"?](#orgaba7750)
    -   [EPC elements](#org1e66d4a)
        -   [Events and functions](#org36424ed)
        -   [Flow](#org791298c)
        -   [Operators and tokens](#org1ae240d)
        -   [Flow](#org05c843c)
        -   [Process interfaces](#org098d490)
        -   [Organizational units](#orgabc4211)
    -   [Extended Event-driven Process Chain (eEPC)](#orgb962049)
    -   [EPC rules summary](#orged6c30f)
-   [Practice](#orge3e14f7)
    -   [Signavio demo](#orgc69cbe2)
    -   [Find the mistakes](#org595309d)
    -   [Fill in a process model](#org94c068e)
    -   [Model a whole process](#org5eefcaa)
    -   [Test (October 26)](#org71de738)
-   [References](#orgf6329f2)



<a id="org4f78cb0"></a>

# What will you learn?

-   What is a process?
-   What is process modeling\*
-   Example: Event-controlled Process Chains (EPC)
-   Practice in the Signavio Process Editor
    
    ![img](./img/pm.png)


<a id="org5f0b54d"></a>

# What's a process?

![img](./img/process.png)

-   What are the elements of any process?<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup>
-   What's special (if anything) about "business processes"?<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>
-   What's special (if anything) about "IT processes"?<sup><a id="fnr.3" class="footref" href="#fn.3">3</a></sup>
-   Does data play any special role?


<a id="org824fcbb"></a>

# Process modeling

The three-fold purpose of process modeling:

-   Shared world view (key)
-   Process standardization (means)
-   Process optimization (end)


<a id="org20854f6"></a>

## Shared world view


<a id="orgea385d2"></a>

### Situation

![img](./img/hiring.gif)


<a id="org2ed1b96"></a>

### Complication & Question

![img](./img/hr_vs_it.jpg)

**Example: hiring process.**

What does an IT person see and talk about?

What does an HR person see and talk about?

-   IT view

    *Image: computer parts - the IT world-view*
    
    ![img](./img/computer.gif)
    
    *Image source: [EngWorkSheets.com 2020](#org01acd9b)*

-   HR view

    *Image: HR and people operations - HR world-view*
    
    ![img](./img/hr.png)
    
    *Image source: [Sturgess, 2019](#orgb1cba0f)*


<a id="org6cee774"></a>

### Answer

![img](./img/hiring.jpg)

New problem: process model is not **standardized**.

*Image source: [CVO-Europe](#org7a5af66)*


<a id="org5723cfc"></a>

## Process standardization

ARIS = Meta model for process modeling ("model of models")

![img](./img/aris.png)

*Image: Architecture of Information Systems (ARIS) [Software AG
2016](#org73314f9)*


<a id="org37c272b"></a>

## Process optimization

![img](./img/camunda.png)

*Image: Own image, modified after Camunda, BPM governance cycle,
2019*

PDF: <https://github.com/birkenkrahe/mod482/blob/main/9_modeling/img/camunda.pdf>


<a id="orga276eb9"></a>

# EPCs


<a id="orgaba7750"></a>

## What are "Event-driven Process Chains"?

> The event-driven Process Chain (EPC) is a flow chart for business
> process modeling introduced by [August-Wilhelm Scheer](https://en.wikipedia.org/wiki/August-Wilhelm_Scheer) in the early
> 1990s. It illustrates the business process workflows. It uses
> graphical symbols to show the control-flow structure of a business
> process as a chain of events and functions. ([Visual Paradigm, 2021](#org76071e0))


<a id="org1e66d4a"></a>

## EPC elements

![img](./img/epc.png)

*Image source: [Dechow et al, 2007](#orge47ec94)*


<a id="org36424ed"></a>

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

Image source: [Software AG](#org73314f9)

-   Event and function rules

    -   Every EPC starts and ends with an event
    -   Events and functions alternate


<a id="org791298c"></a>

### Flow

Flow represents the flow of time, and is itself represented by a
solid arrow with a solid tip.


<a id="org1ae240d"></a>

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
    
    ![img](./img/operators.png)


<a id="org05c843c"></a>

### Flow

-   All process elements must be connected by flow (arrows)
-   Loops are allowed (but careful: maintain model readability)
    
    ![img](./img/loops.png)


<a id="org098d490"></a>

### Process interfaces

-   Process interfaces are used to link independent processes
-   Trigger following process or signal preceding process
-   Can only be at the start or at the end of a process diagram

![img](./img/interface.png)


<a id="orgabc4211"></a>

### Organizational units

-   Organizational units are only connected to functions
-   They are RACI - Responsible, Accountable, Consulted and Informed
    
    ![img](./img/raci.png)


<a id="orgb962049"></a>

## Extended Event-driven Process Chain (eEPC)

eEPCs integrate the other views of the ARIS house:

-   Roles/organization
-   Products/services
-   Data input/output
    
    ![img](./img/eepc.png)


<a id="orged6c30f"></a>

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


<a id="orge3e14f7"></a>

# Practice

![img](./img/practice.gif)

Tip: [This platform allows you to play around in their online editor.](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#)


<a id="orgc69cbe2"></a>

## Signavio demo

-   Fire up the Signavio process editor
-   Let's draw some EPC diagrams
-   Create your models in your own folder


<a id="org595309d"></a>

## Find the mistakes

Find all mistakes in the EPC diagram!


<a id="org94c068e"></a>

## Fill in a process model

(Classroom exercise)


<a id="org5eefcaa"></a>

## Model a whole process

(Graded homework)


<a id="org71de738"></a>

## Test (October 26)


<a id="orgf6329f2"></a>

# References

<a id="org7a5af66"></a> CVO-Europe (n.d.). Our Hiring Process [website]. [Online:
cvo-europe.com](https://www.cvo-europe.com/en/careers/our-hiring-process).

<a id="orge47ec94"></a> Dechow et al (2007). Interactions between modern
information technology and management control [article]. [Online:
researchgate.net.](https://www.researchgate.net/publication/274260317_Interactions_between_modern_information_technology_and_management_control)

<a id="org01acd9b"></a> EngWorkSheets (2020). Computer Parts ESL Vocabulary Matching
Exercise Worksheet For Kids - PDF Preview [website]. [Online:
engworksheets.com](https://www.engworksheets.com/vocabulary-pdf-preview/Computer-Parts/4/computer-parts-esl-vocabulary-matching-exercise-worksheet-for-kids.html).

<a id="org411ff60"></a> Maya G (Jun 29,2021). ITIL Processes [blog]. [Online:
itil-docs.com.](https://www.itil-docs.com/blogs/itil-concepts/itil-processes-functions)

<a id="org90719dc"></a> SAP (n.d.). What is ERP? [website]. [Online:
insights.sap.com.](https://insights.sap.com/what-is-erp/?sred=glo-products-whatiserp)

<a id="org73314f9"></a> Software AG University Relations (2016). BPM with ARIS
[presentation]. [Online: ariscommunity.com.](http://cdn.ariscommunity.com/community2/documents/urelation/BPM-ARIS_Part2.pdf)

<a id="orgb1cba0f"></a> Sturgess G (June 20, 2019). What's the Difference
between HR and People Operations? [website]. [Online:
talentalign.com.](https://www.talentalign.com/whats-the-difference-between-hr-and-people-operations/)

<a id="org76071e0"></a> Visual Paradigm (2021). What is Event-Driven
Process Chain (EPC)? [Website]. [Online: visual-paradigm.com](https://online.visual-paradigm.com/knowledge/business-design-tools/what-is-epc-diagram/#).

<a id="org04578d2"></a> Wikipedia (1 Oct 2021). ITIL [website]. [Online:
en.wikipedia.org](https://en.wikipedia.org/wiki/ITIL).


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> Different languages use different terms:(1)
\*Functions\*/tasks/actions/activities; (2) \*events\*/status/trigger; (3)
\*flow\*/path/sequence/connectors; (4) \*operators\*/gateways/decisions.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> Business processes generate added value.

<sup><a id="fn.3" href="#fnr.3">3</a></sup> Cp. ITIL library of IT processes, especially with regards
to IT services. More: [Wikipedia](#org04578d2) (2021).

![img](./img/itil.jpg)
*Image source: ITIL docs, 2021*

<sup><a id="fn.4" href="#fnr.4">4</a></sup> Any productive ERP system contains many more transactions than
that. In practice, these are often modeled as BPMN diagrams, or as ER
Diagrams, if customer-facing or database operations are being
modeled. For more about ERP systems, see this tutorial ([SAP](#org90719dc)).
