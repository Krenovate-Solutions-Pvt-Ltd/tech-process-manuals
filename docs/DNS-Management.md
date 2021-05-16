#   **DNS Management**

##  **Introduction - DNS Management**

DNS translates domain names to IP addresses and that's why it is often called the "phonebook of the Internet."

Domain Naming Service (DNS) establishes the correspondence between the domain name of your site (e.g : https://agency.krenovate.com/) and the IP address where it is hosted (e.g : 213.244.184.122) on the Internet. A DNS server is a machine which makes this correspondence.

##  **Types of DNS Records**

Some of the type of DNS records used are discussed below:

### **A Records**

A Records direct browser requests to an origin web server.

### **CNAME Records**

CNAME Records direct browser requests to an origin web server, but — unlike an A or AAA record — do so via a hostname like www.agency.krenovate.com instead of an IP address.

### **MX Records**

MX Records are necessary for delivery of email to a mail server. Any MX record Server name requires a corresponding A record that lists the IP address of the mail server.

### **TXT Records**

TXT Records are commonly used for mail authentication.

### **SPF Records**

An SPF record is a type of TXT record that lists all servers authorized to send email messages from a domain.

### **DKIM Record**

DKIM records are a type of TXT record that associate email messages with domain names.

### **NS Records**

NS Records contain information about your nameservers. Use these records to identify which nameservers you should use if you want to manage your domain with a different hosting service.

!!! Note
    The top 4 records are the most commonly used records.

Read more about DNS Record types <a href= "https://support.cloudflare.com/hc/en-us/articles/360019093151-Managing-DNS-records-in-Cloudflare" target="_blank">**here**</a>

##  **Platforms**

At Krenovate, we use 3 platforms to manage the domains for client websites. All 3 are explained below:

### **GoDaddy**

In this case, the domain is registered and hosted with GoDaddy. All the DNS settings will be <a href= "https://in.godaddy.com/help/manage-dns-zone-files-680" target="_blank">**managed**</a> through the GoDaddy account. Follow the below steps:

1.  Login to your GoDaddy account.
2.  Select your domain to access the domain settings page.
3.  Click -> Manage DNS

    ![domains](images\DNS-Management\domains.jpg)

4.  If an A record already exists, you can edit it to the IP you want or Create a new one.
5.  To add “www” subdomain use add a CNAME record which points to “@”.

####    **Edit/Change an A Record**

1.  On the DNS Management page, select the edit dns :pencil2: icon next to the A record you need to edit.

    ![dnsrecords](images\DNS-Management\dnsrecords.jpg)

2.  Edit the below details for your A record:

    -   **Host**: The host name the A record links to. Type @ to point directly to your domain name.
    -   **Points to**: The IP address you are setting as the destination for the host.
    -   **TTL**: How long the server should cache information. The default setting is 1 hour.

        ![arecord](images\DNS-Management\arecord.jpg)

3.  Click -> **Save** to save changes.

!!! Note
    The above process can be followed to edit/add any kind of record. Refer the <a href= "https://in.godaddy.com/help/change-an-a-record-19239" target="_blank">**Link**</a>

### **DigitalOcean**

In this case, if the Domain is registered with other registrar we can manage the DNS on DigitalOcean, hence, the DNS records would be managed through the DigitalOcean account. 

This is determined by where your nameservers are pointing.

####    **Add Domain**

Adding a domain you own to your DigitalOcean account lets you manage the domain’s DNS records with the control panel and API. Below are the steps to follow:

1.  Login to your DigitalOcean Account.
2.  From the control panel, click -> **Create** menu -> **Domains/DNS**.

    ![createdomain](images\DNS-Management\createdomain.jpg)

3.  Networking section - Enter domain name in **Add a Domain** field.

    ![adddomain](images\DNS-Management\adddomain.jpg)

4.  Once you’ve added a domain, click its name to view and modify its DNS records.

    ![modify](images\DNS-Management\modify.jpg)
  
Refer - <a href= "https://docs.digitalocean.com/products/networking/dns/how-to/add-domains/" target="_blank">**How to Add Domain**</a>

####    **Manage DNS Records**

Now, you can add, modify, and delete DNS records for a domain.

#####   **Create a New Record**

To create a record:

1.  Select the record type just below the heading
2.  Fill in the fields required for that record type
3.  Click -> Create record. 

    ![createrecord](images\DNS-Management\createrecord.jpg)


#####   **Modify/Edit a Record**

To modify/update/delete an existing Record:

1.  Open the record's **More** menu
2.  Click -> **Edit Record** - to change/update the record values.
3.  Click -> **Delete** - to permanently delete the record.

    ![modifyrecord](images\DNS-Management\modifyrecord.jpg)

Refer - <a href= "https://docs.digitalocean.com/products/networking/dns/how-to/manage-records/" target="_blank">**Manage DNS Records**

The <a href= "https://docs.digitalocean.com/products/networking/dns/how-to/manage-records/#supported-record-types" target= "_blank">**supported record types**</a> sections have detailed instructions for each type of record.

####    **Nameservers**

This is an important step in order to be able to manage your domain through DigitalOcean.

To connect a GoDaddy domain with the DigitalOcean droplet, we have to replace the GoDaddy nameservers with the DigitalOcean Nameservers. Follow the below steps:

1.  Login to your GoDaddy account.
2.  Go to -> Domain manager
3.  Click on the domain name you want to manage

    ![domainmngr](images\DNS-Management\domainmngr.jpg)

4.  Scroll down to -> **Manage Nameservers**
5.  Click -> **Change**

    ![changens](images\DNS-Management\changens.jpg)

6.  Enter the DigitalOcean Nameservers here. DigitalOcean name servers are by default:  

    * ns1.digitalocean.com
    * ns2.digitalocean.com
    * ns3.digitalocean.com

    ![enterns](images\DNS-Management\enterns.jpg)

7.  Wait for few minutes for GoDaddy to refresh the DNS settings. The Manage DNS should look like this:  

    ![updatedlook](images\DNS-Management\updatedlook.jpg)

### **Cloudflare**

At Cloudflare, DNS can be managed for a domain registered with some other registrar. For this to happen - a unique account for each client has to be setup. To do so, follow below steps in this guide:

####    **Create a Cloudflare Account**

1.  Go to <a href= "https://www.cloudflare.com/" target= "_blank">**www.cloudflare.com**</a>
2.  Signup using an email id and password.
3.  Click -> **Create Account**

    ![cfcreateacct](images\DNS-Management\cfcreateacct.jpg)

####    **Add a Domain to the account**

1.  Login to your Cloudflare account.
2.  Click on **Add Site** from the top navigation bar.
3.  Enter your website’s root domain and then click Add Site. For example, if your website is "www.krenovate.com", type "krenovate.com".

    ![addsite](images\DNS-Management\addsite.jpg)

4.  Cloudflare, will then attempt to automatically identify your DNS records. This process takes approximately 60 seconds to complete.

     >    At this step, make sure that all the important records are being set properly. Some missing records may need to be <a href= "https://support.cloudflare.com/hc/en-us/articles/360019093151" target= "_blank">**added manually**</a>.

    ![krenovatedns](images\DNS-Management\krenovatedns.jpg) 

5.  <a href= "https://www.cloudflare.com/plans/#compare-features" target= "_blank">Select a plan level</a> - click confirm for the selected plan.
6.  Copy the 2 Cloudflare nameservers displayed and click **Continue**. 

    ![krenovatenameservers](images\DNS-Management\krenovatenameservers.jpg)

7.  To finish domain setup and activate your domain on Cloudflare, [change your domain nameservers to Cloudflare](#change-your-domain-nameservers-to-cloudflare), as in the below section.

####    **Change your domain nameservers to Cloudflare**

To change your domain nameservers, you will need to use information from Cloudflare to update admin settings at your current registrar.

1.  Login to your registrar (GoDaddy) account and remove the existing nameservers.

    ![cfns1](images\DNS-Management\cfns1.jpg)

2.  Replace with the Cloudflare nameservers (copied in step 7 in the above section).

    ![cfns2](images\DNS-Management\cfns2.jpg)

3.  Click -> **Save** - wait for a confirmation mail within 24 hrs.

<a href= "https://support.cloudflare.com/hc/en-us/articles/205195708" target= "_blank">**Refer here for more information**</a>

####    **Managing DNS Records**

#####   **Add DNS Records**

If you need to add DNS records manually:

1. Within a specific account and domain, go to DNS.

2. Select -> **Add record**.

3. Based on the record Type, you may have to fill out different fields. Refer <a href= "https://support.cloudflare.com/hc/en-us/articles/360019093151-Managing-DNS-records-in-Cloudflare" target= "_blank">**link**</a> for complete instructions.

#####   **Delete a DNS Record**

1. Within a specific account and domain, go to DNS.

2. On a specific record, select **Edit**.

3. Select -> **Delete**. A confirmation dialog appears.

4. Select **Delete** again to confirm.