---
title: "Week 2 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Master both theoretical concepts and practical skills in configuring AWS VPC virtual networks, security firewalls, deploying secure virtual servers, and establishing advanced connections (Transit Gateway, VPN) through hands-on labs.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Mon | - **VPC Foundations, Subnets & Basic Network Topologies**<br>&emsp; + **Theory:** Learn about VPC, Subnet separation (Public/Private), Route Tables, Elastic Network Interfaces (ENI), and Elastic IP.<br>&emsp; + **Practice (Lab):** Initialize VPC, subnetting, create Internet Gateway (IGW), and associate Route Tables. | 29/06/2026 | 29/06/2026 | • Video *Module 02-01*<br>• Workshop *Section 1 & 3.1 - 3.4* |
| Tue | - **Firewalls, Security & VPC Monitoring**<br>&emsp; + **Theory:** Distinguish Security Groups (Stateful - ENI level) and Network ACLs (Stateless - Subnet level). Logging mechanisms with VPC Flow Logs.<br>&emsp; + **Practice (Lab):** Create dedicated Security Groups for Web/DB servers, configure Network ACLs, and enable VPC Flow Logs. | 30/06/2026 | 30/06/2026 | • Video *Module 02-02*<br>• Workshop *Section 2, 3.5 & 3.6* |
| Wed | - **NAT Gateway & EC2 Instance Deployment**<br>&emsp; + **Theory:** How NAT Gateways work (one-way outbound internet from Private Subnets) and VPC Endpoints.<br>&emsp; + **Practice (Lab):** Launch EC2 instance, test connectivity via Reachability Analyzer. Configure NAT Gateway and secure access via Systems Manager Session Manager. | 01/07/2026 | 01/07/2026 | • Video *Module 02-01*<br>• Workshop *Section 4.1 - 4.7* |
| Thu | - **Inter-VPC Connectivity & Transit Gateway**<br>&emsp; + **Theory:** Understand VPC Peering (non-transitive 1-to-1) and Transit Gateway (enterprise Hub-and-Spoke model).<br>&emsp; + **Practice (Lab):** Set up Transit Gateway environment, create Transit Gateway Attachments, and configure inter-VPC Route Tables. | 02/07/2026 | 02/07/2026 | • Video *Module 02-02*<br>• Workshop *Section 5.3* |
| Fri | - **AWS Site-to-Site VPN & Load Balancer Setup**<br>&emsp; + **Theory:** Hybrid network connectivity using AWS VPN and Direct Connect. Traffic distribution with Elastic Load Balancing (ALB, NLB, GLB).<br>&emsp; + **Practice (Lab):** Create Virtual Private Gateway, Customer Gateway, and configure complete Site-to-Site VPN connection. Perform resource cleanup. | 03/07/2026 | 03/07/2026 | • Video *Module 02-03*<br>• Workshop *Section 5.1 - 5.2 & Section 6* |

### Week 2 Achievements:

* **Production-Grade Infrastructure Setup**: Ability to build practical VPC network topologies including multi-AZ setup and security monitoring with Flow Logs.
* **Mastery of Advanced Connectivity**: Capable of configuring inter-VPC networks via Transit Gateway and setting up encrypted AWS Site-to-Site VPN connections to on-premises environments.
* **Cost Control**: Proficient in optimizing network resources and completing proper cleanup procedures after practice to prevent unexpected AWS charges.
