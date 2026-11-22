# TEST CASES – WEBSITE DEGSLAND

## 1. Thông tin chung

- **Tên dự án:** DegsLand – Website giới thiệu bất động sản
- **Loại website:** Website tĩnh
- **Công nghệ:** HTML5, CSS3
- **Phương pháp kiểm thử:** Kiểm thử thủ công (Manual Testing)
- **Trình duyệt kiểm thử:** Google Chrome
- **Người kiểm thử:** Sinh viên thực hiện dự án

## 2. Mục tiêu kiểm thử

Kiểm tra khả năng hiển thị, điều hướng, bố cục và khả năng tương thích với các kích thước màn hình khác nhau của website DegsLand.

Các nội dung kiểm thử bao gồm:

- Kiểm tra các liên kết điều hướng trên website.
- Kiểm tra hiển thị nội dung và hình ảnh.
- Kiểm tra bố cục trên máy tính, tablet và điện thoại.
- Kiểm tra các liên kết và nút thao tác.
- Kiểm tra hiển thị khu vực thông tin liên hệ.
- Ghi nhận kết quả thực tế và lưu ảnh minh chứng.

## 3. Danh sách test case

| ID | Nội dung kiểm thử | Các bước thực hiện | Kết quả mong đợi | Kết quả thực tế | Trạng thái |
|---|---|---|---|---|---|
| TC01 | Mở trang chủ | Mở `http://127.0.0.1:8080/index.html` bằng Google Chrome | Website tải thành công, không hiển thị lỗi | Trang tải thành công; tiêu đề hiển thị là “DegsLand | Khám phá bất động sản” | Đạt |
| TC02 | Kiểm tra menu điều hướng | Nhấn lần lượt Trang chủ, Giới thiệu, Dự án, Lợi thế, Quy trình, Liên hệ | Mỗi mục điều hướng đến đúng khu vực tương ứng | 6 mục menu đều cập nhật đúng `#` neo và cuộn đến vùng tương ứng | Đạt |
| TC03 | Kiểm tra logo | Nhấn vào logo DegsLand | Logo điều hướng về khu vực trang chủ nếu được thiết lập liên kết | Logo có liên kết `#hero` và tên thương hiệu hiển thị đúng | Đạt |
| TC04 | Kiểm tra khu vực giới thiệu | Cuộn đến phần Giới thiệu | Nội dung, tiêu đề và hình ảnh hiển thị đầy đủ | Phần “Giới thiệu” có tiêu đề, 3 đoạn nội dung và 1 hình ảnh tải thành công | Đạt |
| TC05 | Kiểm tra danh sách dự án | Cuộn đến phần Dự án | Các thẻ dự án hiển thị đầy đủ nội dung và hình ảnh | Có 3 thẻ dự án, đủ tên, vị trí, mô tả và hình ảnh; liên kết trỏ đến `#chi-tiet-du-an` | Đạt |
| TC06 | Kiểm tra khu vực lợi thế | Cuộn đến phần Lợi thế | Các nội dung lợi thế được hiển thị rõ ràng | Phần “Giá trị” hiển thị đầy đủ 4 nội dung lợi thế | Đạt |
| TC07 | Kiểm tra khu vực quy trình | Cuộn đến phần Quy trình | Các bước quy trình hiển thị đầy đủ và đúng bố cục | 4 bước quy trình 01–04 hiển thị đầy đủ cùng hình ảnh minh họa | Đạt |
| TC08 | Kiểm tra khu vực liên hệ | Cuộn đến phần Liên hệ | Thông tin liên hệ và biểu mẫu hiển thị đầy đủ | Hiển thị địa chỉ, điện thoại, email và biểu mẫu Gửi yêu cầu tìm hiểu | Đạt |
| TC09 | Kiểm tra hình ảnh | Quan sát các hình ảnh trên website | Hình ảnh tải thành công, không bị lỗi hoặc mất ảnh | 5/5 hình ảnh đều tải xong và có kích thước gốc hợp lệ (`naturalWidth > 0`) | Đạt |
| TC10 | Kiểm tra giao diện desktop | Mở website ở độ rộng 1200px | Bố cục hiển thị hợp lý, nội dung không bị tràn | `scrollWidth` bằng `clientWidth` (1185px), không có tràn ngang | Đạt |
| TC11 | Kiểm tra giao diện tablet | Mở website ở độ rộng 768px | Bố cục thích ứng với màn hình tablet, không bị tràn ngang | `scrollWidth` bằng `clientWidth` (753px), không có tràn ngang | Đạt |
| TC12 | Kiểm tra giao diện mobile | Mở website ở độ rộng 320px | Nội dung hiển thị phù hợp với màn hình nhỏ, không bị tràn ngang | `scrollWidth` bằng `clientWidth` (305px), không có tràn ngang | Đạt |
| TC13 | Kiểm tra nút và liên kết | Nhấn các nút và liên kết trên website | Các nút và liên kết dẫn đến đúng vị trí hoặc đích đã thiết lập | Tất cả liên kết neo kiểm tra đều có phần tử đích tồn tại; logo, menu, nút CTA hoạt động đúng | Đạt |
| TC14 | Kiểm tra biểu mẫu liên hệ | Nhập dữ liệu hợp lệ và dữ liệu thiếu trường bắt buộc | Trường bắt buộc báo lỗi khi trống, dữ liệu hợp lệ được gửi qua query string | Trống: form không hợp lệ. Sau khi nhập đủ: `name`, `phone`, `email` hợp lệ; form gửi dữ liệu bằng phương thức GET qua query string. Đây mới là biểu mẫu tĩnh, chưa lưu hoặc gửi dữ liệu đến backend | Đạt |
| TC15 | Kiểm tra footer | Cuộn xuống cuối trang | Footer hiển thị đầy đủ thông tin và liên kết nếu có | Footer hiển thị copyright, địa chỉ, điện thoại, email và liên kết “Về đầu trang” (`#hero`) | Đạt |

## 4. Kết quả kiểm thử

Các test case được thực hiện thủ công trên trình duyệt Google Chrome.

Kết quả được cập nhật dựa trên quá trình kiểm thử thực tế. Các lỗi phát hiện sẽ được ghi nhận, sửa chữa và kiểm tra lại trước khi hoàn thiện website.

| Tổng số test case | Đạt | Không đạt | Chưa kiểm tra |
|---|---|---|---|
| 15 | 15 | 0 | 0 |

## 5. Minh chứng kiểm thử

Các ảnh chụp màn hình trong quá trình kiểm thử được lưu tại thư mục:

`docs/screenshots/`

Các ảnh minh chứng đã chụp trong lần kiểm thử thực tế:

- `docs/screenshots/Desktop.png`
- `docs/screenshots/Tablet.png`
- `docs/screenshots/Mobile.png`

Minh chứng có thể bao gồm:

- Giao diện trang chủ.
- Giao diện trên desktop.
- Giao diện trên tablet.
- Giao diện trên mobile.
- Các khu vực nội dung của website.
- Kết quả kiểm tra liên kết và thao tác.

## 6. Kết luận

Việc kiểm thử nhằm đánh giá mức độ hoàn thiện của website DegsLand về giao diện, bố cục, điều hướng và khả năng hiển thị trên nhiều thiết bị.

Các lỗi phát hiện trong quá trình kiểm thử sẽ được sửa chữa và kiểm tra lại. Kết quả cuối cùng được cập nhật dựa trên thực tế triển khai website.
