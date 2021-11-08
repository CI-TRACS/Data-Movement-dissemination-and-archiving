---
title: "Using Globus and Rclone"
teaching: 15
exercises: 5
questions:
- "When to use Globus"
- "when to use Rclone"
objectives:
- "Setup Globus"
- "Use Globus to transfer data"
- "Setup RClone with Google Drive"
- "Transfer files with Rclone"
keypoints:
- ""
---
# Data Transfer Workshop


<img src="../assets/img/globus_rclone/globus_and_rclone0.png" width=500px />

<img src="../assets/img/globus_rclone/globus_and_rclone1.png" width=414px />

# Introduction

<img src="../assets/img/globus_rclone/globus_and_rclone2.jpg" width=500px />

<img src="../assets/img/globus_rclone/globus_and_rclone3.png" width=500px />

<img src="../assets/img/globus_rclone/globus_and_rclone4.png" width=500px />

Globus is a service that makes it easy to move\, sync\, and share large amounts of data\.

Globus will manage file transfers\, monitor performance\, retry failures\, recover from faults automatically when possible\, and report the status of your data transfer\.

Globus uses GridFTP for more reliable and high\-performance file transfer\, and will queue file transfers to be performed asynchronously in the background\.

Globus was developed and is maintained at the University of Chicago and is used extensively at supercomputer centers and major research facilities\. _[https://globus\.org](https://globus.org)_

# When To use Globus

To transfer or share data between two Globus managed endpoints \(e\.g\. two multi\-user systems at different universities\, each running a Globus server\)

To transfer data between a managed endpoint \(e\.g\. UH\-HPC\) to a Globus Connect Personal endpoint \(e\.g\. your desktop\)

# Globus Plus

For some kinds of data transfer or sharing\, you need Globus Plus\. The UH Globus subscription includes Globus Plus for all users\, but you need to to request a Globus Plus invite\.

To transfer data between two Globus Connect Personal endpoints \(e\.g\. your desktop system and a laptop\)\.

To share data from a Globus Connect Personal endpoint \(e\.g\. your desktop system\)

To transfer data from/to a shared endpoint that is hosted on a Globus Connect Personal endpoint\.

Note 1: if your collaborator needs Globus Plus to download data\, and is not at UH\, we cannot provide Globus Plus to that person\.

Note 2: By default\, files on a Globus Connect Personal endpoint \(e\.g\. your laptop or desktop\) may not be shareable\. You will need to configure that via the instructions at these links: Linux\, Mac\, Windows\.

# Transfering Files with Globus

<span style="color:#595959">Creating a Globus Account Using Your UH Credential</span>

<span style="color:#595959">Installing Globus Connect Personal</span>

<span style="color:#595959">Transferring Data from and to Mana</span>

__Creating a Globus Account Using UH Credential__

<span style="color:#595959">Visit</span>  <span style="color:#595959"> _[www\.globus\.org](https://www.globus.org/)_ </span>  <span style="color:#595959">and click "Login" at the top of the page\. On the Globus login page\, type in University of Hawaii\. When you find it\, click Continue\.</span>

<img src="../assets/img/globus_rclone/globus_and_rclone5.png" width=500px />

# You’ll be redirected to your UH login page. Use your UH credentials to login.

<img src="../assets/img/globus_rclone/globus_and_rclone6.png" width=500px />

# Some organizations will ask for your permission to release your account information to Globus. Once you’ve logged in with your UH credentials, Globus will ask if you’d like to link to an existing account. If this is your first time logging in to Globus, click "Continue." If you’ve already used another account with Globus, you can choose "Link to an existing account."

<img src="../assets/img/globus_rclone/globus_and_rclone7.png" width=500px />

# You may be prompted to provide additional information such as your organization and whether or not Globus will be used for commercial purposes. Click on non-profit research or educational purposes. Complete the form and click "Continue."

<img src="../assets/img/globus_rclone/globus_and_rclone8.png" width=500px />

# Finally, you need to give Globus permission to use your identity to access information and perform actions (like file transfers) on your behalf.

<img src="../assets/img/globus_rclone/globus_and_rclone9.png" width=500px />

# Globus Connect Personal

<span style="color:#595959">Globus Connect Personal turns your laptop or other personal computer into a Globus endpoint with just a few clicks\. With Globus Connect Personal you can share and transfer files to/from a local machine—campus server\, desktop computer or laptop—even if it's behind a firewall and you don't have administrator privileges\.</span>

<span style="color:#595959">Globus Connect Personal puts the power of Globus on your computer\.</span>

<span style="color:#595959">Dramatically increases data transfer speeds over scp and other transfer tools\.</span>

<span style="color:#595959">Automatically suspends transfers when computer sleeps and resumes when turned on\.</span>

<span style="color:#595959">Installs in seconds using native operating system install packages\.</span>

<span style="color:#595959">Works with firewalls that block incoming connections\, and behind most NATs\.</span>

<span style="color:#595959">Uses proven Globus infrastructure for security and authentication\.</span>

# Installation Instructions

__Installing Globus Connect Personal__

_[Globus Connect Personal for Mac](https://docs.globus.org/how-to/globus-connect-personal-mac)_  __for Mac OS X 10\.7 or higher \(Intel only\)__

_[Globus Connect Personal for Linux](https://docs.globus.org/how-to/globus-connect-personal-linux)_  __for common x86\-based distributions__

_[Globus Connect Personal for Windows](https://docs.globus.org/how-to/globus-connect-personal-windows)_  __for recent Windows versions__

__Note: Once you are done installing GCP\, the Globus Connect Personal agent will be running in the background\. Once you disconnect from it\, you can__  __launch__  __the application again by__  __clicking__  __“command\+space bar” keys on Mac machine or Windows key on Windows machine and typing “globus” to select the application to restart it\.__

# Transferring Data from and to Mana Using Globus Connect Personal

# The File ManagerAfter you’ve signed up and logged in to Globus, you’ll begin at the File Manager.

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

<img src="../assets/img/globus_rclone/globus_and_rclone21.png" width=300px />

Rclone is a free utility for syncing directories between object storage systems \(such as Amazon S3\, Dropbox\, Google Drive etc\) and file based storage \(e\.g\. /home or /scratch\)\.

<span style="color:#0097A7"> _[https://rclone\.org/](https://rclone.org/)_ </span>

<span style="color:#000000">Note about this tutorial</span>

<span style="color:#595959">Wherever this tutorials uses ‘>’ that means there is a command to execute on the terminal/shell</span>

<span style="color:#595959">Rclone is installed on the Mana Data Transfer Nodes and can be used in the command line via</span>

<span style="color:#595959">> rclone</span>

<span style="color:#000000">Configuring Rclone</span>

<span style="color:#595959">Before you can use Rclone\, you must configure it\. This configuration step will set up access for the remote object storage system that you want to transfer data to and from\.</span>

<span style="color:#595959">In this tutorial we will configure Google Drive since UH has Google for Education and everyone at UH has it\.</span>

<span style="color:#595959">Get a shell session on Mana  \- your own terminal or you can use Open OnDemand via</span>  <span style="color:#0097A7"> _[https://mana\.its\.hawaii\.edu](https://mana.its.hawaii.edu)_ </span>  <span style="color:#595959">and select from the Menu</span>

<span style="color:#595959">Clusters  \->   >\_Mana\_Shell\_Access</span>

<span style="color:#595959">From your terminal/shell ssh to one of the Mana DTNs</span>

<span style="color:#595959">>ssh</span>  <span style="color:#0097A7"> _[username@hpc\-dtn1\.its\.hawaii\.edu](mailto:username@hpc-dtn01.its.hawaii.edu)_ </span>

<span style="color:#595959">Your may be prompted for your password depending on where you are SSHing from and you WILL be prompted for DUO two\-factor verification\.</span>

<span style="color:#595959">\[seanbc@login002 ~\]$ ssh hpc\-dtn1\.its\.hawaii\.edu</span>

<span style="color:#595959">Duo two\-factor login for seanbc</span>

<span style="color:#595959">Enter a passcode or select one of the following options:</span>

<span style="color:#595959">1\. Duo Push to XXX\-XXX\-5555</span>

<span style="color:#595959">2\. Phone call to XXX\-XXX\-5555</span>

<span style="color:#595959">3\. SMS passcodes to XXX\-XXX\-5555 \(next code starts with: 4\)</span>

<span style="color:#595959">Passcode or option \(1\-3\): 1</span>

<span style="color:#595959">Pushed a login request to your device\.\.\.</span>

<span style="color:#595959">Success\. Logging you in\.\.\.</span>

<span style="color:#595959">\[seanbc@hpc\-dtn1 ~\]$</span>

<span style="color:#000000">Step 1 \- Configure RClone to use GDrive</span>

<span style="color:#595959">> rclone config</span>

<span style="color:#595959">2021/01/29 16:16:25 Failed to load config file "/home/xxxx/\.rclone\.conf" \- using defaults: open /home/xxxx/\.rclone\.conf: no such file or directory</span>

<span style="color:#595959">No remotes found \- make a new one</span>

<span style="color:#595959">n\) New remote</span>

<span style="color:#595959">s\) Set configuration password</span>

<span style="color:#595959">q\) Quit config</span>

<span style="color:#595959"> __Type "n" to set up a new object storage system with which to transfer data\.__ </span>

<span style="color:#000000">Choose a name for the remote object storage system</span>

<span style="color:#595959">You'll be prompted for the name of the remote object storage system\, we use "rclone\-gdrive" in this tutorial</span>

<span style="color:#595959">name> rclone\-gdrive</span>

<span style="color:#000000">Select Storage System \- Google Drive 13</span>

<span style="color:#595959">10 / Encrypt/Decrypt a remote</span>

<span style="color:#595959">\\ "crypt"</span>

<span style="color:#595959">11 / FTP Connection</span>

<span style="color:#595959">\\ "ftp"</span>

<span style="color:#595959">12 / Google Cloud Storage \(this is not Google Drive\)</span>

<span style="color:#595959">\\ "google cloud storage"</span>

<span style="color:#595959">13 / Google Drive</span>

<span style="color:#595959">\\ "drive"</span>

<span style="color:#595959">Storage> 13</span>

<span style="color:#595959">There will be a long list of options to choose from \- Google Drive is 13</span>

<span style="color:#000000">Select Google Client \- we will use Rclone’s for now</span>

<span style="color:#595959">Storage> 13</span>

<span style="color:#595959">\*\* See help for drive backend at: https://rclone\.org/drive/ \*\*</span>

<span style="color:#595959">Google Application Client Id</span>

<span style="color:#595959">Setting your own is recommended\.</span>

<span style="color:#595959">See</span>  <span style="color:#595959"> _https://rclone\.org/drive/\#making\-your\-own\-client\-id_ </span>  <span style="color:#595959">for how to create your own\.</span>

<span style="color:#595959">If you leave this blank\, it will use an internal key which is low performance\.</span>

<span style="color:#595959">Enter a string value\. Press Enter for the default \(""\)\.</span>

<span style="color:#595959">client\_id></span>

<span style="color:#000000">Client Secret \- leave it blank</span>

<span style="color:#595959">OAuth Client Secret</span>

<span style="color:#595959">Leave blank normally\.</span>

<span style="color:#595959">Enter a string value\. Press Enter for the default \(""\)\.</span>

<span style="color:#595959">client\_secret></span>

<span style="color:#000000">Pick Rclone’s scope \- choose 1 \- so we can read & write</span>

<span style="color:#595959">Scope that rclone should use when requesting access from drive\.</span>

<span style="color:#595959">Enter a string value\. Press Enter for the default \(""\)\.</span>

<span style="color:#595959">Choose a number from below\, or type in your own value</span>

<span style="color:#595959">1 / Full access all files\, excluding Application Data Folder\.</span>

<span style="color:#595959">\\ "drive"</span>

<span style="color:#595959">2 / Read\-only access to file metadata and file contents\.</span>

<span style="color:#595959">\\ "drive\.readonly"</span>

<span style="color:#595959">/ Access to files created by rclone only\.</span>

<span style="color:#595959">3 | These are visible in the drive website\.</span>

<span style="color:#595959">| File authorization is revoked when the user deauthorizes the app\.</span>

<span style="color:#595959">\\ "drive\.file"</span>

<span style="color:#595959">/ Allows read and write access to the Application Data folder\.</span>

<span style="color:#595959">4 | This is not visible in the drive website\.</span>

<span style="color:#595959">\\ "drive\.appfolder"</span>

<span style="color:#595959">/ Allows read\-only access to file metadata but</span>

<span style="color:#595959">5 | does not allow any access to read or download file content\.</span>

<span style="color:#595959">\\ "drive\.metadata\.readonly"</span>

<span style="color:#595959">scope> 1</span>

<span style="color:#000000">Set the “root” folder \- Rclone can only read files in this folder and it’s sub\-folders</span>

<span style="color:#595959">ID of the root folder</span>

<span style="color:#595959">Leave blank normally\.</span>

<span style="color:#595959">Fill in to access "Computers" folders \(see docs\)\, or for rclone to use</span>

<span style="color:#595959">a non root folder as its starting point\.</span>

<span style="color:#595959">Enter a string value\. Press Enter for the default \(""\)\.</span>

<span style="color:#595959">root\_folder\_id></span>

<span style="color:#000000">Service Account \- leave blank</span>

<span style="color:#595959">Service Account Credentials JSON file path</span>

<span style="color:#595959">Leave blank normally\.</span>

<span style="color:#595959">Needed only if you want use SA instead of interactive login\.</span>

<span style="color:#595959">Leading \`~\` will be expanded in the file name as will environment variables such as \`$\{RCLONE\_CONFIG\_DIR\}\`\.</span>

<span style="color:#595959">Enter a string value\. Press Enter for the default \(""\)\.</span>

<span style="color:#595959">service\_account\_file></span>

<span style="color:#000000">Edit config? \- No</span>

<span style="color:#595959">edit advanced config? \(y/n\)</span>

<span style="color:#595959">y\) Yes</span>

<span style="color:#595959">a non root folder as its starting point\.</span>

<span style="color:#595959">n\) No \(default\)</span>

<span style="color:#595959">y/n> n</span>

<span style="color:#000000">Use Auto config \- No</span>

<span style="color:#595959">Remote config</span>

<span style="color:#595959">Use auto config?</span>

<span style="color:#595959">\* Say Y if not sure</span>

<span style="color:#595959">\* Say N if you are working on a remote or headless machine</span>

<span style="color:#595959">y\) Yes \(default\)</span>

<span style="color:#595959">n\) No</span>

<span style="color:#595959">y/n> n</span>

<span style="color:#000000">Verification Code \- go to “your” link in a browser & authorize then copy the code and paste it</span>

<span style="color:#595959">Please go to the following link: https://accounts\.google\.com/o/oauth2/auth?access\_type=offline&client\_id=202264815644\.apps\.googleusercontent\.com&redirect\_uri=urn%3Aietf%3Awg%3Aoaut</span>

<span style="color:#595959">h%3A2\.0%3Aoob&response\_type=code&scope=https%3A%2F%2Fwww\.googleapis\.com%2Fauth%2Fdrive&state=5ewrjlkjsoeR349302323</span>

<span style="color:#595959">Log in and authorize rclone for access</span>

<span style="color:#595959">Enter verification code></span>  <span style="color:#595959">2334sdffouiewk32EESKDLF324234</span>

<span style="color:#000000">Configure as team drive \- No</span>

<span style="color:#595959">Configure this as a team drive?</span>

<span style="color:#595959">y\) Yes</span>

<span style="color:#595959">n\) No \(default\)</span>

<span style="color:#595959">y/n> n</span>

<span style="color:#000000">Approve setup \- Yes</span>

<span style="color:#595959">\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-</span>

<span style="color:#595959">\[rclone\-gdrive\]</span>

<span style="color:#595959">type = drive</span>

<span style="color:#595959">token = \{"access\_token":"ya29\.a0sdjlkfjwoerjkfsldalsfKSDSD\_$49fKFJDIs02934dsFSDKL"\,"token\_type":"Bearer"\,"refresh\_token":"1//06sejlksfdjlsjfoERE034sREPKSLKCEPROE"\,"expiry":"2021\-02\-02T17:39:51\.393440573Z"\}</span>

<span style="color:#595959">\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-</span>

<span style="color:#595959">y\) Yes this is OK \(default\)</span>

<span style="color:#595959">e\) Edit this remote</span>

<span style="color:#595959">d\) Delete this remote</span>

<span style="color:#595959">y/e/d> y</span>

<span style="color:#000000">Finished Setup \- Quit config</span>

<span style="color:#595959">Current remotes:</span>

<span style="color:#595959">Name                 Type</span>

<span style="color:#595959">====                 ====</span>

<span style="color:#595959">rclone\-gdrive        drive</span>

<span style="color:#595959">e\) Edit existing remote</span>

<span style="color:#595959">n\) New remote</span>

<span style="color:#595959">d\) Delete remote</span>

<span style="color:#595959">r\) Rename remote</span>

<span style="color:#595959">c\) Copy remote</span>

<span style="color:#595959">s\) Set configuration password</span>

<span style="color:#595959">q\) Quit config</span>

<span style="color:#595959">e/n/d/r/c/s/q> q</span>

<span style="color:#000000">Lets list files from GDrive</span>

<span style="color:#595959">‘lsf’ is how we list files using Rclone</span>

<span style="color:#595959">> rclone lsf rclone\-gdrive:/</span>

<span style="color:#000000">Lets create a directory to transfer files to/from</span>

<span style="color:#595959">Make a directory called “rclonefiles” using  the “mkdir” command</span>

<span style="color:#595959">> mkdir rclonefiles</span>

<span style="color:#595959">Move into the directory we just created</span>

<span style="color:#595959">> cd rclonefiles</span>

<span style="color:#595959">‘cd’ is the change directory command</span>

<span style="color:#000000">Create a test document for transfer</span>

<span style="color:#595959">In google drive create a folder name it “rclonetest”\.  Within that folder create a new doc and call it “testfile”\.</span>

<span style="color:#595959">Now copy the directory contents from GDrive to Mana\. ‘rclone copy’ has a source and destination required\. GDrive being the source in the example below and the current directory \(represented by the ‘\.’\) the destination</span>

<span style="color:#595959">> rclone copy rclone\-gdrive:/rclonetest \.</span>

<span style="color:#595959">This will copy the folder contents to the current directory \- Note the ‘\.’ at the end this is represents the current directory as the destination folder \- we could also have used ~/rclonefiles or /home/username/rclonefiles as that same folder path\.</span>

<span style="color:#000000">Lets transfer a file from Mana to GDrive</span>

<span style="color:#595959">Create a testfile2\.docx</span>  <span style="color:#595959">on the Mana DTN by copying testfile\.docx</span>

<span style="color:#595959">> cp testfile\.docx testfile2\.docx</span>

<span style="color:#595959">‘cp’ is the copy command in the terminal/shell</span>

<span style="color:#595959">> ls</span>

<span style="color:#595959">testfile2\.docx  testfile\.docx</span>

<span style="color:#595959">‘ls’ is how we list files in the terminal/shell</span>

<span style="color:#595959">Now copy testfile2\.docx to GDrive \( the source is the Mana testfile2\.docx and the destination is gdrive\)</span>

<span style="color:#595959">>rclone copy testfile2\.docx rclone\-gdrive:/rclonetest</span>

<span style="color:#595959">You can check GDrive and the file should appear</span>

<span style="color:#595959">The ‘rclone copy’ command is the way to move files to or from GDrive\.</span>

<span style="color:#595959">The copy command on a folder will overwrite files that have the same name but if a files exists on the destination that isn’t in the folder being copied it will be retained on the destination \(when we get to sync you will see a difference in this behavior\)</span>

<span style="color:#595959">The sync command is useful to keep a folder on GDrive and somewhere else with identical contents \- meaning that if the destination folder has files that do not exist on the source they will be removed \(so be careful\)</span>

<span style="color:#595959">rclone sync  source destination</span>

<span style="color:#595959">Let remove testfile\.docx and sync our rclonefiles folder to our GDrive rclonetest folder</span>

<span style="color:#595959">> rm testfile\.docx</span>

<span style="color:#595959">> rclone sync  ~/rclonefiles rclone\-gdrive:/rclonetest</span>

<span style="color:#595959">We should see in GDrive that now only testfile2\.docx is there because the folders are in sync \- Mana’s rclonefiles folder was the source so the GDrive rclonetest folder is now identical to rclonefiles</span>

<span style="color:#000000">RClone large transfer \- use nohup</span>

<span style="color:#595959">For transfers that make take a long time that you do not wish to observe or that your connection might disconnect you should use ‘nohup’ so they run in the background until complete\. Example of nohup ‘rclone copy’ below:</span>

<span style="color:#595959">> nohup rclone copy source destination > nohup\.out &</span>

<span style="color:#595959">The ‘>’ after the destination will direct any standard output to be written to the nohup\.out file and the ‘&’ on the end tells the shell to disconnect the command issued and run it in the background so you can still use your terminal/shell for other commands or exiting the session \- the command issued with ‘nohup’ will continue to run\.</span>

<span style="color:#000000">Rclone documentation</span>

<span style="color:#595959">More information about Rclone and Google Drive can be found here:</span>

<span style="color:#0097A7"> _[https://rclone\.org/drive/\#limitations](https://rclone.org/drive/#limitations)_ </span>

<span style="color:#595959">You can download for your machine her</span>  _[https://rclone\.org/downloads/](https://rclone.org/downloads/)_

<span style="color:#595959">Note \- there is an experimental GUI for your laptop/workstation</span>  _[https://rclone\.org/gui/](https://rclone.org/gui/)_

# Questions

__?__
