 
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
{{% timeline start %}} 
PhD Student @ Università di Bologna -- Alma Mater Studiorum  
{{% timeline end %}}    
{{% timeline start %}} 
Background on Software Engineering 
{{% timeline end %}}  
{{% timeline start %}} 
**Main Research Interests** 
{{% timeline end %}}
{{% row %}}
{{% timeline start "fade-in col" %}} 
{{< image height=50 src="/cas.gif" caption="Large Scale Distributed Systems" >}} 
{{% timeline end %}}
{{% timeline start "fade-in col" %}} 
{{% image height=50 src="/collective-artificial-intellingence.gif" caption="Collective Artificial Intelligence" %}} 
{{% timeline end %}}

{{% /row %}}

---

# Table of Content
{{% frag-list kind=ul %}}
{{% frag-li %}} #### Introduction On Cyber-Physical Swarms {{% /frag-li %}}  
{{% frag-li %}} #### Aggregate Computing -- In a nutshell {{% /frag-li %}}  
{{% frag-li %}} #### Main Concept of Multi-Agent (Reinforcement) Learning {{% /frag-li %}}
{{% frag-li %}} #### Preliminary Work & Research Directions {{% /frag-li %}}
{{% /frag-list %}}

---

{{% vertical start%}}

<section data-preload data-background-iframe="boids.html" data-transition="zoom">
  <h1> Cyber Phisysical Swarm </h1>
  <h3 class="accent"> <span class="fragment"> Swarm Behaviours </span> <span class="fragment"> {{< fa plus >}} </span> <span class="fragment"> Cyber-Physical Interaction </span> </h3>
</section>

{{< slide background-color="#fdf6e3">}}

# Context

{{% row %}}
{{% timeline start "fade-in col" %}} 
#### Many Networked Agents
 
{{< image height="30" src="/cas.gif" >}} 

{{% timeline end %}}

{{% timeline start "fade-in col" %}} 
#### Cyber Physical Systems
 {{< image height="30" src="/cas.gif" >}} 

{{% timeline end %}}

{{< timeline start  "fade-in col" >}}

#### Collective Behaviour  
{{< image height="30" src="/cas.gif" >}} 

{{% timeline end %}}

{{% /row %}}

---


{{< slide background-color="#fdf6e3">}}

# Why we care about it?

{{% frag-list kind=ul %}}

{{% frag-li %}} Pervasive/Obiquitous Computing {{% /frag-li %}}
{{% frag-li %}} Systems of today! {{% /frag-li %}}
{{% frag-list kind=ul %}}
  {{% frag-li %}} Swarm Robotics {{% /frag-li %}}
  {{% frag-li %}} Smart Cities {{% /frag-li %}}
  {{% frag-li %}} Large-Scale IoT systems {{% /frag-li %}}
{{% /frag-list %}}
{{% frag-li %}} Traditional "Approaches" are inadequates {{% /frag-li %}}
{{% /frag-list %}}

---

{{< slide background-color="#fdf6e3">}}

# Examples


{{% row %}}
{{% timeline start "col"  %}} 
### Swarm Robotics
{{< image height="30" src="/cas.gif">}} 
{{% timeline end %}}
{{% timeline start "col"  %}} 
### Crowd Engineering
{{< image height="30" src="/cas.gif">}} 
{{% timeline end %}}
{{% timeline start "col"  %}} 
### Smart Cities
{{< image height="30" src="/cas.gif">}} 
{{% timeline end %}}
{{% /row %}}

---
{{< slide background-color="#fdf6e3">}}

# How??
{{% frag-list kind=ul %}}
{{% frag-li %}} ### Goals 
{{% /frag-li %}}
  {{% frag-list kind=ul %}}
  {{% frag-li %}} Robust Collective Behavior {{% /frag-li %}}
  {{% frag-li %}} Self-* Behaviours {{% /frag-li %}}
  {{% frag-li %}} Decoupling from **Functional** and **Non-Functional** aspects {{% /frag-li %}}
  {{% /frag-list %}}
{{% frag-li %}} ### Challenges {{% /frag-li %}}
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

{{% timeline start "fade-in col" %}} 

{{< youtube IpKL-URul2I >}}
###  {{< highlight c="Ants" >}}

{{% timeline end %}}

{{% timeline start "fade-in col" %}} 
{{< youtube UNroEwFxh6I >}}
### {{< highlight c="Bees" >}}

{{% timeline end %}}

{{% timeline start "fade-in col" %}} 

{{< youtube B6M_XgiONoo >}}
### {{< highlight c="Fish School" >}}
{{% timeline end %}}

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
{{% frag-li %}} "Neighborhood" or "Environment" based interactions {{% /frag-li %}} 
{{% frag-li %}} Proactive execution model {{% /frag-li %}} 
{{% /frag-list %}}
{{% /frag-list %}}
{{% frag-li %}} ### Language Specification {.highlight} {{% /frag-li %}}
{{% frag-list kind=ul %}}
{{% frag-li %}} **How can we specify a collective behaviour?** {{% /frag-li %}} 
{{% frag-list kind=ul %}}
{{% frag-li %}} Predicatable Emergent Behaviours {{% /frag-li %}} 
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

<section data-preload data-background-iframe="waves.html" data-transition="zoom">
  <h1 class="white-text"> Aggregate Computing </h1>
  <h4 class="accent"> Programming the aggregate! </h4>
</section>


{{< slide background-color="#fdf6e3">}}
# Super-Condensed Overview

---

{{< slide background-color="#fdf6e3">}}
# Main Constructs

---

{{< slide background-color="#fdf6e3">}}
# Execution Model

---

{{< slide background-color="#fdf6e3">}}
# What can we do with Aggregate Computing? # {.r-fit-text}

---

{{< slide background-color="#fdf6e3">}}
# Relevant examples 

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

## Fallback to shortcodes for resizing


{{< image src="https://upload.wikimedia.org/wikipedia/it/6/6c/Scavolino_innevata.jpg" max-h="20">}}

