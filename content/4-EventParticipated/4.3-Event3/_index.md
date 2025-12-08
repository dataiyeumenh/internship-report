---
title: "Event 3"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Workshop Report: “DevOps on AWS”

**Date:** 17/11/2025  
**Speakers:** Truong Quang Dinh, Van Hoang Kha, Bao Huynh, Thinh Nguyen, Vy Tran

### Event Objectives

- Introduce DevOps mindset and culture.  
- Explain roles and responsibilities related to DevOps.  
- Present CI/CD pipelines, Infrastructure as Code (IaC), and best practices.  
- Introduce container services on AWS, monitoring, and observability.  
- Emphasize hands-on learning and real project implementation.  

### Speakers & Roles

- **Truong Quang Dinh** – DevOps Culture & Mindset  
- **Van Hoang Kha** – CI/CD Pipeline & Infrastructure as Code  
- **Bao Huynh, Thinh Nguyen, Vy Tran** – Container Services, Monitoring & Observability, DevOps Best Practices  

### Key Highlights

#### DevOps Culture

- **Definition:** DevOps engineers act as a bridge between Dev and Ops teams.  
- **Purpose:** Ensure collaboration, optimize delivery, and improve system stability.  
- **Core Elements:**  
  - Collaboration & Shared Responsibility  
  - Automation Everything (reduces human error)  
  - Continuous Learning & Experimentation  
  - Measurement & Metrics  

#### Next-Generation DevOps Roles

- **DevOps Engineer:** Implement and optimize CI/CD pipelines  
- **Cloud Engineer**  
- **Platform Engineer:** Focus on IDP (Internal Developer Portal) and LBAC  
- **Site Reliability Engineer**  

#### Measuring Success: DevOps Metrics

- Monitor deployment health  
- Improve agility  
- Ensure system stability  
- Optimize customer experience  
- Support technology ROI assessment  

#### DevOps Learning Path

- **Do:**  
  - Start with fundamentals  
  - Learn by building real projects  
  - Document everything  
  - Master one skill at a time  
  - Enhance soft skills  

- **Don't:**  
  - Stay in tutorial hell  
  - Copy-paste blindly  
  - Compare progress to others  
  - Give up after failures  

- **Mindset:** Deep knowledge in one area, broad knowledge across many:  
> “Deep in one area - Broad knowledge across many - you don’t need to master everything at once.”  

#### CI/CD Pipeline (Speaker: Van Hoang Kha)

- **Basic workflow:** Development → Peer Review → QA → Preprod → Production  
- **DevOps practices:**  
  - Test before deployment  
  - Automate delivery with a single button  
  - Static analysis & automated testing  
  - Create IaC templates → auto deployment → self-service → full automation  

- **Continuous Delivery vs Continuous Deployment:**  
  - **Continuous Delivery:** Dev → Unit Test → Integration Test → Acceptance Test → Production  
  - **Continuous Deployment:** Dev → Unit Test → Integration Test → Acceptance Test → Production  

#### Infrastructure as Code (IaC)

- **Issue with ClickOps:** Manual management prone to errors, not scalable.  
- **Definition of IaC:** Manage infrastructure using code instead of manual operations.  
- **Benefits:** Automation, Scalability, Reproducibility, Collaboration  

- **AWS IaC Tools:**  
  - **CloudFormation Template:** Declarative infrastructure definition.  
    - Key components:  
      - Format Version  
      - Description  
      - Parameters  
      - Resources  
      - Mappings  
      - Conditions  
      - Outputs  
  - **CloudFormation Stack:** Deployment unit combining all resources in the template; supports update, deletion, and modification.  

#### Container Services on AWS (Bao Huynh, Thinh Nguyen, Vy Tran)

- **Docker Fundamentals:** Microservices and containerization  
- **Amazon ECR:** Image storage, scanning, lifecycle policies  
- **Amazon ECS & EKS:** Deployment strategies, scaling, orchestration  
- **AWS App Runner:** Simplified container deployment  
- Demo & Case Study: Microservices deployment comparison  

#### Monitoring & Observability

- **CloudWatch:** Metrics, logs, alarms, dashboards  
- **AWS X-Ray:** Distributed tracing and performance insights  
- Demo: Full-stack observability setup  
- Best practices: alerting, dashboards, on-call processes  

#### DevOps Best Practices & Case Studies

- Deployment strategies: feature flags, A/B testing  
- Automated testing and CI/CD integration  
- Incident management and postmortems  
- Case studies: startup and enterprise DevOps transformations  

### Key Learnings

- DevOps encompasses CI/CD, culture, collaboration, automation, and continuous learning.  
- Containerization and IaC make infrastructure scalable, reproducible, and manageable.  
- Automation reduces errors and increases productivity.  
- Focus deeply on one area but maintain general knowledge across others.  
- Hands-on project practice is the best way to understand workflows and deploy IaC.  
- Clear communication is key to bridging Dev and Ops teams.  

### Applications at Work

- Implement automated CI/CD pipelines from unit test to deployment.  
- Use AWS CloudFormation for effective infrastructure management.  
- Deploy microservices with ECS, EKS, and App Runner.  
- Monitor and ensure observability with CloudWatch and X-Ray.  
- Apply DevOps mindset: collaboration, automation, measurement.  
- Document and learn from real projects.  

### Event Experience

Workshop **“DevOps Mindset & Container Services on AWS”** provided extensive practical knowledge:  

#### Learning from Speakers

- Hands-on CI/CD, IaC, and container services with AWS tools  
- Insights on Platform Engineer, DevOps Engineer, and Site Reliability Engineer roles  

#### Practical Skills

- Observe workflow from development to production  
- Learn to create and improve CI/CD pipelines  
- Practice automation and deployment using CloudFormation templates and containers  
- Set up full-stack monitoring & observability with CloudWatch and X-Ray  

#### Networking & Interaction

- Interact with speakers and peers  
- Understand the importance of clear communication between Dev and Ops teams  

#### Key Takeaways

- DevOps mindset increases productivity, reduces errors, and ensures system stability  
- Hands-on practice is essential for mastering automation, CI/CD pipelines, and container deployment  
- IaC and containerization make infrastructure scalable, reproducible, and collaborative  
- Monitoring & observability are essential to ensure reliability  

> Overall, the event provided a comprehensive view of DevOps mindset, culture, tools, container services, monitoring & observability, emphasizing automation, collaboration, and hands-on learning.