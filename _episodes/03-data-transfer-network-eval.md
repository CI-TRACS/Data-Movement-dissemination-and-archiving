---
title: "Data Transfer Evaluation Of The Network"
teaching: 10
exercises: 0
question:
-
objectives:
-
---

# Network (Only) Evaluation

# Throughput testing

* Iperf3 \(as distinct from "iperf" which is v2 or less\)
  * https://software\.es\.net/iperf/
  * https://github\.com/esnet/iperf
  * Pre\-compiled binaries for \(everything\)
    * https://iperf\.fr/iperf\-download\.php
* nuttcp
  * http://nuttcp\.org/
  * Much overlap with iperf3
  * Allows "3rd party" operation where one machine can initiate tests between 2 other machines

# perfSONAR test nodes

* Provides test endpoints
  * iperf3
  * owping/ping
  * traceroute/tracepath
* Academic and research centric
* Many servers around the world
* Multiple servers within UH Net
* You can install the clients on Linux laptop
  * Which allows you to control remote servers
* perfSONAR toolkit is available as a Docker Container\, which will work on Linux\-based Docker engines\. Getting the networking side working on MacOS or Windows \(or WSL\) is complicated\, if at all possible

# perfSONAR installation options

https://docs\.perfsonar\.net/install\_options\.html

{% include figure.html url="" max-width="50%"
   file="/fig/ep30.png" width=500px alt="" caption="" %}

# LibreSpeedTest

* https://github\.com/librespeed/speedtest
* Take this code and drop it into a directory on any web server
* It will provide a browser\-based throughput estimate for a path
* I have one in my house
* UH has one on Manoa Campus
  * http://speedtest\.uhnet\.net

# LibreSpeedTest On A Home Network

{% include figure.html url="" max-width="50%"
   file="/fig/ep31.png" width=500px alt="" caption="" %}

# Ookla Speedtest (speedtest.net)

* Allows you to test to many points around the world from a web browser\.
  * https://www\.speedtest\.net/
  * Allow page to load and choose: "Change Server"
* Also offers a command line version
  * https://www\.speedtest\.net/apps/cli
    * Whichcould be used to test from a remote machine via a terminal interface
* Important to recognize that it focuses on testing your tester's Internet connectivity\, possibly from multiple server locations
* Distinct from testing between your location and a specific location
* There are Ookla Speedtest servers at some universities\, and if you test from a U\. Hawaii campus to those servers\, they should use REN paths
* Typically\, an ISP hosted server will use commodity paths

{% include links.md %}
