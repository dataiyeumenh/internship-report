---
title: "Event 3"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# Bài thu hoạch Workshop: “DevOps on AWS”

**Ngày:** 17/11/2025    
**Diễn giả:** Truong Quang Dinh, Van Hoang Kha, Bao Huynh, Thinh Nguyen, Vy Tran

### Mục Đích Của Sự Kiện

- Giới thiệu tư duy và văn hóa DevOps.  
- Giải thích vai trò và trách nhiệm của các vị trí liên quan đến DevOps.  
- Trình bày CI/CD pipelines, Infrastructure as Code (IaC) và best practices.  
- Giới thiệu container services trên AWS, giám sát hệ thống và observability.  
- Nhấn mạnh việc học thực hành và triển khai dự án thực tế.  

### Danh Sách Diễn Giả & Vai Trò

- **Truong Quang Dinh** – DevOps Culture & Mindset  
- **Van Hoang Kha** – CI/CD Pipeline & Infrastructure as Code  
- **Bao Huynh, Thinh Nguyen, Vy Tran** – Container Services, Monitoring & Observability, DevOps Best Practices  

### Nội Dung Nổi Bật

#### Văn Hóa DevOps

- **Định nghĩa:** Kỹ sư DevOps là cầu nối giữa Dev team và Ops team.  
- **Mục đích:** Đảm bảo hợp tác, tối ưu quá trình delivery và cải thiện độ ổn định hệ thống.  
- **Các yếu tố cốt lõi:**  
  - Collaboration & Shared Responsibility  
  - Automation Everything (giảm lỗi từ con người)  
  - Continuous Learning & Experimentation  
  - Measurement & Metrics  

#### Các Vai Trò DevOps Thế Hệ Mới

- **DevOps Engineer:** Triển khai và tối ưu CI/CD pipelines  
- **Cloud Engineer**  
- **Platform Engineer** – Chú trọng IDP (Internal Developer Portal) và LBAC  
- **Site Reliability Engineer**  

#### Đo Lường Thành Công: DevOps Metrics

- Giám sát tình trạng deployment  
- Cải thiện agility  
- Đảm bảo độ ổn định hệ thống  
- Tối ưu trải nghiệm khách hàng  
- Hỗ trợ đánh giá ROI của công nghệ  

#### Lộ Trình Học DevOps

- **Nên làm:**  
  - Bắt đầu từ nền tảng cơ bản  
  - Học bằng cách xây dựng dự án thực tế  
  - Ghi chép toàn bộ quá trình  
  - Thành thạo từng kỹ năng một  
  - Nâng cao kỹ năng mềm  

- **Không nên làm:**  
  - Chỉ xem tutorial mà không thực hành  
  - Copy-paste mà không hiểu  
  - So sánh tiến độ với người khác  
  - Bỏ cuộc sau thất bại  

- **Tư duy:** Tập trung sâu vào một lĩnh vực nhưng có kiến thức tổng quát ở các lĩnh vực khác:  
> “Deep in one area - Broad knowledge across many - you don’t need to master everything at once.”  

#### CI/CD Pipeline (Diễn giả: Van Hoang Kha)

- **Workflow cơ bản:** Development → Peer Review → QA → Preprod → Production  
- **Thực hành DevOps:**  
  - Test trước khi triển khai  
  - Tự động hóa delivery chỉ với 1 nút nhấn  
  - Static analysis và automated testing  
  - Tạo template IaC → triển khai tự động → self-service → full automation  

- **Continuous Delivery vs Continuous Deployment:**  
  - **Continuous Delivery:** Dev → Unit Test → Integration Test → Acceptance Test → Production  
  - **Continuous Deployment:** Dev → Unit Test → Integration Test → Acceptance Test → Production  

#### Infrastructure as Code (IaC)

- **Vấn đề với ClickOps:** Quản lý thủ công dễ lỗi, không scale được.  
- **Định nghĩa IaC:** Quản lý hạ tầng bằng code thay vì thao tác thủ công.  
- **Lợi ích:** Automation, Scalability, Reproducibility, Collaboration  

- **Công cụ IaC của AWS:**  
  - **CloudFormation Template:** Định nghĩa hạ tầng theo dạng declarative.  
    - Các phần chính:  
      - Format Version  
      - Description  
      - Parameters  
      - Resources  
      - Mappings  
      - Conditions  
      - Outputs  
  - **CloudFormation Stack:** Đơn vị triển khai kết hợp tất cả resources trong template; hỗ trợ update, xóa, chỉnh sửa.  

#### Container Services trên AWS (Bao Huynh, Thinh Nguyen, Vy Tran)

- **Docker Fundamentals:** Microservices và containerization.  
- **Amazon ECR:** Lưu trữ image, scanning, lifecycle policies.  
- **Amazon ECS & EKS:** Chiến lược triển khai, scaling, orchestration.  
- **AWS App Runner:** Triển khai container đơn giản.  
- Demo & Case Study: So sánh triển khai microservices.  

#### Monitoring & Observability

- **CloudWatch:** Metrics, logs, alarms, dashboards.  
- **AWS X-Ray:** Distributed tracing và performance insights.  
- Demo: Thiết lập full-stack observability.  
- Best practices: alerting, dashboards, on-call processes.  

#### DevOps Best Practices & Case Studies

- Deployment strategies: feature flags, A/B testing  
- Automated testing và CI/CD integration  
- Incident management và postmortems  
- Case studies: startup và enterprise DevOps transformations  

### Những Gì Học Được

- DevOps không chỉ là CI/CD mà còn bao gồm văn hóa, hợp tác, tự động hóa và học tập liên tục.  
- Containerization và IaC giúp hạ tầng scalable, reproducible và dễ quản lý.  
- Automation giúp giảm lỗi và tăng năng suất.  
- Tập trung sâu vào một lĩnh vực nhưng có kiến thức tổng quát.  
- Thực hành dự án thực tế là cách tốt nhất để hiểu workflow và triển khai IaC.  
- Giao tiếp rõ ràng là chìa khóa để kết nối Dev và Ops teams.  

### Ứng Dụng Vào Công Việc

- Triển khai CI/CD pipelines tự động hóa từ unit test đến deployment.  
- Sử dụng AWS CloudFormation để quản lý hạ tầng hiệu quả.  
- Sử dụng container services (ECS, EKS, App Runner) để deploy microservices.  
- Giám sát và observability với CloudWatch và X-Ray.  
- Áp dụng tư duy DevOps: hợp tác, tự động hóa, đo lường hiệu quả.  
- Ghi chép và học từ dự án thực tế.  

### Trải nghiệm trong sự kiện

Workshop **“DevOps Mindset & Container Services on AWS”** mang lại nhiều kiến thức thực tiễn:  

#### Học hỏi từ diễn giả

- Thực hành CI/CD, IaC và container services với các công cụ AWS.  
- Chia sẻ thực tế về vai trò Platform Engineer, DevOps Engineer, Site Reliability Engineer.  

#### Kỹ thuật thực tế

- Quan sát workflow từ development đến production.  
- Học cách tạo và cải tiến pipeline CI/CD.  
- Thực hành automation và deployment bằng CloudFormation templates và containers.  
- Cài đặt monitoring & observability full-stack với CloudWatch và X-Ray.  

#### Kết nối & Trao đổi

- Tương tác với diễn giả và các đồng nghiệp.  
- Hiểu tầm quan trọng của giao tiếp rõ ràng giữa Dev và Ops teams.  

#### Bài học rút ra

- Tư duy DevOps giúp tăng năng suất, giảm lỗi và đảm bảo hệ thống ổn định.  
- Thực hành là chìa khóa để thành thạo automation, CI/CD pipelines và container deployment.  
- IaC và containerization giúp hạ tầng scalable, reproducible và collaborative.  
- Monitoring & observability là thiết yếu để đảm bảo reliability.  

> Nhìn chung, sự kiện cung cấp cái nhìn toàn diện về tư duy DevOps, văn hóa, công cụ, container services, monitoring & observability, nhấn mạnh tự động hóa, hợp tác và học tập thực tế.