# Request Access to an Existing Amazon QuickSight Account<a name="request-access"></a>

**Note**  
If you are the AWS account administrator, you can enable self\-provisioning for Amazon QuickSight by setting an IAM policy on a role with permissions for `CreateUser` or `CreateAdmin`\. To learn more about this, see [AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\.

If your organization has already signed up for Amazon QuickSight, you can ask your Amazon QuickSight administrator to add you as a user\. Your Amazon QuickSight administrator is the person whose AWS account or IAM credentials were used to create the Amazon QuickSight account\.

For Standard edition accounts, your Amazon QuickSight administrator can give you access through your IAM credentials, through Single Sign\-On \(SSO\), or through your email address\. Use the [Getting Access as a New Amazon QuickSight Standard Edition User](#request-access-standard) section for more information about signing up as a Standard edition user\.

If you have an Enterprise edition account, your Amazon QuickSight administrator must add your network user account to an active directory group that is associated with Amazon QuickSight\. Use the [Getting Access as a New Amazon QuickSight Enterprise Edition User](#request-access-enterprise) section for more information about signing up as an Enterprise edition user\. 

After you sign in for the first time, you can connect to data and creating analyses\. For more information about creating your first analysis, see [Getting Started with Data Analysis in Amazon QuickSight](getting-started.md)\.

## Getting Access as a New Amazon QuickSight Standard Edition User<a name="request-access-standard"></a>

Your Amazon QuickSight administrator uses either your IAM credentials, your Single Sign\-On \(SSO\) service, or your email address to create your Amazon QuickSight user account\. Then Amazon QuickSight sends you an email inviting you to activate it\. The invitation email you receive indicates what type of credentials you should use\.

**Note**  
 If your company is using a Single Sign\-On \(SSO\) service with Amazon QuickSight, your administrator provides instructions on how to sign in\. For more information on how this is set up, see [Enabling Single Sign\-On Access to Amazon QuickSight Using SAML 2\.0](external-identity-providers.md)\. 

### Signing In as a New User Using Credentials Based on Your Email Address<a name="request-access-qs"></a>

Use the following procedure to sign in as a new user who has an Amazon QuickSight–only account based on an email address\.

**To sign in as a new user who has an account based on an email address**

1. In your invitation email, choose the link in the body of the email to open the Amazon QuickSight sign\-up page\.

1. Complete your user account by typing a password\.

   Passwords are case\-sensitive, must be between 8 and 64 characters in length, and must contain at least one character from three of the following four categories:

   + Lowercase letters \(a–z\)

   + Uppercase letters \(A–Z\)

   + Numbers \(0–9\)

   + Nonalphanumeric characters \(\~\!@\#$%^&\*\_\-\+=`|\\\(\)\{\}\[\]:;"'<>,\.?/\)

1. Choose **Create account and sign in**\.

1. Choose **Continue**\. Doing this takes you to the Amazon QuickSight start page\.

### Signing In as a New User Using Your IAM Credentials<a name="request-access-iam"></a>

Use the following procedure to sign in to Amazon QuickSight as a new user who has IAM credentials\.

**To sign in as a new user with IAM credentials**

1. When you receive the invitation email, go to the Amazon QuickSight sign in page, [https://quicksight\.aws](https://quicksight.aws)\.

1. For **Account name**, type the account name in your invitation email, and then choose **Continue**\.

1. Type your IAM user name in **Email address or username**\.

1. Type your IAM password in **Password**\.

1. Choose **Sign in**\.

### Self\-Provisioning an Amazon QuickSight user<a name="self-service-access"></a>

Use the following procedure to sign in to Amazon QuickSight as a new user who has access to Amazon QuickSight, but has not yet created a login\. For this process to work, the AWS administrator must have granted permissions, using an AWS user or group policy in IAM\. For more information, see [AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\. 

**To sign in as a new user with access but no login**

1. When you are invited to do so, go to the Amazon QuickSight sign in page, [https://quicksight\.aws](https://quicksight.aws)\.

1. For **Account name**, type the Amazon QuickSight account name \(not the AWS account number\)\. Your administrator or manager might provide this name\. Then choose **Continue**\.

1. Type your new Amazon QuickSight user name in **Email address or username**\.

1. Type your new Amazon QuickSight password in **Password**\.

1. Choose **Sign in**\.

### Self\-Provisioning an Amazon QuickSight administrator<a name="assigning-the-admin"></a>

 Use the following procedure to set or create the administrator for Amazon QuickSight\. This procedure does not require using an alias for your account or your directory\.

**To make a user the Amazon QuickSight administrator**

1. Create the AWS user

   +  Use IAM to create the user you want to be the administrator of Amazon QuickSight\. Or, identify an existing user in IAM for the administrator role\. If you prefer, you can put the user inside a new group, for manageability\. 

   +  Grant the user \(or group\) sufficient permissions, as described in [Setting Your IAM Policy](set-iam-policy.md)\. 

   +  For more information on working with IAM, see [AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\. 

1. Log in to your AWS console with the target user's credentials\.

1. Go to [http://quicksight.aws.amazon.com/sn/console/get-user-email](http://quicksight.aws.amazon.com/sn/console/get-user-email)

1. Type in your email, and choose **Continue**

1. On success, the target IAM user is now an Amazon QuickSight administrator\.

## Getting Access as a New Amazon QuickSight Enterprise Edition User<a name="request-access-enterprise"></a>

After your Amazon QuickSight administrator adds your network user account to an active directory group associated with Amazon QuickSight, the administrator must notify you\. At that point, the administrator should provide you with the information that you need to activate your Amazon QuickSight user account\. This information must include the Amazon QuickSight account name you use to sign in\.

Use the following procedure to sign in to Amazon QuickSight as a new Enterprise edition user\.

**To sign in as a new Enterprise edition user**

1. When you receive notification from your administrator, go to the Amazon QuickSight sign in page, [https://quicksight\.aws](https://quicksight.aws)\.

1. For **Account name**, type the account name in your administrator provided to you, and then choose **Continue**\.

1. Type your network user name in **Email address or username**\.

1. Type the associated password in **Password**\.

1. Choose **Sign in**\.