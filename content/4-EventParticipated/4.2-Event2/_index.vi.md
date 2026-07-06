---
title: "FCAJ Community Day: Conference Call"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch “FCAJ Community Day: Conference Call”

### Mục Đích Của Sự Kiện

- Là nơi để cộng đồng kết nối, giao lưu, chủ động bắt chuyện và truyền cảm hứng cho nhau (kể cả những anh em ở khu vực tầng 36).
- Cập nhật tình hình thị trường việc làm IT trong kỷ nguyên AI và những kỹ năng/yêu cầu mới mà các kỹ sư phần mềm cần trang bị.
- Đi sâu vào sáu phiên chia sẻ thực tế từ kỹ thuật đến nghiệp vụ, xoay quanh các chủ đề nóng như AI, Cloud (AWS), kiến trúc hệ thống doanh nghiệp và kinh nghiệm thực chiến từ các cuộc thi Hackathon.

### Danh Sách Diễn Giả

- **Trương Tịnh** - platform engineer of GoTymeX
- **Phạm Nguyễn Hải Anh** - AWS Community Builder | Cloud Consultant
- **Nguyễn tuấn Thịnh** - DevOps/Cloud Engineer FCAJ
- **Lê Phạm Ngọc Uyển, Nguyễn Ngọc Quỳnh Mai, Nguyễn Phương Thảo** - Building UTMorpho from Idea to Reality, 36 hrs with LotusHacks team
- **Đào Minh đức** - Solutions Architect
- **Lâm Hoàng Cát Vy** - Sr Business Systems Analyst | Applied AI Initiatives Team Lead | IT Young Talents Program Manager of VPBank | AWS AI Engineering Community Builder

### Nội Dung Nổi Bật

#### Tư duy Nghiệp vụ trong phát triển AI 

- **Sản phẩm phải hướng tới người dùng**: Khi thiết kế một giải pháp AI, không chỉ quan tâm đến công nghệ mà phải trả lời được 4 câu hỏi cốt lõi: Ai xài? Xài cái gì? Tại sao phải xài? Khi nào là lúc thích hợp để triển khai giải pháp đó?.
- **Nghiên cứu thị trường và ROI**: Không thể đề xuất một hệ thống AI tốn kém (ví dụ 1 tỷ đồng) mà không chứng minh được bài toán thị trường và tính khả thi. Mọi giải pháp đều phải đánh giá dựa trên mức độ hồi vốn và lợi ích mang lại (tiết kiệm hàng tỷ đồng thay vì "chém gió" lên hàng triệu đô).
- **Thấu hiểu KPI của Stakeholder**: Trong môi trường doanh nghiệp, kỹ sư cần hiểu KPI và công việc của các phòng ban khác (như Security, Business) để dễ dàng giao tiếp, xin cấp phép và phối hợp triển khai hệ thống.

#### Xây dựng hệ thống Multi-Agent cho Đánh giá Tín dụng Startup

- **Giới hạn của Single Agent**: Với những bài toán phức tạp đòi hỏi nhiều chiều dữ liệu đầu vào (báo cáo tài chính, thị trường, team founder của Startup), một Single Agent sẽ gặp giới hạn về Context Window và thiếu tính chuyên môn sâu, dễ bị quá tải.
- **Kiến trúc Multi-Agent**: Hệ thống được thiết kế như một "Hội đồng tín dụng" bao gồm: Manager (Orchestrator phân chia công việc), Financial Analyst (phân tích báo cáo tài chính), Research (đánh giá thị phần, đối thủ), Evaluator (đánh giá Founder), và Risk Accessor (đánh giá rủi ro).
- **Truyền tri thức**: Việc cung cấp ngữ cảnh cho AI không đơn giản là đẩy hàng trăm trang PDF vào, mà là Context Engineering – trích xuất những "tinh túy" nghiệp vụ từ các chuyên gia để hướng dẫn mô hình xử lý chính xác dữ liệu.

#### Bảo mật, Tuân thủ và Trách nhiệm trong Doanh nghiệp

- **Kiểm soát rủi ro từ MCP và Prompt Injection**: Trong khối tài chính, bảo mật là ưu tiên hàng đầu. Việc cắm các công cụ (MCP) phải được xét duyệt kỹ để tránh rò rỉ dữ liệu. Hệ thống cần các lớp Output/Input filtering để phòng chống Prompt Injection.
- **Quản lý khóa API**: Bắt buộc phải thường xuyên thay đổi (rotate) API Key và Access Key của IAM để tránh rò rỉ chi phí (ví dụ bị đánh cắp key để gọi model lớn tiêu tốn tiền).
- **Audit Trail và Trách nhiệm**: Bất kỳ quyết định nào do AI đưa ra (như duyệt khoản vay 10 tỷ hay 100 tỷ) đều phải lưu vết và có con người rà soát. Người phê duyệt hệ thống mới là người chịu trách nhiệm trước pháp luật, không phải nền tảng AI.

#### Kỹ thuật giao tiếp và tính bất định của AI

- **Tránh tư duy "Internet Builder"**: tránh kéo mọi code, rule trên mạng về dùng mà không hiểu. Cần đưa đúng ngữ cảnh (Mục tiêu, Đối tượng, Định dạng) chuyên biệt của công ty vào prompt.
- **LLM luôn có tính bất định**: Dù cài Temperature = 0, kết quả vẫn có thể khác nhau do cách GPU tính toán hoặc do các nhà cung cấp tối ưu hóa chi phí (Inference optimization - gộp nhiều câu prompt).
- Cần có hệ thống test và downstream linh hoạt để xử lý các kết quả không chuẩn định dạng.

#### Hạ tầng Cloud và Kinh nghiệm Hackathon

- **Amazon CloudFront**: Cung cấp cơ chế Flat-rate pricing giúp doanh nghiệp chặn đứng nỗi lo hóa đơn tăng đột biến (bill spike) khi gặp DDoS, kết hợp các lớp bảo mật như VPC Origin và MTLS.
- **Kinh nghiệm Hackathon**: Khi xây dựng ứng dụng AI tạo UI trong 36 giờ, bài học lớn nhất là tập trung vào tính năng cốt lõi (edit trực tiếp trên UI) thay vì "over-thinking" làm quá nhiều tính năng. Cần cảnh giác với giới hạn token và tình trạng AI "Over-generation" (tự sinh code thừa).

### Những Gì Học Được

#### Tư Duy Thiết Kế & Làm Việc

- **Kiến thức kỹ thuật nền tảng là bắt buộc**: AI chỉ là công cụ hỗ trợ. Để triển khai sản phẩm lên production trong doanh nghiệp, các kiến thức cốt lõi về Software Engineering (Backend, cơ sở dữ liệu, JWT, mã hóa) là yếu tố quyết định.
- **Phục vụ người dùng cuối**: Tư duy xây dựng hệ thống không chỉ dừng ở mức "chạy được demo", mà phải đảm bảo hệ thống vận hành an toàn (Securely) và đáng tin cậy (Reliably).

#### Kiến Trúc Kỹ Thuật & Bảo Mật

- Nắm vững cách thiết kế hệ thống **Multi-Agent**, phân chia chuyên môn rõ ràng cho từng agent để chúng có khả năng **phản biện chéo** và **xử lý song song**.
- Hiểu tầm quan trọng của **IaC** như Terraform để triển khai hạ tầng nhất quán, quản lý các phiên bản cài đặt và lưu vết các thay đổi.

### Ứng Dụng Vào Công Việc

- **Đánh giá tính khả thi bằng ROI**: Áp dụng bài học từ chị Cát Vy, bất kỳ đề xuất hệ thống AI nào trong tương lai cũng cần phân tích chi phí và lợi ích (ROI) trước khi trình bày với cấp quản lý.
- **Cấu trúc Multi-Agent cho tác vụ phức tạp**: Chuyển đổi các tác vụ đọc hiểu tài liệu lớn thành một quy trình gồm nhiều agent (đóng vai trò phân tích, tóm tắt và đánh giá rủi ro) để tăng độ chính xác.
- **Thắt chặt Guardrails**: Thiết lập các lớp kiểm tra đầu vào (Input filtering) chống Prompt Injection và bảo mật API Key nghiêm ngặt cho dự án cá nhân/công ty.
- **Thực hành Context Engineering**: Thay vì nhồi nhét tài liệu thô, tôi sẽ học cách trích lọc kiến thức chuyên môn tinh túy (Knowledge Transfer) để làm ngữ cảnh chuẩn cho LLM.

### Trải nghiệm trong event

#### Học hỏi từ các diễn giả có chuyên môn cao

- Phiên chia sẻ của chị Cát Vy thực sự đã khai mở tư duy của tôi về **"Enterprise-grade AI"**. Tôi nhận ra khoảng cách giữa việc làm một project AI ở nhà và việc đưa nó vào hệ thống ngân hàng là rất lớn, đặc biệt ở khâu tuân thủ và bảo mật dữ liệu.
- Sự khắt khe trong việc cấp quyền công cụ (thậm chí không được tự tiện cài Ollama vì lo ngại rò rỉ dữ liệu) cho thấy trách nhiệm vô cùng nặng nề của một kỹ sư khi thực chiến.

#### Trải nghiệm kỹ thuật thực tế

- Được hướng dẫn cách tiếp cận bài toán Đánh giá tín dụng cho startup – một nhóm đối tượng thiếu vắng báo cáo tài chính truyền thống – bằng sự phối hợp nhịp nhàng của kiến trúc Multi-Agent.
- Nắm bắt được lộ trình triển khai vòng đời sản phẩm chuẩn mực trong doanh nghiệp: Từ POC -> Internal testing -> SIT -> UAT -> Pilot cho đến Scale.

#### Ứng dụng công cụ hiện đại

- Trải nghiệm quy trình **"Knowledge Transfer"** thực tế, kết hợp sức mạnh của LLM với tri thức nghiệp vụ tài chính.
- Mở rộng kiến thức về các framework hỗ trợ doanh nghiệp như Bedrock Agent Core và Terraform để tối ưu hóa việc đóng gói và triển khai hạ tầng.

#### Kết nối và trao đổi

- Sự kiện giúp tôi có cơ hội giao lưu, đặt câu hỏi và hiểu được tầm quan trọng của việc thấu hiểu KPI của đối tác nhằm tạo sự mượt mà trong quá trình làm việc nhóm.

#### Bài học rút ra

- "Numbers speak louder than words": Mọi giải pháp công nghệ đề xuất lên cấp trên đều phải được chứng minh bằng các con số thực tế thay vì những lời hứa hẹn sáo rỗng.
- Con người luôn là yếu tố chốt chặn cuối cùng: Dù AI có thông minh đến đâu, người kỹ sư thiết kế và người phê duyệt hệ thống vẫn phải chịu trách nhiệm hoàn toàn (Audit) về các quyết định được đưa ra.

#### Một số hình ảnh khi tham gia sự kiện

![Ảnh tham gia sự kiện](/images/event2305.jpg)

> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.
