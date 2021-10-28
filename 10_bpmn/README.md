
# Table of Contents

-   [What will you learn?](#orgd677db2)
-   [BPMN object summary](#org71b3938)
    -   [Flow objects (Action/Decision)](#org28e0959)
    -   [Connecting objects (Communication)](#org2cd00ed)
    -   [Participants (Roles/Accountability)](#org6621d4d)
    -   [Artifacts (Details)](#org8b05f2d)
    -   [More information](#org68092f1)
-   [BPMN case](#org902408a)
-   [Pizza example](#org418404d)
    -   [Choreography](#orgd93f74a)
    -   [Collaboration](#orge44c048)
    -   [Enterprise modeling with BPMN](#org14399d6)
-   [Practice](#org7aa38cd)
    -   [BPMN rules](#org5cbe1fa)
    -   [BPMN diagram with mistakes](#org3d8b5c1)
    -   [Build your first own BPMN diagram](#orgf03de00)
    -   [Homework](#org669c224)
-   [References](#org2cf2018)



<a id="orgd677db2"></a>

# What will you learn?

-   Business Process Model and Notation
-   Object-oriented process modeling
-   Practice in the Signavio Process Editor


<a id="org71b3938"></a>

# BPMN object summary

Business Process Model and Notation (BPMN) 2.0 has four main groups
of shapes or objects. Source: [Lucidchart, 2020](#orgc85ef6e).


<a id="org28e0959"></a>

## Flow objects (Action/Decision)

![img](./img/flow.png)


<a id="org2cd00ed"></a>

## Connecting objects (Communication)

![img](./img/connecting.png)


<a id="org6621d4d"></a>

## Participants (Roles/Accountability)

![img](./img/pools.png)


<a id="org8b05f2d"></a>

## Artifacts (Details)

![img](./img/artifacts.png)

-   Groups
-   Documents
-   Annotation
-   Message (data)


<a id="org68092f1"></a>

## More information

For Signavio Process Manager, open the "Getting started" sidebar
inside the Process Manager explorer window under "Help".

![img](./img/signavio.png)

[This Signavio document](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm) gives a complete, structured account of all
the most relevant aspects of BPMN with many examples (SAP Signavio,
2021).

[This guide from Camunda](https://camunda.com/bpmn/reference/) (with link to a free BPMN online editor),
is also very good and complete.

![img](./img/bpmn.png)

*Image: complete list of BPMN symbols and rules ([Signavio](https://www.signavio.com/downloads/short-reads/free-bpmn-2-0-poster/)*[OneDrive](https://1drv.ms/u/s!AhEvK3qWokrvwUVBiCQluz4dwFlM))/


<a id="org902408a"></a>

# BPMN case

Creating and explaining this model takes about as much time as
eating a big icecream (7 min) - [Link](https://youtu.be/BwkNceoybvA?t=346).

![img](./img/icecream.png)


<a id="org418404d"></a>

# Pizza example


<a id="orgd93f74a"></a>

## Choreography

![img](./img/choreography.png)


<a id="orge44c048"></a>

## Collaboration

![img](./img/collaboration.png)


<a id="org14399d6"></a>

## Enterprise modeling with BPMN

[GitHub: Enterprise Modeling with BPMN (PDF)](https://github.com/birkenkrahe/mod482/blob/main/10_bpmn/bpmn_modeling.pdf)

![img](./img/presentation.png)


<a id="org7aa38cd"></a>

# Practice

![img](./img/practice.gif)


<a id="org5cbe1fa"></a>

## BPMN rules

![img](./img/summary.gif)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">NO.</th>
<th scope="col" class="org-left">BPMN MODELING RULE</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">1</td>
<td class="org-left">Every participant gets a pool or a lane inside a pool</td>
</tr>


<tr>
<td class="org-right">2</td>
<td class="org-left">Every pool contains exactly one process</td>
</tr>


<tr>
<td class="org-right">3</td>
<td class="org-left">A process has at least one start and one end event</td>
</tr>


<tr>
<td class="org-right">4</td>
<td class="org-left">Sequence flow (Action) flows only within pools</td>
</tr>


<tr>
<td class="org-right">5</td>
<td class="org-left">Message flow (Communication) flows only between pools</td>
</tr>


<tr>
<td class="org-right">6</td>
<td class="org-left">All process elements must be named</td>
</tr>


<tr>
<td class="org-right">7</td>
<td class="org-left">Decision points (exclusive gateways) have questions</td>
</tr>


<tr>
<td class="org-right">8</td>
<td class="org-left">Actors with little to do can become additional participants</td>
</tr>


<tr>
<td class="org-right">9</td>
<td class="org-left">Split or joined sequence flows need gateways</td>
</tr>


<tr>
<td class="org-right">10</td>
<td class="org-left">Opened gateways must be closed</td>
</tr>
</tbody>
</table>

BPMN has slightly different rules than EPC. In addition, because
it is primarily (though not only - see process mining and BPEL)
for human consumption, the style of a diagram carries extra weight:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">BPMN diagrams should be readable</td>
</tr>


<tr>
<td class="org-left">BPMN diagrams can be infinite in size</td>
</tr>


<tr>
<td class="org-left">BPMN diagrams run from the left to the right</td>
</tr>


<tr>
<td class="org-left">BPMN diagrams avoid loops (instead: attributes)</td>
</tr>


<tr>
<td class="org-left">BPMN diagrams distinguish action and communication</td>
</tr>
</tbody>
</table>

Here is a complete EPC "cheat sheet" (Source: SAP Signavio)

![img](./img/bpmn.png)


<a id="org3d8b5c1"></a>

## BPMN diagram with mistakes


<a id="orgf03de00"></a>

## Build your first own BPMN diagram


<a id="org669c224"></a>

## Homework


<a id="org2cf2018"></a>

# References

<a id="orgc85ef6e"></a> Lucidchart (Apr 28, 2020). Business Process Model and
Notation (BPMN) 2.0 Tutorial [video]. [Online: youtube.com](https://youtu.be/BwkNceoybvA).

<a id="org97e973a"></a> SAP Signavio Process editor version 15.7.1. SAP
(2021). Academic edition [platform]. Online: [www.signavio.com.](https://www.signavio.com/)

<a id="org37b916c"></a> SAP Signavio (n.d.). BPMN modeling [website]. [Online:
signavio.com](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm)

