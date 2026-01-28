## BÀI THỰC HÀNH TUẦN 1 – KIỂM THỬ PHẦN MỀM

### 1. Thông tin sinh viên
- **Họ và tên:** Bùi Quang Hiếu
- **MSSV:** BIT230157
- **Email:** hieub4680@gmail.com
- **Môn học:** Kiểm thử phần mềm
- **Giảng viên:** Trương Anh Hoàng

### 2. Mục tiêu bài thực hành
- Làm quen với GitHub và cách quản lý bài thực hành bằng repository
- Trải nghiệm và đánh giá chất lượng giao diện phần mềm
- Nhận thức được vai trò của trải nghiệm người dùng (UX/UI) trong kiểm thử phần mềm

### 3. Nội dung thực hành

#### 3.1. Tạo GitHub Repository
- Đã tạo repository cá nhân để lưu trữ toàn bộ bài thực hành môn học
- Repository có file `README.md` dùng làm báo cáo tổng hợp

#### 3.2. Trải nghiệm kiểm thử giao diện với CantUnsee
- Truy cập website:  
  👉 https://cantunsee.space/
- Thực hiện các bài kiểm tra phân biệt màu sắc và khả năng nhận diện giao diện
- Mục tiêu: đạt **điểm số cao nhất có thể**

### 4. Minh chứng kết quả
- Ảnh chụp màn hình kết quả làm bài trên CantUnsee
- Ảnh có dấu hiệu cá nhân (ví dụ: đang đăng nhập Chrome)

📌 **Hình ảnh minh chứng:**
https://github.com/hieubui0409/Kiem_Thu_Phan_Mem/blob/main/z7399817825266_e5aa23b9ef114294ac2e33e256ca0d5a.jpg
![Kết quả kiểm tra UI trên cantunsee.space](Báo%20cáo%20cantunsee.jpg)
![z7399817825266_e5aa23b9ef114294ac2e33e256ca0d5a](https://github.com/user-attachments/assets/059ae23d-41f5-4786-9334-e24d8f5fd1ef)

### 5. Nhận xét và đánh giá cá nhân
- Website CantUnsee giúp kiểm tra khả năng nhận diện màu sắc và chi tiết giao diện
- Một số bài kiểm tra gây khó khăn khi các màu có độ tương phản thấp
- Trải nghiệm cho thấy tầm quan trọng của thiết kế giao diện thân thiện với người dùng
- Kiểm thử UI/UX là một phần rất quan trọng trong kiểm thử phần mềm hiện đại

### 6. Kết luận
Thông qua bài thực hành này, sinh viên:
- Biết cách tổ chức và nộp bài bằng GitHub
- Hiểu thêm về kiểm thử giao diện và trải nghiệm người dùng
- Có nền tảng để tiếp cận các công cụ kiểm thử chuyên sâu hơn trong các tuần tiếp theo

 Bài tập thực hành tuần 2 kiểm thử với JUnit – Phân tích dữ liệu điểm số học sinh
1. Giới thiệu
Dự án này xây dựng một chương trình Java đơn giản để phân tích điểm số học sinh và viết kiểm thử đơn vị bằng JUnit 5.
Mục tiêu học tập
Biết cách viết Unit Test với JUnit.
Áp dụng kiểm thử cho các trường hợp:
Bình thường
Biên
Dữ liệu không hợp lệ
Biết cách tổ chức source code và test code trong repository.
Thực hành quản lý công việc bằng GitHub Issues và Commit message.
2. Mô tả bài toán
Chương trình có lớp StudentAnalyzer với 2 phương thức:

2.1 countExcellentStudents(List scores)
Đếm số học sinh có điểm >= 8.0
Chỉ tính các điểm hợp lệ trong khoảng 0 – 10
Bỏ qua:
Điểm < 0
Điểm > 10
Nếu danh sách rỗng → trả về 0
2.2 calculateValidAverage(List scores)
Tính điểm trung bình các điểm hợp lệ (0 – 10)
Bỏ qua điểm không hợp lệ
Nếu không có điểm hợp lệ → trả về 0
3. Cấu trúc thư mục
unit-test/ │ ├── src/ │ └── StudentAna     
lyzer.java │ ├── test/ │ └── StudentAnalyzerTest.java │ └── README.md
  <img width="1493" height="945" alt="Ảnh chụp màn hình 2026-01-14 145358" src="https://github.com/user-attachments/assets/04092bdc-c183-4d47-9bdf-36aab40bdb3f" />

BÀI ĐỌC THÊM 4 KIỂM THỬ JMETER
# JMeter Performance Testing Report

## Target website
- https://www.wikipedia.org

## Test environment
- Tool: Apache JMeter 5.6.3
- OS: Windows
- Test date: 28/01/2026

## Test scenarios

### TG1_Basic
- Users: 10
- Loop count: 5
- Request: GET /

Results:
- Avg Response Time: 697 ms
- Throughput: 1.6 req/sec
- Error Rate: 0.55 %

---

### TG2_Heavy
- Users: 50
- Ramp-up: 30s
- Requests:
  - GET /
  - GET /wiki/Main_Page

Results:
- Avg Response Time: 1025 ms
- Throughput: 1.2 req/sec
- Error Rate: 0.58 %

---

### TG3_Custom_60s
- Users: 20
- Duration: 60s
- Requests:
  - GET /wiki/Software_testing
  - GET /wiki/Apache_JMeter

Results:
- Avg Response Time: 852 ms (SoftwareTesting)
- Avg Response Time: 411 ms (ApacheJMeter)
- Throughput: 14.9 req/sec
- Error Rate: 0.43 % (SoftwareTesting)
- Error Rate: 0.27 % (ApacheJMeter)

---

## Overall Results (Combined)
- Avg Response Time (TOTAL): 650 ms
- Throughput (TOTAL): 32.5 req/sec
- Error Rate (TOTAL): 0.37 %

---

## Analysis & Conclusion
- Khi tăng số lượng người dùng (TG2), thời gian phản hồi trung bình tăng lên rõ rệt so với TG1.
- TG3 cho thấy hệ thống có thể xử lý lưu lượng ổn định trong 60 giây với throughput cao.
- Tỷ lệ lỗi dưới 1% cho thấy hệ thống hoạt động tương đối ổn định dưới tải.
- Website Wikipedia đáp ứng tốt với các kịch bản kiểm thử cơ bản và tải trung bình.

## Files
- plans/perf_test.jmx
- results/tg1.csv
- results/tg2.csv
- results/tg3.csv

ảnh minh chứng<img width="987" height="845" alt="Ảnh chụp màn hình 2026-01-28 124328" src="https://github.com/user-attachments/assets/16b8e1ff-0efc-45b7-98bb-04696d6034e1" />

