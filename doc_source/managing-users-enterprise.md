# Managing User Accounts in Amazon QuickSight Enterprise Edition<a name="managing-users-enterprise"></a>

Use this topic to learn more about managing user accounts in Amazon QuickSight Enterprise edition\. \(For information about managing user accounts in Amazon QuickSight Standard edition, see [Managing User Accounts in Amazon QuickSight Standard Edition](managing-users.md)\.\)

You can add and remove Microsoft AD directory groups to create and deactivate user accounts\. You can access the directory groups directly or by using the AD Connector\. To do this, you must have both administrative privileges in Amazon QuickSight and also appropriate AWS permissions\. The necessary AWS permissions are as follows:

+ ds:DescribeTrusts

+ quicksight:GetGroupMapping

+ quicksight:SearchDirectoryGroups

+ quicksight:SetGroupMapping

Each Amazon QuickSight Enterprise edition account can have an unlimited number of user accounts\. 

Use the following procedures to add, view, and deactivate Amazon QuickSight Enterprise edition user accounts\.

## Adding User Accounts<a name="add-user-accounts-enterprise"></a>

You manage users through Microsoft Active Directory \(AD\) groups\. You can create multiple user accounts at once by choosing one or more AD groups to integrate with Amazon QuickSight\. All users in the selected groups are authorized to sign in to Amazon QuickSight\. You can also add user accounts individually by adding those users to AD groups that are already integrated with Amazon QuickSight\. To see what groups are integrated with your Amazon QuickSight account, use the procedure in [Viewing User Account Details](#view-user-accounts-enterprise)\. For more information about adding a user to a Microsoft AD directory group, see [Add Users and Groups \(Simple AD and Microsoft AD\)](http://docs.aws.amazon.com/directoryservice/latest/admin-guide/creating_ad_users_and_groups.html)\. Or, you can read more about how to [Connect to a Directory](http://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html) using AD Connector\.

Your new users are not automatically notified of their access to Amazon QuickSight\. You must email users with the account name and the sign\-in URL \([https://quicksight\.aws](https://quicksight.aws)\)\. Let them know that they can use their active directory credentials to sign in to Amazon QuickSight\. 

Use the following procedure to add a Microsoft AD directory group to Amazon QuickSight\.

1. Choose your user name on the application bar, and then choose **Manage QuickSight**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/admin-menu.png)

1. Choose **Manage Users**\.

1. Choose **Manage groups**\.

1. On the AWS sign\-in page, enter your AWS or IAM credentials\.

1. To add user accounts with administrative privileges, choose **Add groups** under **Administrator groups**\. Otherwise, add them under the **User groups** section\.

1. For **Search for groups to add to groups list**, type the name of the group you want to use\. A list of matching group names appears\. Choose **Enter** for each to add it to the **Domain/Group name** list\.

   Repeat until you have added all of the groups that you want to use\.

1. Choose **Add selected groups**\.

   All users in the selected groups have Amazon QuickSight user accounts created for them\. You are charged for each user that activates their Amazon QuickSight account\.

1. Send email or otherwise notify users of their new accounts, and provide them the account name and the sign\-in URL\. 

## Viewing User Account Details<a name="view-user-accounts-enterprise"></a>

You can view the Microsoft AD directory groups integrated with Amazon QuickSight on the **Manage users** page\. Use the following procedure to view the Microsoft AD directory groups that are integrated with Amazon QuickSight\.

1. Choose your user name on the application bar and then choose **Manage QuickSight**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/admin-menu.png)

1. Choose **Manage Users**\. On this screen you can see which users were active this month\. You can also see deleted users\.

1. Choose **Manage groups**\. Administrator and user groups are managed from the AWS Console for QuickSight\.

1. On the AWS sign\-in page, enter your AWS or IAM credentials\.

1. View the groups whose users have administrative privileges under **Administrator groups**, and the groups whose users have user privileges under **User groups**\.

## Deactivating User Accounts<a name="deactivate-user-accounts-enterprise"></a>

You can deactivate multiple user accounts at once by choosing one or more Microsoft AD directory groups to remove from integration with Amazon QuickSight\. All users in the selected groups have their Amazon QuickSight deactivated\. Resources are not lost by deactivating an account\. You will get a chance to transfer their orphaned resources to another user\.

To deactivate a user account individually, remove that user from any Microsoft AD directory groups that are already integrated with Amazon QuickSight\. To view the groups integrated with your Amazon QuickSight account, use the procedure in [Viewing User Account Details](#view-user-accounts-enterprise)\. 

Deactivating a user account removes that user's ability to access Amazon QuickSight resources, like analyses or data sets, but doesn't delete that account or any Amazon QuickSight resources associated with it\. 

If you later need to reactivate a user account, put the user into an integrated group with access to Amazon QuickSight\. This restores their ability to access Amazon QuickSight and any existing resources associated with that user account\.

Use the following procedure to remove a Microsoft AD directory group from Amazon QuickSight\.

1. Choose your user name on the application bar and then choose **Manage QuickSight**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/admin-menu.png)

1. Choose **Manage Users**\.

1. Choose **Manage groups**\.

1. On the AWS sign\-in page, enter your AWS or IAM credentials\.

1. Locate the group you want remove under either the **Administrator groups** or the **User groups** section, and then choose the remove icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/deactivate-groups.png)

1.  In the **Manage users** screen, You can view each deactivated user in the **Deleted user** section\. This is located beneath the **Active users this month** section\. 

    To transfer the user's resources, click on the **Action** "x" button beside that user's name\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/transfer-resources.png)

   Choose one of the following:

   +  Transfer ownership of all orphaned resources to a different user in this account\. 

   +  Delete all orphaned resources\. \(This frees the user's SPICE capacity\.\)   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/confirm-deleted-account.png)

   These actions apply to all resources owned solely by that user\. If you transfer ownership, Amazon QuickSight will not make unnecessary duplicates of resources even if the resources are already shared with the receiving user\.