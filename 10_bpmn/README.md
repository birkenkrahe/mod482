
# Table of Contents

-   [What will you learn?](#org9004681)
-   [BPMN object summary](#orgccc146d)
    -   [Flow objects (Action/Decision)](#org1f9df1c)
    -   [Connecting objects (Communication)](#org8a17745)
    -   [Participants (Roles/Accountability)](#org4ed822c)
    -   [Artifacts (Details)](#orgdb36722)
    -   [More information](#orgefd187d)
-   [BPMN case studies](#org494e0ca)
    -   [Eating icecream](#org84ec4d4)
    -   [Job application process](#org6199178)
    -   [IT service](#orgbdb2272)
-   [Pizza example](#org826ddf3)
    -   [Choreography](#orga83f31e)
    -   [Collaboration](#org80439e5)
    -   [Enterprise modeling with BPMN](#orged04835)
-   [Practice I](#org9d48b6f)
    -   [BPMN rules](#org579297c)
    -   [BPMN diagram with mistakes](#orgd190629)
        -   [Problem](#org75d7be5)
        -   [Solution](#orgd491e00)
    -   [Assignment (complete by Nov 2, 2.30 pm)](#org4dae9a8)
-   [Practice II - model simple processes](#org58a4be9)
    -   [Written BPMN test on November 4 at 2.30 pm](#org171e3b5)
    -   [Assignment: Job application process](#org5f2bbf5)
        -   [Problem](#org0a123bf)
        -   [Solution](#orgd31842f)
    -   [Assignment: Build your first own BPMN diagram](#org912dab3)
        -   [Problem](#orge6b8b2a)
        -   [Solution](#orga9483e7)
    -   [Convert an EPC to a BPMN diagram](#orgcd18d7a)
        -   [Problem](#orgc632186)
        -   [Solution](#org2e4c580)
    -   [Car purchase process](#org15c12b5)
        -   [Problem](#org14394e7)
    -   [Practice session process](#org2d11946)
        -   [Problem](#orgdf439e7)
    -   [Supply chain process](#org71f059b)
        -   [Problem](#org9735997)
-   [Practice III - model a design](#org349e772)
    -   [Create a model](#orgfa435f6)
    -   [Run a simulation](#org8d1d934)
-   [References](#org41dd883)



<a id="org9004681"></a>

# What will you learn?

-   Business Process Model and Notation
-   Object-oriented process modeling
-   Practice in the Signavio Process Editor


<a id="orgccc146d"></a>

# BPMN object summary

Business Process Model and Notation (BPMN) 2.0 has four main groups
of shapes or objects. Source: [Lucidchart, 2020](#orgdbbffb9).


<a id="org1f9df1c"></a>

## Flow objects (Action/Decision)

![img](./img/flow.png)


<a id="org8a17745"></a>

## Connecting objects (Communication)

![img](./img/connecting.png)


<a id="org4ed822c"></a>

## Participants (Roles/Accountability)

![img](./img/pools.png)


<a id="orgdb36722"></a>

## Artifacts (Details)

![img](./img/artifacts.png)

-   Groups
-   Documents
-   Annotation
-   Message (data)


<a id="orgefd187d"></a>

## More information

For Signavio Process Manager, open the "Getting started" sidebar
inside the Process Manager explorer window under "Help".

![img](./img/signavio.png)

[This Signavio document](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm) gives a complete, structured account of all
the most relevant aspects of BPMN with many examples (SAP Signavio,
2021).

[This guide from Camunda](https://camunda.com/bpmn/reference/) (with link to a free BPMN online editor),
is also very good and complete.


<a id="org494e0ca"></a>

# BPMN case studies


<a id="org84ec4d4"></a>

## Eating icecream

Creating and explaining this model takes about as much time as
eating a big icecream (7 min) - [Link](https://youtu.be/BwkNceoybvA?t=346).

![img](./img/icecream.png)


<a id="org6199178"></a>

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


<a id="orgbdb2272"></a>

## IT service

This example is (for now) only available in German.

Video: [BPMN 2.0 Prozessmodell in Signavio erzeugen.](https://youtu.be/kYK9t8fPkAY)

![img](./img/german.png)


<a id="org826ddf3"></a>

# Pizza example


<a id="orga83f31e"></a>

## Choreography

![img](./img/choreography.png)


<a id="org80439e5"></a>

## Collaboration

![img](./img/collaboration.png)


<a id="orged04835"></a>

## Enterprise modeling with BPMN

[GitHub: Enterprise Modeling with BPMN (PDF)](https://github.com/birkenkrahe/mod482/blob/main/10_bpmn/bpmn_modeling.pdf)

![img](./img/presentation.png)


<a id="org9d48b6f"></a>

# Practice I

![img](./img/practice.gif)


<a id="org579297c"></a>

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


<a id="orgd190629"></a>

## BPMN diagram with mistakes


<a id="org75d7be5"></a>

### Problem

Which rule violations can you see in the following diagram
(GitHub)? The total number is<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> = 8 errors - I count a total of
11 additional rule violations. So the total is closer to 20.

![img](./img/error.png)


<a id="orgd491e00"></a>

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


<a id="org4dae9a8"></a>

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


<a id="org58a4be9"></a>

# Practice II - model simple processes

![img](./img/practice2.gif)


<a id="org171e3b5"></a>

## Written BPMN test on November 4 at 2.30 pm

Topics:

-   BPMN objects
-   BPMN rules and rule violations
-   BPMN workflow


<a id="org5f2bbf5"></a>

## Assignment: Job application process


<a id="org0a123bf"></a>

### Problem

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


<a id="orgd31842f"></a>

### Solution

-   Applicant - happy path process

    ([Signavio](https://academic.signavio.com/p/editor?id=86d64600d0624b6cb17d7d81d2ef9bb5))
    
    ![img](./img/app1.png)

-   Applicant - complete process

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

-   Recruiter - happy path process

    ([Signavio](https://academic.signavio.com/p/editor?id=2ff1f18657664833af590c6fc7aefbfc))
    
    ![img](./img/app3.png)

-   Applicant and recruiter - happy path process

    ([Signavio](https://academic.signavio.com/p/editor?id=8ce1e76269aa48a3a7d646f29b3caebd))
    
    ![img](./img/app4.png)

-   Recruiter - complete process

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

-   Applicant (complete process) / Recruiter (collapsed process)

    ([Signavio](https://academic.signavio.com/p/editor?id=3be88a96f306465cbb6a0dc486e0f726))
    
    ![img](./img/app6.png)

-   Applicant and recruiter - complete collaborative process

    ([Signavio](https://academic.signavio.com/p/editor?id=e377cc9506544985b3c4978347b72f64))
    
    ![img](./img/app7.png)


<a id="org912dab3"></a>

## Assignment: Build your first own BPMN diagram


<a id="orge6b8b2a"></a>

### Problem

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
<td class="org-left">Which other events or tasks are there?</td>
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
<td class="org-left">Check model</td>
<td class="org-left">Spell checker</td>
</tr>


<tr>
<td class="org-right">10</td>
<td class="org-left">Save and share model diagram</td>
<td class="org-left">Save and share</td>
</tr>
</tbody>
</table>

-   Turn this workflow into a BPMN diagram. It begins with the start
    event "Modeling begins"
-   You should at least complete the happy path model. If you're up
    to it, add gateway points (identify where gateways may be placed)
-   Make sure you save the happy path model before creating a more
    detailed model
-   Save the diagram(s) in your personal folder in Shared Documents
-   Share the diagram with me using the "Share>>Invite to edit" tab


<a id="orga9483e7"></a>

### Solution

![img](./img/workflow.png)


<a id="orgcd18d7a"></a>

## Convert an EPC to a BPMN diagram


<a id="orgc632186"></a>

### Problem

You saw this diagram [in the lecture on modeling and EPCs](https://github.com/birkenkrahe/mod482/tree/main/9_modeling_epc#flow).

![img](./img/convert.png)

Unfortunately, this diagram violates an EPC rule. Can you tell
which one? I've cleaned it up (also avoiding the loop but
retaining all the important information) in the diagram
below. Convert this diagram into a BPMN 2.0 diagram!

For simplicity use only BPMN 2.0 **core** elements (i.e. no
intermediate events). But you can overload tasks with a `loop`
attribute and set a `loop maximum` value by opening the
`Attributes|Views` sidepanel on the right side of the editor.

![img](./img/convert1.png)


<a id="org2e4c580"></a>

### Solution

Solution 1 is a straigthforward translation:

-   The Organizational Unit `User` becomes a pool
-   The events are replaced by gateway outflows
-   The process interface is integrated in the process (this has the
    advantage that the diagram shows the escalation structure
    clearly).
-   If more than one wrong password entry is allowed, the diagram
    must be expanded. That's a limitation.
    
    ![img](./img/login.png)

Solution 2 deals with this limitation: the `Enter password` task
is looped. A loop parameter (`loop maximum`) is set and can be
changed. Now the diagram is generalized.

![img](./img/login1.png)


<a id="org15c12b5"></a>

## Car purchase process


<a id="org14394e7"></a>

### Problem

Model the following process using BPMN 2.0:

> A customer wants to buy a car. He goes to a car dealer to pick a
> car. The dealer has several new, and one used car available. The
> customer picks one, pays for the car, and leaves. She's happy now!

*Tip: you don't need two pools for this process, because the
dealer doesn't have much to do.*


<a id="org2d11946"></a>

## Practice session process


<a id="orgdf439e7"></a>

### Problem

Model the following process using BPMN 2.0:

> The professor demonstrates the modeling language BPMN. After the
> demonstration, he assigns an exercise to the students. Once the
> assignment is completed, the student submits the solution. The
> professor checks the result before ending the class.

*Tip: model the professor first, then add the student as a second
pool.*


<a id="org71f059b"></a>

## Supply chain process


<a id="org9735997"></a>

### Problem

Model the following supply chain process using BPMN 2.0:

> The process begins with a material purchase request, the Resource
> Manager issues a material requisition. Next, Purchasing issues a
> purchase order for the requested material. When the receipt of the
> purchased items has been received by the Resource Manager, the
> Warehouse inspects the items. Now, Accounting processes the
> vendor’s invoice and the purchase process is finished.

*Tip: think about the number of lanes or pools that you need.*


<a id="org349e772"></a>

# Practice III - model a design


<a id="orgfa435f6"></a>

## Create a model

Convert the design of a "simple reflex agent" (like a vacuum robot,
from [AIMA](#org59f4c02)) into a standardized process model. Use either EPCs or
BPMN 2.0. Your input: pseudocode + non-standard diagram.

This agent acts according to a `rule` whose condition matches the
current `state`, as defined by the `percept` (input signals).

Pseudocode:

![img](./img/simplecode.png)

Figure:

![img](./img/simple.png)


<a id="org8d1d934"></a>

## Run a simulation

One of the tests for a good model is to run a "simulation": go
through the process with known input values and obtain known output
values. This is the same procedure used to e.g. improve machine
learning models during training and testing phases.

Here is an example `percept~/~action` sequence for a vacuum robot
whose `world` consists of two adjacent areas A and B that are
either dirty or clean:

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left"><code>percept</code></th>
<th scope="col" class="org-left"><code>action</code></th>
<th scope="col" class="org-left">Interpretation</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left"><code>[A,dirty]</code></td>
<td class="org-left"><code>suck</code></td>
<td class="org-left">Area <code>A</code> is <code>dirty</code>, <code>suck</code> to clean</td>
</tr>


<tr>
<td class="org-left"><code>[A,clean]</code></td>
<td class="org-left"><code>right</code></td>
<td class="org-left">Area <code>A</code> is <code>clean</code>, move <code>right</code> to <code>B</code></td>
</tr>


<tr>
<td class="org-left"><code>[B,dirty]</code></td>
<td class="org-left"><code>suck</code></td>
<td class="org-left">Area <code>B</code> is <code>dirty</code>, <code>suck</code> to clean</td>
</tr>


<tr>
<td class="org-left"><code>[B,clean]</code></td>
<td class="org-left"><code>left</code></td>
<td class="org-left">Area <code>B</code> is <code>clean</code>, move <code>left</code> to <code>A</code></td>
</tr>


<tr>
<td class="org-left"><code>[A,clean],[A,clean]</code></td>
<td class="org-left"><code>right</code></td>
<td class="org-left">Do nothing, then move <code>right</code></td>
</tr>


<tr>
<td class="org-left"><code>[A,clean],[A,dirty]</code></td>
<td class="org-left"><code>suck</code></td>
<td class="org-left">Do nothing, then <code>suck</code></td>
</tr>
</tbody>
</table>

The table continues ad infinitum with arbitrarily long `precept`
sequences.


<a id="org41dd883"></a>

# References

<a id="org59f4c02"></a> Russell/Norvig (2021). AI - A Modern
Approach. Pearson. [URL: berkeley.edu](http://aima.cs.berkeley.edu/).

<a id="orgdbbffb9"></a> Lucidchart (Apr 28, 2020). Business Process Model and
Notation (BPMN) 2.0 Tutorial [video]. [Online: youtube.com](https://youtu.be/BwkNceoybvA).

<a id="orgdaae6e1"></a> SAP Signavio Process editor version 15.7.1. SAP
(2021). Academic edition [platform]. Online: [www.signavio.com.](https://www.signavio.com/)

<a id="orgbadba1b"></a> SAP Signavio (n.d.). BPMN modeling [website]. [Online:
signavio.com](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> According to the Signavio "spell checker" for BPMN 2.0 diagrams.
