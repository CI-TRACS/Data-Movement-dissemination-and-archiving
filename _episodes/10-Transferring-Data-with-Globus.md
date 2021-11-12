---
title: "Transferring Data"
teaching: 1
exercises: 1
questions:
- "How do I move data from my machine to Globus?"
- "How do I move data from Globus to my machine?"
objectives:
- "Move sample data from a repository to Globus, then to your computer to Globus"
keypoints:
- "A collection is a named location containing data you can access with Globus. "
- "Collections can be hosted on many different kinds of systems."
---
# Transferring Data from and to Mana Using Globus Connect Personal

# The File Manager
After you’ve signed up and logged in to Globus, you’ll begin at the File Manager.

<img src="../assets/img/globus_rclone/globus_and_rclone10.png" width=500px />
---

The first time you use the File Manager, all fields will be blank.

<img src="../assets/img/globus_rclone/globus_and_rclone11.png" width=500px />

> ## Tip 

> ### Key Concept: Collection
> A collection is a named location containing data you can access with Globus. Collections can be hosted on many different kinds of systems, including campus storage, HPC clusters, laptops\, Amazon S3 bucket, Google Drive (these are “premium” connectors so seperate a subscription is required), and scientific instruments.
{: .callout}

When you use Globus, you don’t need to know a physical location or details about storage. You only need a collection name. A collection allows authorized Globus users to browse and transfer files. Collections can also be used for sharing data with others and for enabling discovery by other Globus users. [Globus Connect](https://www.globus.org/globus-connect) is used to host collections.

# Access a collection

Click in the Collection field at the top of the File Manager page and type ”UH-HPC". Globus will list collections with matching names. Choose UH-HPC.

<img src="../assets/img/globus_rclone/globus_and_rclone12.png" width=500px />

--- 

Globus will connect to the UH-HPC collection and display the default directory, /~/.  This is your home directory in the Mana Globus endpoint. Click on “Transfer or Sync to”.

<img src="../assets/img/globus_rclone/globus_and_rclone13.png" width=500px />

---

# Request a file transfer

A new collection panel will open\, with a ”Search" field at the top of the panel. Click on it.</span>

<img src="../assets/img/globus_rclone/globus_and_rclone14.png" width=500px />

Click on “Your Collection” tab. Find the Globus Connect Personal endpoint you created earlier and click on it.

<img src="../assets/img/globus_rclone/globus_and_rclone15.png" width=500px />

On the left collection, UH-HPC, select the file you would like to transfer. The Start> button at the top of the panel will activate. Click the Start> button to transfer the selected files to the collection in the right panel.

<img src="../assets/img/globus_rclone/globus_and_rclone16.png" width=500px />

---

Globus will display a green notification panel—​confirming that the transfer request was submitted—​and add a badge to the “Activity” item in the command menu on the left of the page. Click Activity in the command menu on the left of the page to go to the Activity page.

<img src="../assets/img/globus_rclone/globus_and_rclone17.png" width=500px />

Confirm Transfer Completion
- On the Activity page, click the arrow icon on the right to view details about the transfer. You will also receive an email with the transfer details.

<img src="../assets/img/globus_rclone/globus_and_rclone18.png" width=500px />

---

# Activity Page

<img src="../assets/img/globus_rclone/globus_and_rclone19.png" width=500px />

If you notice that the transferred files are not listed in the right panel with your Globus Connect Personal collection. Click the refresh icon (circular arrows) at the top of the collection panel to see the updated contents.

<img src="../assets/img/globus_rclone/globus_and_rclone20.png" width=500px />

---

# Questions about Globus?

{% include links.md %}
