---
title: "Using Rclone"
teaching: 1
exercises: 1
question:
- "How do I Configure Rclone?"
- "How do I move data from Globus to my machine?"
objectives:
- "Move sample data from a repository to Globus, then to your computer to Globus"
---

# Using Rclone
---

<img src="../assets/img/globus_rclone/globus_and_rclone21.png" width=600px />

- Rclone is a free utility for syncing directories between object storage systems (such as Amazon S3, Dropbox, Google Drive etc) and file based storage (e.g. home or scratch))

https://rclone.org

---
# Rclone in MANA

Rclone is installed on the Mana Data Transfer Nodes and can be used in the command line via 

~~~
$ rclone
~~~
{: .language-bash}

# Configuring Rclon

Before you can use Rclone, you must configure it 
This configuration step will set up access for the remote object storage system that you want to transfer data to and from
In this tutorial we will configure Google Drive since UH has Google for Education and everyone at UH has it

# Open a Shell Session on MANA
1.) Start a shell session on MANA through your own terminal or you can use Open OnDemand via https://mana.its.hawaii.edu

Clusters -> >_Mana_Shell_Access

From your terminal/shell ssh to one of the Mana DTNs

~~~
$ ssh username@hpc-dtn1.its.hawaii.edu
~~~
{: .language-bash}

*You may be prompted for your password depending on where you are SSHing from and you WILL be prompted for DUO two-factor verification.

# Two Factor Authentication
Example 

~~~
$ ssh luketn@hpc-dtn1.its.hawaii.edu
~~~
{: .language-bash}

<img src="/fig/RClone 1.png" width=600px />

---

Two Factor Authentication for Duo Push
~~~
$ 1
~~~
{: .language-bash}

Two Factor Authentication for Phone Call
~~~
$ 2
~~~
{: .language-bash}

Two Factor Authentication for SMS
~~~
$ 3
~~~
{: .language-bash}


<img src="/fig/Rclone 2.png" width=600px />
---

# Configuring Rclone

~~~
$ rclone config
~~~
{: .language-bash}

<img src="/fig/RClone 3.png" width=600px />

---

~~~
$ n
~~~
{: .language-bash}

<span style="color:#595959">No remotes found \- make a new one</span>

<span style="color:#595959">n\) New remote</span>

<span style="color:#595959">s\) Set configuration password</span>

<span style="color:#595959">q\) Quit config</span>

---

<span style="color:#000000">Choose a name for the remote object storage system</span>

<img src="/fig/RClone4.png" width=600px />

<span style="color:#595959">You'll be prompted for the name of the remote object storage system\, we use "rclone\-gdrive" in this tutorial</span>

<span style="color:#595959">name> rclone\-gdrive</span>

<img src="/fig/R Clone6.png" width=600px />

---

# Choosing a Storage Option

~~~
$ 15
~~~
{: .language-bash}

<img src="/fig/RClone7.png" width=600px />

- Choose #15, Google Drive as Storage Option
** See help for drive backend at: https://rclone\.org/drive/ **

---

# Google Application Client Id

*Setting your own is recommended, see https://rclone\.org/drive/\#making\-your\-own\-client\-id for how to create your own.
- If you leave this blank, it will use an internal key which is low performance.
- I leave this blank in my tutorial

Client Secret
- I also leave this blank in my tutorial

OAuth Client Secret
- Leave blank normally.

Scope
- 1 / Full access all files, excluding Application Data Folder.
   \ "drive"

- 2 / Read-only access to file metadata and file contents.
   \ "drive.readonly"
   / Access to files created by rclone only.
- 3 | These are visible in the drive website.
   | File authorization is revoked when the user deauthorizes the app.
   \ "drive.file"
   / Allows read and write access to the Application Data folder.
- 4 | This is not visible in the drive website.
   \ "drive.appfolder"
   / Allows read-only access to file metadata but
- 5 | does not allow any access to read or download file content.
   \ "drive.metadata.readonly"
<img src="/fig/RClone8.png" width=600px />

~~~
$ 1
~~~
{: .language-bash}

<img src="/fig/RClone9.png" width=600px />

---

Leave ID of the root folder blank normally

<img src="/fig/RClone10.png" width=600px />

---
# Auto Configuration

~~~
$ n
~~~
{: .language-bash}

<img src="/fig/RClone13.png" width=600px />

---

You should receive a verifiable link after configuration is complete

<img src="/fig/RClone14.png" width=600px />

---

# Google Validation

<img src="/fig/RClone16.png" width=400px />

---
# Copy Validation Code and Enter in MANA

<img src="/fig/RClone21.png" width=400px />

---
# Configuring of Google Drive

<img src="/fig/Rcloneconfig.png" width=400px />

~~~
$ y
~~~
{: .language-bash}

---

-Do not configure as a team drive

<img src="/fig/RClone20.png" width=600px />

~~~
$ n
~~~
{: .language-bash}

- Quit Configuration
~~~
$ q
~~~
{: .language-bash}

---

# Now we can list files from GDrive
- ‘lsf’ is how we list files using Rclone

~~~
$ rclone lsf rclone-gdrive:/
~~~
{: .language-bash}

<img src="/fig/Rclonesuccess.png" width=600px />

---

# Now we can create a directory to transfer files to/from MANA/GDrive
- Make a directory called “rclonefiles” using the “mkdir” command

~~~
$ mkdir rclonefiles
~~~
{: .language-bash}

- Move into the directory we just created

~~~
$ cd rclonefiles
~~~
{: .language-bash}

- ‘cd’ is the change directory command

---

# Create a test document for transfer

In google drive create a folder name it “rclonetest” 

<img src="/fig/RCloneGD1.png" width=300px />

Within that folder create a new doc and call it “testfile”

<img src="/fig/RCloneGD2.png" width=300px />

---

# Copying the directory contents from GDrive to Mana

‘rclone copy’ has a source and destination required

GDrive being the source in the example below and the current directory (represented by the ‘.’) the destination

~~~
$ rclone copy rclone-gdrive:/rclonetest .
~~~
{: .language-bash}

This will copy the folder contents to the current directory - Note the ‘.’ at the end this is represents the current directory as the destination folder - we could also have used ~/rclonefiles or /home/username/rclonefiles as that same folder path.

---

# MANA to GDrive

- Create a testfile2.docx on the Mana DTN by copying testfile.docx

~~~
$ cp testfile.docx testfile2.docx
~~~
{: .language-bash}


<img src="/fig/Rclonecp.png" width=300px />

‘cp’ is the copy command in the terminal/shell

~~~
$ ls
~~~
{: .language-bash}

---

# Now copy testfile2.docx to GDrive 
The source is the Mana testfile2.docx and the destination is gdrive

~~~
$ rclone copy testfile2.docx rclone-gdrive:/rclonetest
~~~
{: .language-bash}

---

You can check GDrive and the file should appear!
<img src="/fig/rclonetf.png" width=300px />

---

The copy command on a folder will overwrite files that have the same name but if a files exists on the destination that isn’t in the folder being copied it will be retained on the destination (when we get to sync you will see a difference in this behavior)

The sync command is useful to keep a folder on GDrive and somewhere else with identical contents - meaning that if the destination folder has files that do not exist on the source they will be removed (so be careful)

---

# Rclone sync source destination

Let's remove testfile.docx and sync our rclonefiles folder to our GDrive rclonetest folder

~~~
$ rm testfile.docx
~~~
{: .language-bash}


~~~
$ rclone sync ~/rclonefiles rclone-gdrive:/rclonetest
~~~
{: .language-bash}

We should see in GDrive that now only testfile2.docx is there because the folders are in sync - Mana’s rclonefiles folder was the source so the GDrive rclonetest folder is now identical to rclonefiles

RClone large transfer - use nohup

For transfers that make take a long time that you do not wish to observe or that your connection might disconnect you should use ‘nohup’ so they run in the background until complete. Example of nohup ‘rclone copy’ below:

~~~
$ nohup rclone copy source destination > nohup.out &
~~~
{: .language-bash}

The ‘>’ after the destination will direct any standard output to be written to the nohup.out file and the ‘&’ on the end tells the shell to disconnect the command issued and run it in the background so you can still use your terminal/shell for other commands or exiting the session - the command issued with ‘nohup’ will continue to run.

---

# Rclone documentation

More information about Rclone and Google Drive can be found here:

https://rclone.org/drive/#limitations

You can download for your machine her https://rclone.org/downloads/

Note - there is an experimental GUI for your laptop/workstation https://rclone.org/gui/

### Questions?

