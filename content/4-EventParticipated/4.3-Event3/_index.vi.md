---
title: "FCAJ Community Day: Mini meet up"
date: 2026-06-06
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---


# Bài thu hoạch “FCAJ Community Day: Mini meet up”

### Mục Đích Của Sự Kiện

- Đào sâu vào các kiến thức kỹ thuật thực tiễn: Triển khai Game Multiplayer bằng Godot & AWS WebSockets, Ảo hóa và Docker, xây dựng kiến trúc GraphRAG, và ứng dụng Machine Learning để phát hiện tấn công mạng.
- Định hướng và chia sẻ kinh nghiệm thực tế về lộ trình phát triển sự nghiệp từ vị trí IT Helpdesk lên System Admin và DevOps Engineer trong môi trường doanh nghiệp lớn.

### Danh Sách Diễn Giả

- **Trần Trung Vinh** - System Administrator at Central Retail Group
- **Việt Phát** - AI majoring at Swinburne University of Technology
- **Trương Huy Phước** - AWS Student
- **Nguyễn Quốc Bảo** - Sinh viên Đại học Swinburne, AWS Student
- **Lê Hoàng Gia Đại** - AWS Student
- **Huỳnh Bảo** - Junior Cloud Native Developer of Endava Vietnam|Founder/Head Lab of ITea Lab

### Nội Dung Nổi Bật

#### Tương lai của AI và Lời khuyên cho giới trẻ

- **AI sẽ nâng cao mức trung bình**: AI sẽ mang lại sự nhất quán và thiết lập một tiêu chuẩn mới, thay thế những hiệu suất công việc ở mức trung bình hoặc dưới trung bình.
- **Định hướng phát triển**: Những người làm việc chỉ vì tiền lương mà không có đam mê sẽ dễ bị AI đào thải. Lời khuyên là hãy tìm kiếm công việc bạn thực sự đam mê, liên tục phát huy thế mạnh để trở nên xuất sắc và biến AI thành công cụ hỗ trợ mình.
- **Hoàn thiện Tech Stack**: Trước khi xây dựng các AI agent phức tạp, doanh nghiệp và kỹ sư cần tự động hóa và tích hợp AI vào chính quy trình phát triển phần mềm (tech stack) hiện tại để đảm bảo an toàn và tốc độ.

#### Kiến trúc Game Multiplayer trên AWS

- **Lựa chọn Protocol**: WebSocket được ưu tiên cho các game Turn-based/Lobby/Chat vì tính năng giao tiếp thời gian thực, nhắn tin song công (full-duplex) và đảm bảo truyền tải, khắc phục được độ trễ cao của HTTP Polling và sự phức tạp của UDP.
- **AWS Architecture**: Kết nối client (Godot) thông qua API Gateway (quản lý $connect, $disconnect, $default). Logic được xử lý tại Lambda Function và trạng thái người chơi được lưu trữ tại DynamoDB.
- **Thách thức**: Cần xử lý tốt "Stale connections" (kết nối ảo khi rớt mạng), chi phí scan DynamoDB khi lượng người chơi lớn, và bản chất Stateless của Lambda.

#### Ảo hóa và Containerization (Docker)

- **Giới hạn của Virtual Machine (VM)**: VM rất nặng vì mỗi máy ảo chạy một hệ điều hành riêng, tốn thời gian khởi động và tiêu tốn nhiều tài nguyên CPU/RAM.
- **Sức mạnh của Container**: Containerization đóng gói code và thư viện cần thiết, chia sẻ chung hệ điều hành máy chủ (Host OS) thông qua Container Engine. Điều này giúp khởi động tính bằng mili-giây, cực kỳ nhẹ và có tính di động cao (chạy được trên mọi môi trường).
- **Docker Layer Caching**: Docker build image theo từng layer từ trên xuống dưới. Nếu không có sự thay đổi ở các layer trên, Docker sẽ dùng lại cache, giúp tiết kiệm tối đa thời gian build.

#### Nâng cấp AI với GraphRAG trên AWS

- **Hạn chế của RAG truyền thống**: RAG cơ bản chỉ lấy thông tin dựa trên độ tương đồng từ vựng/ngữ nghĩa, không thể trả lời các câu hỏi phức tạp đòi hỏi sự suy luận chéo (multi-hop reasoning) giữa nhiều tài liệu rời rạc.
- **Giải pháp GraphRAG**: Sử dụng Graph Database để lưu trữ và hiểu rõ mối quan hệ (relationship) giữa các thực thể (entities).
- **Triển khai trên AWS**: Có 2 hướng. Hướng Fully Managed sử dụng Amazon Bedrock (tự động chunking, extract entity) và Amazon Neptune Analytics. Hướng Custom cho phép tự tinh chỉnh pipeline bằng LlamaIndex kết hợp với Neptune.

#### Phát hiện tấn công mạng bằng WAF và Machine Learning (NIDS)

- **Nhược điểm của WAF**: WAF truyền thống dựa trên các tập luật định trước (Rule-based), do đó dễ dàng bị vượt qua bởi các cuộc tấn công Zero-day, tấn công lai hoặc các hành vi dị thường chưa từng có.
- **Hệ thống NIDS với ML**: Xây dựng mô hình Machine Learning (đặc biệt là thuật toán LightGBM cho độ chính xác cao) học từ tập dữ liệu CICIDS2018 để nhận diện các trang thái traffic bất thường.
- **Vận hành**: Traffic đi qua WAF, sau đó log được đưa về Lambda để mô hình ML phân tích. Nếu phát hiện bất thường, hệ thống tự động gửi cảnh báo qua Security Hub, Inspector và SNS cho quản trị viên.

#### Hành trình từ IT Helpdesk đến Sysadmin/DevOps

- **Bứt phá vùng an toàn**: Từ những công việc lặt vặt (cài Win, sửa máy in, bấm mạng), cần phải xác định lộ trình 5 năm và trang bị kiến thức về Linux, Networking, Virtualization để tiến lên System Admin.
- **Kinh nghiệm thực chiến**: Đối mặt với các sự cố lớn (Concurrent users làm sập database, lỗi phần cứng RAID 5), từ đó nhận ra tầm quan trọng của Cloud (Auto-scaling, RDS) để giải quyết các hạn chế của On-premise.
- **Tư duy phỏng vấn**: Nhà tuyển dụng (đặc biệt ở các tập đoàn lớn) chỉ hỏi 30% technical, phần lớn tập trung vào Mindset và Tư duy hệ thống (cách debug từ request user đến database khi có lỗi).

#### Nghệ thuật làm việc nhóm (Teamwork Efficiency)

- **4 Nguyên tắc vàng**: 
    + Mục tiêu rõ ràng và được chia sẻ
    + Đúng người đúng việc
    + Giao tiếp cởi mở và lắng nghe tích cực
    + Trách nhiệm cá nhân
- Sử dụng thành thạo các công cụ số như Trello, ClickUp, Slack, Discord và Google Workspace để quản lý công việc.

### Những Gì Học Được

#### Tư Duy Thiết Kế & Làm Việc

- **Operational Mindset**: Trong quản trị hệ thống, nguyên tắc tối thượng là "Never test in production" (không bao giờ test trực tiếp trên môi trường thực tế), luôn phải backup, làm tài liệu đầy đủ và thiết lập monitoring trước khi sự cố xảy ra.
- **Làm chủ công nghệ thay vì chạy theo nó**: Không nên dùng AI để thay thế việc học hỏi. Thay vào đó, hãy thấu hiểu nền tảng (Foundation) thật vững chắc để ứng dụng AI làm đòn bẩy gia tăng hiệu suất.
- **Thái độ và sự chuẩn bị**: Khi đi phỏng vấn, thực hành các project cá nhân (hands-on labs) sẽ giúp hình thành tư duy giải quyết sự cố, điều mà nhà tuyển dụng đánh giá cao hơn cả bằng cấp.

#### Kiến Trúc Kỹ Thuật

- **Tối ưu hóa tài nguyên**: Hiểu được sự khác biệt giữa VM và Container để thiết kế hệ thống Microservices nhẹ, linh hoạt và tiết kiệm chi phí hạ tầng.
- **Event-driven & Serverless**: Nắm được luồng kết nối API Gateway - Lambda - DynamoDB để xử lý các ứng dụng real-time (như Game Multiplayer) với độ trễ thấp.
- **Bảo mật đa lớp**: Củng cố hệ thống không chỉ bằng WAF (bảo vệ vòng ngoài) mà còn bằng NIDS tích hợp AI (nhận diện hành vi bất thường vòng trong).
- **Xử lý dữ liệu phức tạp**: Nắm bắt phương pháp GraphRAG để giải quyết các bài toán GenAI cần sự móc nối, suy luận qua lại giữa nhiều nguồn dữ liệu khác nhau.

### Ứng Dụng Vào Công Việc

- **Đóng gói ứng dụng bằng Docker**: Áp dụng Docker ngay vào môi trường phát triển local để giải quyết triệt để vấn đề "Code chạy trên máy tôi nhưng lỗi trên máy người khác", giúp đồng bộ môi trường trong team.
- **Refactor kiến trúc Data**: Thử nghiệm Amazon Bedrock và Neptune để nâng cấp các hệ thống chatbot nội bộ hiện tại từ RAG lên GraphRAG, giúp bot trả lời chính xác các quy trình nghiệp vụ đan chéo của công ty.
- **Xây dựng Lab cá nhân**: Thiết lập các mô hình mạng, Linux server, và pipeline CI/CD cơ bản theo lộ trình DevOps được chia sẻ để rèn luyện tư duy debug hệ thống từ đầu đến cuối.
- **Làm sạch dữ liệu Security**: Áp dụng quy trình tiền xử lý dữ liệu (loại bỏ NaN, dữ liệu lỗi, cân bằng nhãn hiếm) trước khi đưa các log hệ thống vào phân tích bất thường.

### Trải nghiệm trong event

Tham gia sự kiện lần này là một trải nghiệm rất bổ ích, giúp tôi có cái nhìn toàn diện từ tầng hạ tầng, bảo mật, ứng dụng (App/Game), đến các xu hướng AI tối tân nhất. Một số trải nghiệm nổi bật:

#### Học hỏi từ các diễn giả có chuyên môn cao

- Được lắng nghe góc nhìn vĩ mô từ Giám đốc AI toàn cầu của AWS về cách AI tái định hình lực lượng lao động, giúp tôi thoát khỏi sự mơ hồ và xác định được tinh thần "Sử dụng AI như một công cụ để trở nên xuất sắc hơn".
- Trải nghiệm những câu chuyện thực tế "đẫm mồ hôi" của anh Vinh khi hệ thống sập do quá tải người dùng hay chết ổ cứng RAID 5. Điều này thực tế hơn bất kỳ bài học lý thuyết nào trên trường lớp.

#### Trải nghiệm kỹ thuật thực tế

- Được xem trực tiếp các bảng so sánh thuật toán Machine Learning (như LightGBM) phân tích file PCAP để tìm ra hacker.
- Hiểu sâu hơn về cách bộ nhớ Cache của Docker hoạt động khi build Image, tránh được các lỗi cài đặt lặp đi lặp lại không cần thiết khi viết Dockerfile.

#### Kết nối và trao đổi

- Sự kiện cung cấp một không gian mở để kết nối với các chuyên gia qua LinkedIn, GitHub, tạo cơ hội để tìm kiếm sự tư vấn trên con đường phát triển sự nghiệp.

#### Bài học rút ra

Việc làm IT không chỉ là cắm cúi viết code, mà là giải quyết bài toán của doanh nghiệp một cách an toàn, tiết kiệm và đảm bảo tính sẵn sàng cao. Sự tỉ mỉ, khả năng làm việc nhóm và tinh thần không ngại khó chính là chìa khóa để thăng tiến từ những vị trí thấp nhất lên các vai trò cốt cán.

#### Một số hình ảnh khi tham gia sự kiện

![Ảnh tham gia sự kiện 1](/images/event0606.jpg)
![Ảnh tham gia sự kiện 2](/images/event0606_2.jpg)
> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.
