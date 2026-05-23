                                                                             Task 4

                         Project Title
Immutable E-commerce Deployment with ECS & ECR

                              Introduction
The objective of this task was to deploy the Evershop application using containerized infrastructure on AWS. 
The application was Dockerized, stored in Amazon ECR, and deployed through Amazon ECS on EC2 instances with an Application Load Balancer.
AWS Systems Manager Parameter Store was used for centralized configuration management, and CI/CD automation was configured using GitHub, CodeBuild, and CodePipeline.

                             Architecture
The architecture follows an immutable deployment model where the application is packaged as a Docker container image and deployed through ECS services. 
Traffic is routed through an Application Load Balancer to ECS tasks running on EC2 instances. 
Configuration values are securely managed through Parameter Store, while CI/CD automation is integrated with GitHub for automated deployments.

                              AWS Services Used
Service  ---                        	Purpose

1. Amazon Elastic Container Registry   ---	Store Docker images
2. Amazon Elastic Container Service    ---	Deploy and manage containers
3. Elastic Load Balancing	Application --- Load Balancer
4. Amazon Elastic Compute Cloud        --- ECS container instances
5. AWS Systems Manager                 --- Parameter Store configuration
6. AWS CodeBuild                       ---	Build automation
7. AWS CodePipeline                    ---	CI/CD deployment pipeline
8. GitHub                              --- Source code repository

                          Reason for Unfinished CI/CD Execution
The CI/CD configuration was completed successfully, including GitHub integration, buildspec configuration, IAM roles, and CodeBuild project setup. 
However, automated build execution could not be fully tested because the AWS free-tier/lab environment had account-level build queue limitations.

                Error Encountered
Cannot have more than 0 builds in queue for the account

This limitation prevented AWS CodeBuild from starting new builds even though the CI/CD configuration was completed correctly.

                           Conclusion
The Evershop application was successfully containerized, pushed to Amazon ECR, and deployed on Amazon ECS with an Application Load Balancer. 
Systems Manager Parameter Store was integrated for centralized configuration management, and CI/CD pipeline components were configured successfully. 
The remaining CodeBuild execution issue was caused by AWS account limitations rather than deployment or configuration errors.
