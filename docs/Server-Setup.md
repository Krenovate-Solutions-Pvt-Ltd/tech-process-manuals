#   **Setup a Server**

At Krenovate, we use the OpenLiteSpeed WordPress to set up interactive client websites and blogs.

##  **OpenLiteSpeed WordPress**

The OpenLiteSpeed WordPress One-Click app is based on a standard WordPress image, but includes several great performance enhancements, including LiteSpeed's popular LSCache optimization plugin. This Wordpress + OpenLiteSpeed + LSCache image tends to be more than 300 times faster than a regular WordPress image!

OpenLiteSpeed WordPress One-Click automatically installs OpenLiteSpeed, LSCache, WordPress and any dependences. It also automates initial setup for components like Object Cache and PHP OPCache to reduce the time it takes to optimize a web server.


## **Setup the Droplet - Quick Start**

###    **Create Droplet**

At Krenovate, DigitalOcean is used as Host. Below are the steps to create a droplet there:

####    **Choose an Image** 

1.    Click -> **Marketplace** -> Search for OpenLiteSpeed Wordpress.     

      ![image](images\image.jpg)

2.    The above step would take you to this <a href="https://marketplace.digitalocean.com/apps/openlitespeed-wordpress" target="_blank">**Page** </a> 

      ![marketplace](images\marketplace.jpg)

####    **Choose a Plan**

* While creating the droplet you will have to choose the size of CPU.
* There are multiple options which can be seen in the image below.
* There are 2 main things to check - CPU and Disk Space. You should choose the CPU option according to the project requirement. 

  ![plan](images\plan.jpg)

!!! Note
    If you are a Tech lead, then the CPU choice should be discussed with the client and then created.

####    **Choose a Data Center**

* Choose a Data center close to the visitor. (Bangalore in India)

    ![datacenter](images\datacenter.jpg)

####    **Authentication - Password**

1.  Create a root password to access Droplet.
2.  Save root password in Password Cred Sheet.

    ![password](images\password.jpg)

!!! Note
    Do not use the SSH Keys.

####    **Finalize & Create**

Complete the below steps to finalize the Droplet:

1. **How many Droplets?** - This is "1"by default.
2. **Choose a hostname** - You can name it as per your requirement.
3. **Select Projects** - Select the relevant project where you want to assign the droplet.

    ![finalise](images\finalise.jpg)

4. Click -> **Create Droplet**

    ![finalise1](images\finalise1.jpg)

5. The progress is shown as below:

    ![progress](images\progress.jpg)


####    **Add a DNS record**

* Add a DNS record using IP just created.

    ![dnsip](images\dnsip.jpg)
  
* Adding a DNS record for the host depends where the domain is. You can read about the the DNS process under [DNS management](DNS-Management.md).

###    **Login to Droplet**

From a terminal on your local computer, connect to the server as root. Login to the Droplet (Host) as below:

        ssh root@use_your_server_ip

!!! Note 
    Make sure to substitute with the Droplet’s IP address.


###    **Script to add Domain**

An interactive script that runs, will prompt you for the domain & sub-domain and further questions.

    Please input a valid domain:
    Please verify it is correct. [y/N]

You can also automatically apply Let's Encrypt SSL if your domain is pointed to this server already. Enter y and your email address to finish the process.

    Do you wish to issue a Let's encrypt certificate for this domain? [y/N]
    Please enter your E-mail:
    Please verify it is correct: [y/N]


Once finished, you should see Certificate has been successfully installed…

    Do you wish to force HTTPS rewrite rule for this domain? [y/N]

Enter y to force HTTPS rules to be applied

    Do you wish to update the system which include the web server? [Y/n]

This script will automatically go away after your domain has been added.

For more information, refer <a href= "https://marketplace.digitalocean.com/apps/openlitespeed-wordpress" target="_blank">**here**</a>.

### **Setup removal of Temp session files**

Setup removal of temporary session files and run **wp_cron**

#### **Create a Cron job**

Cron tab is already installed. Follow the below link to learn how to create/add/manage a cronjob.

<a href= "https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-ubuntu-1804" target="_blank">**How to use Cron to Automate Tasks**</a>

####    **Delete tmp session files**

1.  Use the below command to delete tmp session files:

        */30 * * * * find -O3 "/tmp" -ignore_readdir_race -depth -mindepth 1 -name 'sess_*' -type f -cmin +180 -delete

2.  Use below command to run cron every 15 mins (Taper as required):

        */15 * * * * wget -q -O

    ![cronjob](images\cronjob.jpg)

!!! Note
    Don't forget to change the url to the website url (sample <a href= "https://www.mycrush.fit/wp-cron.php?doing_wp_cron"target="_blank">**Link**</a>)

####    **Disabling CRON job from WordPress**

1.  Navigate to **wp_config.php** file by navigating to public file (/var/www/html/)
2.  Add the following line after WP_DEBUG:

        define( ‘'DISABLE_WP_CRON', true );

3. The above command will disable WP CRON and use system CRON - <a href= "https://kinsta.com/knowledgebase/disable-wp-cron/#disable-wp-cron" target="_blank">**Refer Link**</a>

#### **Security - Prevent File Edits**

In order to maintain the security and avoid any file edits, follow the <a href="https://www.isitwp.com/disable-editors-and-plugin-modifications-entirely/" target="_blank">**below**</a> step:

1.  Add the below code to the wp_config.php file:

        (‘DISALLOW_FILE_EDIT', true);

    ![security](images\security.jpg)












