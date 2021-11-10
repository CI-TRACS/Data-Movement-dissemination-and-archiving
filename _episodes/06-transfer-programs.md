---
title: "Transfer Programs"
teaching: 10
exercises: 0
question:
-
objectives:
-
---

# $0.02 About Transfer Programs

> ## Scp\, sftp\, rsync\, other SSH\-based
>  * Very accessible
>  * Have a problem with long\-haul
>    * [https://www\.psc\.edu/hpn\-ssh\-home/hpn\-ssh\-faq/](https://www\.psc\.edu/hpn\-ssh\-home/hpn\-ssh\-faq/)
>    * Can be patched to work very better\, if you are invested in an ssh\-based workflow
>  * Common tools in this category are single\-threaded
>    * Versus supportingparallel transfers
{: .callout}

> ## GridFTP \(including Globus GridFTP\)
>  * Breaks files into small pieces\, transfers many pieces concurrently\, and reassembles them at the receiving end
>  * Tends to get better performance out of networks with symptoms\.
>  * May not tend to get better performance out of transfer paths with other problems
>  * Authentication and licensing might present obstacles to use in ad\-hoc workflows
{: .callout}

> ## Lftp
>  * Very versatile \(Russian origin\) program with features such as mirroring and parallel transfers
{: .callout}

{% include figure.html url=""
   file="/fig/ep60.png" width=500px alt="" caption="" %}

{% include links.md %}
