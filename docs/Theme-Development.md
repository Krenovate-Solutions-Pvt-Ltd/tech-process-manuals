#   **Development Environment Setup for theme development**

:pencil:  **This documentation is for the Windows user only.**

In this section of the manual, we will learn the steps to develop environment setup for theme development.

##  **Install Laragon Software**

<a href= "https://laragon.org/" target= "_blank">**Laragon**</a> is a portable, isolated, fast & powerful universal development environment for PHP, Node.js, Python, Java, Go, Ruby. It is fast, lightweight, easy-to-use and easy-to-extend.

Laragon is great for building and managing modern web applications. It is focused on performance - designed around stability, simplicity, flexibility and freedom.

Below, we will see steps to install. setup and use Laragon.

### **Download Laragon**

To start the journey with Laragon, just <a href= "https://laragon.org/download/" target= "_blank">**download**</a> the latest version and click Next, Next, Next...

![download](images\Theme-Development\download.jpg)

### **Setup Guide**

Below are the setup steps:

#### **Setup - Welcome Page**

![welcome](images\Theme-Development\welcome.jpg)

#### **Setup - Select Location**

![location](images\Theme-Development\location.jpg)

#### **Setup - Options**

![options](images\Theme-Development\options.jpg)

### **Getting Started**

Below are <a href= "https://laragon.org/docs/quick-start.html" target= "_blank">**steps**</a> to have a Wordpress CMS in a few minutes:

1.  Start Laragon, then cick -> **Start All**

    ![quickapp](images\Theme-Development\quickapp.jpg)

2.  Click **Menu** -> **Quick app** -> **Wordpress**, type a name - such myblog

    ![projectname](images\Theme-Development\projectname.jpg)

3.  Laragon will display a Window and:

    * Create correspond database: myblog
    * Download the latest version of Wordpress
    * Extract the code to C:\laragon\www\myblog
    * Generate correspond pretty URL:
    * http://myblog.test

    ![progress](images\Theme-Development\progress.jpg)

##  **Create a Local copy of the Website**

### **New Website**

Create a new wordpress site :Eg. client.test using quick app - Follow the <a href= "https://laragon.org/docs/quick-app.html" target= "_blank">**Link**</a> for steps.

### **Existing Website**

To create a local copy of an existing website, follow below steps:

1.  Create a new wordpress site :Eg. Existing client.test using quick app - as discussed in [New Website](#new-website) above.
2.  Now, go to the already live version of the website eg. live.com
3.  Use [duplicator plugin](https://wordpress.org/plugins/duplicator/) to create a backup of the site. You can read about the steps in [here](https://www.wpkube.com/move-backup-website-wordpress-duplicator-plugin/
) 
4.  Once you have backup files, replace the wordpress files from exsitingclient.test with these backup file
5.  Visit oldclient.test/installer.php to start restore the website.
6.  Use your database credentials when asked and follow the steps.
7.  Once setup, make sure to do the following:

    -   Remove all the Social Media Tracking code from plugin or theme
        * Facebook Analytics
        * Google Analytics
        * Any other
    -   Use [Disable Emails](https://wordpress.org/plugins/disable-emails/) plugin to disable all outgoing emails.

## **Setup Theme**

### **New Website**

1.  We use <a href= "https://roots.io/sage/" target= "_blank">**sage**</a> as our starter theme.
2.  <a href= "https://roots.io/docs/sage/9.x/installation/" target= "_blank">**Install**</a> the theme in the themes directory.
3.  Create a github private repository inside our <a href= "https://github.com/Krenovate-Solutions-Pvt-Ltd" target= "_blank">**organization**</a>. 
4.  Repository name should be set as **project-name-theme**
5.  Push all the initial code to the remote repository.

### **Existing Website**

1.  Clone the client's theme from github to your theme folder.
2.  Run composer and yarn - you can start working on the theme.
3.  You are advised to work on a new branch when a new feature is being created.

##  **Deploying Integration: Setup**

1.  We use github actions to deploy changes to a particular server eg. Live, staging.
2.  You can setup the deployment integration by reading this <a href= "https://bhanusingh.in/deploying-sagewordpress-starter-theme-to-your-host-using-github-actions" target= "_blank">**article**</a>.














