📘 StudentAnalyzer – Phân tích điểm học sinh
Dự án này cung cấp 2 chức năng chính giúp xử lý và phân tích điểm số của học sinh từ một danh sách điểm:

Đếm số học sinh đạt loại giỏi (điểm từ 8.0 trở lên)

Tính điểm trung bình hợp lệ (trong khoảng từ 0 đến 10)

📂 Cấu trúc thư mục
css
Copy
Edit
phamnhatminh/
├── .idea/               # Cấu hình IDE (IntelliJ)
├── src/                 # Mã nguồn chính
│   └── StudentAnalyzer.java
├── README.md            # Tài liệu hướng dẫn (bạn đang đọc)
└── pom.xml              # Tệp cấu hình Maven (nếu dùng Maven)
🧠 Chức năng chi tiết
1. countExcellentStudents(List<Double> scores)
   Chức năng: Đếm số học sinh có điểm từ 8.0 trở lên

Yêu cầu:

Chỉ tính điểm hợp lệ (0 ≤ điểm ≤ 10)

Nếu danh sách rỗng hoặc không có điểm hợp lệ → trả về 0

Ví dụ:

java
Copy
Edit
List<Double> scores = Arrays.asList(9.0, 7.5, 8.5, -1.0, 11.0);
int count = StudentAnalyzer.countExcellentStudents(scores);
// Kết quả: 2 (vì 9.0 và 8.5 là >= 8.0)
2. calculateValidAverage(List<Double> scores)
   Chức năng: Tính điểm trung bình của các điểm hợp lệ (0 đến 10)

Yêu cầu:

Bỏ qua điểm không hợp lệ (<0 hoặc >10)

Nếu không có điểm hợp lệ → trả về 0.0

Ví dụ:

java
Copy
Edit
List<Double> scores = Arrays.asList(8.0, 7.0, 11.0, -2.0);
double avg = StudentAnalyzer.calculateValidAverage(scores);
// Kết quả: 7.5
🛠️ Hướng dẫn chạy chương trình
✅ Yêu cầu
Java 8 trở lên

IDE như IntelliJ hoặc Eclipse

(Tùy chọn) Maven để build

▶️ Cách chạy
Mở dự án trong IntelliJ hoặc IDE khác

Tạo class Main.java để gọi hàm:

java
Copy
Edit
import java.util.Arrays;

public class Main {
public static void main(String[] args) {
var scores = Arrays.asList(8.5, 6.0, 9.0, -1.0, 12.0);

        int count = StudentAnalyzer.countExcellentStudents(scores);
        double avg = StudentAnalyzer.calculateValidAverage(scores);

        System.out.println("Số học sinh giỏi: " + count);
        System.out.println("Điểm trung bình hợp lệ: " + avg);
    }
}
Chạy chương trình để xem kết quả.

🧪 (Tùy chọn) Kiểm thử đơn vị
Bạn nên viết kiểm thử (JUnit):

java
Copy
Edit
@Test
void testCountExcellentStudents() {
List<Double> scores = Arrays.asList(9.0, 8.0, 7.0, -1.0);
assertEquals(2, StudentAnalyzer.countExcellentStudents(scores));
}