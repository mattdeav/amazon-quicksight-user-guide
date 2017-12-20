# Working with Amazon QuickSight Log Files<a name="log-files"></a>

You can store your log files in your Amazon S3 bucket for as long as you want\. Alternatively, you can also define Amazon S3 lifecycle rules to automatically archive or delete log files\. By default, your log files are encrypted with Amazon S3 server\-side encryption \(SSE\)\.

If you want to be notified when log files are delivered, you can configure CloudTrail to publish Amazon SNS notifications on log file delivery\. For more information, see [Configuring Amazon SNS Notifications for CloudTrail](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/getting_notifications_top_level.html)\.

You can also aggregate Amazon QuickSight log files from multiple AWS regions and multiple AWS accounts into a single Amazon S3 bucket\. For more information, see [Receiving CloudTrail Log Files from Multiple Regions](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-receive-logs-from-multiple-accounts.html) and [Receiving CloudTrail Log Files from Multiple Accounts](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-receive-logs-from-multiple-accounts.html)\.