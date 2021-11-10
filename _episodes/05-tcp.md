---
title: "Transmission Control Protocol (TCP)"
teaching: 10
exercises: 0
question:
-
objectives:
-
---

# Why TCP Acts As It Does

{% include figure.html url="" max-width="50%"
   file="/fig/ep50.png" width=500px alt="" caption="" %}

__Let's say a packet takes 10 milliseconds to travel from sender to receiver\.__

{% include figure.html url="" max-width="50%"
   file="/fig/ep51.png" width=500px alt="" caption="" %}

{% include figure.html url="" max-width="50%"
   file="/fig/ep52.png" width=500px alt="" caption="" %}

__An acknowledgment from receiver to sender would take 10 mS to return to the sender\.__

__If we wait for and acknowledgment for each packet before sending another\, then we can only deliver 1 packet every 20 milliseconds\.__

__Most packets have max size of about 1500 bytes\, so this limits throughput to about 0\.6 Megabits/sec on this 20 mS round\-trip\-time path__

{% include figure.html url="" max-width="50%"
   file="/fig/ep53.png" width=500px alt="" caption="" %}

__If we establish a rule that 10 packets can be sent before any acknowledgment is received by the sender\, then 15\,000 bytes can be sent every 20 milliseconds\, or 6 Megabits per second\.__

__The number of unacknowledged packets is call a TCP window\, more specifically a TCP receive window\, which can be affected by user settings in most computer operating systems\.__

{% include figure.html url="" max-width="50%"
   file="/fig/ep54.png" width=500px alt="" caption="" %}

__\(drawing does not scale\)__

__The throughput benefit of increasing the TCP window is limited on a 20 millisecond RTT path by the transmission speed\.__

__When the window size equals max amount of data that can be sent by the sender's interface during 20 milliseconds\, then making the window larger has no further benefit\.__

__For example\, if the sender has a 1 Gigabit Ethernet interface\, then each 1500 byte packet takes 12\.4 microseconds to transmit\, meaning that TCP window of about 1\,612 packets reaches maximum TCP throughput\.__

__In practice\, this__  __windows__  __size is expressed as 2\.4 Megabytes\. Using the Bandwidth Delay Product equation we're about to develop\, it is estimated at 2\.5 Megabytes__

# TCP Tuning

* Bandwidth Delay Product \(BDP\)
  * TCP receive window = round\_trip\_time \* effective\_bit\_rate
    * "Effective bit rate" is usually the smallest link in a path
    * Round Trip Time is propagation delay\, queuing delay\, backlog delay
  * TCP RWIN max is 2 Gigabytes
  * The max RTT that can support 100 Gbit/sec is 171\.8 milliseconds
    * Meaning: in order to go further\, you'd need more than max window
  * Most modern OS auto\-tune\, but have limits to the auto that can be raised\.
  * Most default limits are insufficient for moving data fast over long distances
* Fasterdata\.es\.net
  * A good resource for research data transfer information including TCP stuff

{% include figure.html url="" max-width="50%"
   file="/fig/ep55.png" width=500px alt="" caption="" %}

{% include figure.html url="" max-width="50%"
   file="/fig/ep56.png" width=500px alt="" caption="" %}

_Bursting_  __\-\-__

__Showing the packets as evenly spaced is not realistic\. The actions of machines made of processes and queues tend to make transfers "bursty"\.__

__Meaning that a 100 Mbps transfer across a 1 Gbps path is really more like small bursts of 1 Gbps packet trains\, with long gaps between them\.__

__If two such bursts from multiple sources arrive at the same queue somewhere in the middle\, some packets may get dropped\.__

{% include figure.html url="" max-width="50%"
   file="/fig/ep57.png" width=500px alt="" caption="" %}

__If we pace the packets so that they're evenly spaced\, the queues have a better chance of passing all packets\.__

__\(This is typically done in practice by using a feature in Linux called "Fair\-Queuing"\)__

__This site addresses using queue pacing \(throttling\) on MacOS__

__https://blog\.leiy\.me/post/bw\-throttling\-on\-mac/__

__\(I have not tried it\)__

# 4 streams, into a 12 Gbps disk system
No FQ pacing, 640 GB in 577 seconds

{% include figure.html url="" max-width="50%"
   file="/fig/ep58.png" width=500px alt="" caption="" %}

{% include figure.html url="" max-width="50%"
   file="/fig/ep59.png" width=500px alt="" caption="" %}

# 4 streams, into a 12 Gbps disk system
3Gb per stream FQ pacing, 640 GB in 487 seconds

{% include figure.html url="" max-width="50%"
   file="/fig/ep510.png" width=500px alt="" caption="" %}

{% include figure.html url="" max-width="50%"
   file="/fig/ep511.png" width=500px alt="" caption="" %}

# Other tuning

* Ethernet driver ring buffers
  * The first and last queues in your network path
* Ethernet Offloading
  * The Ethernet card does such things as TCP segmentation and checksums\, relieving the computer operating system of those tasks
* Ethernet flow control \-\- sometimes mitigates buffer issues
* Storage system \(formerly "disks"\) configuration
  * Multi\-devices under a single volume \(RAID\-1 or mdadm\)
  * high performance files systems
  * If you have a fast\, clean 100G network\, the next limit will be your storage throughput
  * https://fasterdata\.es\.net/science\-dmz/DTN/hardware\-selection/storage/
* MTU \(IP maximum transmission unit\) akin to Ethernet frame size

# Sometimes Less Is More

* If you experience sickly performance due to queue loss
  * You might try reducing the max TCP receive window\, if you can't affect queue pacing
  * Congested paths might get more done whenpresentedwith a lower rate that doesn't cause queue drops
* This is a temporary\, stop\-gap suggestion

# Parallelism

Currently\, up to 10 Gigabit Ethernet can be filled by a typical server grade computer

On 100 Gigabit\,varioustransfer speeds > 80 Gbps have been recorded \(see pic\)

Working 100G flows tend to be 30 Gbps or less

Most transfers over 10 Gbps is using multiple connections

Globus GridFTP opens on the order of several hundred connections at once\.

{% include figure.html url="" max-width="50%"
   file="/fig/ep512.jpg" width=500px alt="" caption="" %}

_PUBLIC DOMAIN IMAGE: https://commons\.wikimedia\.org/wiki/File:Goodwood2007\-121\_The\_Blue\_Flame\.jpg_
