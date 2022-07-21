# How Amazon EventBridge uses AWS Secrets Manager<a name="integrating_how-services-use-secrets_events"></a>

Amazon EventBridge is a serverless event bus service that you can use to connect your applications with data from a variety of sources\. 

EventBridge *API destinations* are HTTP endpoints that you can invoke as the target of an EventBridge rule\. When you create an API destination, EventBridge stores the connection for it in a Secrets Manager secret with the prefix `events`\. The cost of storing the secret is included with the charge for using an API destination\. To update the secret, you must use EventBridge rather than Secrets Manager\. For more information, see [API destinations](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-api-destinations.html) in the *Amazon EventBridge User Guide*\.