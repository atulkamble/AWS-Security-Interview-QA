# ✅ **AWS Security – Interview Questions & Answers (With Important Points)**

---

# 🔷 **1. What is the AWS Shared Responsibility Model?**

### **Answer:**

The AWS Shared Responsibility Model defines how AWS and the customer share security duties.

* **AWS is responsible for “Security *OF* the Cloud.”**
  Includes physical data centers, network, hardware, virtualization layers, availability zones, and global infrastructure.

* **Customers are responsible for “Security *IN* the Cloud.”**
  Includes data, IAM, encryption, application security, OS hardening, security groups, NACLs, patching, and monitoring.

### **Important Points to Note**

* Customers must secure **their workloads**, not the underlying infrastructure.
* Responsibility varies based on the service type (IaaS, PaaS, SaaS).
* AWS handles physical security, but customers handle logical security.

---

# 🔷 **2. How does AWS secure its global infrastructure?**

### **Answer:**

AWS secures infrastructure through:

* Redundant and layered security controls
* Continuous validation and testing
* Data center security (biometrics, surveillance, guards)
* Automatic network encryption across the AWS backbone
* 24×7 monitoring and automated threat detection

### **Important Points**

* AWS replicates the same controls in every region and data center.
* Customers benefit from security built for highly regulated industries.

---

# 🔷 **3. What are some AWS services that help with Infrastructure Security?**

### **Answer:**

Key services include:

* **Amazon VPC** → Network isolation, Security Groups, NACLs
* **AWS Shield** → DDoS protection
* **AWS WAF** → Web application firewall
* **AWS Direct Connect / VPN** → Private connectivity
* **TLS encryption** → In-transit data protection

### **Important Points**

* Security Groups are *stateful*, NACLs are *stateless*.
* AWS global network traffic is automatically encrypted.

---

# 🔷 **4. What tools does AWS provide for Inventory and Configuration Management?**

### **Answer:**

Tools include:

* **AWS CloudFormation** → Deploy standard templates
* **AWS Config** → Track configuration changes and compliance
* **AWS Service Catalog** → Control approved resources
* **Pre-hardened AMIs** → Standard secure machine images

### **Important Points**

* AWS Config helps detect drift from organizational standards.
* CloudFormation ensures infrastructure consistency.

---

# 🔷 **5. How does AWS provide encryption for data at rest?**

### **Answer:**

AWS provides:

* **EBS, S3, RDS, Redshift, ElastiCache** – encryption at rest
* **KMS** → Managed key creation and rotation
* **CloudHSM** → Hardware-based key storage
* **SSE for SQS** → Encrypted message queues

### **Important Points**

* Encryption is available across most AWS services.
* Customers can choose AWS-managed or customer-managed keys.
* CloudHSM satisfies strict compliance requirements.

---

# 🔷 **6. What is AWS Key Management Service (KMS)?**

### **Answer:**

AWS KMS is a managed service for creating, storing, and controlling encryption keys.

### **Key Features:**

* Automatic key rotation
* Integration with major AWS services
* Customer-managed keys for granular control
* Logging through CloudTrail

### **Important Note**

KMS is software-based; for hardware-backed keys, use **CloudHSM**.

---

# 🔷 **7. What Identity and Access Management (IAM) capabilities does AWS provide?**

### **Answer:**

AWS IAM provides:

* Users, Groups, Roles
* JSON-based permission policies
* MFA for privileged accounts
* Federated access using Active Directory or SAML
* AWS SSO for centralized management of multiple accounts

### **Important Points**

* Always enable MFA for root account.
* Prefer Roles over long-term access keys.
* IAM integrates natively with almost all AWS services.

---

# 🔷 **8. What tools help with monitoring and logging in AWS?**

### **Answer:**

AWS monitoring tools include:

### **✔ CloudTrail**

* Logs API calls
* Tracks “who did what and when”
* Essential for auditing

### **✔ CloudWatch**

* Metrics
* Logs
* Alarms and automation

### **✔ Amazon GuardDuty**

* Machine-learning threat detection
* Detects suspicious activity

### **Important Points**

* CloudTrail should be enabled in every region.
* GuardDuty is account-wide and lightweight.
* CloudWatch can trigger automatic remediation.

---

# 🔷 **9. What is AWS Trusted Advisor?**

### **Answer:**

AWS Trusted Advisor analyzes your AWS environment and provides recommendations in:

* Cost optimization
* Performance
* Security
* Reliability
* Operational excellence

### **Important Points**

* Checks for public S3 buckets
* Flags weak IAM security (no MFA, overly permissive policies)
* Enterprise support accounts get full checks

---

# 🔷 **10. What are AWS Marketplace Security Products?**

### **Answer:**

AWS Marketplace provides 3rd-party tools such as:

* Firewalls (Palo Alto, Check Point)
* SIEM (Splunk, Sumo Logic)
* Antivirus / Endpoint Protection
* Vulnerability scanners (Tenable, Qualys)
* Compliance solutions

### **Important Points**

* These solutions integrate natively with AWS.
* Customers can replicate on-prem security architectures.

---

# 🔷 **11. What compliance certifications does AWS hold?**

### **Answer:**

AWS is certified with:

* SOC 1, SOC 2, SOC 3
* ISO 27001, ISO 9001
* FedRAMP, DoD SRG
* PCI DSS Level 1

### **GDPR Support**

* AWS provides GDPR Data Processing Addendum
* Supports EU–US Privacy Shield

### **Important Points**

* Customers inherit AWS infrastructure compliance.
* Compliance becomes easier through AWS automated tools:

  * Config
  * Security Hub
  * CloudTrail

---

# 🔷 **12. What is AWS Well-Architected Security Pillar?**

### **Answer:**

It is part of the AWS Well-Architected Framework focusing on:

* Identity & Access Management
* Data Protection
* Infrastructure Protection
* Detecting Security Events
* Incident Response

### **Important Points**

* Used to evaluate and improve workload security.
* Available directly in the AWS Console.

---

# 🔷 **13. What is Amazon GuardDuty and what does it detect?**

### **Answer:**

GuardDuty is a managed threat detection service that analyzes:

* VPC Flow Logs
* DNS logs
* CloudTrail events
* Threat intelligence feeds

### **Detects:**

* Compromised EC2 instances
* Unauthorized access attempts
* Cryptocurrency mining
* Malicious IP behavior

### **Important Points**

* No agents required
* Integrates with CloudWatch for auto-remediation
* Covers multi-account environments

---

# 🔷 **14. How do AWS Config and CloudTrail differ?**

### **Answer:**

| Feature    | AWS Config                                       | AWS CloudTrail          |
| ---------- | ------------------------------------------------ | ----------------------- |
| Purpose    | Resource configuration tracking                  | API call logging        |
| Tracks     | “How resources are configured now and over time” | “Who did what and when” |
| Compliance | Yes                                              | Indirect                |
| Alerts     | Yes                                              | Yes                     |

### **Important Note**

Use both together to achieve full visibility.

---

# 🔷 **15. What does AWS CloudHSM provide?**

### **Answer:**

AWS CloudHSM is a hardware security module service that provides:

* Dedicated HSM appliances
* FIPS 140-2 Level 3 compliance
* Full customer control over keys
* Support for PKCS#11 & industry-standard APIs

### **Important Points**

* Needed for regulated industries (banking, pharma, government).
* Unlike KMS, CloudHSM keys are **not** managed by AWS.

---

# 🟦 **Important Points to Note (Summary Cheat Sheet)**

### 🔐 **Security in AWS is Shared**

* AWS → Data center, hardware, global network
* Customer → Data, IAM, encryption, OS, and apps

### 🔐 **Identity & Access**

* IAM, MFA, AWS SSO, Directory Service
* Use least privilege and role-based access

### 🔐 **Data Protection**

* KMS, CloudHSM
* Encryption at rest (EBS, S3, RDS)
* Encryption in transit (TLS)

### 🔐 **Monitoring**

* CloudTrail logs all API calls
* CloudWatch for metrics and alerts
* GuardDuty for threat detection

### 🔐 **Compliance**

* SOC, ISO, PCI, GDPR
* Automated compliance with AWS Config & Security Hub

### 🔐 **Best Practices**

* Enable MFA for root
* Use IAM Roles, not long-term keys
* Turn on CloudTrail in all regions
* Use VPC Flow Logs and GuardDuty
* Apply least privilege access
* Encrypt everything by default

---
