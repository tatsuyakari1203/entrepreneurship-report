## **PHẦN 5: KẾ HOẠCH VẬN HÀNH (OPERATION PLAN)**

Kế hoạch vận hành của CogniMind được thiết kế để đảm bảo sự linh hoạt, hiệu quả và khả năng mở rộng, áp dụng các phương pháp luận hiện đại trong phát triển sản phẩm và quản lý dịch vụ.


### **5.1. Quy trình Vận hành (Operational Workflow)**

Chúng tôi áp dụng mô hình Agile kết hợp DevOps để tối ưu hóa vòng đời sản phẩm và dịch vụ.

- **Quy trình Phát triển Sản phẩm (Product Development Lifecycle):**

  1. **Thu thập Yêu cầu (Requirement Gathering):** Liên tục thu thập phản hồi từ người dùng qua các kênh khảo sát, phỏng vấn, và phân tích dữ liệu hành vi. Đồng thời, đội ngũ chiến lược sẽ nghiên cứu thị trường và các xu hướng giáo dục để xác định các tính năng ưu tiên.

  2. **Thiết kế & Prototype (Design & Prototyping):** Đội ngũ UX/UI sẽ tạo ra các wireframe và prototype tương tác. Song song, đội ngũ AI sẽ thiết kế và thử nghiệm các cấu trúc prompt và workflow cho mô hình ngôn ngữ lớn (LLM).

  3. **Phát triển & Kiểm thử (Development & QA):** Sản phẩm được phát triển theo các chu kỳ ngắn (sprint 2 tuần). Sau mỗi sprint, đội ngũ QA (Quality Assurance) sẽ tiến hành kiểm thử toàn diện, từ unit test, integration test đến user acceptance test (UAT) để đảm bảo chất lượng.

  4. **Triển khai & Giám sát (Deployment & Monitoring):** Sử dụng quy trình CI/CD (Continuous Integration/Continuous Deployment) để tự động hóa việc triển khai phiên bản mới. Các hệ thống giám sát hiệu suất và lỗi sẽ hoạt động 24/7 để phát hiện và khắc phục sự cố kịp thời.

- **Quy trình Cung cấp Dịch vụ (Service Delivery Process):**

  1. **Onboarding Người dùng:** Quy trình đăng ký được tối giản hóa. Người dùng mới sẽ được hướng dẫn qua một tour giới thiệu ngắn gọn các tính năng chính để có thể bắt đầu sử dụng ngay lập tức.

  2. **Dịch vụ Lõi (AI Tutoring):** Khi người dùng gửi yêu cầu, hệ thống sẽ xử lý thông qua một workflow AI phức hợp để tạo ra các gợi ý và giải thích mang tính sư phạm, đảm bảo tính chính xác và phù hợp với trình độ người học.

  3. **Theo dõi & Phân tích:** Hệ thống sẽ thu thập dữ liệu (ẩn danh) về quá trình học tập, giúp người dùng theo dõi tiến độ của mình và giúp CogniMind hiểu rõ hơn hành vi người dùng để cải tiến sản phẩm.

- **Quy trình Hỗ trợ Khách hàng (Customer Support Process):**

  1. **Tiếp nhận:** Người dùng có thể gửi yêu cầu hỗ trợ qua email, chatbot tích hợp trong ứng dụng, và các kênh mạng xã hội.

  2. **Phân loại & Xử lý:** Các yêu cầu sẽ được tự động phân loại (lỗi kỹ thuật, câu hỏi về thanh toán, góp ý tính năng) và chuyển đến bộ phận phù hợp. Đội ngũ hỗ trợ cam kết phản hồi trong vòng 24 giờ.

  3. **Giải quyết & Cải tiến:** Sau khi giải quyết vấn đề, các phản hồi và báo cáo lỗi sẽ được tổng hợp và đưa vào backlog của đội ngũ phát triển sản phẩm để cải tiến trong các phiên bản tiếp theo.


### **5.2. Công nghệ và Thiết bị (Technology and Equipment)**

Nền tảng công nghệ của CogniMind được xây dựng trên các framework hiện đại, có khả năng mở rộng cao và tối ưu chi phí.

- **GUI Framework:**

  - **React Native:** Được lựa chọn làm framework chính để phát triển ứng dụng. Lợi thế lớn nhất là khả năng xây dựng ứng dụng cho cả iOS và Android từ một codebase duy nhất, giúp tiết kiệm đáng kể thời gian và chi phí phát triển. Hệ sinh thái component phong phú và cộng đồng hỗ trợ lớn mạnh cũng là một điểm cộng.

- **Hạ tầng LLMs (LLMs Infrastructure):**

  - **Core Engine:** Sử dụng **Google Gemini API** (ví dụ: Gemini 1.5 Pro) làm động cơ AI chính nhờ khả năng xử lý đa phương thức, cửa sổ ngữ cảnh lớn và hiệu suất tối ưu.

  - **Backup & Alternative:** **OpenAI GPT-4 Series** sẽ được sử dụng làm mô hình dự phòng và để so sánh, đối chiếu kết quả, đảm bảo tính liên tục của dịch vụ.

  - **Kiến trúc:** Chúng tôi xây dựng một **Agentic Workflow** độc quyền, cho phép AI tự động thực hiện một chuỗi các bước suy luận, tra cứu kiến thức từ cơ sở dữ liệu RAG, và tự kiểm tra lại câu trả lời trước khi đưa ra gợi ý cho người dùng.

- **Phát triển Nội dung & Dữ liệu (Content & Data Development):**

  - **Clean Room Implementation:** Để tránh mọi vấn đề về bản quyền, chúng tôi không sao chép trực tiếp nội dung từ sách giáo khoa. Thay vào đó, chúng tôi phân tích cấu trúc chương trình của Bộ GD&ĐT để xây dựng một "bộ xương kiến thức" (knowledge skeleton).

  - **Knowledge Graph:** Từ bộ xương này, đội ngũ chuyên môn sẽ tự xây dựng các ví dụ, dạng bài tập và lời giải chi tiết. Dữ liệu này được cấu trúc thành một đồ thị tri thức (knowledge graph), giúp AI tra cứu và liên kết thông tin hiệu quả.

  - **Human-in-the-Loop:** Tất cả nội dung do AI tạo ra sẽ được kiểm duyệt và tinh chỉnh bởi đội ngũ giáo viên và chuyên gia môn học để đảm bảo tính chính xác, phù hợp và sư phạm.

- **Yêu cầu Công nghệ Bổ sung:**

  - **Hạ tầng Đám mây (Cloud Infrastructure):** Toàn bộ hệ thống sẽ được vận hành trên nền tảng **Google Cloud Platform (GCP)** hoặc **Amazon Web Services (AWS)** để tận dụng khả năng tự động co giãn, bảo mật và các dịch vụ quản lý.

  - **Cơ sở dữ liệu:** Sử dụng **PostgreSQL** cho dữ liệu có cấu trúc (thông tin người dùng, thanh toán) và **MongoDB** hoặc một vector database chuyên dụng cho hệ thống RAG.

  - **Bảo mật:** Áp dụng mã hóa đầu cuối (end-to-end encryption) cho dữ liệu nhạy cảm của người dùng và sử dụng phương thức xác thực **OAuth 2.0/JWT**.


### **5.3. Địa điểm (Location)**

- **Văn phòng chính:** Đặt tại **TP. Hồ Chí Minh**, có thể là một không gian làm việc chung (co-working space) hiện đại như WeWork, Dreamplex tại Quận 1, Quận 2 hoặc gần khu Công nghệ cao (TP. Thủ Đức) để dễ dàng tiếp cận nguồn nhân lực công nghệ chất lượng cao từ các trường đại học.

- **Mô hình làm việc:** Áp dụng mô hình làm việc linh hoạt **Hybrid (3 ngày tại văn phòng, 2 ngày làm việc từ xa)** để thu hút nhân tài trên cả nước, tăng sự hài lòng của nhân viên và tối ưu hóa chi phí vận hành.


### **5.4. Quản lý Chuỗi cung ứng và Đối tác (Supply Chain and Partner Management)**

- **Nhà cung cấp chính (Key Suppliers):**

  - **Công nghệ:** Google (Gemini API, GCP), OpenAI, AWS.

  - **Nội dung:** Các giáo viên, giảng viên, chuyên gia giáo dục hợp tác dưới dạng cộng tác viên (freelancer) để xây dựng và kiểm duyệt nội dung học liệu.

- **Đối tác chiến lược (Strategic Partners):**

  - **Tổ chức giáo dục:** Hợp tác với các trường THPT và Đại học tiên phong về công nghệ (ví dụ: FPT Schools, Vinschool, Đại học RMIT, Đại học Fulbright) để triển khai các chương trình thí điểm (pilot programs).

  - **Đối tác công nghệ:** Kết nối với các công ty EdTech khác (không cạnh tranh trực tiếp) để tích hợp chéo dịch vụ, ví dụ như các nền tảng quản lý học tập (LMS) hoặc các ứng dụng học ngoại ngữ.

- **Quản lý đối tác:**

  - Xây dựng các **Thỏa thuận mức độ dịch vụ (SLA)** rõ ràng với các nhà cung cấp công nghệ.

  - Tổ chức các buổi đánh giá hiệu quả hợp tác định kỳ hàng quý với các đối tác giáo dục để thu thập phản hồi và lên kế hoạch cho các hoạt động tiếp theo.
