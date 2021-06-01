#   **Website Optimization**

Website optimization is the process of using tools, advanced strategies, and experiments to improve the performance of your website, further drive more traffic, increase conversions, and grow revenue.

##  **Client Optimization**

-   WordPress frontend optimization constitutes the performance of the website when the website loads in the browser.
-   We use <a href= "https://gtmetrix.com/" target= "_blank">**GTMetrix**</a> to analyse and investigate our problem. Other tools used are:

    -   <a href= "https://developers.google.com/speed/pagespeed/insights/" target= "_blank">Google Page Speed Insight</a>
    -   <a href= "https://tools.pingdom.com/" target= "_blank">Pingdom</a>
    -   <a href= "https://developers.google.com/web/tools/lighthouse" target= "_blank">Chrome LightHouse</a>

###  **Basics of Website Optimization**

The main aim of Website Optimization is to get good scores in all the key metrics. A <a href= "https://gtmetrix.com/reports/agency.krenovate.com/ZTs9ivNS/" target= "_blank">sample report</a> is below:

![metrics](images\Website-Optimization\metrics.jpg)

For every report you get GTMerix grade, consisting of 2 parts:

#### **Performance Score**

The Performance Score tells you how well your page performs from a user perspective.

Your Performance Score is essentially your Lighthouse Performance Score, as captured by GTmetrix, with their custom audits, Analysis Options, browser and hardware specifications.


Know more about the Performance score <a href= "https://gtmetrix.com/blog/everything-you-need-to-know-about-the-new-gtmetrix-report-powered-by-lighthouse/#performance-score" target= "_blank">here</a>.

#####    **Performance Metrics**

The Performance score is made up of 6 key metrics:

![performancemetric](images\Website-Optimization\performancemetric.jpg)

The 6 key metrics hold the following weightage:

1.  <a href= "https://gtmetrix.com/first-contentful-paint.html" target= "_blank">First Contentful Paint (**15%**)</a> - How quickly content like text or images are painted onto your page. 
2.  <a href= "https://gtmetrix.com/speed-index.html" target= "_blank">Speed Index (**15%**)</a> - How quickly the contents of your page are visibly populated.
3.  <a href= "https://gtmetrix.com/largest-contentful-paint.html" target= "_blank">Largest Contentful Paint (**25%**)</a> - How long it takes for the largest element of content (e.g. a hero image) to be painted on your page.
4.  <a href= "https://gtmetrix.com/time-to-interactive.html" target= "_blank">Time to Interactive (**15%**)</a> - How long it takes for your page to become fully interactive.
5.  <a href= "https://gtmetrix.com/total-blocking-time.html" target= "_blank">Total Blocking Time (**25%**)</a> - How much time is blocked by scripts during your page loading process.
6.  <a href= "https://gtmetrix.com/cumulative-layout-shift.html" target= "_blank">Cumulative Layout Shift (**5%**)</a> - How much your page's layout shifts as it loads.

#### **Structure Score**

The Structure Score tells you how well your page is built for optimal performance.

<a href= "https://gtmetrix.com/blog/everything-you-need-to-know-about-the-new-gtmetrix-report-powered-by-lighthouse/#structure-score" target= "_blank">**Everything you need to know about the Structure Score**</a>


:pencil: **Note:**

The sample test was done for Desktop from Chennai, India. These settings also matter. You can change the location to where your customers are to get more relevant report and change your device to Mobile in order to get your mobile score.

![analyse](images\Website-Optimization\analyse.jpg)

###  **Optimizing your Website**

Once your <a href= "https://gtmetrix.com/reports/agency.krenovate.com/ZTs9ivNS/" target= "_blank">report</a> is ready you can follow the below steps to increase the performance of your website.

You can scroll down to **Page Details** to understand what is the request size and how is it distributed amongst assets.

![pagedetails](images\Website-Optimization\pagedetail.jpg)

#### **Structure Tab**

1.  Visit the Structure tab.
2.  You will be able to see multiple impact type issues.

    ![structuretab](images\Website-Optimization\structuretab.jpg)

3.  Open each issue to learn what it says - there can be links to other articles which tells better about the issue.

    ![openissue](images\Website-Optimization\openissue.jpg)

4.  Figure out the issue after reading it. Solve it. Push it. Retest to see if it gets fixed or not.
5.  You should start from High Impact Issue and then go down to Lower once and try to fix as many as possible.

#### **Waterfall Tab**

1.  Visit the Waterfall tab
2.  You can see exact resources being loaded.

    ![waterfalltab](images\Website-Optimization\waterfalltab.jpg)

3.  Select only CSS to check all CSS files. Remove the unnecessary files and retest.

    ![css](images\Website-Optimization\css.jpg)

4.  Repeat step 3 for JS, Fonts and Images. 
5.  Keep a check that no unnecessary files are being loaded.

###  **Common Practices**

Some common practices to follow during development to make sure the website performance is well optimized:

1.  Use optimized images:

    *   Use add_image_size hook to predefine image sizes so that when someone uploads the image, it gets cropped and resized to the required size.
    *   Read on <a href= "https://developer.wordpress.org/reference/functions/add_image_size/" target= "_blank">how to use add_image_size</a> 
    -   Eg: `add_image_size ('soi-card', 561, 786, true);`

2.  Optimize Font: 

    *    When adding font in your theme make sure you load the font with display the font as `swap` - This solves the <a href= "https://gtmetrix.com/ensure-text-remains-visible-during-webfont-load.html" target= "_blank">Flash of Unstyled Text (FOUT) problem</a>. 
    *   Use woff/woff2  format as it compresses the files and is supported by all modern browsers.

3.  CSS & JS:

    *   Keep your CSS and JS in modules so that when the production theme is built, only the concerned CSS and JS are loaded for a particular page.
    *   Avoid @import rule for adding any external js/css file. Instead use `wp_enqueue_script()/wp_enqueue_style()` functions.

    <a href= "https://developer.wordpress.org/reference/functions/wp_enqueue_script/" target= "_blank">Script Reference</a>

    <a href= "https://developer.wordpress.org/reference/functions/wp_enqueue_style/" target= "_blank">Style Reference</a>



##  **Server Size Optimization**

When you do a GTMetrix test for a particular website, you get an <a href= "https://gtmetrix.com/reduce-initial-server-response-time.html" target= "_blank">initial server response time</a> which basically **“is the time it takes for the browser to receive the first byte in response to the browser request.”** 

![speedvisual](images\Website-Optimization\speedvisual.jpg)

This can greatly affect your website performance, as it is responsible for fetching the code from the server before the CSS and JS is compiled in the browser. There are multiple reasons for this to be slow. A score of more than **300ms** is considered not good for a website. 

![topissue](images\Website-Optimization\topissue.jpg)

You can do the following to optimize the Server Response Time:

1.  Optimizing your application code
2.  Implementing server-side caching
3.  upgrading server hardware for more CPU or memory resources

There are **APM's** (application performance management tools) which can be used to monitor and debug, to optimize performance. We use one such APM called - **Newrelic**.

### **Installing Newrelic on a Server**

**Step1** : 

Install the Newrelic application on a particular server. Follow the below steps to install:

1.  Ensure your system meets the <a href= "https://docs.newrelic.com/docs/agents/php-agent/getting-started/php-agent-compatibility-requirements/" target= "_blank">agent's requirements</a>, including appropriate <a href= "https://docs.newrelic.com/docs/agents/php-agent/getting-started/php-agent-compatibility-requirements/#permissions" target= "_blank">system permissions</a>.

2.  If you do not already have a New Relic account, <a href= "https://docs.newrelic.com/docs/subscriptions/creating-your-new-relic-account/" target= "_blank">create one</a>.

3.  From your Account settings, copy your <a href= "https://docs.newrelic.com/docs/agents/php-agent/getting-started/php-agent-compatibility-requirements/#license_key" target= "_blank">license key</a> information.

4.  Install the agent package or tar archive on your system.
    *   Ubuntu or Debian:
        -   <a href= "https://docs.newrelic.com/docs/agents/php-agent/installation/php-agent-installation-ubuntu-debian/" target= "_blank">Install the package</a> either with `apt-get` or with `dpkg` commands. Typically, running the newrelic-install script is not required.

5.  Change the default <a href= "https://docs.newrelic.com/docs/site/naming-your-application/" target= "_blank">application name</a> to a meaningful name.

6.  Optional: Change other agent <a href= "https://docs.newrelic.com/docs/agents/php-agent/configuration/php-agent-configuration/" target= "_blank">configuration</a> settings to further customize your installation.

7.  Restart your web server (Apache, Nginx, PHP-FPM, etc.).

8.  Recommendation: To help ensure the PHP agent is initiated, especially if your application has infrequent activity, generate some data by using the app for a few seconds.

9.  Wait a few minutes for your application to send data to New Relic.


:computer: <a href= "https://docs.newrelic.com/docs/agents/php-agent/installation/php-agent-installation-overview/" target= "_blank">**Newrelic Installation Guide**</a>

The above process will install PHP Newrelic on your server. 

**Step 2:** 

Install WordPress specific functionalities for better data and reporting.


If you install <a href= "https://docs.newrelic.com/docs/agents/php-agent/installation/install-php-agent-shared-hosting-service/" target= "_blank">New Relic for WordPress websites</a>, the PHP agent receives additional metrics. A WordPress page appears in the New Relic user interface: Go to -> <a href= "one.newrelic.com" target= "_blank">one.newrelic.com</a> -> **APM** -> (**select a WordPress app**).

Once the above is set and data starts to come in, you can start analysing the report and fixing them.

### **Newrelic Application Decoded**


Below, we will learn how to use the Newrelic functionalities to optimize the server performance. For the purpose of example, we will use the Shades of India (SOI) account details.

1.  Login to your Newrelic account.
2.  This is the Dashboard that is visible

    ![nrdashboard](images\Website-Optimization\nrdashboard.jpg)

3.  Select the Shades of India Live application - it will take you to the explorer view

    ![nrexplorerview](images\Website-Optimization\nrexplorerview.jpg)

4.  In order to start analysing the requests -> change the view from Explorer to APM. Follow below steps:

    -   Click on explorer
    -   Select APM

        ![apm](images\Website-Optimization\apm.jpg)

    -   Select the application name -> Shades of India Live:

        ![selectapp](images\Website-Optimization\selectapp.jpg)
    
    -   You will reach the below screen:

        ![apmview](images\Website-Optimization\apmview.jpg)

####    **Transactions**

-   The best place to start your optimization is **Transactions** tab, see below:

    ![transact](images\Website-Optimization\transact.jpg)

    ![transact1](images\Website-Optimization\transact1.jpg)

-   When you scroll to the bottom of the page, you will see -> **Transaction Traces** - these are the recent requests which are probably taking long durations. 

    ![transtrace](images\Website-Optimization\transtrace.jpg)

    ![transactiontraces](images\Website-Optimization\transactiontraces.jpg)

For example: you can see **‘/product/fulva-kurta/’** taking **1s** of backend response time. You can click on the Transaction to know more about it. 

![tt](images\Website-Optimization\tt.jpg)

![propups](images\Website-Optimization\propups.jpg)

This propup has 3 tabs to analyse the request:

-   Summary
-   Trace Details
-   Database

#####   **Summary**

-   Once you have analysed the summary you can understand which are the most slow and time taking process for that particular request.
-   This graph tells you in an overview:

    ![summary1](images\Website-Optimization\summary1.jpg)

#####   **Trace Details**

-   This is the most important part of this task and it will give you the most important insights into your request.
-   Click on expand all button to expand every request

    ![tracedet](images\Website-Optimization\tracedet.jpg)

-   You will get a Waterfall graph - gives you an idea of time taken by every function in that particular request

    ![waterfallgraph](images\Website-Optimization\waterfallgraph.jpg)

-   Now the bottom most blue-bar gives you a relative idea of the time utilized by that particular function and its children. You can scroll down and take a quick look at every bar to find the longest one. This is the view you will get:
-   Once you spot the time consuming function, for example :  "**getRecentlyViewedSingleProduct**" function seems to be taking **97ms**. 

    ![tracedet1](images\Website-Optimization\tracedet1.jpg)

    In this case:

    -   Optimize your code for that function
    -   Again visit this particular page to get a transaction function.

-   You can now check the time of this function again to see if it got better scores now. This way you can basically identify the functions which are creating bottlenecks and then you can:

    -   Optimize the function
    -   Or, replace the function.

> **The above activity has to be done until you reach a response time near to 300ms.**
>

!!! Note
    Once you have fully optimized your application, it is recommended that you uninstall the Newrelic agent.
    Follow the <a href= "https://docs.newrelic.com/docs/infrastructure/install-infrastructure-agent/update-or-uninstall/uninstall-infrastructure-agent/" target= "_blank">instructions</a>. 








