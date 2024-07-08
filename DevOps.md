### CodeCommit
**Description:** A fully managed source control service that makes it easy for teams to host secure and scalable Git repositories.
- **Key Features:**
  - Secure, private Git repositories
  - Integration with AWS services and third-party tools
  - High availability and durability
  - Customizable access control policies
  - Automatic scaling

### CodeBuild
**Description:** A fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy.
- **Key Features:**
  - Fully managed build service
  - Continuous scaling
  - Pay-as-you-go pricing
  - Integration with other AWS services and third-party tools
  - Supports multiple programming languages and build environments

### CodeDeploy
**Description:** A service that automates application deployments to a variety of compute services such as Amazon EC2, AWS Lambda, and on-premises servers.
- **Key Features:**
  - Automated deployments
  - Blue/green deployments
  - Rollback capabilities
  - Integration with other AWS services
  - Centralized control

### CodePipeline
**Description:** A continuous delivery service for fast and reliable application and infrastructure updates.
- **Key Features:**
  - Automates build, test, and deploy phases
  - Customizable workflows
  - Integration with third-party services
  - Parallel execution
  - Manual approvals

### CloudWatch Dashboards
**Description:** Customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view.
- **Key Features:**
  - Customizable visualizations
  - Real-time data
  - Multi-region dashboards
  - Integration with AWS services
  - Easy to share

### CloudWatch Alarms
**Description:** A feature that watches a single metric over a specified time period and performs one or more specified actions based on the value of the metric relative to a threshold.
- **Key Features:**
  - Threshold-based alarms
  - Notification and automated actions
  - Metric math
  - Anomaly detection
  - Composite alarms

### CloudWatch Logs Filters and Subscriptions
**Description:** Filters allow you to extract meaningful information from logs, while subscriptions enable real-time log processing and analysis.
- **Key Features:**
  - Real-time log data streaming
  - Integration with AWS Lambda, Kinesis, and Elasticsearch
  - Customizable log patterns
  - Monitoring and troubleshooting
  - Security and compliance

### AWS Config
**Description:** A service that enables you to assess, audit, and evaluate the configurations of your AWS resources.
- **Key Features:**
  - Resource configuration history
  - Compliance and security analysis
  - Change notifications
  - Remediation actions
  - Integration with other AWS services

### GuardDuty
**Description:** A threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data.
- **Key Features:**
  - Continuous threat detection
  - Machine learning and threat intelligence
  - Integration with AWS services
  - Automated response actions
  - Centralized management

### S3 Query Data
**Description:** Amazon S3 Select and S3 Glacier Select allow you to run SQL queries directly on data stored in S3 without having to move the data to a database or analytics tool.
- **Key Features:**
  - Query data in place
  - Cost-effective
  - Integration with other AWS services
  - Supports CSV, JSON, and Parquet formats
  - Secure and scalable

### AWS Organizations (SCP and Compliance)
**Description:** A service that helps you centrally manage and govern your environment as you grow and scale your AWS resources.
- **Key Features:**
  - Centralized management of multiple AWS accounts
  - Service Control Policies (SCPs) for governance
  - Consolidated billing
  - Account creation automation
  - Compliance management

### How to Use Pass Role
**Description:** PassRole is an IAM feature that allows one service to pass a role to another service.
- **Key Features:**
  - Grants permissions to pass roles
  - Used in services like Lambda, ECS, and CodePipeline
  - Ensures secure role delegation
  - Fine-grained access control

### How to Track Root User Activities
**Description:** Monitoring the root user’s activities is crucial for security and compliance.
- **Key Features:**
  - CloudTrail logging
  - CloudWatch alarms for root user actions
  - IAM policies restricting root user access
  - Multi-factor authentication (MFA) for the root account
  - AWS Config for compliance tracking

### IAM Roles Anywhere
**Description:** IAM Roles Anywhere allows workloads that run outside of AWS to obtain temporary AWS credentials.
- **Key Features:**
  - Secure access to AWS services from outside AWS
  - Integration with on-premises or other cloud environments
  - Temporary security credentials
  - Integration with AWS IAM and AWS STS

### EKS Logging and Monitoring
**Description:** Ensuring visibility into the performance and health of Amazon EKS clusters.
- **Key Features:**
  - Integration with CloudWatch Logs and Prometheus
  - Container Insights for performance monitoring
  - Fluent Bit and Fluentd for log aggregation
  - Prometheus and Grafana for metric visualization
  - Automated monitoring with AWS Managed Service for Prometheus

### AMI Automation
**Description:** Automating the creation, maintenance, and deployment of Amazon Machine Images (AMIs).
- **Key Features:**
  - AWS Systems Manager Automation
  - EC2 Image Builder
  - Integration with CodePipeline and CodeBuild
  - Automated patching and compliance checks
  - Scheduled AMI creation

### Systems Manager Related Questions
**Description:** AWS Systems Manager provides a unified user interface to view operational data from multiple AWS services and automate operational tasks across AWS resources.
- **Key Features:**
  - Run Command for remote management
  - Automation for repetitive tasks
  - Patch Manager for automated patching
  - Parameter Store for configuration data management
  - OpsCenter for managing and resolving operational issues