---
title: "Data Movement and Dissemination: Globus and Rclone"
teaching: 5
exercises: 2
questions:
- "What does Globus do and how can I use it with my data?"
- "How does Rclone improve data movement and management?"
objectives:
- "Have a basic understanding of Globus and how to move data"
- "Have a basic understanding of Rclone and how to use it"
- "Able to Move Data to a from Mana HPC using Globus and Rclone"
- "Able to Move Google Drive Data to/from Mana HPC with Rclone"
- "Explain how the Globus works and how to initialize an account."
- keypoints:
- "Globus is useful for transfering data to and from MANA at UH."
- "Rclone is an open source, multi threaded, command line computer program to manage or migrate content on cloud and other high latency storage. Its capabilities    include sync, transfer, crypt, cache, union, and compress data"
---
<img src="../assets/img/globus_rclone/globus_and_rclone0.png" width=500px />

<img src="../assets/img/globus_rclone/globus_and_rclone1.png" width=414px />


### Background

Globus can use several different systems to move data
'Laptop? HPC cluster? Cloud storage? Tape archive? Access them all using just a web browser.

Data stored at a different institution? At a supercomputing facility? All you need is your campus login'

Globus is a service that makes it easy to move, sync, and share large amounts of data.

Globus will manage file transfers, monitor performance, retry failures, recover from faults automatically when possible, and report the status of your data transfer.

Globus uses GridFTP for more reliable and high-performance file transfer, and will queue file transfers to be performed asynchronously in the background.

Globus was developed and is maintained at the University of Chicago and is used extensively at supercomputer centers and major research facilities. https://globus.org

