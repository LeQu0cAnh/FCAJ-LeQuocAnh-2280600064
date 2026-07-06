---
title: "Event 4"
date: 2026-06-27
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Bài thu hoạch "FCAJ Community Day: Data Driven, AI Risen"

### Mục Đích Của Sự Kiện

- Cập nhật xu hướng tác động của AI đến thị trường việc làm, đặc biệt đối với các vị trí Developer và Cloud Engineer.
- Mang đến góc nhìn chuyên sâu về sự tác động của AI đến thị trường lao động, các kiến trúc Multi-agent, DevOps Agent, Amazon Q,...
- Đi sâu vào các giải pháp ứng dụng AI tạo sinh (GenAI) trong doanh nghiệp như: Voice AI, Agentic Platform cho hạ tầng Cloud, DevOps AI Agent, tự động hóa quy trình HR và các tiêu chuẩn bảo mật hệ thống.

### Danh Sách Diễn Giả

- **Steve Trần** - Founder/CTO of CloudThinker
- **Trung Vũ** - CEO Revve AI
- **Kiệt Trần** - AI Engineer | AWS Student Builder Group
- **Danh Hoàng Hiếu Nghị** - AI Engineer Renova Cloud
- **Phan Kim Bảo** - Cloud Engineer
- **Nguyễn Minh Nguyên** - Cloud Engineer
- **Trần Trường** - PM, AI & MULTI CLOUD SOLUTIONS of Noventiq Vietnam
- **Đặng Cao Minh Anh** - Intern Solution Sales of Noventiq Vietnam
- **Nguyễn Đức Toàn** - AWS Security Builder

### Nội Dung Nổi Bật

#### Định hình lại thị trường việc làm và Agentic Platform cho Cloud

- **Sự dịch chuyển của thị trường**: Các công cụ AI đang đẩy nhanh tốc độ coding, khiến các công ty ngưng tuyển dụng ồ ạt Developer truyền thống mà tập trung tìm kiếm các nhân sự Senior hoặc những người có khả năng sử dụng AI xuất sắc.
- **Bài toán vận hành Cloud**: Khi hệ thống doanh nghiệp lớn lên, độ phức tạp (complexity) tăng cao, đòi hỏi các công cụ AI không chỉ hỗ trợ coding mà còn phải quản lý và giám sát hạ tầng một cách an toàn.
- **Giải pháp**: Sử dụng hệ thống Multi-Agent và Agentic Platform để hỗ trợ con người xử lý sự cố nhanh chóng, đánh giá bảo mật (pentest tự động) và tối ưu hóa chi phí (FinOps), tuy nhiên AI ở tầng production đòi hỏi kiểm soát quyền (approval) rất khắt khe để tránh rủi ro.

#### Kiến trúc và Tối ưu Voice AI cho thị trường Tiếng Việt

Phần trình bày của anh Trung Vũ đem đến một góc nhìn thực tế và sâu sắc nhất về việc triển khai AI tổng đài giọng nói cho các ngân hàng lớn tại Việt Nam, giải quyết triệt để các rào cản về ngôn ngữ và nghiệp vụ.

- **Tại sao không dùng Speech-to-Speech?** Hiện tại, các mô hình STT (Speech-to-Speech) đa số hỗ trợ tiếng Anh và thiếu tài nguyên cho tiếng Việt.
- **Giải pháp thực tiễn**: Sử dụng kiến trúc ba bước: Speech-to-Text (nhận diện giọng nói) -> LLM (xử lý văn bản) -> Text-to-Speech (chuyển văn bản thành giọng nói). Kiến trúc này giúp doanh nghiệp kiểm soát chặt chẽ nội dung AI phát ngôn, tránh "ảo giác" và dễ dàng thực hiện thao tác gọi hàm (Tool Calling) như khóa thẻ ngân hàng theo yêu cầu.
- **Tối ưu tốc độ (Latency)**: Để Voice AI phản hồi tự nhiên, toàn bộ quy trình nhận diện, xử lý văn bản và xuất giọng nói phải được thực hiện thông qua cơ chế Streaming liên tục, giúp AI bắt giọng và trả lời gần như ngay lập tức mà không cần chờ xử lý xong toàn bộ câu.
- **Xử lý đặc thù Tiếng Việt**:
  + **Nhận diện giới tính**: Tiếng Việt yêu cầu nhân xưng chuẩn mực (anh/chị). AI cần được huấn luyện để nghe giọng và tự động nhận diện giới tính của khách hàng nhằm xưng hô cho chính xác.
  + **Ngữ cảnh khoảng lặng và ngắt lời**: AI phải hiểu được khi nào khách hàng đang dừng lại để suy nghĩ (ví dụ: đang nhớ số điện thoại) thay vì nhảy vào cướp lời. Đồng thời, bot cũng phải tự động im lặng khi bị khách hàng ngắt lời.
- **Ứng dụng giọng vùng miền**: Dữ liệu huấn luyện được bổ sung 10-20% giọng vùng miền. Điều này đặc biệt hữu hiệu trong các kịch bản nhắc nợ, vì một con bot nói giọng vùng miền sẽ thu hút sự chú ý của người nghe hơn so với giọng chuẩn phổ thông
- **Handover cho con người**: Hệ thống cho phép con người giám sát các cuộc gọi và AI có thể tự động chuyển máy (pass) sang nhân viên thật một cách tự nhiên khi bị khách hàng la mắng hoặc khi không thể tự xử lý.

#### Tự động hóa vận hành với DevOps AI Agent

- **Vấn đề của kỹ sư vận hành**: Truy xuất log và telemetry bị phân mảnh ở nhiều nơi, gây mất ngữ cảnh (context loss) và kéo dài thời gian xử lý sự cố (MTTR).
- **Giải pháp**: DevOps AI Agent tự động học (Context Learning) để vẽ ra sơ đồ hệ thống (Topology), tự động kích hoạt khi có cảnh báo lỗi, thu thập log, đưa ra giả thuyết và cung cấp nguyên nhân gốc rễ (Root Cause).
- **Ranh giới an toàn**: AI chỉ đưa ra kế hoạch khắc phục (Mitigation Plan) chứ không tự động thực thi. Quyết định bấm nút chạy script sửa lỗi luôn phụ thuộc vào sự phê duyệt của con người.

#### Tối ưu quy trình Nhân sự (HR) bằng Amazon Quick/Q

- **Thách thức**: HR tốn rất nhiều thời gian lọc CV thủ công, dễ bỏ sót nhân tài và thường đánh giá dựa trên cảm tính thiếu bộ khung chuẩn.
- **Ứng dụng AI**: Amazon Quick (Amazon Q) đóng vai trò là một trợ lý thông minh giúp xây dựng skill đánh giá ứng viên. Hệ thống có thể tự động đọc file CV, đối chiếu với Job Description (JD), tự động chấm điểm kỹ năng và đưa ra khuyến nghị rõ ràng nên nhận hay loại bỏ ứng viên.
- **Tích hợp linh hoạt**: Cho phép trích xuất an toàn từ các nguồn tài liệu của doanh nghiệp (OneDrive, SharePoint, Google Workspace, GitHub) mà không bị gò bó vào một hệ sinh thái duy nhất.

#### Bảo mật kết nối MCP (Model Context Protocol) Server

- **Rủi ro**: Khi AI Agent gọi ra các công cụ bên thứ 3 (MCP Server) qua Internet public, hệ thống dễ trở thành mục tiêu của tấn công DOS hoặc bị đánh cắp dữ liệu qua hình thức Man-in-the-middle.
- **Kiến trúc bảo mật**: Đưa MCP Server vào Private Subnet, sử dụng VPC Connection (kết nối nội bộ) cùng Application Load Balancer (ALB) để mã hóa TLS. Toàn bộ dữ liệu truy vấn giữa AI và MCP sẽ được lưu thông nội bộ, không lộ ra public, tuân thủ tiêu chuẩn bảo mật doanh nghiệp khắt khe.

### Những Gì Học Được

#### Tư Duy Thiết Kế & Làm Việc

- **AI là công cụ hỗ trợ, không thay thế hoàn toàn con người**: Dù là ứng dụng quản lý hạ tầng Cloud hay Voice AI cho tổng đài, các hệ thống lõi vẫn cần những nhân sự thực sự giỏi để phê duyệt hành động (Approval) và giám sát.
- **Customer-Centric trong thiết kế AI**: Xây dựng Voice AI không chỉ là ráp các công nghệ lại với nhau, mà là thấu hiểu tâm lý khách hàng (cách xưng hô, thói quen ngắt lời, sự khó chịu khi bị AI nhảy vào họng) để tinh chỉnh mô hình.
- **Sẵn sàng thay đổi quy trình**: Khi áp dụng hệ thống Agentic, doanh nghiệp có thể phải thay đổi đến 50% quy trình vận hành so với việc dùng nhân sự truyền thống.

#### Kiến Trúc Kỹ Thuật

- **Kiến trúc Voice Pipeline**: Việc chia nhỏ Speech-to-Text -> LLM -> Text-to-Speech cùng kiến trúc Streaming là chìa khóa để triển khai Voice bot tiếng Việt có độ trễ thấp và kiểm soát chặt chẽ đầu ra.
- **Security-First Architecture**: Bất cứ kết nối nào từ AI ra các hệ thống nghiệp vụ (MCP) đều phải đi qua các Endpoint riêng tư (VPC Connection, Private DNS) nhằm bảo vệ an toàn thông tin.
- **Custom Agent Skills**: Có thể tự thiết kế các tính năng cho AI Agent dựa trên File MD (Markdown) mô tả nhiệm vụ, định nghĩa rõ ràng các bước thực hiện để phục vụ từng phòng ban chuyên biệt (ví dụ: HR Talent Review).

### Ứng Dụng Vào Công Việc

- **Triển khai Voice bot nội bộ**: Ứng dụng mô hình xử lý STT-LLM-TTS để xây dựng các bot hỗ trợ tự động nội bộ bằng tiếng Việt, thiết lập thêm các bộ phân tích ngữ cảnh (nhận diện độ trễ, khoảng lặng) để giao tiếp mượt mà hơn.
- **Tối ưu Troubleshooting**: Thử nghiệm DevOps AI Agent bằng cách liên kết nó với CloudWatch/Datadog nhằm giảm bớt công sức dò log thủ công khi có sự cố hệ thống xảy ra.
- **Xây dựng Custom AI Assistant cho team**: Sử dụng Amazon Q (hoặc các AI platform tương đương) để tạo bộ tiêu chí tự động chấm điểm CV, từ đó giúp team HR và kỹ thuật rút ngắn thời gian sàng lọc ứng viên.
- **Rà soát kiến trúc bảo mật**: Đảm bảo mọi kết nối API từ LLM đến các tool/database nội bộ đều được thiết lập qua Private VPC, từ chối việc public API trực tiếp ra Internet.

### Trải nghiệm trong event

Tham gia workshop **“FCAJ Community Day: Data Driven, AI Risen”** là một trải nghiệm rất bổ ích, giúp tôi có cái nhìn toàn diện về cách hiện đại hóa ứng dụng và cơ sở dữ liệu bằng các phương pháp và công cụ hiện đại. Một số trải nghiệm nổi bật:

#### Học hỏi từ các diễn giả có chuyên môn cao

- Phiên chia sẻ của anh Trung Vũ thực sự mở mang tư duy về cách xây dựng sản phẩm **Voice AI** ứng dụng thực tế. Việc đào sâu vào những tiểu tiết như phân biệt giới tính, hiểu khoảng lặng khi đọc số điện thoại, và áp dụng giọng vùng miền cho thấy sự khác biệt giữa một bản "demo" và một sản phẩm Enterprise "thực chiến".

#### Trải nghiệm kỹ thuật thực tế

- Được xem trực tiếp demo Voice Agent truy vấn thông tin MacBook và demo mô phỏng một cuộc tấn công DDoS để xem cách DevOps AI Agent tự động trích xuất nguyên nhân (Root Cause) và đưa ra hướng xử lý chỉ trong vài phút.
  Chứng kiến khả năng "hiểu việc" của Amazon Q khi tự động phân tích CV tiếng Việt, đưa ra các nhận xét ưu/nhược điểm chuẩn xác.

#### Ứng dụng công cụ hiện đại

- Mở rộng tầm nhìn về Model Context Protocol (MCP) và cách kết nối bảo mật qua VPC.
  Tìm hiểu khái niệm "Agent Space" – không gian giới hạn quyền để AI học ngữ cảnh hệ thống (Topology) một cách an toàn mà không chạm vào dữ liệu cấm.

#### Bài học rút ra

Hiểu sâu về bối cảnh thay vì chỉ chạy theo công nghệ: Một mô hình AI tốt không nằm ở việc nó to hay hiện đại thế nào, mà nằm ở chỗ nó giải quyết bài toán đặc thù ngôn ngữ, nghiệp vụ của doanh nghiệp ra sao (như cách xử lý tiếng Việt của Revve AI).
Luôn giữ vòng lặp Human-in-the-loop: Dù AI có khả năng tự động hóa cực mạnh, từ DevOps đến Nhân sự, con người vẫn phải là người ra quyết định cuối cùng để đảm bảo tính an toàn và minh bạch.

#### Một số hình ảnh khi tham gia sự kiện

![Ảnh tham gia sự kiện](/images/event2706.jpg)

> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.
