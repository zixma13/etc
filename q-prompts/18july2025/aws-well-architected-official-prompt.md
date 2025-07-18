Please perform an AWS Well-Architected Framework audit for Singapore region (ap-southeast-1) focusing on Security and Reliability pillars following the official AWS Well-Architected Framework structure. Return results in checklist format with pass/fail status.

=== SECURITY PILLAR ===
Based on AWS Well-Architected Security Pillar Design Principles:
• Implement a strong identity foundation
• Apply security at all layers  
• Automate security best practices
• Protect data in transit and at rest
• Keep people away from data
• Prepare for security events

SEC 1: Identity and Access Management
How do you manage identities for people and machines?
- SEC 1.1: Use strong identity foundation (root account protection, MFA enforcement)
- SEC 1.2: Secure AWS account root user (MFA, no daily usage, access keys removal)
- SEC 1.3: Identify and authenticate users (centralized identity provider, temporary credentials)
- SEC 1.4: Identify and authenticate machines (IAM roles for applications, instance profiles)
- SEC 1.5: Manage permissions dynamically (attribute-based access control, just-in-time access)

SEC 2: Detective Controls  
How do you detect and investigate security events?
- SEC 2.1: Configure service and application logging (CloudTrail, VPC Flow Logs, DNS logs)
- SEC 2.2: Analyze logs, findings, and metrics centrally (Security Hub, GuardDuty, Config)
- SEC 2.3: Automate response to events (EventBridge rules, Lambda automation, Systems Manager)

SEC 3: Infrastructure Protection
How do you protect your network resources?
- SEC 3.1: Create network layers (VPC, subnets, security groups, NACLs)
- SEC 3.2: Control traffic at all layers (WAF, Shield, security groups, NACLs)
- SEC 3.3: Automate network protection (AWS Firewall Manager, centralized rules)

SEC 4: Data Protection
How do you classify your data and protect it in transit and at rest?
- SEC 4.1: Identify and classify data (data classification, tagging, inventory)
- SEC 4.2: Protect data at rest (encryption, key management, access controls)
- SEC 4.3: Protect data in transit (TLS/SSL, VPN, certificate management)
- SEC 4.4: Automate data protection (automated encryption, DLP, backup encryption)

SEC 5: Incident Response
How do you anticipate, respond to, and recover from incidents?
- SEC 5.1: Educate your team (security training, incident response training)
- SEC 5.2: Prepare for incidents (incident response plan, communication plan, tools)
- SEC 5.3: Simulate incidents (game days, tabletop exercises, chaos engineering)
- SEC 5.4: Iterate on incident response (lessons learned, process improvement)

=== RELIABILITY PILLAR ===
Based on AWS Well-Architected Reliability Pillar Design Principles:
• Automatically recover from failure
• Test recovery procedures
• Scale horizontally to increase aggregate workload availability
• Stop guessing capacity
• Manage change in automation

REL 1: Foundations
How do you manage service quotas and constraints?
- REL 1.1: Manage service quotas and constraints (service limits monitoring, quota increases)
- REL 1.2: Plan your network topology (multi-AZ, multi-region, fault isolation)
- REL 1.3: Automate deployments (Infrastructure as Code, automated testing)

REL 2: Workload Architecture  
How do you design your workload service architecture?
- REL 2.1: Design your workload to withstand component failures (loose coupling, graceful degradation)
- REL 2.2: Build services focused on specific business domains (microservices, domain boundaries)
- REL 2.3: Provide cross-cutting concerns via platforms or libraries (shared services, common patterns)

REL 3: Change Management
How do you design your workload to adapt to changes in demand?
- REL 3.1: Monitor workload resources (CloudWatch metrics, custom metrics, dashboards)
- REL 3.2: Design your workload to adapt to changes in demand (Auto Scaling, load balancing)
- REL 3.3: Implement change management (deployment strategies, rollback procedures, testing)

REL 4: Failure Management
How do you back up data and test backup and recovery procedures?
- REL 4.1: Back up data (automated backups, cross-region replication, retention policies)
- REL 4.2: Use fault isolation to protect your workload (bulkheads, circuit breakers, timeouts)
- REL 4.3: Design your workload to withstand component failures (redundancy, health checks)
- REL 4.4: Test reliability (disaster recovery testing, chaos engineering, failure injection)

PRIORITY LEVELS:
🔴 CRITICAL - Violates core security/availability principles, immediate risk
🟠 HIGH - Significant gap in best practices, address within 1-2 weeks  
🟡 MEDIUM - Improvement opportunity, address within 1 month
🟢 LOW - Enhancement, address when resources allow

Format each item as: [✓] PASS, [✗] FAIL, or [⚠] WARNING - Question/Check: Specific findings and recommendations
