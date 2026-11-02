**Bài 2 : Xử lý Sự cố Cache và Phiên Đăng nhập trong Doanh nghiệp** 

**Phần 1: Phân tích**

- CSS không cập nhật vì: do Browser Cache, trình duyệt đã lưu file CSS cũ, nên khi bấm F5, trình duyệt vẫn đọc lại file cũ từ máy thôi, không có lấy file mới của CSS.

- Tại sao phiên đăng nhập bị mất khi tắt trình duyệt vì: Cookie đăng nhập của An là Session Cookie nó sẽ tự xóa  trình duyệt. Do mã nguồn không có thuộc tính Max-Age hay Expires, trình duyệt sẽ coi là dữ liệu tạm thời và sẽ xóa ngay khi đóng trình duyệt. Cho nên, cần dùng Persistent Cookie để duy trì đến ngày hết hạn

**Phần 2: Sửa lỗi** 

- Bấm Ctrl \+ F5 để buộc trình duyệt bỏ qua cache của trang hiện tại và tải lại toàn bộ file CSS mới nhất.     
- Thêm thuộc tính Max-Age hoặc Expires vào cookie để chuyển thành Persistent Cookie.. 