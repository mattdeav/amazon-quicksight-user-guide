# Sharing Data Sets<a name="sharing-data-sets"></a>

You can give other Amazon QuickSight users access to a data set by sharing it with them\. Any user you share the data set with can create analyses from it\. If you make a user an owner when you share the data set with them, then that user can also refresh, edit, delete, or re\-share the data set\. 

## Sharing a Data Set<a name="share-a-data-set"></a>

Use the following procedure to share a data set\.

1. On the **Your Data Sets** page, choose the data set, and then choose **Share** \(if this data set hasn't been shared with anyone\) or **Shared with <X> users** \(if the data set has been shared with others\)\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/share-data-set.png)

1. Choose **Invite Users**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/data-set-invite.png)

1. In the **Type a user name or email** box, type the user name of a person with whom you want to share this data set and then choose the add icon\. You can only invite users who belong to the current Amazon QuickSight account\.

   Repeat this step until you have entered information for everyone you want to share the data set with\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/data-set-add-user.png)

1. For **Permission**, choose the role to assign to each person you are sharing the data set with\. A role determines the permission level to grant to that user account\.

   Choose **User** to allow the user to create analyses from the data set\. Choose **Owner** to allow the user to do that and also refresh, edit, delete, and re\-share the data set\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/data-set-share.png)

1. Choose **Share**\.

   The users you have shared the data set with receive emails with a link that gives them access to the data set\.

## Viewing and Editing the Permissions of Users That a Data Set Is Shared With<a name="view-users-data-set"></a>

If you have Owner permissions on a data set, you can use the following procedure to see which users have access to the data set, and to change the role of any user in order to modify their permissions\.

1. On the **Your Data Sets** page, choose the data set, and then choose **Share** \(if this data set hasn't been shared with anyone\) or **Shared with <X> users** \(if the data set has been shared with others\)\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/share-data-set1.png)

   A list of all users with access to the data set is displayed\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/list-data-set-users.png)

1. \(Optional\) To change a user's role and modify their permissions, choose the field in the **Permission** column for that user and then choose either **User** or **Owner**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/change-data-set-users.png)

## Revoking Access to a Data Set<a name="revoke-access-to-a-data-set"></a>

If you have Owner permissions on a data set, you can use the following procedure to revoke user access to a data set\.

1. On the **Your Data Sets** page, choose the data set, and then choose **Share** \(if this data set hasn't been shared with anyone\) or **Shared with <X> users** \(if the data set has been shared with others\)\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/share-data-set1.png)

   A list of all users with access to the data set is displayed\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/list-data-set-users.png)

1. In the **Actions** column for the user, choose **Revoke access**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/remove-data-set-users.png)