---
title: "Event 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch “FCAJ Community Day: Meet up”

### Mục Đích Của Sự Kiện

- Khuyến khích các bạn trẻ tự tin chia sẻ kiến thức mới, rèn luyện kỹ năng thuyết trình và nâng cao thái độ tự tin trước đám đông.
- Chia sẻ các phương pháp học tập hiệu quả, cách sử dụng Dopamine để biến việc học thành thói quen thú vị.
- Nâng cao kỹ năng giao tiếp với AI thông qua Prompt Engineering và giới thiệu các công cụ hỗ trợ tự động hóa trong phát triển phần mềm.
- Cung cấp góc nhìn thực tế từ doanh nghiệp về tư duy làm nghề, sự liêm chính và định hướng phát triển dài hạn cho Fresher.

### Danh Sách Diễn Giả

- **Huỳnh Hoàng Long** - Admin of FCAJ
- **Nguyễn Tuấn Thịnh** - DevOps/Cloud Engineer FCAJ
- **Nguyễn Duy Khang** - Solution Architect of Cloud Kinetics
- **Nguyễn Phương Thảo** - Application Cloud Dev of VIB, FCJ Ambassador

### Nội Dung Nổi Bật

#### Kỹ thuật giao tiếp với AI

- Cần cung cấp **prompt rõ ràng** → AI không sinh ra kết quả kém chất lượng hoặc bị ảo giác (hallucination).
- Cần viết **promp chi tiết**, tránh dùng các lệnh cấm đoán chung chung → thu nhỏ vùng và tập trung vào nội dung cần thiết.

#### 7 thành phần của một Prompt chuẩn

- Các thành phần của 1 prompt chuẩn bao gồm:
+ **Vai trò** 
+ **Hướng dẫn** 
+ **Ngữ cảnh** 
+ **Đầu vào** 
+ **Định dạng đầu ra** 
+ **Ví dụ** 
+ **Ràng buộc**

#### Hiểu về Token và các kỹ thuật nâng cao

- Ngôn ngữ khác nhau tốn lượng token khác nhau (tiếng Việt tốn gấp đôi tiếng Anh).
- Nên tận dụng các **kỹ thuật tư duy** của AI như **Chain of Thought** (suy nghĩ từng bước) hoặc **Tree of Thought** để ra kết quả tốt nhất.

#### Kiến trúc dự án AWS thực tế

- Áp dụng hệ thống **Serverless** với các dịch vụ cốt lõi như CloudFront, S3 (lưu trữ frontend/data lake), Cognito (xác thực người dùng), API Gateway, Lambda (backend serverless không cần quản lý máy chủ), Bedrock (tích hợp AI Foundation Model) và DynamoDB.

#### Tư duy và Định hướng

- **Nền tảng là yếu tố bất biến**: Công cụ thay đổi mỗi ngày, nhưng thứ nhà tuyển dụng cần là quy trình tư duy và kiến thức nền tảng vững chắc để giải quyết vấn đề.
- **AI là công cụ khuếch đại**: AI không thay thế tư duy. Nếu bạn làm tệ, AI làm bạn tệ hơn; nếu bạn làm tốt, AI giúp năng suất tăng x2, x10. Không bao giờ được "outsource" sự thấu hiểu của bản thân cho AI.
- **Văn hóa đặt câu hỏi "Tại sao"**: Phải luôn tự chất vấn lý do đằng sau các quyết định chọn công nghệ hay viết code thay vì chỉ chăm chăm vào "làm cái gì".

#### Sự liêm chính và thái độ:

- **Trong công việc**: Làm việc cần sự chính trực, chủ động đào sâu các trường hợp ngoại lệ (edge cases) dù không ai yêu cầu.
- **Đối với nhà tuyển dụng**: Tiêu chí ưu tiên đối với Fresher là Thái độ, tiếp theo mới đến Trình độ/Học vấn, Kinh nghiệm và Tố chất.

### Những Gì Học Được

#### Tư Duy Thiết Kế & Làm Việc

- **Foundation-first approach**: Luôn bắt đầu từ kiến thức nền tảng và quy trình tư duy thay vì chạy theo các service hay công cụ hào nhoáng.
- **Văn hóa "Why"**: Đặt câu hỏi chất vấn lý do đằng sau mọi quyết định chọn công nghệ hay kiến trúc hệ thống, không chỉ dừng lại ở việc làm cho code chạy được.
- **Sự liêm chính**: Tự giác quản lý và xử lý các trường hợp ngoại lệ dù không có trong yêu cầu gốc, thể hiện thái độ làm việc đường dài.

#### Kiến Trúc Kỹ Thuật

- **Ultimate Prompt Engineering**: Nắm vững cấu trúc 7 thành phần (Role, Instruction, Context, Input, Output, Example, Constraint) để giao tiếp chuẩn xác với AI, giảm thiểu hallucination.
- Sử dụng **Serverless Architecture** thay vì tự quản lý máy chủ bằng EC2.
- **Integration patterns**: Tích hợp luồng dữ liệu mượt mà qua các dịch vụ như CloudFront, S3, Cognito, API Gateway, Lambda và DynamoDB để xây dựng hệ thống web thực tế.
- **Advanced AI Reasoning**: Hiểu và sử dụng các kỹ thuật suy luận AI như Chain of Thought (suy nghĩ từng bước) hay Tree of Thought để tối ưu chất lượng đầu ra.

#### Chiến Lược Phát Triển & Sử Dụng AI

- **AI Amplification**: Coi AI là công cụ khuếch đại năng suất x2, x10, nhưng tuyệt đối không được giao phó tư duy cốt lõi của bản thân cho nó
- **Phased approach cho sự nghiệp**: Nhìn nhận chặng đường dài hạn, sẵn sàng trải nghiệm và chấp nhận mắc sai lầm để trưởng thành nhanh hơn
- **Định giá đa chiều**: Đánh giá giá trị công việc qua Kinh nghiệm , **Mạng lưới quan hệ , và Kiến thức  thay vì chỉ chăm chăm vào mức lương

### Ứng Dụng Vào Công Việc

- **Áp dụng Ultimate Prompting** cho project hiện tại: Đặt ngữ cảnh và chia nhỏ task để AI sinh code hoặc viết document chính xác, tránh hiện tượng chồng chéo thông tin.
- **Refactor kiến trúc cloud**: Áp dụng thử nghiệm các dịch vụ Serverless (như AWS Lambda, API Gateway) để giảm thiểu effort quản lý hạ tầng cho các dự án nhỏ.
- **Implement Integrity**: Chủ động vạch ra và xử lý thêm 20-30 edge cases thay vì chỉ đáp ứng 10 yêu cầu cốt lõi được giao.
- **Thử dùng AI Extensions**: Cài đặt và sử dụng các AI extension (ví dụ: Promptizer) trực tiếp trên trình duyệt để tối ưu hóa prompt nhanh chóng, nâng cao năng suất hằng ngày.
- **Xây dựng mạng lưới**: Tập trung làm việc nhóm và chủ động đặt câu hỏi nhiều hơn để rèn luyện kỹ năng trao đổi, không nên tự "đi một mình" trong dự án.

### Trải nghiệm trong event

Tham gia sự kiện **FCAJ Community Day** lần này là một trải nghiệm rất bổ ích, giúp tôi có cái nhìn toàn diện về cách ứng dụng AI và xây dựng tư duy làm nghề vững chắc. Một số trải nghiệm nổi bật:

#### Học hỏi từ các diễn giả có chuyên môn cao

- Các diễn giả (như anh Khang từ Cloud Kinetics) đã chia sẻ best practices trong tư duy làm việc, giúp tôi hiểu rằng doanh nghiệp cần "thought process" thay vì một người chỉ biết xài tool vô hồn.
- Qua các chia sẻ thực tế, tôi hiểu rõ hơn cách nhà tuyển dụng đánh giá một Fresher: Thái độ luôn đặt lên hàng đầu, tiếp đến mới là Trình độ và Kinh nghiệm.

#### Trải nghiệm kỹ thuật thực tế

- Tham gia phiên chia sẻ của anh Thịnh giúp tôi hình dung cách thiết kế một kiến trúc Serverless thực tiễn, từ lưu trữ bằng S3 đến quản lý user bằng Cognito và xử lý logic bằng Lambda.
- Học cách cấu trúc một prompt chuẩn chỉnh 7 thành phần và tránh hiện tượng ảo giác của AI bằng cách tách nhỏ ngữ cảnh.
- Hiểu rõ trade-offs giữa Serverless (Lambda) và compute truyền thống (như EC2) khi bắt tay vào thiết kế backend.

#### Ứng dụng công cụ hiện đại

- Trực tiếp tìm hiểu về các AI extension trên trình duyệt, công cụ hỗ trợ tối ưu hóa và sinh prompt nhanh chóng.
- Học cách **tự động hóa** **và boost productivity** thông qua việc tận dụng AI như một đòn bẩy khuếch đại năng lực mà vẫn giữ lại sự thấu hiểu cốt lõi.

#### Kết nối và trao đổi

- Sự kiện tạo cơ hội trao đổi cởi mở với cộng đồng, rèn luyện thái độ dạn dĩ khi chia sẻ kiến thức và xây dựng mạng lưới quan hệ (network)
- Qua các câu chuyện được kể, tôi nhận ra tầm quan trọng của **foundation-first approach**, luôn bắt đầu từ kiến thức nền tảng thay vì chỉ tập trung đuổi theo các service mới

#### Bài học rút ra

- Việc áp dụng văn hóa "Why" và sự liêm chính giúp tôi tăng tính chủ động, khả năng giải quyết vấn đề sâu sắc khi đối mặt với các kiến trúc phần mềm thực tế
- Định hướng sự nghiệp cần tầm nhìn dài hạn và ưu tiên việc trau dồi trải nghiệm, không nên vội vàng từ bỏ khi gặp những khó khăn ngắn hạn
- Các công cụ AI có thể boost productivity lên rất cao nếu được sử dụng đúng cách, nhưng tuyệt đối không được để chúng thay thế tư duy phản biện của chính bản thân mình

#### Một số hình ảnh khi tham gia sự kiện

![Ảnh tham gia sự kiện](/images/event0905.jpg)

> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.
