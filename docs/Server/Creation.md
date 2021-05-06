#   **Create a Server**

##  **How to create a Server?**

In this section, we will see all the steps to create a server on DigitalOcean.

There are different ways to host a website on DigitalOcean depending on the requirements. Here we will discuss steps to manually control the infrastructure ourselves. This is done through creating Droplets.

### **Droplets**

Droplets are Linux-based virtual machines (VMs) that run on top of virtualized hardware. Each Droplet you create is a new server you can use, either standalone or as part of a larger, cloud-based infrastructure.

Get more information on droplets <a href="https://docs.digitalocean.com/products/droplets/" target="_blank">**here**</a>

####    **Steps to create a Droplet**

Below are the basic steps to follow to create a Droplet:

1.  From the Create menu in the top right of the control panel, click Droplets.

2.  Choose an image, which can be a Linux distribution, container distribution, one-click app, snapshot, or backup.
 
3.  Choose a plan and size for your Droplet, which determines its RAM, disk space, and vCPUs as well as its price. Learn more about how to choose the right Droplet plan.

The Droplet create screen has a number of options after this, which you can customize now or after creation. To accept the defaults, scroll to the bottom and click Create. Otherwise:

4.  Optionally, add block storage.

5.  Choose a datacenter region.

6.  Select additional options, like IPv6 and monitoring. These options come at no additional cost, and are easier to enable now than after creation.

7.  Select a VPC network for the Droplet.

8.  Select additional options, like IPv6 and monitoring. These options come at no additional cost, and are easier to enable now than after creation.

9.  Choose an SSH key, if you’ve added one, or create a root password for the Droplet.

10. Enter a name and click Create.

For a more descriptive process, follow the <a href="https://docs.digitalocean.com/products/droplets/how-to/create/" target="_blank">**link**</a>


####    **Connect the Droplet**

Once the above steps have been followed and you have the Droplet's IP address, username and password, follow the <a href="https://docs.digitalocean.com/products/droplets/how-to/connect-with-ssh/openssh/" target="_blank">**instructions**</a>  to connect to the Droplet with SSH.


####    **Droplet Resources**

Information on additional tools and more droplet resources is available on this <a href="https://docs.digitalocean.com/products/droplets/resources/" target="_blank">**link**</a>


