# Setting Your IAM Policy<a name="set-iam-policy"></a>

You can use AWS root credentials or IAM user credentials to create an Amazon QuickSight account\. AWS root credentials already have all of the required permissions for managing Amazon QuickSight access to AWS resources\. 

We recommend that you protect your root credentials, and instead use IAM user credentials\. To do this, create a policy and attach it to the IAM user and roles that you plan to use for Amazon QuickSight\. The policy must include the appropriate statements for the Amazon QuickSight administrative tasks you need to perform, as described in the following table\.


****  

| Task | Permissions for Standard Edition | Permissions for Enterprise Edition | 
| --- | --- | --- | 
|  Sign up for Amazon QuickSight and set Amazon QuickSight permissions to AWS resources\.  For more information, see [Managing Amazon QuickSight Permissions to AWS Resources](managing-permissions.md)\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  | 
| Creating administrators and users inside of Amazon QuickSight\. For more information, see [AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  | 
| Associating active directory groups with Amazon QuickSight during sign up, and managing group association going forward\. This task is only required for Enterprise edition accounts\. For more information, see [Managing User Accounts in Amazon QuickSight Enterprise Edition](managing-users-enterprise.md)\.  | [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  | 
| Set Amazon QuickSight permissions to AWS resources\. For more information, see [Managing Amazon QuickSight Permissions to AWS Resources](managing-permissions.md)\.  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  | 
| Unsubscribe from Amazon QuickSight\.  For more information, see [Closing Your Amazon QuickSight Account](closing-account.md)\. |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/set-iam-policy.html)  | 

The following example shows an IAM policy that enables active directory group management for an Amazon QuickSight Enterprise edition account\.

```
{
    "Statement": [
        {
            "Action": [
                "ds:DescribeTrusts",
                "quicksight:GetGroupMapping",
                "quicksight:SearchDirectoryGroups",
                "quicksight:SetGroupMapping"
            ],
            "Effect": "Allow",
            "Resource": [
                "arn:aws:quicksight::<YOUR_AWS_ACCOUNT_ID>:user/${aws:userid}"
            ]
        }
    ],
    "Version": "2012-10-17"
}
```

The following example shows a policy that enables creating Amazon QuickSight users\.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "quicksight:CreateUser"
            ],
            "Effect": "Allow",
            "Resource": "arn:aws:quicksight::<YOUR_AWS_ACCOUNT_ID>:user/${aws:userid}"
        }
    ]
}
```

For information about Amazon QuickSight actions like `quicksight:GetGroupMapping`, see [IAM Actions and Permissions for Amazon QuickSight users](iam-actions.md)\.

**Note**  
 Avoid modifying a policy that was created by Amazon QuickSight\. When you modify it yourself, Amazon QuickSight won't be able to edit it\. This can cause issues with the policy\. To fix the issue, delete the previously modified policy\. 