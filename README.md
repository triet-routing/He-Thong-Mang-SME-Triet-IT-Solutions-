# Triet-IT Solutions: Thiết kế & Triển khai Hạ tầng Mạng SME

Dự án tập trung xây dựng hệ thống mạng phân tầng, bảo mật và có tính dự phòng cao cho doanh nghiệp vừa và nhỏ (SME).
<img width="1153" height="693" alt="Mang-SME-Triet-IT-Solutions" src="https://github.com/user-attachments/assets/6f7cd4bd-5d98-450e-a03d-43bee7f1237a" />
##  Quy hoạch địa chỉ IP (IP Planning)

<img width="975" height="365" alt="quyhoaochip" src="https://github.com/user-attachments/assets/a8bbf3a5-feaa-49da-8994-006e9e590999" />

##  Các tính năng cốt lõi
*   **Layer 2 Redundancy**:Chia Vlan , cấu hình **VTP** và sử dụng **STP** chống Loop và đảm bảo tính sẵn sàng cao cho hệ thống Switch Core.
*   **Kiến trúc Router-on-a-Stick**: Triển khai Sub-interfaces tối ưu hóa định tuyến liên mạng Inter-VLAN.
*   **Vùng Server Farm (Vip Server)**: Thiết lập **SERVER ZONE (VLAN 11)** biệt lập quản lý tài nguyên nhạy cảm.
*   **Dịch vụ mạng**: Triển khai **DHCP** cấp phát IP động, định tuyến tĩnh **Static Route** hướng Internet.
*   **Bảo mật đa lớp**: Thiết lập **ACL** ngăn chặn VLAN Khách truy cập vùng Server và bảo mật quản trị VTY.
*   **Kết nối Internet**: Cấu hình **NAT Overload** và **Static NAT** để công khai Web Server ra bên ngoài.

##  Kiến trúc hệ thống (Topology)
Hệ thống được thiết kế theo mô hình 3 lớp chuẩn: **Core – Distribution – Access**
*   **Edge Layer**: Router 2811 đóng vai trò cửa ngõ NAT và Firewall.
*   **Core Layer**: 02 Multilayer Switch 3560 chạy STP dự phòng.
*   **Access Layer**: Các Switch 2960 kết nối trực tiếp đến máy trạm.
 ##  Cấu trúc thư mục
Triển khai lưu trữ khoa học để dễ dàng quản lý và truy xuất tài liệu:
├── lab_files/         # File mô phỏng thực tế (.pkt)
├── documentation/     # Báo cáo chi tiết và hướng dẫn 
└── topology/          # Hình ảnh sơ đồ mạng kiến trúc 3 lớp

---
> **Lưu ý**: Các bạn tham khảo tài liệu nếu thấy mình làm có sai sót mong hãy phản hồi lại để mình biết nha. Chúc các bạn học tốt!
