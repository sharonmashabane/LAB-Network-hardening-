# LAB-Network-hardening-

OVERVIEW:

In this lab, you utilize Amazon Inspector to scan for vulnerabilities in your AWS resources, specifically AWS Lambda functions. You learn how to activate Amazon Inspector, interpret the vulnerability reports, and remediate the findings.

The developers at AnyCompany are in the initial phases of building an application primarily using AWS Lambda. Throughout the development process, they need an automated security tool that not only scans for vulnerable software packages, but also scans within the code itself. You decide to utilize Amazon Inspector to fill this need.

Amazon Inspector meets the requirements of being able to scan AWS Lambda functions by quickly responding to new deployments. It also automatically scans additional resources such as EC2 instances, Amazon ECRs within AnyCompany’s AWS account.

What I Configured

Created a VPC with both public and private subnets.

Launched EC2 instances into each subnet for testing access.

Configured Security Groups to strictly control inbound and outbound traffic.

Set up Network ACLs (NACLs) at the subnet level to provide another layer of protection.

Restricted access so only specific IP ranges and ports were allowed (e.g., SSH only from my IP, HTTP only for web traffic).

Tested connectivity between instances to confirm that rules were applied correctly.

> What I Learned

Principle of Least Privilege

Only open the ports and IP ranges that are required.

Example: Allowing SSH access only from my IP address instead of from the whole internet.

Security Groups vs NACLs

Security Groups are stateful → if inbound traffic is allowed, the response is automatically allowed.

NACLs are stateless → inbound and outbound rules must be set explicitly.

Both work together to protect resources.

Layered Security

Using multiple controls (SG + NACL) reduces the risk of unauthorized access.

Public resources (e.g., web servers) go in public subnets, while sensitive systems (e.g., databases) stay private.

Testing & Validation

Connectivity checks are essential — just setting rules isn’t enough.

I practiced troubleshooting with ping, curl, and SSH to confirm configurations.

> Reflections

Network hardening is about proactive defense, not just connecting services.

I realized how easy it is to accidentally make resources public if rules are too open.

This lab helped me appreciate why network security is a top priority in cloud environments.

The combination of theory (least privilege, segmentation) and practice (SGs, NACLs, VPC design) made the concepts clear.

> Takeaway

Through this lab, I learned how to:

Apply network security best practices in AWS.

Use Security Groups and NACLs effectively.

![NEYWORK HARDENING](https://github.com/user-attachments/assets/bc829422-3bf8-499f-b1c3-a3f2ab8ec4ad)


Harden AWS environments by limiting access to only what is necessary.

Build confidence in troubleshooting cloud networking issues.
