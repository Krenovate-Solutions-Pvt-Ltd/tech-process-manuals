#   **Setup a Server**

At Krenovate, we use the OpenLiteSpeed WordPress to set up interactive client websites and blogs.

##  **OpenLiteSpeed WordPress**

The OpenLiteSpeed WordPress One-Click app is based on a standard WordPress image, but includes several great performance enhancements, including LiteSpeed's popular LSCache optimization plugin. This Wordpress + OpenLiteSpeed + LSCache image tends to be more than 300 times faster than a regular WordPress image!

OpenLiteSpeed WordPress One-Click automatically installs OpenLiteSpeed, LSCache, WordPress and any dependences. It also automates initial setup for components like Object Cache and PHP OPCache to reduce the time it takes to optimize a web server.


## **Setup the Droplet - Quick Start**

###    **Step 1**

1.  DigitalOcean used as Host
2.  <a href="https://marketplace.digitalocean.com/apps/openlitespeed-wordpress" target="_blank">**Setup** </a> an OpenLiteSpeed Server on a $5 droplet server (use recommended size if told otherwise)
3.  Choose a Data center close to the visitor. (Bangalore in India)
4.  Save root password in Password Cred Sheet.
5.  Add a DNS record using IP just created.

###    **Step 2**

From a terminal on your local computer, connect to the server as root. Login to the Droplet (Host) as below:

>   **ssh root@use_your_server_ip**

**Note:** Be sure to substitute the server’s public IP address for use_your_server_ip.


###    **Step 3**

An interactive script that runs, will prompt you for the domain & sub-domain and further questions.

>   **Please input a valid domain:**

>   **Please verify it is correct. [y/N]**

Further questions are explained <a href= "https://marketplace.digitalocean.com/apps/openlitespeed-wordpress" target="_blank">**here**</a>.

### **Step 4**

Setup removal of temporary session files and run **wp_cron**


####  **What is Cron?**

**Cron** is a time-based job scheduling daemon found in Unix-like operating systems, including Linux distributions. Cron runs in the background and tasks scheduled with cron, referred to as “**cron jobs**,” are executed automatically, making cron useful for automating maintenance-related tasks.


#### **Create a Cron job**

Cron tab is already installed. Follow the below link to learn how to create/add/manage a cronjob.

<a href= "https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-ubuntu-1804" target="_blank">**How to use Cron to Automate Tasks**</a>

####    **Delete tmp session files**

1.  Use the below command to delete tml session files:

>   **/30 * * * * find -O3 "/tmp" -ignore_readdir_race -depth -mindepth 1 -name 'sess_*' -type f -cmin +180 -delete

2.  Use below command to run cron every 15 mins:

>   */15 * * * * wget -q -O

**Note:** Don't forget to change the url to the website url.

####    **Disabling CRON job from WordPress**

1.  Navigate to **wp_config.php** file by navigating to public file (/var/www/html/)
2.  Add the following line after WP_DEBUG:

>   **define( ‘'DISABLE_WP_CRON', true );**

The above command will disable WP CRON and use system CRON

<a href= "https://kinsta.com/knowledgebase/disable-wp-cron/#disable-wp-cron" target="_blank">**Refer Link**</a>

### **Security - Prevent File Edits**

In order to maintain the security and avoid any file edits, follow the <a href="https://www.isitwp.com/disable-editors-and-plugin-modifications-entirely/" target="_blank">**below**</a> step:

1.  Add the below code to the wp_config.php file:

>   **(‘DISALLOW_FILE_EDIT', true);**












