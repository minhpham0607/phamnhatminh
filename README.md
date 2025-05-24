# StudentAnalyzer Java Project

## 📘 Mô tả bài tập

Dự án này yêu cầu xây dựng một lớp Java tên là `StudentAnalyzer` để phân tích danh sách điểm số của học sinh. Lớp này gồm hai phương thức chính:

### 1. `countExcellentStudents(List<Double> scores)`
- Trả về số lượng học sinh đạt loại **Giỏi** (điểm ≥ 8.0).
- Bỏ qua các điểm không hợp lệ (nhỏ hơn 0 hoặc lớn hơn 10).
- Trả về `0` nếu danh sách rỗng.

### 2. `calculateValidAverage(List<Double> scores)`
- Tính và trả về **điểm trung bình** của các điểm hợp lệ (trong khoảng 0 đến 10).
- Trả về `0.0` nếu danh sách không chứa điểm hợp lệ.

## 🔧 Yêu cầu kỹ thuật

- **Điều kiện lọc dữ liệu**:
    - Bỏ qua điểm âm hoặc lớn hơn 10 (dữ liệu sai).
- **Xử lý danh sách trống**:
    - Trả về `0` nếu danh sách rỗng.
- **Duyệt danh sách**:
    - Một vòng lặp để đếm số học sinh giỏi.
    - Một vòng lặp để tính trung bình hợp lệ.

## 🧪 Kiểm thử với JUnit

Dự án bao gồm kiểm thử đơn vị với JUnit 5. Các tình huống kiểm thử bao gồm:

- ✅ Danh sách có điểm hợp lệ và không hợp lệ
- ✅ Danh sách chỉ chứa điểm hợp lệ
- ✅ Danh sách trống
- ✅ Danh sách chỉ gồm 0 hoặc 10
- ✅ Có điểm không hợp lệ (< 0 hoặc > 10)
*Hướng dẫn chạy test
1. Cài đặt JDK
     Cài Java JDK (phiên bản 11 trở lên). Có thể kiểm tra bằng lệnh: 
          java -version
2.  Thiết lập dự án
    Sử dụng IDE như IntelliJ IDEA, Eclipse, hoặc build tool như Maven/Gradle. Cấu trúc thư mục:
    /src
    /main/java
    StudentAnalyzer.java
    /test/java
    StudentAnalyzerTest.java
3. Chạy test với Maven (nếu dùng Maven)
   mvn test 
4. Hoặc chạy test trực tiếp trong IDE
   Click chuột phải vào file StudentAnalyzerTest.java → chọn Run 'StudentAnalyzerTest'.
*Kết luận
Bài tập giúp sinh viên thực hành:

Xử lý dữ liệu hợp lệ.

Sử dụng vòng lặp và điều kiện.

Viết kiểm thử đơn vị với JUnit.


