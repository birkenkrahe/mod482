
# Table of Contents

-   [What will you learn?](#orgc0892ae)
-   [BPMN object summary](#orgd1b096b)
    -   [Flow objects (Action/Decision)](#org8252365)
    -   [Connecting objects (Communication)](#org5c93280)
    -   [Participants (Roles/Accountability)](#org08f661f)
    -   [Artifacts (Details)](#org0df0411)
    -   [More information](#org79008a5)
-   [BPMN case studies](#orgdffe797)
    -   [Eating icecream](#orgcf13091)
    -   [Job application process](#orgfc05e81)
    -   [IT service](#org8af1ba7)
-   [Pizza example](#org640c78d)
    -   [Choreography](#org55abad6)
    -   [Collaboration](#orgcd48df3)
    -   [Enterprise modeling with BPMN](#org5160e98)
-   [Practice I](#org4ccdfcd)
    -   [BPMN rules](#orgf36d60a)
    -   [BPMN diagram with mistakes](#org40f0641)
        -   [Problem](#org9ca2b85)
        -   [Solution](#org889f700)
    -   [Assignment (complete by Nov 2, 2.30 pm)](#org3d5dc08)
-   [Practice II](#orge36708c)
    -   [Written BPMN test on November 2 at 2.30 pm](#org0e24d55)
    -   [Build your first own BPMN diagram](#orgfcb57ce)
    -   [Convert an EPC to a BPMN diagram](#org5527da2)
    -   [Car purchase process](#org251ce74)
    -   [Practice session process](#org6ca809e)
    -   [IT support process](#orgb1e86c8)
-   [References](#org0464e88)



<a id="orgc0892ae"></a>

# What will you learn?

-   Business Process Model and Notation
-   Object-oriented process modeling
-   Practice in the Signavio Process Editor


<a id="orgd1b096b"></a>

# BPMN object summary

Business Process Model and Notation (BPMN) 2.0 has four main groups
of shapes or objects. Source: [Lucidchart, 2020](#org76c3040).


<a id="org8252365"></a>

## Flow objects (Action/Decision)

![img](./img/flow.png)


<a id="org5c93280"></a>

## Connecting objects (Communication)

![img](./img/connecting.png)


<a id="org08f661f"></a>

## Participants (Roles/Accountability)

![img](./img/pools.png)


<a id="org0df0411"></a>

## Artifacts (Details)

![img](./img/artifacts.png)

-   Groups
-   Documents
-   Annotation
-   Message (data)


<a id="org79008a5"></a>

## More information

For Signavio Process Manager, open the "Getting started" sidebar
inside the Process Manager explorer window under "Help".

![img](./img/signavio.png)

[This Signavio document](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm) gives a complete, structured account of all
the most relevant aspects of BPMN with many examples (SAP Signavio,
2021).

[This guide from Camunda](https://camunda.com/bpmn/reference/) (with link to a free BPMN online editor),
is also very good and complete.


<a id="orgdffe797"></a>

# BPMN case studies


<a id="orgcf13091"></a>

## Eating icecream

Creating and explaining this model takes about as much time as
eating a big icecream (7 min) - [Link](https://youtu.be/BwkNceoybvA?t=346).

![img](./img/icecream.png)


<a id="orgfc05e81"></a>

## Job application process

Part 1: demonstration of creating a simple BPMN workflow for an
application process. The software used here is irrelevant - you're
still using the BPMN standard and you can recreate these models in
a process modeling editor of your choice - bpmn.io, signavio, ARIS
or even MS Visio will do. Source: Aptero Solutions, 2011.

Youtube: <https://youtu.be/WtOzW8Ck5LY>

Part 2: in this demonstration, which follows on part 1, you see how
to implement the concept of multiple pools and message flow across
pools using the same example as before, an application process. The
process participants involved are: the applicant and the HR
department of a company. Source: Aptero Solutions, 2011.

Youtube: <https://youtu.be/B5H2K8wcBGU>


<a id="org8af1ba7"></a>

## IT service

This example is (for now) only available in German.

Video: [BPMN 2.0 Prozessmodell in Signavio erzeugen.](https://youtu.be/kYK9t8fPkAY)

![img](./img/german.png)


<a id="org640c78d"></a>

# Pizza example


<a id="org55abad6"></a>

## Choreography

![img](./img/choreography.png)


<a id="orgcd48df3"></a>

## Collaboration

![img](./img/collaboration.png)


<a id="org5160e98"></a>

## Enterprise modeling with BPMN

[GitHub: Enterprise Modeling with BPMN (PDF)](https://github.com/birkenkrahe/mod482/blob/main/10_bpmn/bpmn_modeling.pdf)

![img](./img/presentation.png)


<a id="org4ccdfcd"></a>

# Practice I

![img](./img/practice.gif)


<a id="orgf36d60a"></a>

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


<a id="org40f0641"></a>

## BPMN diagram with mistakes


<a id="org9ca2b85"></a>

### Problem

Which rule violations can you see in the following diagram
(GitHub)? The total number is<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> = 8 errors - I count a total of
11 additional rule violations. So the total is closer to 20.

![img](./img/error.png)


<a id="org889f700"></a>

### Solution

![img](./img/error_solution.png)

1.  Pool name must be actor or organization
2.  Between pools only message flows
3.  Collapsed pool needs a name
4.  Whole process must be inside pool
5.  Inside pools only sequence flows
6.  Only one start event per pool
7.  Only one end event per pool
8.  Default flow only after exclusive gateway
9.  Bi-directional association serves no purpose here
10. "No" as flow title, and question at exclusive gateway missing
11. Receiving intermediate message event wrongly named
12. Task name missing
13. End event name missing
14. Sending end event neds to send something
15. Need gateway here (flow splits)
16. Start event need title
17. Task needs title
18. Task needs title
19. Artifact needs title
20. Swimline needs title


<a id="org3d5dc08"></a>

## Assignment (complete by Nov 2, 2.30 pm)

![img](./img/h5p.png)

-   Review the rules using [this online lesson](https://h5p.org/node/1138751) (<https://h5p.org/node/1138751>)
-   Complete the summary quiz at the end of the lesson.
-   Watch both videos at the end (`Job application`, 20 min)
-   Rebuild the diagram in Signavio as a `new>>BPMN 2.0 diagram`
    while you watch
-   Save them in your personal folder in `Shared Documents`
-   Share the diagram with me using the `Share>>Invite for feedback` tab
-   Enter `birkenkrahe@lyon.edu` and check `Send a copy to me` for
    proof - as shown in the image.
    
    ![img](./img/share.png)


<a id="orge36708c"></a>

# Practice II

![img](./img/practice2.gif)


<a id="org0e24d55"></a>

## Written BPMN test on November 2 at 2.30 pm

Topics:

-   BPMN objects
-   BPMN rules and rule violations
-   BPMN workflow


<a id="orgfcb57ce"></a>

## Build your first own BPMN diagram

Here is my (recommended) BPMN modeling workflow.

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">NO.</th>
<th scope="col" class="org-left">STEP</th>
<th scope="col" class="org-left">ACTION</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">1</td>
<td class="org-left">Who are the actors (organizational units)?</td>
<td class="org-left">Pools and lanes</td>
</tr>


<tr>
<td class="org-right">2</td>
<td class="org-left">What are the start and end events?</td>
<td class="org-left">Gather them</td>
</tr>


<tr>
<td class="org-right">3</td>
<td class="org-left">Which other events or functions are there?</td>
<td class="org-left">Gather them</td>
</tr>


<tr>
<td class="org-right">4</td>
<td class="org-left">Is there any communication?</td>
<td class="org-left">Add message flow</td>
</tr>


<tr>
<td class="org-right">5</td>
<td class="org-left">What is the happy path?</td>
<td class="org-left">Model it</td>
</tr>


<tr>
<td class="org-right">6</td>
<td class="org-left">Can any events or tasks be parallelized?</td>
<td class="org-left">Add gateways</td>
</tr>


<tr>
<td class="org-right">7</td>
<td class="org-left">Which decisions or changes are involved?</td>
<td class="org-left">Add gateways</td>
</tr>


<tr>
<td class="org-right">8</td>
<td class="org-left">Anything else?</td>
<td class="org-left">Add it</td>
</tr>


<tr>
<td class="org-right">9</td>
<td class="org-left">Check diagram</td>
<td class="org-left">Spell checker</td>
</tr>


<tr>
<td class="org-right">10</td>
<td class="org-left">Save and share diagram</td>
<td class="org-left">Save and share</td>
</tr>
</tbody>
</table>

-   Turn this workflow into a BPMN diagram
-   Save the diagram in your personal folder in Shared Documents
-   Share the diagram with me using the "Share>>Invite to edit" tab


<a id="org5527da2"></a>

## TODO Convert an EPC to a BPMN diagram


<a id="org251ce74"></a>

## TODO Car purchase process


<a id="org6ca809e"></a>

## TODO Practice session process


<a id="orgb1e86c8"></a>

## TODO IT support process


<a id="org0464e88"></a>

# References

<a id="org76c3040"></a> Lucidchart (Apr 28, 2020). Business Process Model and
Notation (BPMN) 2.0 Tutorial [video]. [Online: youtube.com](https://youtu.be/BwkNceoybvA).

<a id="orgabc82fd"></a> SAP Signavio Process editor version 15.7.1. SAP
(2021). Academic edition [platform]. Online: [www.signavio.com.](https://www.signavio.com/)

<a id="org8077db9"></a> SAP Signavio (n.d.). BPMN modeling [website]. [Online:
signavio.com](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> According to the Signavio "spell checker" for BPMN 2.0 diagrams.
