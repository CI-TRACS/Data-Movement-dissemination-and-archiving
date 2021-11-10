---
title: "Processes and Queues"
teaching: 10
exercises: 0
question:
-
objectives:
-
---

# Queues (also known as buffers)

Queues are places where things arrive to wait for something

Data waits in queues for a chance to be transmitted further

> ## Queues are the reason that everything in the universe isn't stuck waiting for everything else.
{: .callout}

{% include figure.html url="" 
   file="/fig/ep40.jpg" width=500px alt="" caption="" %}

<span style="color:#202122"> __Attribution:__ </span>  <span style="color:#202122"> __© Vulphere / Wikimedia Commons / CC BY 4\.0__ </span>

<span style="color:#202122"> __https://creativecommons\.org/licenses/by/4\.0/deed\.en__ </span>

{% include figure.html url="" 
   file="/fig/ep41.png" width=500px alt="" caption="" %}

{% include figure.html url="" 
   file="/fig/ep42.png" width=500px alt="" caption="" %}

{% include figure.html url="" "
   file="/fig/ep43.png" width=500px alt="" caption="" %}

{% include figure.html url="" 
   file="/fig/ep44.png" width=500px alt="" caption="" %}

# A Salient Point

* Data moves by processes:
  * Enqueuing data
  * Dequeuing data
* Some Network queues have "easy" adjustments because
  * the large variation in latency
  * Optimizations vary by use-case
* Storage systems benefit from design choices
* Most defaults support many users sharing a resource
* Our use case is more about committing entire machines to a single purpose

{% include links.md %}
