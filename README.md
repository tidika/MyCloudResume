# MyCloudResume

Welcome to this repo!!!

This repository comprises all the essential files required to host and operate my resume website on AWS.  

**Note:** The implementation details in this project adhere to the instruction provided in this [link](https://medium.com/@meachamdillon52/how-to-create-a-cloud-resume-with-aws-a-step-by-step-guide-b087ddef6b32). This project is part of my [CloudResume Challenge](https://cloudresumechallenge.dev/).

<img width="677" alt="image" src="https://github.com/tidika/MyCloudResume/assets/115043340/aa077a7f-a85a-4ff1-87ca-47d695bf7e7e">


**A high level explanation of AWS architectural resources**

**Route53:** It is used to register the domain **tochiidika.net** and to create a domain name system (DNS) **A record** to manage domain name resolution. 

**CloudFront:** It is a service that caches and serves global contents from edge locations, thereby reducting latency and improving the delivery of web resources to end-users.

**AWS Certificate Manager:** It is used to manage SSL/TLS certifacts for my resume website. Because we intend to use tochiidika.net as the domain name for accessing the cloudFront endpoint instead of relying on the default HTTPS endpoint generated by CloudFront when it is setup, ACM is used to secure the domain with encrypted HTTPS. 

**S3 Bucket:** It is a highly scalable and durable object storage that is used to host the static resume website.

**Lambda:** It is a serverless compute service used that responds to synchronous and asynchronous events. In this project, when a request is made to an S3 bucket, it triggers a Lambda function that increments the total number of site visitors. 

**DynamoDB:** It is amazon NOSQL database that is designed for high-performance, scalable and low-latency application. In this project, it is used to store the number of site visitors. However, any RDS database eg MySQL, PostgreSQL, MSSQL etc can also suffice. 








