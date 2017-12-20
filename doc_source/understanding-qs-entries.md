# Understanding Amazon QuickSight Log File Entries<a name="understanding-qs-entries"></a>

CloudTrail log files contain one or more log entries\. Each entry lists multiple JSON\-formatted events\. A log entry represents a single request from any source and includes information about the requested action, the date and time of the action, request parameters, and so on\. The log entries are not an ordered stack trace of the public API calls, so they don't appear in any specific order\.

The following example shows a CloudTrail log entry\.

**BatchCreateUser**

```
{ 
   "eventVersion":"1.05",
   "userIdentity":
	{ 
	   "type":"Root",
	   "principalId":"123456789012",
	   "arn":"arn:aws:iam::123456789012:root",
	   "accountId":"123456789012",
	   "userName":"test-username"
	},
	   "eventTime":"2017-04-19T03:16:13Z",
	   "eventSource":"quicksight.amazonaws.com",
	   "eventName":"BatchCreateUser",
	   "awsRegion":"us-west-2",
	   "requestParameters":null,
	   "responseElements":null,
	   "eventID":"e7d2382e-70a0-3fb7-9d41-a7a913422240",
	   "readOnly":false,
	   "eventType":"AwsServiceEvent",
	   "recipientAccountId":"123456789012",
	   "serviceEventDetails":
	   { 
		   "eventRequestDetails":
		   { 
				"users":
				{ 
					"test-user-11":
					{ 
						"role":"USER"
					},
					"test-user-22":
					{ 
						"role":"ADMIN"
					}
				}
			},
			"eventResponseDetails":
			{ 
			"validUsers":[ 
				],
			"InvalidUsers":[ 
				"test-user-11",
				"test-user-22"
				]
			}
	   }
   }
```