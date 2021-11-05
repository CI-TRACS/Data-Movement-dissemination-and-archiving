---
title: "Introducing the Globus"
teaching: 5
exercises: 0
questions:
- "What does Globus do and how can I use it with my data??"
objectives:
- "Explain how the Globus works and how to initialize an account."
keypoints:
- "Globus is useful for transfering data to and from MANA at UH."
-  "Globus security is not necessarily guaranteed"
---
### Background

Globus can use several different systems to move data
'Laptop? HPC cluster? Cloud storage? Tape archive? Access them all using just a web browser.

Data stored at a different institution? At a supercomputing facility? All you need is your campus login'

While the visual aid of a GUI makes it intuitive to learn,
this way of delivering instructions to a computer scales very poorly.
Imagine the following task:
for a literature search, you have to copy the third line of one thousand text files in one thousand
different directories and paste it into a single file.
Using a GUI, you would not only be clicking at your desk for several hours,
but you could potentially also commit an error in the process of completing this repetitive task.
This is where we take advantage of the Unix shell.
The Unix shell is both a **command-line interface** (CLI) and a scripting language,
allowing such repetitive tasks to be done automatically and fast.
With the proper commands, the shell can repeat tasks with or without some modification
as many times as we want.
Using the shell, the task in the literature example can be accomplished in seconds.
