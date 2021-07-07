# coursera-aws-fundamentals-serverless

## About the course
- https://www.coursera.org/learn/aws-fundamentals-building-serverless-applications
- A Chatbot built using Serverless approach.
### What are we doing here
- **Amazon LEX** is used to build Entities and Intents.
  - Slots, fulfilment
  - Text to speech is leveraged by **Amazon Poly**, which is consulted by Amazon LEX.
  - ElicitSlot and Delegate with AWS Lambda.
  - Sesion Attributes are used within square brackets [].
- **Amazon S3** object storage services ( eleven 9s )
  - Big Data, Static tWebsite hosting in S3 public bucket ( Public Read Access ). Extremely reliable.
- **Amazon CloufFront** is a Content Delivery Network
  - Edge locations
  - Serving files from CloudFront is more cost efficient than serving them directly from S3.
  - Client retrieves the content from the closest CloudFront to it.
  - Basically, CDNs are caches.
  - With CloudFront, the S3 buckets can be private.
  - ![image](https://user-images.githubusercontent.com/42272776/124812536-5c76d900-df81-11eb-85de-04587380ccc1.png)
  - CloudFront integrates with both AWS WAF, a web application firewall that helps protect web applications from common web exploits, and AWS Shield, a managed DDoS protection service for web applications running on AWS.
- **Amazon API Gateway** is an API Gateway
  - Multiple API versions management
  - Easy monitoring
  - Performance by taking network of Edge locations
  - Cache output of API calls
  - Authentication for APIs
  - Supports REST and WebSocket APIs
  - ![image](https://user-images.githubusercontent.com/42272776/124817856-f2adfd80-df87-11eb-9362-3af1534d7784.png)
- **Amazon IAM**
  - Create policies, roles and assign to users to authorize them for doing activities on AWS.
  - Create groups and apply policies on them.
- **AWS Lambdba**
  - Serverless compute service that can be authored in Java, NodeJS, Python, Go etc.
  - Pay only for requests served
  - Less than 15 minutes per request.
  - ![image](https://user-images.githubusercontent.com/42272776/124815730-394e2880-df85-11eb-97f7-b0103c36e6b8.png)
  - Lambda may need to access other services like DynamoDB or CloudWatch (AWSLambdaBasicExecutionRole). This is made possible by creating roles in IAM.
  - Triggers actually trigger the Lambda service - S3, CloudFront, API Gateway etc.
  - Ex: A lambda function may be triggered after uploading a new picture to S3 bucket to flip the picture upside down.
  - ![image](https://user-images.githubusercontent.com/42272776/124816419-24be6000-df86-11eb-95da-a96b9b18614c.png)
  - Handler tells which file/class the method to be invoked lies. It receives an Event Payload that contains the source, event information. Ex:, bucket name and key of object within the bucket.
  - Can be used in API gateways ( synchronous ) and S3 example above ( asynchronous ).
  - ![image](https://user-images.githubusercontent.com/42272776/124817692-bf6b6e80-df87-11eb-9d7c-37cb44969601.png)
- **Amazon DynamoDB**
  - Partitions keys, sort keys, local and global secondary indexes.
  - Primary key = partition key + sort key.

## Serverless Computing
- Is an architecture to build and run applications and services without having to manage the infrastructure behind it.
- It means you no longer need to provision, scale, maintain services to run your applications, databases or storage systems.
- With serverless architecture, you can execute your code only when needed and scale automatically from a few requests per day to thousands of requests per second while only
paying for the compute time you consume.
- There is no charge when your code is not running.
- Inheritently highly available as AWS serverless gurantees built-in availability and fault tolerance.
### Advantages
- Lower total cost of ownership.
- Developers just need to focus on building your product instead of managing the infra.


