# Sign Up for Amazon QuickSight with an Existing AWS Account<a name="sign-up-existing"></a>

Use this topic to sign up for Amazon QuickSight using an existing AWS account\.

Amazon QuickSight accounts are provisioned by AWS accounts\. Once set up for a specific AWS account, Amazon QuickSight can be integrated with your AWS resources such as data sources or active directories\. 

**Note**  
 Before you begin, you must have a way to connect to an existing AWS account\. Then you can integrate your AWS resources \(such as data sources or active directories\) with Amazon QuickSight\. If your company already has an AWS account, contact your administrator if you need assistance\. If you don't already have an AWS account and you want to create one, see [Sign Up for Amazon QuickSight with a New AWS Account](sign-up-new.md) for more information\. 

Users in your organization who use Amazon QuickSight are part of an Amazon QuickSight account\. They can be IAM users\. Alternatively, they can be users who only have access to Amazon QuickSight\. To avoid confusion, we refer to all Amazon QuickSight users as *QuickSight users* or *QuickSight administrators\.*

For details on setting up AWS users and permissions for Amazon QuickSight, see [AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](set-iam-policy.md)\. 

## Create an Amazon QuickSight Account<a name="create-account-existing"></a>

After you have completed any needed configuration of your existing AWS resources, as discussed preceding, use the following procedures to create an Amazon QuickSight account\. 

**To create an Amazon QuickSight account**

1. Follow the instructions in [Sign In to Your AWS Root Account or an AWS Account with Administrator Access](#sign-up-existing-aws)\.

1. Do one of the following:

   1. To integrate user accounts from a Microsoft AD directory in AWS Directory Service, follow the instructions in [Create an Amazon QuickSight Enterprise Edition Account](#sign-up-existing-enterprise)\.

   1. If you don't want to integrate user accounts from an active directory, follow the instructions in [Create an Amazon QuickSight Standard Edition Account](#sign-up-existing-standard)\.

When you have finished signing up, you can connect to your data and start to create analyses\. For more information about creating your first analysis, see [Getting Started with Data Analysis in Amazon QuickSight](getting-started.md)\. 

For more information about managing users in Amazon QuickSight Standard edition, see [Managing User Accounts in Amazon QuickSight Standard Edition](managing-users.md)\. 

For more information about managing users in Amazon QuickSight Enterprise edition, see [Managing User Accounts in Amazon QuickSight Enterprise Edition](managing-users-enterprise.md)\.


+ [Sign In to Your AWS Root Account or an AWS Account with Administrator Access](#sign-up-existing-aws)
+ [Create an Amazon QuickSight Standard Edition Account](#sign-up-existing-standard)
+ [Create an Amazon QuickSight Enterprise Edition Account](#sign-up-existing-enterprise)

### Sign In to Your AWS Root Account or an AWS Account with Administrator Access<a name="sign-up-existing-aws"></a>

Start the Amazon QuickSight sign\-up process and sign in to your AWS account\.

**To sign in to your AWS root account or an account with administrator access**

1. Go to [https://quicksight\.aws](https://quicksight.aws) and choose **Sign up for free**\. For information about Amazon QuickSight pricing, including the limits for free tier and free trial usage, see [Amazon QuickSight Pricing](https://quicksight.aws)\.

1. On the **Sign In or Create an AWS Account** page, type your email address, choose **I am a returning user and my password is**, type your password, and then choose** Sign in using our secure server**\.

1. Go to [Create an Amazon QuickSight Standard Edition Account](#sign-up-existing-standard) if you want to use Amazon QuickSight Standard edition or [Create an Amazon QuickSight Enterprise Edition Account](#sign-up-existing-enterprise) if you want to use Amazon QuickSight Enterprise edition\.

1. When you are done signing in to AWS, the Amazon QuickSight sign up page displays\. Here, you specify an account name, an email address for Amazon QuickSight notifications, and a home capacity region:

   + For **QuickSight account name**, Amazon QuickSight defaults to the IAM alias for your AWS account, if you have one\. Type a unique account name for your company and team\. It should be representative of your organization if possible, for example **examplecompany** or **examplecompany\-finance**\. 

     Your account name can only contain characters \(A–Z and a–z\), digits \(0–9\), and hyphens \(\-\)\. 
**Note**  
Account names are unique in Amazon QuickSight\. Thus, if you expect to have multiple Amazon QuickSight accounts within your company, you should plan ahead to avoid any conflict\.

   + For **Notification email address**, type the email address where Amazon QuickSight should send service and usage notifications\.

   + For **QuickSight capacity region**, choose the AWS Region where you want Amazon QuickSight to allocate the SPICE capacity for all your users\. Typically, this region is the same one where you have the majority of your other AWS resources \(like Amazon RDS DB instances\)\. For more information about using AWS regions with Amazon QuickSight, see [AWS Regions and IP Address Ranges](regions.md)\. For more information about how SPICE capacity is allocated, see [Managing SPICE Capacity](managing-spice-capacity.md)\.

1. Choose **Continue**\.
**Note**  
When you create an Amazon QuickSight account, an AWS Directory Service directory is created in the US East \(N\. Virginia\) \(us\-east\-1\) Region, which Amazon QuickSight uses for account management\. You are not charged for this directory, and it is automatically deleted if you unsubscribe from Amazon QuickSight\.

1. On the **Grant Amazon QuickSight read\-only access to AWS resources** page, choose to enable all the services you want to autodiscover from Amazon QuickSight\.
**Important**  
You can enable any or all of these options\. We recommend leaving these options selected even if you don't currently use a given service\. Selecting them makes it possible for Amazon QuickSight to access AWS resources you might create in the future\.

1. Choose **Finish** and go to Amazon QuickSight\.

### Create an Amazon QuickSight Standard Edition Account<a name="sign-up-existing-standard"></a>

Create an Amazon QuickSight Standard edition account as described following\.

**To create a Standard edition account**

1. In Amazon QuickSight, choose **Standard edition**, and then choose **Continue**\.

1. For **QuickSight account name**, type a unique account name for your company and team\. This name should be representative of your organization if possible, for example **examplecompany** or **examplecompany\-finance**\. 

   Your account name can only contain characters \(A–Z and a–z\), digits \(0–9\), and hyphens \(\-\)\. 
**Note**  
Account names are unique in Amazon QuickSight\. Thus, if you expect to have multiple Amazon QuickSight accounts within your company, you should plan ahead to avoid any conflict\.

1. For **Notification email address**, type the email address where Amazon QuickSight should send service and usage notifications\.

1. For **QuickSight capacity region**, choose the AWS Region where you want Amazon QuickSight to allocate the SPICE capacity for all your users\. Typically, this is the same region where you have the majority of your other AWS resources \(like Amazon RDS instances\)\. For more information about using AWS Regions with Amazon QuickSight, see [AWS Regions and IP Address Ranges](regions.md)\. For more information about how SPICE capacity is allocated, see [Managing SPICE Capacity](managing-spice-capacity.md)\.

1. Leave **Enable autodiscovery of your data and users in your AWS Redshift, RDS, and IAM services** selected to allow Amazon QuickSight to autodiscover any of these types of resources associated with your AWS account\. Alternatively, expand this section and deselect the individual options for the resources that you don't want to use with Amazon QuickSight\.

1. If you have Amazon S3 buckets, choose **Amazon S3 \(all buckets\)** to allow Amazon QuickSight to access all of them, or choose **Choose S3 buckets** to select specific buckets\.

1. If you have Amazon Athena databases, choose **Athena** to allow Amazon QuickSight to access them\. If you choose to use Athena as a data source, make sure that in the prior step you have enabled Amazon QuickSight access to the Amazon S3 buckets in which your Athena data resides\.

1. Choose **Finish**\.
**Note**  
When you create an Amazon QuickSight account, an AWS Directory Service directory is created in the US East \(N\. Virginia\) \(us\-east\-1\) Region, which Amazon QuickSight uses for account management\. You are not charged for this directory, and it is automatically deleted if you unsubscribe from Amazon QuickSight\.

1. Choose **Go to Amazon QuickSight**\.

### Create an Amazon QuickSight Enterprise Edition Account<a name="sign-up-existing-enterprise"></a>

Create an Amazon QuickSight Enterprise edition account as described following\.

**To create an Enterprise edition account**

1. In Amazon QuickSight, choose Enterprise edition, and then choose **Continue**\.

1. Under **Active directory**, choose **Select a directory**, and then choose the Microsoft AD that contains the user accounts you want to integrate with Amazon QuickSight\. If you don't see that directory, choose **Refresh list**\. If you want to create a new directory rather than using an existing one, choose **Create directory** to go to the AWS Directory Service console\.

   Currently, Amazon QuickSight Enterprise edition is available only in the US East \(N\. Virginia\) Region, so the Microsoft AD you select must reside in that region\. The US East \(N\. Virginia\) Region is also where default SPICE capacity for your account is allocated if you choose to use Enterprise edition\.

1. Choose **Authorize** to grant Amazon QuickSight administrative permissions to the directory you selected\. Authorization allows Amazon QuickSight to list, add, and remove users and groups from this directory\.

1. If there is a default alias for the active directory you selected, it is used as your Amazon QuickSight account name\. If not, type an account name in **QuickSight account name**\. The account name should be representative of your organization if possible, for example **examplecompany** or **examplecompany\-finance**\. 
**Note**  
Account names are unique in Amazon QuickSight\. Thus, if you expect to have multiple Amazon QuickSight accounts within your company, you should plan ahead to avoid any conflict\.

   Your account name can only contain characters \(A–Z and a–z\), digits \(0–9\), and hyphens \(\-\)\. 

1. For **Admin group**, type the name of administrator group you want to use\.

   All users in this group have Amazon QuickSight user accounts with administrative privileges created for them\. You are charged for each user that activates their Amazon QuickSight account\.

   If you want to add another administrator group, choose **Add another admin group**, and then type an administrator group into the new box that displays\.

   Repeat until you have added all of the administrator groups you want to use\.

1. For **User group**, type the name of the user group you want to use\.

   All users in this group have Amazon QuickSight user accounts with user privileges created for them\. You are charged for each user that activates their Amazon QuickSight account\.

   If you want to add another user group, choose **Add another user group**, and then type a user group into the new box that displays\.

   Repeat until you have added all of the user groups you want to use\.

1. Leave **Enable autodiscovery of your data and users in your AWS Redshift, RDS, and IAM services** selected to allow Amazon QuickSight to autodiscover any of these types of resources associated with your AWS account\. Alternatively, expand this section and deselect the individual options for the resources that you don't want to use with Amazon QuickSight\.

1. If you have Amazon S3 buckets, choose **Amazon S3 \(all buckets\)** to allow Amazon QuickSight to access all of them, or choose **Choose S3 buckets** to select specific buckets\.

1. If you have Amazon Athena databases, choose **Athena** to allow Amazon QuickSight to access them\. If you choose to use Athena as a data source, make sure that in the prior step you have enabled Amazon QuickSight access to the Amazon S3 buckets in which your Athena data resides\.

1. Choose **Finish**\.

1. Choose **Go to Amazon QuickSight**\.