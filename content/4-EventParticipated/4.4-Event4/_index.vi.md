---
title: "Event 4"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 4.4. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# Bài thu hoạch Workshop: “AWS Security & GuardDuty”

**Ngày:** 29/11/2025    
**Diễn giả:** Tran Duc Anh, Nguyen Tuan Thinh, Nguyen Do Thanh Dat

### Mục Đích Của Sự Kiện

- Giới thiệu các công cụ bảo mật AWS ở cấp tổ chức (org-level).  
- Hiểu cách vận hành GuardDuty như một Managed IDS/IPS thông minh.  
- Học cách triển khai Detection-as-Code và tự động hóa alerting.  

### Danh Sách Diễn Giả & Vai Trò

- **Tran Duc Anh** – CloudTrail (org-level)  
- **Nguyen Tuan Thinh** – Tổng quan GuardDuty, Protection Plans, Alerting & Automation  
- **Nguyen Do Thanh Dat** – Detection-as-Code (infrastructure + rules)  

### Nội Dung Nổi Bật

#### CloudTrail (Speaker: Tran Duc Anh)

- Giám sát hoạt động trên toàn bộ tổ chức AWS (org-level)  
- Lưu trữ và phân tích logs từ các tài khoản con để đảm bảo compliance và forensic  

#### GuardDuty Overview (Speaker: Nguyen Tuan Thinh)

- **Managed IDS/IPS thông minh:** giám sát liên tục các tài khoản AWS  
- **Nguồn dữ liệu chính:**  
  - CloudTrail Events  
  - VPC Flow Logs  
  - DNS Logs  
- **Zero configuration:** bật là chạy, phân tích tự động  
- **Protection Plans nổi bật:**  
  - S3 Protection  
  - EKS Protection  
  - Malware Protection (EBS scan)  
  - RDS Protection  
  - Lambda Protection  
  - Runtime Monitoring qua GuardDuty Agent  

#### Alerting & Automation

- **Detection-as-Code demo bằng CloudFormation:**  
  - EventBridge rule chỉ trigger khi GuardDuty finding có severity High hoặc Critical  
  - Tự động invoke Lambda để remediation (isolate instance, disable keys, tag resource…)  
  - Gửi alert real-time qua SNS (email/SMS) tới team hoặc khách hàng  

#### Detection-as-Code (Speaker: Nguyen Do Thanh Dat)

- Triển khai detection dựa trên **infrastructure + rules**  
- Quản lý bảo mật theo code, reproducible và dễ audit  
- Tích hợp với CI/CD để tự động hóa quá trình phát hiện và phản ứng  

### Những Gì Học Được

- AWS GuardDuty là một công cụ mạnh mẽ để giám sát và phát hiện bất thường trên nhiều tài khoản AWS.  
- Zero configuration giúp tiết kiệm thời gian triển khai nhưng vẫn đảm bảo hiệu quả giám sát.  
- Alerting & Automation giúp giảm thời gian phản ứng và tăng hiệu quả remediation.  
- Detection-as-Code biến quy trình bảo mật thành code, dễ kiểm soát và audit.  

### Ứng Dụng Vào Công Việc

- Thiết lập GuardDuty cho toàn bộ tổ chức AWS để giám sát và phát hiện sự cố.  
- Tích hợp EventBridge + Lambda + SNS để tự động hóa alert và remediation.  
- Viết và triển khai Detection-as-Code để chuẩn hóa quy trình bảo mật.  
- Giám sát các dịch vụ AWS quan trọng: S3, EKS, RDS, Lambda, EBS.  

### Trải nghiệm trong sự kiện

Workshop cung cấp trải nghiệm thực tế về giám sát bảo mật và automation:  

#### Học hỏi từ diễn giả

- Thực hành triển khai CloudTrail ở cấp tổ chức  
- Demo Alerting & Automation với GuardDuty, Lambda và SNS  
- Học cách viết Detection-as-Code để triển khai bảo mật reproducible  

#### Kỹ thuật thực tế

- Quan sát luồng dữ liệu CloudTrail, VPC Flow Logs, DNS Logs  
- Thiết lập EventBridge rules và Lambda remediation automation  
- Tích hợp SNS để nhận alert real-time  

#### Kết nối & Trao đổi

- Trao đổi về best practices triển khai GuardDuty cho tổ chức  
- Hiểu tầm quan trọng của tự động hóa alert và detection-as-code  

#### Bài học rút ra

- Zero configuration GuardDuty giúp giám sát hiệu quả và nhanh chóng.  
- Alerting & Automation giảm thiểu thời gian phản hồi và rủi ro bảo mật.  
- Detection-as-Code là cách tiếp cận hiện đại, reproducible và có thể audit.  

> Tổng thể, sự kiện giúp nắm rõ cách AWS cung cấp giám sát bảo mật tự động, phát hiện bất thường và triển khai remediation theo code.