+++
weight = 5
+++

{{% vertical start %}}

# Collective Program Sketching
### Aggregate Computing {{< fa solid plus >}} (Hysteretic) Q-Learning {.accent} 

**Reference:** G. Aguzzi et al, {{% accent c="Towards Reinforcement Learning-based Aggregate Computing" %}}

---

## High-Level idea {.accent}

{{%row%}}
{{%fragment%}}
{{< image height=30 src="/synthesis-1.png"  >}}
#### Aggregate Program
{{%/fragment%}}

{{%fragment%}}
{{< image height=30 src="/synthesis-2.png"  >}}
#### System-Dynamic Specific Part {{%accent c="(Hole)" %}}
{{%/fragment%}}

{{%fragment%}}

{{< image height=30 src="/synthesis-3.png"  >}}
#### Fill the Hole through {{%accent c="Experience" %}}
{{%/fragment%}}

{{%/row%}}

---

# Execution Model
## Revised {.accent}

{{% col class="r-stack" %}}
{{% fragment class="fade-in" index="0" %}}
{{< image height=30 src="/structure-revised-1.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="1" %}}
{{< image height=30 src="/structure-revised-2.png" >}}
{{% /fragment %}}
{{% fragment class="fade-in" index="2" %}}
{{< image height=30 src="/structure-revised-3.png" >}}
{{% /fragment %}}
{{% fragment class="fade-in" index="3" %}}
{{< image height=30 src="/structure-revised-4.png" >}}
{{% /fragment %}}
{{% /col %}}

---

# Learning Settings

{{% row %}}
{{% fragment class="col" index="0" %}}
{{%accent c="**Multi Agent Systems**" %}}
{{% /fragment %}}

{{% fragment class="col" index="1" %}}
{{%accent c="**Homogenous Behaviour**" %}}
{{% /fragment %}}

{{% fragment class="col" index="2" %}}
{{%accent c="**Centralised Traning Decentralised Execution**" %}}
{{% /fragment %}}
{{% /row %}}

{{% col class="r-stack" %}}
{{% fragment class="fade-in" index="0" %}}
{{< image height=30 src="/algorithm-learning-1.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="1" %}}
{{< image height=30 src="/algorithm-learning-2.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="2" %}}
{{< image height=30 src="/algorithm-learning-3.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="3" %}}
{{< image height=30 src="/algorithm-learning-4.png" >}} 
{{% /fragment %}}
{{% fragment class="fade-in" index="4" %}}
{{< image height=30 src="/algorithm-learning-5.png" >}} 
{{% /fragment %}}
{{% /col %}}

---

# Case Study
## Improve Gradient Cast {.accent}

{{% frag-list kind="ul" %}}
{{% frag-li %}} Gradient Cast Main block for collective behavior {{% /frag-li %}}
{{% frag-list kind="ul" %}}
{{% frag-li %}} Broadcast information {{% /frag-li %}}
{{% frag-li %}} Team formation {{% /frag-li %}}
{{% frag-li %}} High-Level pattern {{% /frag-li %}}
{{% /frag-list %}}
{{% frag-li %}} The behaviour could depend of the environment dynamics {{% /frag-li %}}
{{% frag-list kind="ul" %}}
{{% frag-li %}} Several Issues: non-smooth output, slow-rising problem, problem with highly-dynamic nodes  {{% /frag-li %}}
{{% frag-li %}} Typical approach: {{%highlight c="ad-hoc heuristic" %}} {{% /frag-li %}}
{{% /frag-list %}}
{{% /frag-list %}}

---

# Preliminary Result
## Handle slow rising problem {.accent}
{{%frag-list kind="ul"%}}
{{%frag-li%}} {{%accent c="**State**"%}}: a window of neighbours output {{%/frag-li%}}
{{%frag-li%}} {{%accent c="**Actions**"%}}: decrease or increase output {{%/frag-li%}}
{{%frag-li%}} {{%accent c="**Reward**"%}}: 0 if the output is the same of an oracle, -1 otherwise {{%/frag-li%}}
{{%/frag-list%}}
{{%fragment%}}
{{< image height=40 src="/output-many-nodes.png" >}} 
{{%/fragment%}}

{{%frag-list kind="ul"%}}
{{%/frag-list%}}

---

# Addressing Collective Computation Efficency {.r-fit-text}
### Distributed Schedulers through Q-Learning {.accent} 

**Reference:** G. Aguzzi et al, {{% accent c="Addressing Collective Computations Efficiency through Reinforcement Learning" %}}

---

# High-Level Idea
### Adjust local scheduling following environment condition {.accent}
{{% frag-list kind="ul" %}}
{{% frag-li "fade-in" "0" %}} The Aggregate Computing model {{%accent c="does not"%}} enforce a global-synchronization {{% /frag-li %}}
{{% frag-li "fade-in" "1" %}} Current Implementation {{% highlight c="{{% fa solid arrow-right %}}" %}} Periodic possibly async execution {{% /frag-li %}}
{{% frag-li "fade-in" "2" %}} Frontier: {{% accent c="Time-Fluid Field-Based Coordination through Programmable Distributed Schedulers" %}}   {{% /frag-li %}}
{{% frag-li "fade-in" "3" %}} **{{% accent c="Reinforcement Learning"%}}** agent tunes the local node schedulers {{% /frag-li %}}
{{% /frag-list %}}

---

# Integration perspective
### Learning goals {.accent}
{{% frag-list kind="ul" %}}
{{% frag-li "fade-in" %}} Reducing the collective power consumption {{%frag c="{{% fa solid arrow-right %}} **{{% accent c=green %}} {{% accent c=computing %}}** " %}} {{% /frag-li %}}
{{% frag-li "fade-in" %}} Improve collective computation convergence time {{% /frag-li %}}
{{% frag-li "fade-in" %}} Multi-Objective problems {{% /frag-li %}}
{{% frag-list kind="ul" %}}
{{% frag-li %}} Configurable balance between performance w.r.t. consumption {{% /frag-li %}}
{{% /frag-list %}}
{{% /frag-list %}}


---

# Case Study
### Reduce the Power consumption of self-stabilizing Building blocks {.accent}

{{% frag-list kind="ul" %}}
{{%frag-li%}} {{%accent c="**State**"%}}: local output derivate {{%/frag-li%}}
{{%frag-li%}} {{%accent c="**Actions**"%}}: next wake-up time {{%/frag-li%}}
{{%frag-li%}} {{%accent c="**Reward**"%}}: near 0 if the output is stable, -1 in the other cases  {{%/frag-li%}}
{{% /frag-list %}}


{{% fragment class="col" %}}
#### Result overview {.highlight}
{{< image height=30 src="/image-rl-500-plain.png" >}} 
{{% /fragment %}}


---

# What we learn so far
## Challenges {.accent}

{{%frag-list kind="ul"%}}
{{%frag-li%}} Multi-agent credit assignment problem {{%/frag-li%}}
{{%frag-li%}} Multi-objective goals {{%/frag-li%}}
{{%frag-li%}} Hand-crafted state encoding are inadequate (variable neighborhood) {{%/frag-li%}}
{{%frag-li%}} Environment partial observability {{%/frag-li%}}

{{%/frag-list%}}

{{% vertical end %}}

---

{{% slide preload=true background-iframe="waves-thanks.html" transition="zoom" background-color="black" %}}

# Thank you! {.white-text }