---
title: "Processes and Queues"
teaching: 10
exercises: 0
questions:
- "What are Queues/Buffers?"
- "How does data actually move from machine to machine?"
objectives:
- "Understand the processes involved in transfering data from one machine to another."
keypoints:
- "There are many processes in transfering data that can cause bottlenecks and degrade performance, the network is only one of many of those."
---

# Queues (also known as buffers)

Queues are places where things arrive to wait for something

Data waits in queues for a chance to be transmitted further

> ## Queues are the reason that everything in the universe isn't stuck waiting for everything else.
{: .callout}

<img src="/fig/ep40.jpg" width=500px alt="Attribution: © Vulphere Wikimedia Commons CC BY 4.0 https://creativecommons.org/licenses/by/4.0/deed.en"/>

<img src="/fig/ep41.png" width=500px />

<img src="/fig/ep42.png" width=500px />

<img src="/fig/ep43.png" width=500px />

<img src="/fig/ep43.png" width=500px />

<img src="/fig/ep44.png" width=500px />

# Notable Points

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
