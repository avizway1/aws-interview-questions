#### AWS Multi-Account Architecture with Organizations:

**Common Accounts we use in most of the environments.**
*Answer:* Training Account, Dev Account, Quality Assurance Account, UAT Account, Production Account.
Central Networking Account, Central Logging Account and Management Account.

1. **What is AWS Organizations and how does it help in multi-account architecture?**
  *Answer:* AWS Organizations is a service that allows you to centrally manage multiple AWS accounts. It helps in creating a hierarchical structure for accounts and enables central policy management.

2. **What is an SCP (Service Control Policy) in AWS Organizations?**
  *Answer:* An SCP is a policy that defines the maximum permissions that can be granted to resources within an AWS account. It helps in controlling what actions and services can be used within member accounts.

3. **How does Centralized Billing work in AWS Organizations?**
  *Answer:* Centralized Billing allows you to consolidate billing and payment information for multiple AWS accounts. It helps in tracking and managing costs across the organization.

4. **What is IAM Identity Center in the context of AWS Organizations?**
  *Answer:* IAM Identity Center provides a centralized view of all users, groups, and roles across all AWS accounts in the organization. It simplifies identity management and access control.
  
5. **What are the benefits of using AWS Organizations for multi-account architecture?**
   *Answer:* Benefits include centralized management, better security through SCPs, simplified billing, and improved compliance.

6. **How can you enforce a specific policy across multiple AWS accounts using SCPs?**
   *Answer:* You can attach an SCP to the root of your organization, which will be inherited by all member accounts. This allows you to enforce policies organization-wide. Or, We can apply at OU level, All OU level added accounts.

#### CloudTrail:

7. **What is AWS CloudTrail and what does it do?**
  *Answer:* AWS CloudTrail is a service that records AWS API calls made on our account. It provides detailed information about who made the call, what action was performed, and more.

8. **Why is CloudTrail important for security and compliance?**
  *Answer:* CloudTrail provides an audit trail of all API activity, which is crucial for security analysis, troubleshooting, and meeting compliance requirements.

9. **How can you access CloudTrail logs?**
  *Answer:* CloudTrail logs can be accessed through the AWS Management Console and AWS CLI, We can even send logs to S3 bucket and query it with Athena Service.

#### Amazon Config:

10. **What is AWS Config and how does it work?**
  *Answer:* AWS Config is a service that continuously monitors and records AWS resource configurations. It helps in assessing, auditing, and evaluating compliance with desired configurations.

11. **How does AWS Config help with compliance management?**
  *Answer:* AWS Config tracks changes to resource configurations and evaluates them against defined rules. It provides a compliance dashboard and can send notifications for non-compliant resources.

12. **What is a Config Rule in AWS Config?**
   *Answer:* A Config Rule is a customizable rule that checks whether your AWS resources comply with your desired configurations. It can be an AWS-managed rule or a custom rule.

13. **How does AWS Config handle resources that were created before it was enabled?**
   *Answer:* AWS Config retroactively records configuration changes for resources created before it was enabled, allowing you to assess historical compliance.
   
14. **What is the role of CloudTrail in AWS Config?**
   *Answer:* CloudTrail records API calls made on your AWS account, which is used by AWS Config to track and record changes to resource configurations.

#### Trusted Advisor:

15. **What is AWS Trusted Advisor?**
   *Answer:* AWS Trusted Advisor is a service that provides real-time guidance to help you optimize your AWS infrastructure, improve security, save money, and increase performance.

16. **What are the key areas that Trusted Advisor provides recommendations for?**
   *Answer:* Trusted Advisor provides recommendations in areas like Cost Optimization, Performance, Security, Fault Tolerance, and Service Limits.

17. **How does Trusted Advisor help in cost optimization?**
   *Answer:* Trusted Advisor analyzes your AWS environment and provides recommendations to reduce costs by identifying idle resources, underutilized instances, and more.

18. **Can Trusted Advisor make changes to your AWS environment automatically?**
   *Answer:* No, Trusted Advisor provides recommendations, but you need to manually apply the changes based on the suggestions.

### AWS Support Plans:

19. **What is AWS Support?**
   *Answer:* AWS Support provides a range of plans that offer access to AWS experts, resources, and technical support to help you successfully build, deploy, and manage applications on the AWS platform.

20. **What are the different AWS Support plans available?**
   *Answer:* AWS offers four support plans: Basic, Developer, Business, and Enterprise. Each plan provides different levels of support, response times, and features.

21. **What is included in the AWS Basic Support plan?**
   *Answer:* The AWS Basic Support plan includes 24/7 access to customer service, documentation, whitepapers, and support forums. It also provides access to AWS Trusted Advisor and AWS Personal Health Dashboard.

22. **What are the key features of the AWS Developer Support plan?**
   *Answer:* The AWS Developer Support plan includes all the features of Basic Support, as well as general guidance on AWS architecture and best practices, and an unlimited number of support cases with a 12-hour response time.

23. **What additional benefits does the AWS Business Support plan offer over Developer Support?**
   *Answer:* The AWS Business Support plan includes all the features of Developer Support, with faster response times (1-hour response for urgent cases), access to Infrastructure Event Management, and AWS Trusted Advisor checks.

24. **What is the AWS Enterprise Support plan designed for?**
   *Answer:* The AWS Enterprise Support plan is designed for large-scale enterprises with mission-critical workloads. It provides personalized, proactive support, a dedicated Technical Account Manager (TAM), and additional features for optimizing AWS infrastructure.

25. **How can you choose the right AWS Support plan for your organization?**
   *Answer:* Choosing the right support plan depends on your organization's specific needs, such as the level of criticality of your workloads, response time requirements, and the level of personalized support and guidance required.

26. **Can you upgrade or downgrade your AWS Support plan?**
   *Answer:* Yes, you can upgrade or downgrade your AWS Support plan at any time. Keep in mind that any changes to the plan will be effective from the beginning of the next billing cycle.

27. **What is AWS Personal Health Dashboard and how does it benefit AWS customers?**
   *Answer:* AWS Personal Health Dashboard provides personalized information about the performance and availability of AWS services that you're using. It helps you stay informed about events that may impact your AWS resources.

28. **How does AWS Infrastructure Event Management assist in operational readiness?**
   *Answer:* AWS Infrastructure Event Management helps you plan for and respond to AWS infrastructure events. It provides personalized alerts and guidance to help you prepare for and respond to events that may impact your AWS resources.

