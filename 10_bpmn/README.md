
# Table of Contents

-   [What will you learn?](#orgdb26ca8)
-   [BPMN object summary](#org3106779)
    -   [Flow objects (Action/Decision)](#org6531a6e)
    -   [Connecting objects (Communication)](#org76c5094)
    -   [Participants (Roles/Accountability)](#org5594732)
    -   [Artifacts (Details)](#orgc0733bd)
    -   [More information](#orge6a2a4f)
-   [BPMN case studies](#org02dbec7)
    -   [Eating icecream](#org9a31233)
    -   [Job application process](#orgdbc783b)
    -   [IT service](#org79b509f)
-   [Pizza example](#orgc782d0e)
    -   [Choreography](#orgfc44dff)
    -   [Collaboration](#orga8d97d3)
    -   [Enterprise modeling with BPMN](#org79bf789)
-   [Practice I](#org220c542)
    -   [BPMN rules](#orgbdf8351)
    -   [BPMN diagram with mistakes](#org7a821ae)
        -   [Problem](#org0f92c6d)
        -   [Solution](#org2407229)
    -   [Assignment (complete by Nov 2, 2.30 pm)](#orgec965b7)
-   [Practice II](#orgeea3dbc)
    -   [Written BPMN test on November 4 at 2.30 pm](#org6d13cdd)
    -   [Assignment: Job application process](#org843b964)
        -   [Problem](#org462cf17)
        -   [Solution](#org2c4601b)
    -   [Assignment: Build your first own BPMN diagram](#orga41c6de)
        -   [Problem](#org371fb58)
        -   [Solution](#org6a9cfaa)
    -   [Convert an EPC to a BPMN diagram](#org8ebc151)
        -   [Problem](#org3471f92)
        -   [Solution](#orgb128f7b)
    -   [Car purchase process](#org9b938a7)
        -   [Problem](#org62a07df)
    -   [Practice session process](#org076f240)
        -   [Problem](#org1eac8b7)
    -   [Supply chain process](#org4185500)
        -   [Problem](#org4a05ebf)
-   [References](#org78c715d)



<a id="orgdb26ca8"></a>

# What will you learn?

-   Business Process Model and Notation
-   Object-oriented process modeling
-   Practice in the Signavio Process Editor


<a id="org3106779"></a>

# BPMN object summary

Business Process Model and Notation (BPMN) 2.0 has four main groups
of shapes or objects. Source: [Lucidchart, 2020](#org5255c17).


<a id="org6531a6e"></a>

## Flow objects (Action/Decision)

![img](./img/flow.png)


<a id="org76c5094"></a>

## Connecting objects (Communication)

![img](./img/connecting.png)


<a id="org5594732"></a>

## Participants (Roles/Accountability)

![img](./img/pools.png)


<a id="orgc0733bd"></a>

## Artifacts (Details)

![img](./img/artifacts.png)

-   Groups
-   Documents
-   Annotation
-   Message (data)


<a id="orge6a2a4f"></a>

## More information

For Signavio Process Manager, open the "Getting started" sidebar
inside the Process Manager explorer window under "Help".

![img](./img/signavio.png)

[This Signavio document](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm) gives a complete, structured account of all
the most relevant aspects of BPMN with many examples (SAP Signavio,
2021).

[This guide from Camunda](https://camunda.com/bpmn/reference/) (with link to a free BPMN online editor),
is also very good and complete.


<a id="org02dbec7"></a>

# BPMN case studies


<a id="org9a31233"></a>

## Eating icecream

Creating and explaining this model takes about as much time as
eating a big icecream (7 min) - [Link](https://youtu.be/BwkNceoybvA?t=346).

![img](./img/icecream.png)


<a id="orgdbc783b"></a>

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


<a id="org79b509f"></a>

## IT service

This example is (for now) only available in German.

Video: [BPMN 2.0 Prozessmodell in Signavio erzeugen.](https://youtu.be/kYK9t8fPkAY)

![img](./img/german.png)


<a id="orgc782d0e"></a>

# Pizza example


<a id="orgfc44dff"></a>

## Choreography

![img](./img/choreography.png)


<a id="orga8d97d3"></a>

## Collaboration

![img](./img/collaboration.png)


<a id="org79bf789"></a>

## Enterprise modeling with BPMN

[GitHub: Enterprise Modeling with BPMN (PDF)](https://github.com/birkenkrahe/mod482/blob/main/10_bpmn/bpmn_modeling.pdf)

![img](./img/presentation.png)


<a id="org220c542"></a>

# Practice I

![img](./img/practice.gif)


<a id="orgbdf8351"></a>

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


<a id="org7a821ae"></a>

## BPMN diagram with mistakes


<a id="org0f92c6d"></a>

### Problem

Which rule violations can you see in the following diagram
(GitHub)? The total number is<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> = 8 errors - I count a total of
11 additional rule violations. So the total is closer to 20.

![img](./img/error.png)


<a id="org2407229"></a>

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


<a id="orgec965b7"></a>

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


<a id="orgeea3dbc"></a>

# Practice II

![img](./img/practice2.gif)


<a id="org6d13cdd"></a>

## Written BPMN test on November 4 at 2.30 pm

Topics:

-   BPMN objects
-   BPMN rules and rule violations
-   BPMN workflow


<a id="org843b964"></a>

## Assignment: Job application process


<a id="org462cf17"></a>

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


<a id="org2c4601b"></a>

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


<a id="orga41c6de"></a>

## Assignment: Build your first own BPMN diagram


<a id="org371fb58"></a>

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


<a id="org6a9cfaa"></a>

### Solution

![img](./img/workflow.png)


<a id="org8ebc151"></a>

## Convert an EPC to a BPMN diagram


<a id="org3471f92"></a>

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


<a id="orgb128f7b"></a>

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


<a id="org9b938a7"></a>

## Car purchase process


<a id="org62a07df"></a>

### Problem

Model the following process using BPMN 2.0:

> A customer wants to buy a car. He goes to a car dealer to pick a
> car. The dealer has several new, and one used car available. The
> customer picks one, pays for the car, and leaves. She's happy now!

*Tip: you don't need two pools for this process, because the
dealer doesn't have much to do.*


<a id="org076f240"></a>

## Practice session process


<a id="org1eac8b7"></a>

### Problem

Model the following process using BPMN 2.0:

> The professor demonstrates the modeling language BPMN. After the
> demonstration, he assigns an exercise to the students. Once the
> assignment is completed, the student submits the solution. The
> professor checks the result before ending the class.

*Tip: model the professor first, then add the student as a second
pool.*


<a id="org4185500"></a>

## Supply chain process


<a id="org4a05ebf"></a>

### Problem

Model the following supply chain process using BPMN 2.0:

> The process begins with a material purchase request, the Resource
> Manager issues a material requisition. Next, Purchasing issues a
> purchase order for the requested material. When the receipt of the
> purchased items has been received by the Resource Manager, the
> Warehouse inspects the items. Now, Accounting processes the
> vendor’s invoice and the purchase process is finished.

*Tip: think about the number of lanes or pools that you need.*


<a id="org78c715d"></a>

# References

<a id="org5255c17"></a> Lucidchart (Apr 28, 2020). Business Process Model and
Notation (BPMN) 2.0 Tutorial [video]. [Online: youtube.com](https://youtu.be/BwkNceoybvA).

<a id="orga5d12ac"></a> SAP Signavio Process editor version 15.7.1. SAP
(2021). Academic edition [platform]. Online: [www.signavio.com.](https://www.signavio.com/)

<a id="org05a26c1"></a> SAP Signavio (n.d.). BPMN modeling [website]. [Online:
signavio.com](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> According to the Signavio "spell checker" for BPMN 2.0 diagrams.
