
+++
weight = 2
+++
{{% vertical start %}}

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

{{% row %}}
{{% fragment class="col" %}}
#### Gradient Cast
Brodcast information from *sink* nodes
{{% /fragment %}}

{{% fragment class="col" %}}
#### Collecting Cast
Collect data into *sink* nodes
{{% /fragment %}}

{{% fragment class="col" %}}
#### Sparse Choice
Distributed leader election
{{% /fragment %}}

{{% /row %}}

{{% fragment %}} {{< fa thumbs-up >}}  {{% accent c="**Self-organising blocks**" %}} {{% /fragment %}}  

---

# What can we do with Aggregate Computing? # {.r-fit-text}
## Relevant examples {.accent }

{{% row %}}
{{% fragment class="col" %}}
#### Crowd Engineering
{{% highlight c="High-Level API" %}}
{{% /fragment %}}

{{% fragment class="col" %}}
#### Distributed Reslint Sensing
{{% highlight c="SCR pattern" %}}
{{% /fragment %}}

{{% fragment class="col" %}}

#### Concurrent Activities
{{% highlight c="Aggregate Processess" %}}

{{% /fragment %}}

{{% /row %}}

---

# Why Aggregate Computing?
{{% frag-list kind="ul" %}}

{{% frag-li %}} {{% accent c="**Is practical!**" %}} {{% /frag-li %}}
{{% frag-list kind="ul" %}} 
{{% frag-li %}} Programming Languages: [ScaFi](https://scafi.github.io/), [Protelis](http://protelis.github.io/), [FCPP](https://fcpp.github.io/) {{% /frag-li %}}
{{% frag-li %}} Simulation Framework: [Alchemist](http://alchemistsimulator.github.io/) {{% /frag-li %}}
{{% frag-li %}} Simulation Framework: [Playground](https://scafi.github.io/web) {{% /frag-li %}}

{{% /frag-list %}} 
{{% frag-li %}} {{% accent c="**Relevant properties have been proven !**" %}} {{% /frag-li %}}
{{% frag-list kind="ul" %}} 
{{% frag-li %}} [Self-stabilization](https://ieeexplore.ieee.org/document/7306598) {{% /frag-li %}}
{{% frag-li %}} [Time-space universalily](https://link-springer-com.ezproxy.unibo.it/chapter/10.1007/978-3-319-92408-3_1) {{% /frag-li %}}
{{% frag-li %}} [Eventual Consistency](https://ieeexplore.ieee.org/abstract/document/7774387/) {{% /frag-li %}}

{{% /frag-list %}} 
{{% /frag-list %}}

{{% vertical end %}}
