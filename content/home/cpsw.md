+++
weight = 1
+++
{{% vertical start %}}

{{% slide preload=true background-iframe="boids.html" transition="zoom" %}}

# Cyber Phisysical Swarm
<h3 class="accent"> <span class="fragment"> Swarm Behaviours </span> <span class="fragment"> {{< fa plus >}} </span> <span class="fragment"> Cyber-Physical Interaction </span> </h3>

---

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

# Why we do care about it?

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

