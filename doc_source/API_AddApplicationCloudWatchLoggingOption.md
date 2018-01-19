# AddApplicationCloudWatchLoggingOption<a name="API_AddApplicationCloudWatchLoggingOption"></a>

Adds a CloudWatch log stream to monitor application configuration errors\. For more information about using CloudWatch log streams with Amazon Kinesis Analytics applications, see [Working with Amazon CloudWatch Logs](http://docs.aws.amazon.com/kinesisanalytics/latest/dev/cloudwatch-logs.html)\.

## Request Syntax<a name="API_AddApplicationCloudWatchLoggingOption_RequestSyntax"></a>

```
{
   "ApplicationName": "string",
   "CloudWatchLoggingOption": { 
      "LogStreamARN": "string",
      "RoleARN": "string"
   },
   "CurrentApplicationVersionId": number
}
```

## Request Parameters<a name="API_AddApplicationCloudWatchLoggingOption_RequestParameters"></a>

The request accepts the following data in JSON format\.

 ** ApplicationName **   
The Kinesis Analytics application name\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 128\.  
Pattern: `[a-zA-Z0-9_.-]+`   
Required: Yes

 ** CloudWatchLoggingOption **   
Provides the CloudWatch log stream Amazon Resource Name \(ARN\) and the IAM role ARN\. Note: To write application messages to CloudWatch, the IAM role that is used must have the `PutLogEvents` policy action enabled\.  
Type: [CloudWatchLoggingOption](API_CloudWatchLoggingOption.md) object  
Required: Yes

 ** CurrentApplicationVersionId **   
The version ID of the Kinesis Analytics application\.  
Type: Long  
Valid Range: Minimum value of 1\. Maximum value of 999999999\.  
Required: Yes

## Response Elements<a name="API_AddApplicationCloudWatchLoggingOption_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response with an empty HTTP body\.

## Errors<a name="API_AddApplicationCloudWatchLoggingOption_Errors"></a>

 **ConcurrentModificationException**   
Exception thrown as a result of concurrent modification to an application\. For example, two individuals attempting to edit the same application at the same time\.  
HTTP Status Code: 400

 **InvalidArgumentException**   
Specified input parameter value is invalid\.  
HTTP Status Code: 400

 **ResourceInUseException**   
Application is not available for this operation\.  
HTTP Status Code: 400

 **ResourceNotFoundException**   
Specified application can't be found\.  
HTTP Status Code: 400

## See Also<a name="API_AddApplicationCloudWatchLoggingOption_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:

+  [AWS Command Line Interface](http://docs.aws.amazon.com/goto/aws-cli/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for \.NET](http://docs.aws.amazon.com/goto/DotNetSDKV3/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for C\+\+](http://docs.aws.amazon.com/goto/SdkForCpp/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for Go](http://docs.aws.amazon.com/goto/SdkForGoV1/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for Java](http://docs.aws.amazon.com/goto/SdkForJava/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for JavaScript](http://docs.aws.amazon.com/goto/AWSJavaScriptSDK/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for PHP V3](http://docs.aws.amazon.com/goto/SdkForPHPV3/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for Python](http://docs.aws.amazon.com/goto/boto3/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 

+  [AWS SDK for Ruby V2](http://docs.aws.amazon.com/goto/SdkForRubyV2/kinesisanalytics-2015-08-14/AddApplicationCloudWatchLoggingOption) 