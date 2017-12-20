# Managing SPICE Capacity<a name="managing-spice-capacity"></a>

You can use the admin page to see how much SPICE capacity you have overall, and how much of that you are using\. SPICE capacity is allocated by region, so the information displayed is for the currently selected region\.

SPICE is Amazon QuickSight's in\-memory optimized calculation engine, designed specifically for fast, ad\-hoc data visualization\. SPICE stores your data in a system architected for high availability, where it is saved until you choose to delete it\. You can improve the performance of database data sets by importing the data into SPICE instead of using a direct query to the database\. All non\-database data sets must use SPICE\.

 Each Amazon QuickSight account receives 10 GB of SPICE capacity per paid user, which is allocated when the user signs into Amazon QuickSight for the first time\. Each Amazon QuickSight account also receives one free user with 1 GB of SPICE capacity\. SPICE capacity is pooled across users for the Amazon QuickSight account\. For example, if you have 4 users \(3 paid and 1 free\), you have 31 GB of SPICE capacity available, which can be utilized by any of the users in the account\. All of your default SPICE capacity is allocated to your home region, and the other regions have no SPICE capacity unless you choose to purchase some\.

To free up SPICE capacity, delete any unused data sets that you have imported into SPICE\. For more information about deleting a data set, see [Deleting a Data Set](delete-a-data-set.md)\. 

You can purchase additional SPICE capacity if you want to, up to a limit of 1TB total capacity per QuickSight account\. If you need an exception to this limit, follow the instructions at [AWS Service Limits](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) to submit a limit increase request\. You can also release purchased SPICE capacity that you aren't using\. Purchasing or releasing SPICE capacity only affects the capacity for the currently selected region\. For information about additional SPICE pricing, see [Amazon QuickSight](https://quicksight.aws)\.

## View SPICE Capacity and Usage<a name="view-spice-capacity"></a>

Use the following procedure to review your SPICE capacity and usage\.

1. Choose your user name on the application bar and then choose **Manage QuickSight**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/admin-menu.png)
**Note**  
If you are low on SPICE capacity, you can also choose the **Buy SPICE** alert that appears on the **Your Data Sets** and **Create a Data Set** pages\.

1. Choose **SPICE Capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-capacity2.png)

1. Use the **Total SPICE Capacity** meter to see your SPICE capacity, broken out by type\. Capacity types are as follows:

   + Free tier: This is the 1 GB of capacity associated with the free user you get with every Amazon QuickSight account\.

   + Free bundled: This is the total default capacity associated with your paid users\. You get 10 GB of default SPICE capacity per paid user\.

   + Purchased: This is the additional SPICE capacity you have purchased\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-capacity.png)

   Hover over any section of the meter to see details on that capacity type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-capacity-detail.png)

1. Use the **SPICE Usage** meter to see your SPICE usage, broken out by type\. Usage types are as follows:

   + Used capacity: This is used portion of the default SPICE capacity you get per user\.

   + Unused capacity: This is unused portion of the default SPICE capacity you get per user\.

   + Releasable unused capacity: This is purchased capacity that isn't in use, and so can be released to reduce costs\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-usage.png)

   Hover over any section of the meter to see details on that usage type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-usage-detail.png)

## Purchase SPICE Capacity<a name="purchase-spice-capacity"></a>

Use the following procedure to purchase additional SPICE capacity\.

1. Choose your user name on the application bar and then choose **Manage QuickSight**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/admin-menu.png)
**Note**  
If you are low on SPICE capacity, you can also choose the **Buy SPICE** alert that appears on the **Your Data Sets** and **Create a Data Set** pages\.

1. Choose **SPICE Capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-capacity2.png)

1. Choose **Purchase more capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/more-capacity.png)

1. For **How much SPICE capacity do you need?**, type the number of gigabytes \(GBs\) you want to purchase\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/more-capacity1.png)

1. Choose **Purchase SPICE capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/more-capacity2.png)

## Release SPICE Capacity<a name="release-spice-capacity"></a>

Use the following procedure to release unused purchased SPICE capacity\.

1. Choose your user name on the application bar and then choose **Manage QuickSight**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/admin-menu.png)
**Note**  
If you are low on SPICE capacity, you can also choose the **Buy SPICE** alert that appears on the **Your Data Sets** and **Create a Data Set** pages\.

1. Choose **SPICE Capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-capacity2.png)

1. Choose **Release unused purchased capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/less-capacity.png)

1. For **How much SPICE capacity do you need to release?**, choose **Release all** if you want to release all unused purchased capacity, or choose **Release <amount> GB** and type the number of gigabytes \(GBs\) that you want to release\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/release-capacity.png)

1. Choose **Release SPICE capacity**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/release-capacity2.png)