#   **Website Maintenance Processes**

At Krenovate, we do weekly maintenance activities for clients who have opted for an AMC. In this section, we will learn about all the activities that need to be undertaken

##  **Software Upgrade**

### **Importance of Software Upgrade**

With every new release, the following benefits can be reaped:

1.  Enhanced security
2.  Cool new features for an enriching experience
3.  Improved speed and performance
4.  Bug fixes for any known issues
5.  Better compatibility

Read more about software upgrade <a href= "https://www.wpbeginner.com/beginners-guide/why-you-should-always-use-the-latest-version-of-wordpress/" target= "_blank">**here**</a>.

### **Updates to be Checked**

On the assigned day of the week, the below updates are checked:

1.  Plugin Updates
2.  WordPress Core updates

### **Activities to be Performed**

In order to check for updates, the following activites need to be performed:

1.  Identify updates required for the client
2.  Perform the update on a development(desktop)/staging server
3.  Test for any broken feature/functionality on the site.
4.  Take a backup of the live site.
5.  Perform all the updates on Live.


##  **Server Reviews**

### **Importance of Server Review**

Below are reasons to review a server:

1.  Proactively and quickly detects outages and protocol failures.
2.  Provides trend identification and capacity planning of the server resources.
3.  Enables you to address unattended situations and performance bottlenecks, that may lead to revenue loss and downtime.
4.  Notifies authorized personnel at your site in the event of a problem.
5.  Helps system admins to verify and confirm the availability and status of the servers and application processes.
6.  Helps you troubleshoot server issues and improve server performance.

### **Activities to be Performed**

To review a Server, on the assigned day of the week, the following activites need to be performed:

1.  Go to all digital ocean accounts and check for unused droplets.
2.  Confirm with the team, and delete (droplets) if unused.
3.  Check for any unusual spike in the Digital Ocean metrics (CPU/Bandwidth Usage). The below image shows an example:

    ![performance](images\Website-Maintenance\performance.jpg)

4.  Report/Investigate in case of spikes
5.  Login to each server (SSH login), take a look at server logs 
6.  You can go to server logs at  `“cd /usr/local/lsws/logs”`
7.  Report/Investigate in case of unusual logs. For example:

    -   stderr.log log files contains LSAPI Childern shortage error

8.  Check storage available and resources usage [using “top”]

    ![tops](images\Website-Maintenance\tops.jpg)

9.  Check for SSL expiries and Fix it.
10. Make sure that the backups are being automatically taken. See [Backups](#backups) below.

##  **Backups**

### **Importance of Backups**

A good backup solution creates a copy of your latest data and stores it safely so that it is available for a quick restore in the case of an unforeseen event, like:

-   Human Error
-   Website Hack
-   Natural Disasters
-   Server Crash or Failure
-   Unsuccessful updates

Read more about Backups <a href= "https://geekflare.com/wordpress-backup-importance/" target= "_blank">**here**</a>.

### **Activities to be Performed**

We have an automatic backup schedule for every client which we manage.

### **How to Setup Backup for a Client**

Follow the steps below in case you have to setup a backup for a client website:

1. We use <a href= "https://updraftplus.com/" target= "_blank">**Updraft**</a> plugin to run our automatic backups.
2.  <a href= "https://updraftplus.com/faqs/how-do-i-install-updraftplus/" target= "_blank">**Install**</a> Updraft Plugin from here: <a href= "https://updraftplus.com/download/" target= "_blank">**"How to install Updraft Plus"**</a>
3.  We use **Dropbox** as our remote storage.
4.  **Connect** Updraft to Dropbox. [ You can get the dropbox credentials from the team ]
5.  Fix a daily Database backup and Weekly Full file backup at night.
6.  Add your name in the settings to receive email notifications in case backup falls.







