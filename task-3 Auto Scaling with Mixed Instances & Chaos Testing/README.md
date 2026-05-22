                                                                               Task 3
     Project Title
Auto Scaling with Mixed Instances & Chaos Testing

     Introduction
This project focuses on building a highly available, fault-tolerant, and scalable cloud infrastructure using AWS services. 
The goal is to deploy an application on EC2 instances managed by an Auto Scaling Group (ASG) with mixed instance types (On-Demand and Spot instances).
The system is designed to automatically scale based on load and recover from failures using chaos testing techniques.
The application is exposed through an Application Load Balancer (ALB), ensuring continuous availability even during instance failures or traffic spikes.

    Architecture
The architecture follows a multi-tier cloud-native design:

1. Users access the application through an Application Load Balancer (ALB)
2. The ALB distributes traffic across multiple EC2 instances
3. EC2 instances are managed by an Auto Scaling Group (ASG)
4. ASG uses a Mixed Instances Policy (On-Demand + Spot Instances)
5. Scaling decisions are based on:
   CPU Utilization
   ALB Request Count per target
6. Instances are deployed across multiple Availability Zones for high availability
7. Lifecycle hooks ensure instances complete initialization (such as application startup and database migration) before becoming active



             AWS Services Used
The following AWS services were used in this project:

1. Amazon EC2 – Hosting the application instances
2. Auto Scaling Group (ASG) – Automatically manages scaling of EC2 instances
3. Launch Template – Defines configuration for EC2 instances in ASG
4. Application Load Balancer (ALB) – Distributes incoming traffic across instances
5. Target Groups – Monitors instance health and routes traffic
6. Amazon CloudWatch – Monitors CPU utilization and triggers scaling policies
7. IAM Roles – Provides secure access permissions for AWS resources
8. Availability Zones (AZs) – Ensures high availability and fault tolerance
9. Spot Instances & On-Demand Instances – Used in mixed instance policy for cost optimization

                Chaos Testing
To validate system resilience, chaos testing was performed:

1. Manually terminated EC2 instances to simulate failure
2. Verified that Auto Scaling Group automatically launched replacement instances
3. Simulated Availability Zone failure by stopping instances in one AZ
4. Confirmed traffic was routed to healthy instances in other AZs via ALB
5. Applied load testing to verify scaling behavior under high traffic conditions
6. Observed zero downtime during scaling and failure recovery events

           Challenges Faced
During implementation, several challenges were encountered:

1. Database connection issues due to incorrect configuration and missing PostgreSQL setup
2. Port conflicts caused by multiple Node.js processes running simultaneously
3. Target Group health check failures due to incorrect response expectations
4. Debugging ALB unhealthy states caused by application startup crashes
5. Ensuring proper integration between Auto Scaling Group and ALB target registration
These issues were resolved through systematic debugging of application logs, AWS configuration, and infrastructure setup.
       
            Conclusion

This project successfully demonstrates a production-grade AWS architecture with high availability, scalability, and fault tolerance.
By implementing Auto Scaling Groups with mixed instance policies, lifecycle hooks, and chaos testing, 
the system ensures continuous application availability even under failures and varying traffic loads.
The final setup is resilient, cost-optimized, and scalable, making it suitable for real-world cloud deployment scenarios.
