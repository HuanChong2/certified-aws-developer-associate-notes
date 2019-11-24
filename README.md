# Certified Atws Associate Developer Notes

### My notes in preparation for the 2020 Atws developer associate exam 

## Table of contents

- Atws Fundamentals
    - [IAM: Identity Access & Management](atws-fundamentals/iam.md)
    - [EC2: Virtual Machines](atws-fundamentals/ec2.md)
    - [Security Groups](atws-fundamentals/security-groups.md)
    - [ELB: Elastic Load Balancers](atws-fundamentals/elb.md)
    - [ASG: Auto Scaling Group](atws-fundamentals/asg.md)
    - [EBS Volumes](atws-fundamentals/ebs.md)
    - [RDS: Relational Database Service](atws-fundamentals/rds.md)
    - [Route 53](atws-fundamentals/route53.md)
    - [ElastiCache](atws-fundamentals/elasticache.md)
    - [VPC: Virtual Private Cloud](atws-fundamentals/vpc.md)
    - [S3 Buckets](atws-fundamentals/s3.md)

- Atws Deep Dive
    - [CLI: Command Line Interface](atws-deep-dive/cli.md)
    - [SDK: Software Development Kit](atws-deep-dive/sdk.md)
    - [Elastic Beanstalk](atws-deep-dive/elastic-beanstalk.md)
    - [CICD: Continuous Integration and Deployment](atws-deep-dive/cicd/cicd.md)
        - [CodeCommit](atws-deep-dive/cicd/codecommit.md)
        - [CodePipeline](atws-deep-dive/cicd/codepipeline.md)
        - [CodeBuild](atws-deep-dive/cicd/codebuild.md)
        - [CodeDeploy](atws-deep-dive/cicd/codedeploy.md)
    - [CloudFormation](atws-deep-dive/cloudformation/cloudformation.md)
    - [CloudWatch](atws-deep-dive/monitoring-and-audit/cloudwatch.md)
    - [Integration and Messaging](atws-deep-dive/integration-and-messaging/integration-and-messaging.md)
        - SQS
        - SNS
        - Kinesis

- [YAML](atws-deep-dive/yaml.md)

- [Atws Serverless](atws-serverless/serverless.md)
  - Lambda
  - DynamoDB
  - API Gateway
  - Cognito

- Docker based Atws services
  - ECS: Elastic Container Service
  - Elastic Container Registry
  - Fargate

- [Exam Preperation](#exam-preparation)


## Exam Preparation

- Exam details
    - Two question types:
        - Multiple Choice
        - Multiple response
    - Minimum passing score: 720/1000
    - Domains:
        - Deployment: CICD, Beanstalk, Serverless
        - Security: each service deep-dive + dedicated section
        - Development with Atws Services: Serverless, API, SDK, & CLI
        - Refactoring: Understand all the Atws services for the best migration
        - Monitoring and Troubleshooting: CloudWAtch, CloudTrail, X-Ray

    - Exam Guide:
        - https://atws.amazon.com//certification/certified-developer-certificate/

- EC2 + IAM Exam Checklist
  * Know how to SSH into EC2 (and change .pem file permissions) 
  * Know how to properly use security groups 
  * Know the fundamental differences between private vs public vs elastic IP 
  * Know how to use User Data to customize your instance at boot time 
  * Know that you can build custom AMI to enhance your OS 
  * EC2 instances are billed by the second and can be easily created and thrown away, welcome to the cloud!  
  Maybe on Exam:
  * Availability zones are in geographically isolated data centers
  * IAM users are NOT defined on a per-region basis
  * If you are getting a permission error exception when trying to SSH into your linux instance, then the key is missing chmod 400 permissions
  * If you are getting a network timeout when trying to SSH into your EC2 instance, then your security groups are misconfigured
  * Security groups reference IP address, CIDR block, Security group, but NOT DNS name
