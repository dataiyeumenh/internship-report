---
title: "Event 4"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 4.4. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Workshop Report: “AWS Security & GuardDuty”

**Date:** 29/11/2025    
**Speakers:** Tran Duc Anh, Nguyen Tuan Thinh, Nguyen Do Thanh Dat

### Event Objectives

- Introduce AWS security tools at the organization (org-level).  
- Understand how GuardDuty operates as an intelligent managed IDS/IPS.  
- Learn Detection-as-Code and automate alerting and remediation.  

### Speakers & Roles

- **Tran Duc Anh** – CloudTrail (org-level)  
- **Nguyen Tuan Thinh** – GuardDuty Overview, Protection Plans, Alerting & Automation  
- **Nguyen Do Thanh Dat** – Detection-as-Code (infrastructure + rules)  

### Key Content

#### CloudTrail (Speaker: Tran Duc Anh)

- Monitor activities across all AWS accounts at the organization level.  
- Collect and analyze logs from member accounts to ensure compliance and support forensic analysis.  

#### GuardDuty Overview (Speaker: Nguyen Tuan Thinh)

- **Managed IDS/IPS:** continuously monitor multiple AWS accounts.  
- **Main data sources:**  
  - CloudTrail Events  
  - VPC Flow Logs  
  - DNS Logs  
- **Zero configuration:** enable and run automatically  
- **Highlighted Protection Plans:**  
  - S3 Protection  
  - EKS Protection  
  - Malware Protection (EBS scan)  
  - RDS Protection  
  - Lambda Protection  
  - Runtime Monitoring via GuardDuty Agent  

#### Alerting & Automation

- **Detection-as-Code demo using CloudFormation:**  
  - EventBridge rules trigger only on High or Critical GuardDuty findings  
  - Automatically invoke Lambda for remediation (isolate instance, disable keys, tag resource…)  
  - Send real-time alerts via SNS (email/SMS) to teams or customers  

#### Detection-as-Code (Speaker: Nguyen Do Thanh Dat)

- Deploy detection based on **infrastructure + rules**  
- Security managed as code, reproducible, and auditable  
- Integrate with CI/CD for automated detection and response  

### Key Takeaways

- AWS GuardDuty is a powerful tool for monitoring and detecting anomalies across accounts.  
- Zero configuration saves setup time while providing effective monitoring.  
- Alerting & Automation reduce response time and increase remediation efficiency.  
- Detection-as-Code transforms security processes into code, making them reproducible and auditable.  

### Workplace Applications

- Set up GuardDuty at the organization level for comprehensive monitoring.  
- Integrate EventBridge + Lambda + SNS for automated alerts and remediation.  
- Write and deploy Detection-as-Code to standardize security procedures.  
- Monitor critical AWS services: S3, EKS, RDS, Lambda, EBS.  

### Event Experience

The workshop provided practical experience in security monitoring and automation:  

#### Learning from Speakers

- Hands-on CloudTrail implementation at org-level  
- Demo of GuardDuty Alerting & Automation with Lambda and SNS  
- Learn to write Detection-as-Code for reproducible security deployment  

#### Technical Practice

- Observe CloudTrail, VPC Flow Logs, and DNS Logs workflow  
- Set up EventBridge rules and Lambda remediation automation  
- Integrate SNS for real-time alert notifications  

#### Networking & Exchange

- Exchange best practices for deploying GuardDuty organization-wide  
- Understand the importance of automated alerting and detection-as-code  

#### Lessons Learned

- Zero configuration GuardDuty enables quick and effective monitoring.  
- Alerting & Automation minimize response time and security risk.  
- Detection-as-Code provides a modern, reproducible, and auditable approach to security.  

> Overall, the event offered a comprehensive understanding of AWS automated security monitoring, anomaly detection, and code-driven remediation.