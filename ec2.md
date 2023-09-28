### EC2 Instance:

1. **What is an EC2 instance?**
  **Answer:** An EC2 instance is a virtual server in the Amazon Elastic Compute Cloud (EC2) service. It provides scalable computing capacity in the AWS cloud, allowing users to run applications and services.

2. **Can you explain the difference between an instance and an AMI?**
  **Answer:** An instance is a running virtual server in EC2, while an AMI (Amazon Machine Image) is a pre-configured virtual machine template that serves as a blueprint for launching instances. You use an AMI to create, launch, and clone instances.

3. **How do you launch an EC2 instance?**
  **Answer:** You can launch an EC2 instance through the AWS Management Console, AWS CLI (Command Line Interface), or SDKs using the "RunInstances" command.

4. **What is the significance of an instance type?**
  **Answer:** An instance type defines the hardware of the host computer used for your instance. Each instance type offers different combinations of CPU, memory, storage, and networking capacity. It determines the performance and pricing of your instance.

5. **What is the purpose of user data in EC2 instances?**
  **Answer:** User data allows you to run scripts or provide configuration information when launching an instance. This is useful for tasks like installing software, setting up configurations, or running custom startup scripts.

6. **How can you stop and start an EC2 instance?**
  **Answer:** You can stop an EC2 instance through the AWS Management Console, AWS CLI, or SDKs. To start a stopped instance, use the same methods.

7. **What is the difference between stopping and terminating an EC2 instance?**
  **Answer:** When you stop an instance, it is turned off but remains in the AWS infrastructure. You can start it again later. Terminating an instance permanently deletes it and its associated resources.

8. **How do you resize an EC2 instance?**
  **Answer:** You can resize an EC2 instance by stopping it, changing its instance type in the AWS Management Console, and then starting it again.

9. **Can you attach an IAM role to an existing EC2 instance?**
  **Answer:** Yes, you can associate an IAM role with an existing EC2 instance. You do this by stopping the instance, modifying the instance settings, and attaching the desired IAM role.

10. **Explain the concept of an Elastic IP address in EC2.**
   **Answer:** An Elastic IP address is a static, public IPv4 address that you can allocate to your AWS account. It's designed for dynamic cloud computing to ensure that the IP address of your EC2 instance doesn't change if the instance is stopped or terminated.

### Security Groups:

11. **What is a security group in EC2?**
   **Answer:** A security group acts as a virtual firewall for an instance. It controls inbound and outbound traffic, allowing or denying communication based on rules defined for the group.

12. **How is a security group different from a Network Access Control List (NACL)?**
   **Answer:** A security group operates at the instance level, while a Network Access Control List (NACL) operates at the subnet level. Security groups are stateful, while NACLs are stateless.

13. **Can you associate multiple security groups with a single EC2 instance?**
   **Answer:** Yes, you can associate multiple security groups with a single EC2 instance. The rules of all associated security groups are aggregated.

14. **What are inbound and outbound rules in a security group?**
   **Answer:** Inbound rules control the incoming traffic to an instance, while outbound rules control the outgoing traffic. Each rule defines a combination of protocol, port, and source/destination for the traffic.

15. **How does security group evaluation work?**
   **Answer:** Security group rules are evaluated based on the most specific rule that matches the traffic. If no rule explicitly allows the traffic, it is denied by default. The rule with the highest priority takes precedence.

### EBS Volumes:

16. **What is an EBS volume?**
   **Answer:** An EBS (Elastic Block Store) volume is a block-level storage device that you can attach to an EC2 instance. It provides persistent storage that persists independently from the life of an instance.

17. **What is the difference between EBS-backed and instance-store backed instances?**
   **Answer:** EBS-backed instances store the root file system on an EBS volume, providing persistent storage. Instance-store backed instances use the instance's root disk that is physically attached to the host computer.

18. **How can you increase the size of an EBS volume?**
   **Answer:** You can increase the size of an EBS volume, but it requires creating a snapshot of the existing volume, then creating a larger volume from that snapshot, and finally attaching it to the instance.

19. **Can you attach multiple EBS volumes to a single EC2 instance?**
   **Answer:** Yes, you can attach multiple EBS volumes to a single EC2 instance, each identified by a unique device name.

20. **Explain the difference between General Purpose SSD (gp2) and Provisioned IOPS SSD (io1).**
   **Answer:** General Purpose SSD (gp2) provides balanced performance for a wide range of workloads. Provisioned IOPS SSD (io1) allows you to specify a consistent IOPS rate, making it ideal for I/O-intensive applications.

### DLM (Data Lifecycle Manager):

21. **What is AWS Data Lifecycle Manager (DLM)?**
   **Answer:** AWS Data Lifecycle Manager is a service that automates the creation, retention, and deletion of EBS snapshots. It helps in managing the lifecycle of your EBS volumes' backups.

22. **How do you create a lifecycle policy for EBS snapshots?**
   **Answer:** You create a lifecycle policy in the AWS DLM console or by using the DLM API. The policy defines the rules for creating and retaining snapshots, such as the frequency and retention period.

23. **Explain the concept of retention policies in DLM.**
   **Answer:** Retention policies in DLM specify how many snapshots to retain and for how long. You can set up policies to keep a certain number of snapshots, or to retain snapshots for a specific number of days.

### Snapshots:

24. **What is an EBS snapshot?**
   **Answer:** An EBS snapshot is a point-in-time copy of an EBS volume. It captures the data and configuration of the volume, allowing you to restore it or create new volumes from the snapshot.

25. **How do you create a snapshot of an EBS volume?**
   **Answer:** You can create a snapshot using the AWS Management Console, AWS CLI, or SDKs. You select the EBS volume, initiate the snapshot process, and it will be created asynchronously.

26. **Can you create a snapshot of a root volume that is attached to a running EC2 instance?**
   **Answer:** Yes, you can create a snapshot of a root volume while it is attached to a running instance. However, it's recommended to stop the instance to ensure data consistency.

27. **What is the difference between a snapshot and an AMI?**
   **Answer:** A snapshot is a point-in-time copy of an EBS volume, while an AMI (Amazon Machine Image) is a pre-configured image that can be used to launch EC2 instances. An AMI can include multiple snapshots.

### Load Balancers:

28. **What is an Elastic Load Balancer (ELB)?**
   **Answer:** An Elastic Load Balancer (ELB) is a service that automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, or IP addresses.

29. **Can you explain the types of load balancers in AWS?**
   **Answer:** AWS offers three types of load balancers: Application Load Balancer (ALB), Network Load Balancer (NLB), and Classic Load Balancer. ALB operates at the application layer, NLB operates at the transport layer, and Classic Load Balancer provides basic load balancing.

30. **How does an Application Load Balancer (ALB) differ from a Network Load Balancer (NLB)?**
   **Answer:** ALB operates at the application layer and can route traffic based on content. It's best suited for web applications. NLB operates at the transport layer and is ideal for high-performance, low-latency use cases.

31. **What is the purpose of a Target Group?**
   **Answer:** A Target Group is used with an Application Load Balancer or Network Load Balancer. It routes traffic to registered targets based on health checks and load balancing algorithms.

### Auto Scaling Group:

32. **What is Auto Scaling in AWS?**
   **Answer:** Auto Scaling is a feature that automatically adjusts the number and size of your EC2 instances based on the conditions you set. It helps maintain application availability and scale resources efficiently.

33. **How do you set up an Auto Scaling group?**
   **Answer:** To set up an Auto Scaling group, you define a launch configuration or launch template that specifies the instance type, AMI, key pair, and security groups. Then, you create an Auto Scaling group using this configuration.

34. **Explain the significance of Launch Configurations in Auto Scaling.**
   **Answer:** A Launch Configuration is a template that defines the parameters for launching instances in an Auto Scaling group. It includes information like the instance type, AMI, key pair, and security groups.

### IAM Roles for EC2:

35. **What is an IAM role?**
   **Answer:** An IAM role is an AWS identity with permissions policies that determine what tasks it can perform. It is used to grant permissions to resources within your AWS account.

36. **How do you associate an IAM role with an EC2 instance?**
   **Answer:** You associate an IAM role with an EC2 instance by attaching the role to the instance during launch or by stopping the instance, modifying the instance settings, and then attaching the role.

37. **What are the advantages of using IAM roles with EC2 instances?**
   **Answer:** Using IAM roles allows you to grant specific permissions to instances without having to share security credentials. This enhances security and simplifies management.

### Elastic Beanstalk:

38. **What is AWS Elastic Beanstalk?**
   **Answer:** AWS Elastic Beanstalk is a fully managed service that makes it easy to deploy and run applications in multiple languages. It automatically handles the details of capacity provisioning, load balancing, and application deployment.

39. **How does Elastic Beanstalk differ from EC2 instances?**
   **Answer:** Elastic Beanstalk abstracts away the underlying infrastructure, automating deployment, scaling, and management tasks. EC2 instances, on the other hand, require manual configuration and management.

40. **What programming languages and platforms are supported by Elastic Beanstalk?**
   **Answer:** Elastic Beanstalk supports a wide range of programming languages and platforms, including Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker.

### Placement Groups:

41. **What is a placement group in EC2?**
   **Answer:** A placement group is a logical grouping of instances within a single Availability Zone. It is used to influence the placement of instances to meet specific requirements, such as low latency or high network throughput.

42. **What are the types of placement groups available?**
   **Answer:** There are three types of placement groups: Cluster Placement Group, Spread Placement Group, and Partition Placement Group.

43. **When would you use a cluster placement group vs a spread placement group?**
   **Answer:** A cluster placement group is suitable for applications that require low network latency and high network throughput within the group. A spread placement group is used when you want to distribute instances across distinct underlying hardware.

44. **Can you move an existing instance into a placement group?**
   **Answer:** No, you cannot move an existing instance into a placement group. You can only launch an instance into a placement group, or create a new AMI from the existing instance and then launch a new instance into the group.


### Systems ManagerRun Command:

45. **What is AWS Systems Manager Run Command?**
  **Answer:** AWS Systems Manager Run Command is a service that lets you remotely and securely manage the configuration of your EC2 instances or on-premises machines at scale.

46. **How do you execute a command on multiple instances using Run Command?**
  **Answer:** You can execute a command on multiple instances by creating a document in Systems Manager, selecting the target instances, and specifying the command to be executed.

47. **What is the benefit of using Run Command over traditional remote access methods (like SSH or RDP)?**
  **Answer:** Run Command provides a centralized and secure way to execute commands across multiple instances without the need for direct access. It also tracks command execution and logs output.

48. **Can you explain the concept of SSM Documents?**
  **Answer:** SSM Documents are JSON or YAML scripts that define the actions that Run Command performs on your instances. They contain the steps and parameters needed to execute commands.

49. **How do you schedule commands using Systems Manager?**
  **Answer:** You can schedule commands using Systems Manager State Manager. State Manager allows you to define a desired state, and Systems Manager will automatically enforce that state on your instances.

50. **What is the difference between Run Command and Automation in Systems Manager?**
  **Answer:** Run Command allows you to manually execute commands on instances, while Automation in Systems Manager allows you to create workflows that can be executed automatically in response to events.

### Systems ManagerParameter Store:

51. **What is AWS Systems Manager Parameter Store?**
  **Answer:** AWS Systems Manager Parameter Store provides secure, hierarchical storage for configuration data management. It's used to store sensitive information like database passwords, API keys, and configuration values.

52. **What are the different types of parameters in Parameter Store?**
  **Answer:** Parameter Store supports two types of parameters: SecureString, which encrypts the parameter value, and String, which stores the parameter value as plain text.

53. **How do you retrieve a parameter from Parameter Store in an EC2 instance?**
  **Answer:** You can use the AWS Systems Manager Agent (SSM Agent) on an EC2 instance to retrieve parameters from Parameter Store using the `aws ssm get-parameter` command.

54. **What is the benefit of using Parameter Store over environment variables or configuration files?**
   **Answer:** Parameter Store provides a centralized and secure way to manage configuration data. It supports versioning, encryption, and access control, making it suitable for sensitive information.

55. **Explain the difference between SecureString and String parameters.**
   **Answer:** SecureString parameters are encrypted using AWS Key Management Service (KMS), providing an extra layer of security for sensitive information. String parameters store the value as plain text.

### Systems ManagerSession Manager:

56. **What is AWS Systems Manager Session Manager?**
   **Answer:** AWS Systems Manager Session Manager allows you to manage your EC2 instances through an interactive browser-based shell or through the AWS CLI. It provides secure and auditable access without requiring a direct SSH or RDP connection.

57. **How does Session Manager ensure secure access to instances?**
   **Answer:** Session Manager uses AWS Identity and Access Management (IAM) policies to control access. It also provides detailed audit logs that track all session activity.

58. **Can you use Session Manager to connect to on-premises servers or other cloud platforms?**
   **Answer:** Yes, Session Manager can be used to connect to on-premises servers or other cloud platforms that have the SSM Agent installed.

59. **What are the advantages of using Session Manager over traditional remote access methods?**
   **Answer:** Session Manager provides secure, auditable access without exposing public IP addresses or requiring direct inbound connections. It also allows for fine-grained access control through IAM policies.

60. **How do you configure Session Manager on an EC2 instance?**
   **Answer:** To configure Session Manager, you need to ensure that the AWS Systems Manager Agent (SSM Agent) is installed and running on the instance. You also need the necessary IAM permissions to start sessions.
