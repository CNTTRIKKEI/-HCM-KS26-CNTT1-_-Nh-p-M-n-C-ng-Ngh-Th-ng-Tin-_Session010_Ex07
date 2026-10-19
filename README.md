# PHẦN 1: PHÂN TÍCH LỖI VĂN BẢN & CƠ CHẾ AUTO TOC
## 1. Nguyên nhân định dạng thủ công khiến Auto TOC trống & Cơ chế quét của Word
- Cơ chế hoạt động của Auto TOC: Tính năng Table of Contents tự động quét toàn bộ văn bản để tìm các đoạn văn bản (Paragraphs) mang thuộc tính nhãn Heading Styles (Heading 1, Heading 2, Heading 3...) hoặc các đoạn văn có thiết lập Outline Level (Level 1, Level 2, Level 3...).
Lỗi cụ thể của các dòng tiêu đề:

- Các mục 1, 1.1, 1.2, 2, 2.1, 2.1.1: Tất cả đều sử dụng thuộc tính kiểu dáng văn bản thường (Normal Style) và áp dụng định dạng thủ công (Manual Formatting) như thay đổi cỡ chữ, in đậm, đổi màu chữ, tô màu nền (highlight). Word vẫn coi đây là văn bản thường (Body Text), do đó hệ thống không nhận diện được tiêu đề nào và xuất ra bảng mục lục trống.

- Mục 3 ("3. Lịch trình sự kiện"): Hoàn toàn là văn bản thường (Normal) không có định dạng, dẫn đến bị bỏ qua khi tạo mục lục.

## 2. Tác hại của việc gán sai cấp độ Heading (Trường hợp "2.1.1. Tiểu ban Kỹ thuật")
- Nguyên nhân: Mặc dù số thứ tự là 2.1.1 (thuộc cấp 3), nhưng trong file hiện tại đang gán nhãn nhầm thành Heading 2 (cấp 2).

- Ảnh hưởng đến cấu trúc thị giác (Indentation/Thụt lùi đầu dòng): Bảng mục lục tự động thiết lập mức độ thụt lùi đầu dòng (Indent Level) tăng dần theo cấp bậc của Heading (H1 sát lề trái, H2 thụt vào 1 khoảng, H3 thụt sâu hơn).

- Hậu quả: Việc gán sai 2.1.1 thành Heading 2 sẽ khiến dòng này đứng ngang hàng với mục cha 2.1. Ban Nội dung trên bảng mục lục, làm phá vỡ logic phân cấp thông tin kỹ thuật, gây hiểu lầm rằng Tiểu ban Kỹ thuật ngang cấp với Ban Nội dung.

# PHẦN 2: HƯỚNG DẪN SỬA LỖI & NGHIỆM THU
## 3. Các bước chuẩn hóa Heading cho 7 dòng tiêu đề  
| Dòng tiêu đề | Thao tác sửa nhãn | Phím tắt áp dụng | Cấp bậc chuẩn |
| --- | --- | --- | --- |
| 1.Thông TIn chung hội nghị | Bôi --> Gán Nhãn Heading 1 | Ctrl + alt + 1 | level 1 (Chương) |
| 1.1 Tên hội nghị | Bôi đen --> Gán nhãn Heading 2 | ctrl + alt +2 | level 2 (mục con) |
| 1.2 Thời gian và địa điểm | Bôi đen--> Gán nhãn Heading 2 | ctrl + alt +2 | level 2 (mục con) |
| 2.Cơ cấu ban tổ chức | Bôi đen --> Gán nhãn Heaing 1 | ctrl + alt + 1 | level 1 (Chương) |
| 2.1 Ban nội dung | Bôi đen --> Gán nhãn heading 2 | ctrl + alt + 2 | level 2 (mục con) |
| 2.1.1 Tiểu ban kỹ thuật | Bôi đen --> Gán nhãn Heading 3( sửa lại cấp đúng | Ctrl + alt + 3 | level 3(chi tiết) |
| 3. lịch trình sự kiện | Bôi đen --> Gán nhãn Heading 1 | Ctrl + alt + 1 | level 1 (Chương) |
### Mẹo chuẩn hóa giao diện (Format Painter/Modify Style):
> - Sau khi gán nhãn, để xóa bỏ hoàn toàn các thuộc tính định dạng thủ công cũ (như màu tô vàng), bôi đen dòng tiêu đề và nhấn Ctrl + Shift + N (trở về Normal) rồi nhấn lại phím tắt Heading tương ứng.
> -  Để tùy chỉnh màu sắc/phông chữ đồng bộ cho toàn bộ tiêu đề mà không phải sửa tay: Nhấp chuột phải vào ô Heading tương ứng trên thanh Styles --> Chọn Modify --> Cập nhật định dạng chuẩn --> Chọn OK.
## 4. Thao tác cập nhật số trang khi nội dung bị thay đổi (Bẫy dữ liệu)
 cập nhật số trang mới (mục 3 vẫn hiển thị ở trang 2 thay vì trang 4).
 Thao tác cần thực hiện:
 1. Click chuột vào bất kỳ vị trí nào trên Bảng mục lục tự động (Auto TOC).
 2. Chọn nút Update Table... hiển thị phía trên khung mục lục (hoặc nhấp chuột phải vào mục lục --> chọn Update Field).
 3. Khi hộp thoại Update Table of Contents xuất hiện:

- Chọn Update page numbers only nếu chỉ muốn cập nhật lại số trang.

- Chọn Update entire table nếu muốn cập nhật cả số trang lẫn các tiêu đề mới thêm/bớt (khuyên dùng).

4. Nhấn OK
