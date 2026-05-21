                                                                          TASK 2 DOCUMENT
    Project Title
Secure RDS Deployment with IAM & Rotation
 
    Introduction
This project demonstrates the deployment of a secure, production-grade Amazon RDS MySQL database within a private VPC environment.
The architecture is designed following AWS security best practices, ensuring that the database is not publicly accessible and can only be accessed through controlled 
and secure methods.The main objective of this task is to implement IAM-based authentication, encrypted communication, 
and automated credential management, along with validating database recovery capabilities using Point-in-Time Recovery (PITR).
This setup simulates a real-world enterprise database environment where security, scalability, and reliability are critical.

    Architecture
1. VPC with public/private subnets
2. RDS MySQL in private subnet
3. EC2 in public subnet

    AWS Services Used
1. Amazon VPC
2. Amazon RDS (MySQL)
3. AWS IAM (Identity and Access Management)
4. AWS Secrets Manager
5. Amazon EC2
6. SSL/TLS Encryption
7. AWS RDS Point-in-Time Recovery (PITR)

    Security Implementation
1. Database deployed in private subnet (no public access)
2. IAM authentication used instead of passwords
3. Secrets Manager used for credential storage and rotation
4. TLS enforced for all database connections
5. Security groups restricted access to required ports only

    Conclusion

This project successfully demonstrates a secure and scalable AWS RDS MySQL deployment with enterprise-grade security controls.
Key achievements include:
Secure private database architecture using VPC
IAM-based authentication with temporary credentials
Automated credential management using Secrets Manager
Encrypted database communication using TLS
Verified data recovery using Point-in-Time Restore
Overall, this setup reflects real-world cloud database security practices and ensures confidentiality, integrity, and availability of data.
