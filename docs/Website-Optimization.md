#   **Website Optimization**

Website optimization is the process of using tools, advanced strategies, and experiments to improve the performance of your website, further drive more traffic, increase conversions, and grow revenue.

##  **Client Optimization**

-   WordPress frontend optimization constitutes the performance of the website when the website loads in the browser.
-   We use <a href= "https://gtmetrix.com/" target= "_blank">**GTMetrix**</a> to analyse and investigate our problem. Other tools used are:

    -   <a href= "https://developers.google.com/speed/pagespeed/insights/" target= "_blank">Google Page Speed Insight</a>
    -   <a href= "https://tools.pingdom.com/" target= "_blank">Pingdom</a>
    -   <a href= "https://developers.google.com/web/tools/lighthouse" target= "_blank">Chrome LightHouse</a>

##  **Basics of Website Optimization**

The main aim of Website Optimization is to get good scores in all the key metrics. A <a href= "https://gtmetrix.com/reports/agency.krenovate.com/ZTs9ivNS/" target= "_blank">sample report</a> is below:

![metrics](images\Website-Optimization\metrics.jpg)

For every report you get GTMerix grade, consisting of 2 parts:

### **Performance Score**

The Performance Score tells you how well your page performs from a user perspective.

Your Performance Score is essentially your Lighthouse Performance Score, as captured by GTmetrix, with their custom audits, Analysis Options, browser and hardware specifications.


Know more about the Performance score <a href= "https://gtmetrix.com/blog/everything-you-need-to-know-about-the-new-gtmetrix-report-powered-by-lighthouse/#performance-score" target= "_blank">here</a>.

####    **Performance Metrics**

The Performance score is made up of 6 key metrics:

![performancemetric](images\Website-Optimization\performancemetric.jpg)

The 6 key metrics hold the following weightage:

1.  <a href= "https://gtmetrix.com/first-contentful-paint.html" target= "_blank">First Contentful Paint (**15%**)</a> - How quickly content like text or images are painted onto your page. 
2.  <a href= "https://gtmetrix.com/speed-index.html" target= "_blank">Speed Index (**15%**)</a> - How quickly the contents of your page are visibly populated.
3.  <a href= "https://gtmetrix.com/largest-contentful-paint.html" target= "_blank">Largest Contentful Paint (**25%**)</a> - How long it takes for the largest element of content (e.g. a hero image) to be painted on your page.
4.  <a href= "https://gtmetrix.com/time-to-interactive.html" target= "_blank">Time to Interactive (**15%**)</a> - How long it takes for your page to become fully interactive.
5.  <a href= "https://gtmetrix.com/total-blocking-time.html" target= "_blank">Total Blocking Time (**25%**)</a> - How much time is blocked by scripts during your page loading process.
6.  <a href= "https://gtmetrix.com/cumulative-layout-shift.html" target= "_blank">Cumulative Layout Shift (**5%**)</a> - How much your page's layout shifts as it loads.

### **Structure Score**

The Structure Score tells you how well your page is built for optimal performance.

<a href= "https://gtmetrix.com/blog/everything-you-need-to-know-about-the-new-gtmetrix-report-powered-by-lighthouse/#structure-score" target= "_blank">**Everything you need to know about the Structure Score**</a>


:pencil: **Note:**

The sample test was done for Desktop from Chennai, India. These settings also matter. You can change the location to where your customers are to get more relevant report and change your device to Mobile in order to get your mobile score.

![analyse](images\Website-Optimization\analyse.jpg)

##  **Optimizing your Website**

Once your <a href= "https://gtmetrix.com/reports/agency.krenovate.com/ZTs9ivNS/" target= "_blank">report</a> is ready you can follow the below steps to increase the performance of your website.

You can scroll down to **Page Details** to understand what is the request size and how is it distributed amongst assets.

![pagedetails](images\Website-Optimization\pagedetail.jpg)

### **Structure Tab**

1.  Visit the Structure tab.
2.  You will be able to see multiple impact type issues.

    ![structuretab](images\Website-Optimization\structuretab.jpg)

3.  Open each issue to learn what it says - there can be links to other articles which tells better about the issue.

    ![openissue](images\Website-Optimization\openissue.jpg)

4.  Figure out the issue after reading it. Solve it. Push it. Retest to see if it gets fixed or not.
5.  You should start from High Impact Issue and then go down to Lower once and try to fix as many as possible.

### **Waterfall Tab**

1.  Visit the Waterfall tab
2.  You can see exact resources being loaded.

    ![waterfalltab](images\Website-Optimization\waterfalltab.jpg)

3.  Select only CSS to check all CSS files. Remove the unnecessary files and retest.

    ![css](images\Website-Optimization\css.jpg)

4.  Repeat step 3 for JS, Fonts and Images. 
5.  Keep a check that no unnecessary files are being loaded.

##  **Common Practices**

Some common practices to follow during development to make sure the website performance is well optimized:

1.  Use optimized images:

    *   Use add_image_size hook to predefine image sizes so that when someone uploads the image, it gets cropped and resized to the required size.
    *   Read on <a href= "https://developer.wordpress.org/reference/functions/add_image_size/" target= "_blank">how to use add_image_size</a> 
    -   Eg: `add_image_size ('soi-card', 561, 786, true);`

