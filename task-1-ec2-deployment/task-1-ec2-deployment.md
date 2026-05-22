                                                                            TASK 1 DOCUMENT
    Project Title

AWS Secure Scalable E-Commerce Infrastructure Deployment using ALB, WAF, Route 53 and Cloud Architecture Design

    Introduction

This project focuses on designing and implementing a secure, scalable, and highly available AWS-based infrastructure for an e-commerce application (EverShop).
The architecture follows AWS best practices for load balancing, security, and future CDN integration.
The solution is built using core AWS services including EC2, ALB, WAF, Route 53, and S3 for static maintenance hosting.

    Architecture :
            
    Implemented Architecture-

User
  ↓
Route 53 (Hosted Zone - Configured)
  ↓
Application Load Balancer (ALB)
  ↓
AWS WAF (Security Layer)
  ↓
EC2 Instances (EverShop Web Application)
  ↓
Backend Services (App Layer)

     Planned Production Architecture (Partially Blocked)-

User
  ↓
Route 53 (Domain DNS - Restricted)
  ↓
CloudFront (Blocked due to account verification)
  ↓
AWS WAF
  ↓
ALB
  ↓
EC2
  ↓
S3 (Maintenance Site - Failover)

    AWS Services Used

1. Amazon EC2 (Application hosting)
2. Elastic Load Balancer (ALB)
3. AWS WAF (Web Application Firewall)
4. Amazon Route 53 (Hosted Zone configuration)
5. Amazon S3 (Static maintenance site)
6. AWS Certificate Manager (ACM - Pending validation)

    Working Application URL

evershop-ALB-1176732267.ap-south-1.elb.amazonaws.com

    Challenges / Limitations Faced

1. Route 53 NS migration restricted by internship policy
2. ACM certificate pending due to DNS validation restriction
3. CloudFront deployment blocked due to AWS account verification requirement
4. Production domain mapping not available at this stage

    Conclusion

The project successfully demonstrates a secure and scalable AWS architecture for an e-commerce application.
 All core infrastructure components have been implemented and tested successfully within the allowed environment constraints.

Although production-level DNS and CloudFront deployment are currently restricted,
the system is fully functional using ALB and WAF, and is ready for production enhancement once domain-level access is enabled.
