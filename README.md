# coursera-aws-fundamentals-serverless

## About the course
- https://www.coursera.org/learn/aws-fundamentals-building-serverless-applications
- A Chatbot built using Serverless approach.
### What are we doing here
- We used **Amazon LEX** to build Entities and Intents.
  - Slots, fulfilment
- Text to speech is leveraged by **Amazon Polly**, which is consulted by Amazon LEX.
- **Amazon S3** object storage services ( eleven 9s )
  - Big Data, Static tWebsite hosting in S3 public bucket ( Public Read Access ). Extremely reliable.
- **Amazon CloufFront** is a Content Delivery Network
  - Edge locations
  - Serving files from CloudFront is more cost efficient than serving them directly from S3.
  - Client retrieves the content from the closest CloudFront to it.
  - Basically, CDNs are caches.
  - ![image](https://user-images.githubusercontent.com/42272776/124812536-5c76d900-df81-11eb-85de-04587380ccc1.png)
  - CloudFront integrates with both AWS WAF, a web application firewall that helps protect web applications from common web exploits, and AWS Shield, a managed DDoS protection service for web applications running on AWS.


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
