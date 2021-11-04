
# Table of Contents

-   [What will you learn?](#orgfd2cd5e)
-   [BPMN object summary](#orgaafa2d0)
    -   [Flow objects (Action/Decision)](#org5a23e8b)
    -   [Connecting objects (Communication)](#orgaae739e)
    -   [Participants (Roles/Accountability)](#org3b4b7e4)
    -   [Artifacts (Details)](#orgaba9521)
    -   [More information](#org45bc86b)
-   [BPMN case studies](#orgdf84cab)
    -   [Eating icecream](#org49be54f)
    -   [Job application process](#orgffa2264)
    -   [IT service](#orgc39bbec)
-   [Pizza example](#orgcc717f2)
    -   [Choreography](#org4381983)
    -   [Collaboration](#org697000d)
    -   [Enterprise modeling with BPMN](#org7c40e12)
-   [Practice I](#org7209e4c)
    -   [BPMN rules](#org183736f)
    -   [BPMN diagram with mistakes](#org6441543)
        -   [Problem](#orgcf3159a)
        -   [Solution](#org6d9528f)
    -   [Assignment (complete by Nov 2, 2.30 pm)](#org94d1b7e)
-   [Practice II](#org81e3269)
    -   [Written BPMN test on November 4 at 2.30 pm](#orgdbe5c23)
    -   [Assignment: Job application process](#org666edf4)
    -   [Assignment: Build your first own BPMN diagram](#orga966cb3)
    -   [Convert an EPC to a BPMN diagram](#orgcca13f0)
    -   [Car purchase process](#orgaabc130)
        -   [Problem](#org15638da)
    -   [Practice session process](#org9b5146c)
        -   [Problem](#org54ed2e3)
    -   [Supply chain process](#org46993ac)
        -   [Problem](#org2e22da6)
-   [References](#org3e983e9)



<a id="orgfd2cd5e"></a>

# What will you learn?

-   Business Process Model and Notation
-   Object-oriented process modeling
-   Practice in the Signavio Process Editor


<a id="orgaafa2d0"></a>

# BPMN object summary

Business Process Model and Notation (BPMN) 2.0 has four main groups
of shapes or objects. Source: [Lucidchart, 2020](#orga97c04e).


<a id="org5a23e8b"></a>

## Flow objects (Action/Decision)

![img](./img/flow.png)


<a id="orgaae739e"></a>

## Connecting objects (Communication)

![img](./img/connecting.png)


<a id="org3b4b7e4"></a>

## Participants (Roles/Accountability)

![img](./img/pools.png)


<a id="orgaba9521"></a>

## Artifacts (Details)

![img](./img/artifacts.png)

-   Groups
-   Documents
-   Annotation
-   Message (data)


<a id="org45bc86b"></a>

## More information

For Signavio Process Manager, open the "Getting started" sidebar
inside the Process Manager explorer window under "Help".

![img](./img/signavio.png)

[This Signavio document](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm) gives a complete, structured account of all
the most relevant aspects of BPMN with many examples (SAP Signavio,
2021).

[This guide from Camunda](https://camunda.com/bpmn/reference/) (with link to a free BPMN online editor),
is also very good and complete.


<a id="orgdf84cab"></a>

# BPMN case studies


<a id="org49be54f"></a>

## Eating icecream

Creating and explaining this model takes about as much time as
eating a big icecream (7 min) - [Link](https://youtu.be/BwkNceoybvA?t=346).

![img](./img/icecream.png)


<a id="orgffa2264"></a>

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


<a id="orgc39bbec"></a>

## IT service

This example is (for now) only available in German.

Video: [BPMN 2.0 Prozessmodell in Signavio erzeugen.](https://youtu.be/kYK9t8fPkAY)

![img](./img/german.png)


<a id="orgcc717f2"></a>

# Pizza example


<a id="org4381983"></a>

## Choreography

![img](./img/choreography.png)


<a id="org697000d"></a>

## Collaboration

![img](./img/collaboration.png)


<a id="org7c40e12"></a>

## Enterprise modeling with BPMN

[GitHub: Enterprise Modeling with BPMN (PDF)](https://github.com/birkenkrahe/mod482/blob/main/10_bpmn/bpmn_modeling.pdf)

![img](./img/presentation.png)


<a id="org7209e4c"></a>

# Practice I

![img](./img/practice.gif)


<a id="org183736f"></a>

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


<a id="org6441543"></a>

## BPMN diagram with mistakes


<a id="orgcf3159a"></a>

### Problem

Which rule violations can you see in the following diagram
(GitHub)? The total number is<sup><a id="fnr.1" class="footref" href="#fn.1">1</a></sup> = 8 errors - I count a total of
11 additional rule violations. So the total is closer to 20.

![img](./img/error.png)


<a id="org6d9528f"></a>

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


<a id="org94d1b7e"></a>

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


<a id="org81e3269"></a>

# Practice II

![img](./img/practice2.gif)


<a id="orgdbe5c23"></a>

## Written BPMN test on November 4 at 2.30 pm

Topics:

-   BPMN objects
-   BPMN rules and rule violations
-   BPMN workflow


<a id="org666edf4"></a>

## Assignment: Job application process

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

[[Solutions]​](https://github.com/birkenkrahe/admin/blob/main/mod482.org)


<a id="orga966cb3"></a>

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


<a id="orgcca13f0"></a>

## Convert an EPC to a BPMN diagram

You saw this diagram [in the lecture on modeling and EPCs](https://github.com/birkenkrahe/mod482/tree/main/9_modeling_epc#flow).

![img](./img/convert.png)

Unfortunately, this diagram violates an EPC rule. Can you tell
which one?<sup><a id="fnr.2" class="footref" href="#fn.2">2</a></sup>. I've cleaned it up (also avoiding the loop but
retaining all the important information) in the diagram
below. Convert this diagram ([Signavio](https://academic.signavio.com/p/editor?id=6a471b2d78384fc4b278ceb678f675ee)) into a BPMN 2.0 diagram!

For simplicity use only BPMN 2.0 **core** elements (i.e. no
intermediate events). But you can overload tasks with a `loop`
attribute and set a `loop maximum` value by opening the
`Attributes|Views` sidepanel on the right side of the editor.

![img](./img/convert1.png)


<a id="orgaabc130"></a>

## Car purchase process


<a id="org15638da"></a>

### Problem

Model the following process using BPMN 2.0:

> A customer wants to buy a car. He goes to a car dealer to pick a
> car. The dealer has several new, and one used car available. The
> customer picks one, pays for the car, and leaves. She's happy now!

*Tip: you don't need two pools for this process, because the
dealer doesn't have much to do.*


<a id="org9b5146c"></a>

## Practice session process


<a id="org54ed2e3"></a>

### Problem

Model the following process using BPMN 2.0:

> The professor demonstrates the modeling language BPMN. After the
> demonstration, he assigns an exercise to the students. Once the
> assignment is completed, the student submits the solution. The
> professor checks the result before ending the class.

*Tip: model the professor first, then add the student as a second
pool.*


<a id="org46993ac"></a>

## Supply chain process


<a id="org2e22da6"></a>

### Problem

Model the following supply chain process using BPMN 2.0:

> The process begins with a material purchase request, the Resource
> Manager issues a material requisition. Next, Purchasing issues a
> purchase order for the requested material. When the receipt of the
> purchased items has been received by the Resource Manager, the
> Warehouse inspects the items. Now, Accounting processes the
> vendor’s invoice and the purchase process is finished.

*Tip: think about the number of lanes or pools that you need.*


<a id="org3e983e9"></a>

# References

<a id="orga97c04e"></a> Lucidchart (Apr 28, 2020). Business Process Model and
Notation (BPMN) 2.0 Tutorial [video]. [Online: youtube.com](https://youtu.be/BwkNceoybvA).

<a id="org01005cc"></a> SAP Signavio Process editor version 15.7.1. SAP
(2021). Academic edition [platform]. Online: [www.signavio.com.](https://www.signavio.com/)

<a id="orgd96d31e"></a> SAP Signavio (n.d.). BPMN modeling [website]. [Online:
signavio.com](https://documentation.signavio.com/suite/en-us/Content/process-manager/userguide/bpmn/modeling.htm)


# Footnotes

<sup><a id="fn.1" href="#fnr.1">1</a></sup> According to the Signavio "spell checker" for BPMN 2.0 diagrams.

<sup><a id="fn.2" href="#fnr.2">2</a></sup> The second XOR operator has not two but three outgoing events,
and the flow splits without an operator. The third event was put in so
that the loop does not become infinite in case the wrong password is
entered more than twice. The problem is that an event has been
forgotten: "wrong password entered" vs. "correct password entered".
