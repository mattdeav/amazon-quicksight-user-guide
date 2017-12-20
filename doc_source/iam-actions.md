# IAM Actions and Permissions for Amazon QuickSight users<a name="iam-actions"></a>

Amazon QuickSight provides a number of AWS Identity and Access Management \(IAM\) actions that you can use for creating or removing an Amazon QuickSight account\. All Amazon QuickSight actions are prefixed with `quicksight:`, such as `quicksight:Subscribe`\. For information about using Amazon QuickSight actions in an IAM policy, see [Setting Your IAM Policy](set-iam-policy.md)\.

The following list shows the supported Amazon QuickSight actions:

+ **`"quicksight:CreateAdmin"`**

  `CreateAdmin` lets authenticated users provision Amazon QuickSight administrator users\.

+ **`"quicksight:CreateUser"`**

  `CreateUser` lets authenticated users provision Amazon QuickSight users\.

+ **`"quicksight:GetGroupMapping"`**

  `GetGroupMapping` is used only in Amazon QuickSight Enterprise edition accounts\. It lets Amazon QuickSight identify and display the Microsoft AD directory groups that are mapped to roles in Amazon QuickSight\. 

+ **`"quicksight:SearchDirectoryGroups"`**

  `SearchDirectoryGroups` is used only in Amazon QuickSight Enterprise edition accounts\. It lets Amazon QuickSight display your Microsoft AD directory groups so that you can choose which ones to map to roles in Amazon QuickSight\. 

+ **`"quicksight:SetGroupMapping"`**

  SetGroupMapping is used only in Amazon QuickSight Enterprise edition accounts\. It lets Amazon QuickSight map the Microsoft AD directory groups that you select to roles in Amazon QuickSight\. 

+ **`"quicksight:Subscribe"`**

  `Subscribe` lets you subscribe to Amazon QuickSight\.

+ **`"quicksight:Unsubscribe"`**

  `Unsubscribe` lets you unsubscribe from Amazon QuickSight\.