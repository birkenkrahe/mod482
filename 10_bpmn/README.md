
# Table of Contents

-   [What will you learn?](#orgb3d84c0)
-   [BPMN object summary](#org0c58a1f)
    -   [Flow objects (Action/Decision)](#orga6f672a)
    -   [Connecting objects (Communication)](#orga368ff6)
    -   [Participants (Roles/Accountability)](#org519a639)
    -   [Artifacts (Details)](#org6b026e4)
    -   [More information](#org62efd16)
-   [BPMN case studies](#orgb1b57bc)
    -   [Eating icecream](#org5e2d96c)
    -   [Job application process](#org9b7e24f)
    -   [IT service](#orgf7ad699)
-   [Pizza example](#orgc32b64f)
    -   [Choreography](#org52dc846)
    -   [Collaboration](#org3fb76cc)
    -   [Enterprise modeling with BPMN](#orgd3f431f)
-   [Practice I](#org1b5573a)
    -   [BPMN rules](#org788030b)
    -   [BPMN diagram with mistakes](#org986006d)
        -   [Problem](#org5a7146d)
        -   [Solution](#org5e2f8a9)
    -   [Assignment (complete by Nov 2, 2.30 pm)](#orga4ea1ce)
-   [Practice II](#orgd4fee0d)
    -   [Written BPMN test on November 4 at 2.30 pm](#org0fb8bf9)
    -   [Assignment: Job application process (by Nov 2, 2.30 pm)](#org6fa2646)
        -   [Applicant - happy path process](#orgea3c9ad)
        -   [Applicant - complete process](#org0bcd242)
        -   [Recruiter - happy path process](#org04092f8)
        -   [Applicant and recruiter - happy path process](#orgcb685ca)
        -   [Recruiter - complete process](#org0881ca2)
        -   [Applicant (complete process) / Recruiter (collapsed process)](#org6ef0dd7)
        -   [Applicant and recruiter - complete collaborative process](#orge6439a3)
    -   [Assignment: Build your first own BPMN diagram](#orgf4f23f5)
    -   [Convert an EPC to a BPMN diagram](#org2c047b3)
    -   [Car purchase process](#orga234a34)
    -   [Practice session process](#orgf03c9cd)
    -   [IT support process](#org7be0fdc)
-   [References](#orgb43bf3a)



<a id="orgb3d84c0"></a>

# What will you learn?

-   Business Process Model and Notation
-   Object-oriented process modeling
-   Practice in the Signavio Process Editor


<a id="org0c58a1f"></a>

# BPMN object summary

Business Process Model and Notation (BPMN) 2.0 has four main groups
of shapes or objects. Source: [Lucidchart, 2020](#orga66079c).


<a id="orga6f672a"></a>

## Flow objects (Action/Decision)

![img](./img/flow.png)


<a id="orga368ff6"></a>

## Connecting objects (Communication)

![img](./img/connecting.png)


<a id="org519a639"></a>

## Participants (Roles/Accountability)

![img](./img/pools.png)


<a id="org6b026e4"></a>

## Artifacts (Details)

![img](./img/artifacts.png)

-   Groups
-   Documents
-   Annotation
-   Message (data)


<a id="org62efd16"></a>

## More information

For Signavio Process Manager, open the "Getting started" sidebar
inside the Process Manager explorer window under "Help".

![img](./img/signavio.png)

[This Signavio document](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm) gives a complete, structured account of all
the most relevant aspects of BPMN with many examples (SAP Signavio,
2021).

[This guide from Camunda](https://camunda.com/bpmn/reference/) (with link to a free BPMN online editor),
is also very good and complete.


<a id="orgb1b57bc"></a>

# BPMN case studies


<a id="org5e2d96c"></a>

## Eating icecream

Creating and explaining this model takes about as much time as
eating a big icecream (7 min) - [Link](https://youtu.be/BwkNceoybvA?t=346).

![img](./img/icecream.png)


<a id="org9b7e24f"></a>

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


<a id="orgf7ad699"></a>

## IT service

This example is (for now) only available in German.

Video: [BPMN 2.0 Prozessmodell in Signavio erzeugen.](https://youtu.be/kYK9t8fPkAY)

![img](./img/german.png)


<a id="orgc32b64f"></a>

# Pizza example


<a id="org52dc846"></a>

## Choreography

![img](./img/choreography.png)


<a id="org3fb76cc"></a>

## Collaboration

![img](./img/collaboration.png)


<a id="orgd3f431f"></a>

## Enterprise modeling with BPMN

[GitHub: Enterprise Modeling with BPMN (PDF)](https://github.com/birkenkrahe/mod482/blob/main/10_bpmn/bpmn_modeling.pdf)

![img](./img/presentation.png)


<a id="org1b5573a"></a>

# Practice I

![img](./img/practice.gif)


<a id="org788030b"></a>

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


<a id="org986006d"></a>

## BPMN diagram with mistakes


<a id="org5a7146d"></a>

### Problem

Which rule violations can you see in the following diagram
(GitHub)? The total number is<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> = 8 errors - I count a total of
11 additional rule violations. So the total is closer to 20.

![img](./img/error.png)


<a id="org5e2f8a9"></a>

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


<a id="orga4ea1ce"></a>

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


<a id="orgd4fee0d"></a>

# Practice II

![img](./img/practice2.gif)


<a id="org0fb8bf9"></a>

## Written BPMN test on November 4 at 2.30 pm

Topics:

-   BPMN objects
-   BPMN rules and rule violations
-   BPMN workflow


<a id="org6fa2646"></a>

## Assignment: Job application process (by Nov 2, 2.30 pm)

-   Review the rules using this online lesson
    (<https://h5p.org/node/1138751>)
-   Complete the summary quiz at the end of the lesson.
-   Watch both videos at the end ("Job application", 20 min)
-   Rebuild the diagram for the **Applicant** only (= 1 pool) in
    Signavio as a BPMN 2.0 diagram while you watch the first
    video. For the second video, rebuild only the diagram that is
    finished after 7 minutes\* (= complete applicant process with
    message flows to the collapsed recruiter pool).
-   I made [this short screencast](https://youtu.be/l6-fCtOXin4) to help you get started.
-   Save the diagram in your personal folder in "Shared Documents"
-   Share the diagram with me using the "Share>>Invite for feedback"
    tab
-   Enter "birkenkrahe@lyon.edu" and check "Send a copy to me" for
    proof (as shown below)

\*) the complete model that is shown is unfortunately not very
good. I'll share my complete, rule-compliant solution with you in
class. Though BPMN 2.0 did exist in 2011, the diagram owes too much to
version 1.0.


<a id="orgea3c9ad"></a>

### Applicant - happy path process

([Signavio](https://academic.signavio.com/p/editor?id=86d64600d0624b6cb17d7d81d2ef9bb5))

![img](./img/app1.png)


<a id="org0bcd242"></a>

### Applicant - complete process

([Signavio](https://academic.signavio.com/p/editor?id=d82bf0c4c92248e89874950b78ff23b0))

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Above: model in video</td>
</tr>


<tr>
<td class="org-left">Below: rule compliant model</td>
</tr>
</tbody>
</table>

![img](./img/app2.png)


<a id="org04092f8"></a>

### Recruiter - happy path process

([Signavio](https://academic.signavio.com/p/editor?id=2ff1f18657664833af590c6fc7aefbfc))

![img](./img/app3.png)


<a id="orgcb685ca"></a>

### Applicant and recruiter - happy path process

([Signavio](https://academic.signavio.com/p/editor?id=8ce1e76269aa48a3a7d646f29b3caebd))

![img](./img/app4.png)


<a id="org0881ca2"></a>

### Recruiter - complete process

([Signavio](https://academic.signavio.com/p/editor?id=39830914287c4e658b5bf49584ba1c58))

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">Above: model in video</td>
</tr>


<tr>
<td class="org-left">Below: rule compliant model</td>
</tr>
</tbody>
</table>

![img](./img/app5.png)


<a id="org6ef0dd7"></a>

### Applicant (complete process) / Recruiter (collapsed process)

([Signavio](https://academic.signavio.com/p/editor?id=3be88a96f306465cbb6a0dc486e0f726))

![img](./img/app6.png)


<a id="orge6439a3"></a>

### Applicant and recruiter - complete collaborative process

([Signavio](https://academic.signavio.com/p/editor?id=e377cc9506544985b3c4978347b72f64))

![img](./img/app7.png)


<a id="orgf4f23f5"></a>

## Assignment: Build your first own BPMN diagram

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

-   Turn this workflow into a BPMN diagram. It begins with the start
    event "Modeling begins"
-   You should at least complete the happy path model. If you're up
    to it, add gateways
-   Make sure you save the happy path model before creating a more
    detailed model
-   Save the diagram(s) in your personal folder in Shared Documents
-   Share the diagram with me using the "Share>>Invite to edit" tab


<a id="org2c047b3"></a>

## TODO Convert an EPC to a BPMN diagram


<a id="orga234a34"></a>

## TODO Car purchase process


<a id="orgf03c9cd"></a>

## TODO Practice session process


<a id="org7be0fdc"></a>

## TODO IT support process


<a id="orgb43bf3a"></a>

# References

<a id="orga66079c"></a> Lucidchart (Apr 28, 2020). Business Process Model and
Notation (BPMN) 2.0 Tutorial [video]. [Online: youtube.com](https://youtu.be/BwkNceoybvA).

<a id="orgb4da9f8"></a> SAP Signavio Process editor version 15.7.1. SAP
(2021). Academic edition [platform]. Online: [www.signavio.com.](https://www.signavio.com/)

<a id="orgb9042f2"></a> SAP Signavio (n.d.). BPMN modeling [website]. [Online:
signavio.com](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> According to the Signavio "spell checker" for BPMN 2.0 diagrams.
