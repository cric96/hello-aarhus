+++
weight = 4
+++

{{% vertical start %}}
{{% slide background-image=background-marl.jpg background-opacity=0.3 preload=true %}}

# Multi-Agent Reinforcement Learning {.r-fit-text }
## Overview {.accent}


---

## Reinforcement Learning
{{% col class="r-stack" %}}

{{% fragment  index="0" %}}
{{< image height=35 src="/rl-1.png" >}} 
{{% /fragment %}}

{{% fragment index="1" %}}
{{< image height=35 src="/rl-2.png" >}} 
{{% /fragment %}}

{{% fragment index="2" %}}
{{< image height=35 src="/rl-3.png" >}} 
{{% /fragment %}}

{{% /col %}}
{{% fragment index="3" %}}
**Simple**, but **flexible** and {{% accent c="**extremely powerful**" %}}
{{% /fragment %}}
{{% row %}}
{{% fragment index="4" class="col" %}}
#### DQN in Atari
{{% youtube TmPfTpjtdgg %}}
{{% /fragment %}}

{{% fragment index="5" class="col" %}}

#### Alpha Zero
{{% youtube 7L2sUGcOgh0 %}}

{{% /fragment %}}

{{% fragment index="6" class="col" %}}

#### Hike And Seek
{{% youtube kopoLzvh5jY %}}

{{% /fragment %}}
{{% /row %}}

---

# From Single-Agent To Multi Agent

{{% accent c="Multiple agents learn together the best policy that maximises a long term reward signal." %}}

---

# Multi-Agent Tasks

{{% row %}}
{{% fragment class="col" index="0" %}}
{{% col class="r-stack" %}}
{{% fragment index="0" %}}
### Cooperative {.highlight}
{{% /fragment %}}
{{% fragment index="3" %}}
### Cooperative {.accent}
{{% /fragment %}}
{{% /col %}}
{{< image height=30 src="/cooperative.jpg" >}} 
{{% /fragment %}}
{{% fragment class="col" index="1" %}}
{{%col%}}### Competitive {.highlight}{{%/col%}}
{{< image height=30 src="/competitive.jpg" >}} 
{{% /fragment %}}
{{% fragment class="col" index="2" %}}
{{%col%}}### Mixed {.highlight}{{%/col%}}
{{< image height=30 src="/mixed.jpg" >}} 
{{% /fragment %}}
{{% /row %}}

---

# Cooperative Task

{{% row %}}
{{% fragment class="col" index="0" %}}
{{% col class="r-stack" %}}
{{% frag index="0" c="### Homogenous" %}}
{{% frag c="### Homogenous {.accent}" index="6" %}}
{{% /col %}}
{{% frag-list kind="ul" %}}
{{% frag-li "fade-in" 2 %}} each agent has the {{% accent c="same" %}} **capabilities** {{% /frag-li %}}
{{% frag-li "fade-in" 3 %}} **{{% accent c="goal" %}}**: find the same policy that maximise the collective good {{% /frag-li %}}
{{% frag-li "fade-in" 6 %}} typical choice for swarm-like systems {{% /frag-li %}}

{{%/ frag-list %}}
{{% /fragment %}}

{{% fragment class="col" index="1" %}}
### Heterogeneous

{{% frag-li "fade-in" 4 %}} each agent could have {{% accent c="different" %}} **capabilities** {{% /frag-li %}}
{{% frag-li "fade-in" 5 %}}  **{{% accent c="goal" %}}**: maximise each policy to maximise the collective good {{% /frag-li %}}

{{% /fragment %}}

{{% /row %}}

---

# Learning Settings

{{% row %}}
{{% fragment class="col" index="0" %}}
#### Centralised Traning Centralised Execution {.highlight}
{{< image height=30 src="/learning-scheme-clce.jpg" >}} 
{{% /fragment %}}
{{% fragment index="1" class="col" %}}
#### Decentralised Training Decentralised Execution {.highlight }
{{< image height=30 src="/learning-scheme-dtde.jpg" >}} 
{{% /fragment %}}
{{% fragment class="col" index="2" %}}
#### Centralised Training Decentralised Execution  {.highlight}
{{< image height=30 src="/learning-scheme-ctde.jpg" >}} 
{{% /fragment %}}
{{% /row %}}

{{% vertical end %}}
