 
+++

title = "Hello Aarhus!"
description = "A presentation about my research interest and topics"
outputs = ["Reveal"]
aliases = [
    "/intro/"
]

+++

# Engineering Cyber Physical Swarms # {class="r-fit-text" }


**Talk @ Aarhus Universitat**

🎤 *Gianluca Aguzzi*

📧 [gianluca.aguzzi@unibo.it](mailto:gianluca.aguzzi@unibo.it)

{{< fa fab github 2 >}} [@cric96](https://github.com/cric96)

{{% today %}}

{{% note %}}
Don't forget to thank the audience.
{{% /note %}}

---

# About Me
{{% fragment %}} PhD Student @ Università di Bologna -- Alma Mater Studiorum  {{% /fragment %}}    
{{% fragment %}} Background on {{% highlight c="Software Engineering" %}} {{% /fragment %}}  
{{% fragment %}} {{% accent c="**Main Research Interests**" %}} {{% /fragment %}}

{{% row %}}
{{% fragment class="col" %}}
{{< image height=50 src="/cas.gif" caption="Large Scale Distributed Systems" >}} 
{{% /fragment %}}
{{% fragment class="col" %}} 
{{% image height=50 src="/collective-artificial-intellingence.gif" caption="Collective Artificial Intelligence" %}}
{{% /fragment %}}
{{% /row %}}

---

<section data-preload data-background-iframe="net.html" data-transition="zoom">

# Table of Content
{{% frag-list kind=ul %}}
{{% frag-li %}} #### Introduction On Cyber-Physical Swarms {{% /frag-li %}}  
{{% frag-li %}} #### Aggregate Computing -- In a nutshell {{% /frag-li %}}  
{{% frag-li %}} #### Main Concept of Multi-Agent (Reinforcement) Learning {{% /frag-li %}}
{{% frag-li %}} #### Preliminary Work & Research Directions {{% /frag-li %}}
{{% /frag-list %}}

</section>

{{% vertical start%}}

<section data-preload data-background-iframe="boids.html">

# Cyber Phisysical Swarm
<h3 class="accent"> <span class="fragment"> Swarm Behaviours </span> <span class="fragment"> {{< fa plus >}} </span> <span class="fragment"> Cyber-Physical Interaction </span> </h3>
</section>

{{< slide background-color="#fdf6e3">}}

# Context

{{% row %}}
{{% fragment class="col" %}} 
#### Many Networked Agents
{{< image height="30" src="/cas.gif" >}} 
{{% /fragment %}}
{{% fragment class="col" %}} 
#### Cyber Physical Systems
{{< image height="30" src="/cas.gif" >}} 
{{% /fragment %}}
{{% fragment class="col" %}} 
#### Collective Behaviour  
{{< image height="30" src="/cas.gif" >}} 
{{% /fragment %}}

{{% /row %}}

---


{{< slide background-color="#fdf6e3">}}

# Why we care about it?

{{% frag-list kind=ul %}}

{{% frag-li %}} Pervasive/Obiquitous Computing {{% /frag-li %}}
{{% frag-li %}} **{{% accent c="Systems of today!" %}}** {{% /frag-li %}}
{{% frag-list kind=ul %}}
  {{% frag-li %}} Swarm Robotics {{% /frag-li %}}
  {{% frag-li %}} Smart Cities {{% /frag-li %}}
  {{% frag-li %}} Large-Scale IoT systems {{% /frag-li %}}
{{% /frag-list %}}
{{% frag-li %}} Traditional "Approaches" are *{{% highlight c=inadequate %}}* {{% /frag-li %}}
{{% /frag-list %}}

---

{{< slide background-color="#fdf6e3">}}

# Examples


{{% row %}}
{{% fragment class="col" %}}
### Swarm Robotics
{{< image height="30" src="/cas.gif">}} 
{{% /fragment %}}
{{% fragment class="col" %}}
### Crowd Engineering
{{< image height="30" src="/cas.gif">}} 
{{% /fragment %}}
{{% fragment class="col" %}}
### Smart Cities
{{< image height="30" src="/cas.gif">}} 
{{% /fragment %}}
{{% /row %}}

---
{{< slide background-color="#fdf6e3">}}

# How??
{{% frag-list kind=ul %}}
{{% frag-li %}} ### Goals {.highlight}
{{% /frag-li %}}
  {{% frag-list kind=ul %}}
  {{% frag-li %}} Robust Collective Behavior {{% /frag-li %}}
  {{% frag-li %}} Self-* Behaviours {{% /frag-li %}}
  {{% frag-li %}} Decoupling from **{{%accent c=Functional %}}** and **{{% accent c=Non-Functional %}}** aspects {{% /frag-li %}}
  {{% /frag-list %}}
{{% frag-li %}} ### Challenges {.highlight} {{% /frag-li %}}
  {{% frag-list kind=ul %}}

  {{% frag-li %}} Distributed Control {{% /frag-li %}}
  {{% frag-li %}} Failures {{% /frag-li %}}
  {{% frag-li %}} Global-to-local mapping {{% /frag-li %}}
  {{% frag-li %}} Uncertanties {{% /frag-li %}}
  {{% /frag-list %}}
{{% /frag-list %}}

---

{{< slide background-color="#fdf6e3">}}

# Inspiration {{< fa fa arrow-right 2 >}} {{%fragment%}} {{< highlight c="Nature" >}} {{%/fragment%}}

{{% row %}}

{{% fragment class="col" %}} 
{{< youtube IpKL-URul2I >}}
###  {{< highlight c="Ants" >}}
{{% /fragment %}}

{{% fragment class="col" %}}  
{{< youtube UNroEwFxh6I >}}
### {{< highlight c="Bees" >}}
{{% /fragment %}}

{{% fragment class="col" %}}  
{{< youtube B6M_XgiONoo >}}
### {{< highlight c="Fish School" >}}
{{% /fragment %}}

{{% /row %}}

---

{{< slide background-color="#fdf6e3">}}

# Engineering "Artifical" Swarms
{{% frag-list kind=ul %}}
{{% frag-li %}} ### Model {.highlight} {{% /frag-li %}} 
{{% frag-list kind=ul %}}
{{% frag-li %}} **How can we describe the dynamics of a systems?** {{% /frag-li %}} 
{{% frag-list kind=ul %}}
{{% frag-li %}} Homogenenous Behaviour {{% /frag-li %}} 
{{% frag-li %}} {{% accent c=Neighborhood %}} or {{% accent c=Environment %}} based interactions {{% /frag-li %}} 
{{% frag-li %}} Proactive execution model {{% /frag-li %}} 
{{% /frag-list %}}
{{% /frag-list %}}
{{% frag-li %}} ### Language Specification {.highlight} {{% /frag-li %}}
{{% frag-list kind=ul %}}
{{% frag-li %}} **How can we specify a collective behaviour?** {{% /frag-li %}} 
{{% frag-list kind=ul %}}
{{% frag-li %}} **{{% accent c="Predicatable Emergent" %}}** Behaviours {{% /frag-li %}} 
{{% frag-li %}} Good abstractions {{% /frag-li %}} 
{{% /frag-list %}}

{{% /frag-list%}}
{{% frag-li %}} ### Simulation {.highlight} {{% /frag-li %}}
{{% frag-list kind=ul %}}
{{% frag-li %}} **How can we verify our collective programs?"** {{% /frag-li %}} 
{{% /frag-list %}}
{{% /frag-list %}}

{{% vertical end %}}

---
{{% vertical start%}}

<section data-preload data-background-iframe="waves.html" data-transition="zoom" data-background-color="black">
  <h1 class="white-text"> Aggregate Computing </h1>
  <h4 class="accent"> Programming the aggregate! </h4>
</section>


{{< slide background-color="#fdf6e3">}}

# Super-Condensed Overview
**{{% highlight c="Aggregate Computing" %}}** {{< fa fa arrow-right 2 >}} A {{% accent c="top-down" %}} *{{% highlight c="global to local" %}}* {{% accent c=functional %}} progromming approach to express {{% accent c="self-organising" %}} collective behaviours


{{% row %}}

{{% fragment class="col" %}}  
### Computational Field {.accent }
{{< image height=50 src="/ac.png"  >}} 
{{% /fragment %}}

{{% fragment class="col" %}}  
### Field Calculus {.accent }
{{< image height=50 src="/high-level-examples.png"  >}} 
{{% /fragment %}}

{{% fragment class="col" %}}  
### Composable API {.accent }
{{< image height=50 src="/full-stack.png"  >}} 
{{% /fragment %}}

{{% /row %}}


**Reference:** J. Beal et al, {{% accent c="Aggregate Programming for the Internet of Things" %}}

--- 

# Computational fields

Distributed space-time data structure {{% accent c="$ \phi: D \rightarrow V $" %}}
{{% frag-list kind=ul %}}
{{% frag-li %}} {{% accent c="E" %}}: a triple {{% accent c="$\langle\delta, t, p\rangle$" %}} – device {{% accent c="$\delta$" %}}, {{% highlight c="**firing**" %}} at time {{% accent c="$t$" %}} in position {{% accent c="$p$" %}} {{% /frag-li %}}  
{{% frag-li %}} {{% accent c="Event domains D" %}}: a coherent set of events (devices cannot move too fast) {{% /frag-li %}}  
{{% frag-li %}} {{%accent c=" field values V" %}}: any data values {{% /frag-li %}}
{{% /frag-list %}}

{{% row %}}
{{% fragment class="col" %}}  
### Constant
{{< image height=20 src="/constant.png"  >}}
{{% /fragment %}}
{{% fragment class="col" %}}  
### Input (Sensors)
{{< image height=20 src="/sensor.png"  >}}
{{% /fragment %}}
{{% fragment class="col" %}}   
### Actuations
{{< image height=20 src="/actuation.png"  >}} 
{{% /fragment %}}

{{% /row %}}

---

# Main Constructs
## Field calculus {.accent}
{{% fragment %}} **{{% highlight c="Conceptually" %}}**: $ \phi \rightarrow \phi$ {{% /fragment %}}
{{% row %}}
{{% fragment class="col" %}}  
**Field Evolution**
```scala
def rep[X](init: => X)(evolution: X => X): X
```
{{% /fragment %}}
{{% fragment class="col" %}}  
**Neighborhood Interaction**

```scala
def nbr[X](query: => X): X
def foldhood[X]
  (init: => X)
  (accumulator: (X, X) => X)
  (query: => X): X
```
{{% /fragment %}}
{{% fragment class="col" %}}  
**Domain Partition**
```scala
def branch[X]
  (condition: Boolean)
  (th: => X)
  (el: => X): X
```
{{% /fragment %}}
{{% /row %}}

{{% fragment %}} {{< fa thumbs-up >}}  {{% accent c="**Space-time Universal**" %}} {{% /fragment %}}  

{{% fragment %}} {{< fa thumbs-up >}}  {{% accent c="**Global interpretation**" %}} {{% /fragment %}}  

---

# Execution Model
Proactive and Periodioc execution of **{{% accent c="rounds" %}}** 
{{% row %}}
{{% col %}}
{{% frag-list kind="ol" %}}
{{% frag-li "fade-in" "0" %}} 
#### Context Acquisition {.highlight}
- Sensors Data
- Neighborhood Information

{{% /frag-li %}}

{{% frag-li "fade-in" 1 %}}
#### Program Evaluation {.highlight} 
-  **Export** Generation 
{{% /frag-li %}}
{{% frag-li "fade-in" 2 %}} 
#### Context Action {.highlight}
- **Export** Sharing
- Actuations 
{{% /frag-li %}}
{{% /frag-list %}}
{{% /col %}}
{{% col class="r-stack" %}}

{{% fragment class="fade-in" index="0" %}}
{{< image height=30 src="/execution-steps-0.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="1" %}}
{{< image height=30 src="/execution-steps-1.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="2" %}}
{{< image height=30 src="/execution-steps-2.png" >}} 
{{% /fragment %}}

{{% /col %}}
{{% /row %}}

---

# What can we do with Aggregate Computing? # {.r-fit-text}
## Collective pattern {.accent } 


---

# What can we do with Aggregate Computing? # {.r-fit-text}
## Relevant examples {.accent } 

---


# Why Aggregate Computing?

---
{{% vertical end %}}
{{< slide transition="zoom" >}}

{{% vertical start%}}

# Research Directions

{{< fragment >}} Hybrid Programing Model: Learning {{% fa solid plus %}} Programming {{< /fragment >}}  
{{< fragment >}} Flexible Deployment of Collective Application {{< /fragment >}}  

---

# Broad Impact


- {{< fragment >}} Hybrid Programing Model: Learning {{% fa solid plus %}} Programming {{< /fragment >}}  
- {{% fragment %}} Flexible Deployment of Collective Application {{% /fragment %}}  

{{% vertical end %}}

---


