
### Creating a Globus account and transferring data
---

### Prerequisite
-  Have duo mobile or other 2 factor authenticator linked to your device and UH account
---
### Creating a Globus Account Using UH Credential
- Visit www.globus.org and click "Login" at the top of the page. On the Globus login page, type in University of Hawaii. When you find it, click Continue.
- You’ll be redirected to your UH login page. Use your UH credentials to login.
- Some organizations will ask for your permission to release your account information to Globus
- Once you've logged in with your UH credentials, Globus will ask if you want to link to an existing account. If this is your first time using Globus, just "Continue"
- You may be prompted to provide additional information such as your organization and whether or not Globus will be used for commercial purposes. Click on non-profit research or educational purposes. Complete the form and click "Continue."
- Finally, you need to give Globus permission to use your identity to access information and perform actions (like file transfers) on your behalf.
---
### Advantages of Globus Connect Personal
---
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

- 

