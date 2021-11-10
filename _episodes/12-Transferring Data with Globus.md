---
title: "Transferring Data"
teaching: 1
exercises: 1
question:
- "How do I move data from my machine to Globus?"
- "How do I move data from Globus to my machine?"
objectives:
- "Move sample data from a repository to Globus, then to your computer to Globus"
---
### Transferring Data from and to Mana Using Globus Connect Personal
---

# The File Manager
- After you’ve signed up and logged in to Globus, you’ll begin at the File Manager.
-  Have duo mobile or other 2 factor authenticator linked to your device and UH account
<img src="../assets/img/globus_rclone/globus_and_rclone10.png" width=500px />

# The first time you use the File Manager, all fields will be blank.

<img src="../assets/img/globus_rclone/globus_and_rclone11.png" width=500px />

<span style="color:#595959"> __Tip__ </span>

<span style="color:#595959"> __Key Concept:__ </span>  <span style="color:#595959"> _Collection_ </span>

<span style="color:#595959">A collection is a named location containing data you can access with Globus\. Collections can be hosted on many different kinds of systems\, including campus storage\, HPC clusters\, laptops\,</span>  <span style="color:#595959"> _Amazon S3 buckets\, Google Drive_ </span>  <span style="color:#595959"> _\(these are_ </span>  <span style="color:#595959"> _“premium” connectors so seperate subscription is required\)_ </span>  <span style="color:#595959">\, and scientific instruments\.</span>

<span style="color:#595959">When you use Globus\, you don’t need to know a physical location or details about storage\. You only need a collection name\. A collection allows authorized Globus users to browse and transfer files\. Collections can also be used for sharing data with others and for enabling discovery by other Globus users\.</span>  <span style="color:#595959"> _[Globus Connect](https://www.globus.org/globus-connect)_ </span>  <span style="color:#595959">is used to host collections\.</span>

# Access a collection

<span style="color:#595959">Click in the Collection field at the top of the File Manager page and type ”UH\-HPC"\. Globus will list collections with matching names\. Choose UH\-HPC\.</span>

<img src="../assets/img/globus_rclone/globus_and_rclone12.png" width=500px />

# Globus will connect to the UH-HPC collection and display the default directory, /~/.  This is your home directory in the Mana Globus endpoint. Click on “Transfer or Sync to”.

<img src="../assets/img/globus_rclone/globus_and_rclone13.png" width=500px />

# Request a file transfer

<span style="color:#595959">A new collection panel will open\, with a ”Search" field at the top of the panel\. Click on it\.</span>

<img src="../assets/img/globus_rclone/globus_and_rclone14.png" width=500px />

# Click on “Your Collection” tab. Find the Globus Connect Personal endpoint you created earlier and click on it.

<img src="../assets/img/globus_rclone/globus_and_rclone15.png" width=500px />

# On the left collection, UH-HPC, select the file you would like to transfer. The Start> button at the top of the panel will activate. Click the Start> button to transfer the selected files to the collection in the right panel.

<img src="../assets/img/globus_rclone/globus_and_rclone16.png" width=500px />

# Globus will display a green notification panel—​confirming that the transfer request was submitted—​and add a badge to the “Activity” item in the command menu on the left of the page. Click Activity in the command menu on the left of the page to go to the Activity page.

<img src="../assets/img/globus_rclone/globus_and_rclone17.png" width=500px />

# Confirm Transfer CompletionOn the Activity page, click the arrow icon on the right to view details about the transfer. You will also receive an email with the transfer details.

<img src="../assets/img/globus_rclone/globus_and_rclone18.png" width=500px />

# Activity Page

<img src="../assets/img/globus_rclone/globus_and_rclone19.png" width=500px />

# If you notice that the transferred files are not listed in the right panel with your Globus Connect Personal collection. Click the refresh icon (circular arrows) at the top of the collection panel to see the updated contents.

<img src="../assets/img/globus_rclone/globus_and_rclone20.png" width=500px />

# Questions about Globus

__?__

With Globus Connect Personal you can share and transfer files to/from a local machine—campus server, desktop computer or laptop—even if it's behind a firewall and you don't have administrator privileges.
- 1.) Dramatically increases data transfer speeds over scp and other transfer tools
- 2.) Automatically suspends transfers when computer sleeps and resumes when turned on
- 3.) Installs in seconds using native operating system install packages.
- 4.) Uses proven Globus infrastructure for security and authentication.
- 5.) Works with firewalls that block incoming connections, and behind most NATs.
---
### Installing Globus Connect Personal
---
- Globus Connect Personal for Mac for Mac OS X 10.7 or higher (Intel only) https://docs.globus.org/how-to/globus-connect-personal-mac

- Globus Connect Personal for Linux for common x86-based distributions https://docs.globus.org/how-to/globus-connect-personal-linux

- Globus Connect Personal for Windows for recent Windows versions https://docs.globus.org/how-to/globus-connect-personal-windows

*Note: Once you are done installing GCP, the Globus Connect Personal agent will be running in the background. Once you disconnect from it, you can launch the application again by clicking “command+space bar” keys on Mac machine or Windows key on Windows machine and typing “globus” to select the application to restart it.

---
### The File Manager
--- 
After you’ve signed up and logged in to Globus, you’ll begin at the File Manager.

After you’ve signed up and logged in to Globus, you’ll begin at the File Manager.

The first time you use the File Manager, all fields will be blank

### Key Concept: Collection
A collection is a named location containing data you can access with Globus. Collections can be hosted on many different kinds of systems, including campus storage, HPC clusters, laptops, Amazon S3 buckets, Google Drive (these are “premium” connectors so separate subscription is required), and scientific instruments.
When you use Globus, you don’t need to know a physical location or details about storage. You only need a collection name. A collection allows authorized Globus users to browse and transfer files. Collections can also be used for sharing data with others and for enabling discovery by other Globus users. Globus Connect is used to host collections.

--- 
### Accessing a Collection
- Click on 'Collection Field' at the top of the 'File Manager' page and enter "UH-HPC" . Globus will list collections matching your search. Choose UH-HPC
- Globus will connect to the UH-HPC collection and display the default directory /~/
This is your home directory in the MANA Globus endpoint
---
### Request a File Transfer
- A new collection panel will open, with a "Search” field at the top of the panel. Click on it.
- Click on “Your Collection” tab. Find the Globus Connect Personal endpoint you created earlier
and click on it.

- On the left collection, UH-HPC, select the file you would like to transfer
- Press the "Start" button to activate the transfer the selected files (right side collection)
- A green panel will pop up announcing the successful submission of a transfer request
- Click "Activity" in the command menu on the left side of the page, the Activity page should present a checked transfer under recent activity
---
### Troubleshooting Transfer Experience
- If transferred files are not listed under your activity page, try and refresh the uploaded contents at the top of the collections page
---
### Questions?
---

