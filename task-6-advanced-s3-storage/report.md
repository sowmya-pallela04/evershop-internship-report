                                                                                Task 6

                  Project Title
Advanced S3 Storage for Product Images

                      Introduction
This task focused on building a secure and scalable image storage architecture using AWS S3 and related AWS services. 
The implementation included private object storage, encrypted uploads, pre-signed URL access, CloudFront content delivery, 
lifecycle management, inventory tracking, and automated malware scanning using AWS Lambda.
The project was designed to simulate a production-level product image storage system for an e-commerce platform

                       Architecture
User → Pre-Signed URL → Amazon S3 Bucket  
1. Amazon S3 → CloudFront → Public Content Delivery  
2. Amazon S3 → Lambda Trigger → Malware Scan Workflow  
3. Amazon S3 → Lifecycle Policies → Intelligent-Tiering / Glacier  
4. Amazon S3 → Inventory Reports → Storage Monitoring

                         AWS Services Used
Amazon S3
1. AWS Lambda
2. Amazon CloudFront
3. IAM Roles and Policies
4. S3 Lifecycle Rules
5. S3 Inventory
6. CloudWatch Logs

                       Challenges Faced
 Lambda syntax and permission errors during pre-signed URL generation
1. Signature mismatch errors while testing uploads
2. Temporary redirect issues caused by incorrect S3 endpoints
3. IAM permission issues for S3 PutObject operations
4. AWS account restriction preventing S3 Object Lambda deployment

These issues were resolved through IAM policy updates, correct regional endpoints, and Lambda debugging.

                           Conclusion
Successfully implemented an advanced AWS S3 storage architecture for product image management with secure uploads, CloudFront delivery, lifecycle optimization, 
inventory tracking, and automated malware scanning workflows.

The task demonstrated practical experience with AWS storage services, security configurations, automation using Lambda, and cloud architecture design 
for scalable e-commerce applications.
