<!-- loio88b86dbbbee34092a2e30a32ada5dc19 -->

# Define How a Failover Is Detected

Define in which cases the automatic failover from one data center to the other is triggered.

You can choose from different test categories to decide when the automatic switch from your primary to the backup application is triggered. Either define these test categories manually in your code or use rule-based performance solutions such as [Akamai ION](https://www.akamai.com/us/en/products/performance/web-performance-optimization.jsp). At each user request, you could, for example, check for a combination of a predefined maximum read timeout and set HTTP status codes. If one of these two checks responds an unwanted behavior of your application, the failover is triggered.

The following figure illustrates this procedure:

   
  
<a name="loio88b86dbbbee34092a2e30a32ada5dc19__fig_o11_gks_yhb"/>Failover Detection

 ![Failover Detection](images/Failover_Detection_4713dc4.png "Failover Detection") 

> ### Example:  
> As an example, you could define `25` seconds as maximum read timeout and set a number of server error codes \(`5xx`\) to be checked. At each first HTTP request towards the URL of your application, both checks are triggered. All following HTTP requests are ignored to avoid an unnecessary failover if, for example, only an image resource is missing. If one of the two checks fails, the user is automatically redirected to an HTML down page, which must not be cached. This down page provides the link to your failover application. Strictly speaking, the failover itself is therefore manually performed by the user of your application.

