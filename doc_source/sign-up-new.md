# Sign Up for Amazon QuickSight with a New AWS Account<a name="sign-up-new"></a>

If you are new to AWS and don't have any AWS resources that you want to make available in Amazon QuickSight, use the following procedure to create an Amazon QuickSight Standard edition account\. If you want to connect to AWS resources, or integrate user accounts from a Microsoft AD directory in AWS Directory Service, see [Sign Up for Amazon QuickSight with an Existing AWS Account](sign-up-existing.md) for more information\.

When you have finished signing up, you can proceed with connecting to data and creating analyses\. For more information about creating your first analysis, see [Getting Started](getting-started.md)\. You can also invite other users to access Amazon QuickSight\. For more information, see [Managing User Accounts in Amazon QuickSight Standard Edition](managing-users.md)\.

**To create an AWS account and an Amazon QuickSight account**

1. Go to [https://quicksight\.aws](https://quicksight.aws) and choose **Try for free**\. For information about QuickSight pricing, including the limits for free tier and free trial usage, see [Amazon QuickSight Pricing](https://quicksight.aws)\.

1. On the **Sign In or Create an AWS Account** page, choose **I am a new user**, and then choose ** Sign in using our secure server**\. Follow the online instructions to create an AWS account\. Part of the sign\-up procedure involves receiving a phone call and entering a PIN using the phone keypad\.

1. Choose **Standard edition**, and then choose **Continue**\.

1. For **QuickSight account name**, type a unique account name for your company or team\. It should be representative of your organization if possible, for example **examplecompany** or **examplecompany\-finance**\. Account names are unique in Amazon QuickSight, so if you expect to have multiple Amazon QuickSight accounts within your company, you should plan ahead to avoid any conflict\.

   Your account name can only contain characters \(A–Z and a–z\), digits \(0–9\), and hyphens \(\-\)\. 

1. For **Notification email address**, type the email address where Amazon QuickSight should send service and usage notifications\.

1. For **QuickSight capacity region**, choose the AWS Region where you want Amazon QuickSight to allocate the SPICE capacity associated with any user accounts you create\. Typically, this is the region closest to your physical location\. For more information about using AWS Regions with Amazon QuickSight, see [AWS Regions and IP Address Ranges](regions.md)\. For more information about how SPICE capacity is allocated, see [Managing SPICE Capacity](managing-spice-capacity.md)\.

1. Leave **Enable autodiscovery of your data and users in your AWS Redshift, RDS, and IAM services** selected to allow Amazon QuickSight to autodiscover any of these types of resources associated with your AWS account\. Alternatively, expand this section and deselect the individual options for the resources that you don't want to use with Amazon QuickSight\.

1. If you have Amazon S3 buckets, choose **Amazon S3 \(all buckets\)** to allow Amazon QuickSight to access all of them, or choose **Choose S3 buckets** to select specific buckets\.

1. If you have Amazon Athena databases, choose **Athena** to allow Amazon QuickSight to access them\. If you choose to use Athena as a data source, make sure that in the prior step you have enabled Amazon QuickSight access to the Amazon S3 buckets in which your Athena data resides\.

1. Choose **Finish**\.
**Note**  
When you create an Amazon QuickSight account, an AWS Directory Service directory is created in the US East \(N\. Virginia\) \(us\-east\-1\) Region, which Amazon QuickSight uses for account management\. You are not charged for this directory, and it is automatically deleted if you unsubscribe from Amazon QuickSight\.

1. Choose **Go to Amazon QuickSight**\.