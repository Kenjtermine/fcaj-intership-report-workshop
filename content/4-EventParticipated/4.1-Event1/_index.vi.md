---
title: "Event 1: AWS Enterprise Cloud Architectures & Industry Application"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

### Mục tiêu sự kiện (Event Objectives)
* Khám phá các phương pháp và kiến trúc Cloud cấp doanh nghiệp (Enterprise-scale) trên nền tảng AWS.
* Lắng nghe chia sẻ thực chiến từ các đối tác hàng đầu của AWS tại Việt Nam và khu vực: Cloud Kinetics và Renova Cloud.
* Phân tích các ca ứng dụng thực tế (Industry Applications) trong quá trình chuyển đổi số, tối ưu hóa chi phí (FinOps) và hiện đại hóa hệ thống.

### Các chuyên đề và giải pháp tiêu biểu (Featured Topics & Solutions)
* **Cloud Kinetics - Tối ưu hóa Hành trình Lên mây (Cloud Migration & FinOps):** Trình bày về khung kiến trúc chuyển đổi quy mô lớn. Nhấn mạnh vào cách áp dụng FinOps để quản trị chi phí AWS hiệu quả, kiểm soát dòng tiền Cloud - cực kỳ phù hợp khi xây dựng các hệ thống tài chính cần Audit chặt chẽ.
* **Renova Cloud - Hiện đại hóa Ứng dụng & Dữ liệu (App Modernization & Data):** Chia sẻ cách tái cấu trúc ứng dụng nguyên khối (Monolith) sang Vi dịch vụ (Microservices) sử dụng Serverless và EKS. Ứng dụng AI/ML và Data Lake vào phân tích dữ liệu ngành bán lẻ và sản xuất.
* **Industry Applications (Ứng dụng đặc thù ngành):** Phân tích sâu về các giải pháp bảo mật và tuân thủ (Security & Compliance) dành riêng cho khối FSI (Financial Services Industry). Cách thiết lập Landing Zone chuẩn bảo mật để ngăn chặn rò rỉ dữ liệu.

### Trải nghiệm sự kiện (Event Experience)
Việc phân tích góc nhìn từ các chuyên gia Kiến trúc Giải pháp (Solutions Architects) của mạng lưới đối tác AWS (APN) mang lại một lăng kính bao quát hơn rất nhiều so với việc chỉ tự build Lab cá nhân.
* **Tư duy Enterprise (Quy mô doanh nghiệp):** Nhận ra rằng ở hệ thống lớn, kiến trúc không chỉ là code chạy được (Functional), mà phải giải quyết bài toán về bảo mật nhiều lớp (Defense in Depth), tính khả dụng cao (Multi-AZ) và khắc phục thảm họa (Disaster Recovery).
* **Kết nối thực tiễn dự án FCAJ:** Những kiến thức về bảo mật ranh giới và cách các doanh nghiệp cô lập dữ liệu hoàn toàn khớp với cách chúng ta đang thiết kế luồng Identity (Cognito) và tách bạch quyền hạn IAM (Security Isolation) cho các Lambda function (như TransactionEngine vs. ReportGenerator) trong dự án Digital Bank.

### Tổng kết (Lessons Learned)
* **Kiến trúc Cloud bám sát bài toán Kinh doanh:** Mọi quyết định lựa chọn công nghệ (Ví dụ: dùng Aurora Serverless hay DynamoDB, dùng EC2 hay Fargate) đều phải phục vụ trực tiếp cho bài toán kinh doanh với SLA (Cam kết chất lượng) và chi phí tối ưu nhất.
* **FinOps là liên tục:** Không phải đưa hệ thống lên Cloud là xong. Việc giám sát, gắn Tag (như sử dụng AWS Resource Groups thay thế myApplications) để truy vết chi phí là kỹ năng sống còn của một Cloud Architect.
* **Tận dụng Hệ sinh thái:** Đối với các dự án lớn, việc đứng trên vai người khổng lồ (sử dụng Managed Services của AWS và Best Practices từ Partners) giúp rút ngắn thời gian ra mắt thị trường (Time-to-market) và giảm rủi ro vận hành (Operational Overhead).