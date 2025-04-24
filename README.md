==== Hướng dẫn sử dụng phần mềm tạo proxy 2D Proxy Server ====

Để vào trang quản lý truy cập http://xxx.2dproxy.com:8000 hoặc 
qua IP Public http://IP_PUBLIC:8000

Có thể truy cập proxy từ bên ngoài qua tên miền xxx.2dproxy.com hoặc IP_PUBLIC

Quý khách đổi mật khẩu mặc định vào trang quản lý và key, mật khẩu của proxy để bảo mật

* API
1. API Lấy Proxy
http://HOST:8000/api/get_proxy?access_key=TOKEN

Có thể lấy proxy theo định dạng ví dụ:
http://HOST:8000/api/get_proxy?access_key=TOKEN&format=HOST|PORT|username|password&delimiter=:
HOST thay bằng: host_public hoặc host_local
PORT thay bằng: port_http hoặc port_socks5

2. API Đổi IP của Proxy
http://HOST:8000/api/change_ip?access_key=TOKEN

TOKEN thay bằng: 
-Token tài khoản sẽ áp dụng cho tất cả proxy của tài khoản (truy cập thông tin tài khoản để lấy)
-Key cụ thể của 1 proxy sẽ áp dụng cho proxy (mỗi proxy có key cụ thể)
HOST thay bằng xxx.2dproxy.com hoặc IP_PUBLIC

Lưu ý: Với phần mềm chạy trên máy ảo, máy ảo phải chạy để duy trì hoạt động của proxy và máy chính mới có mạng, Nếu tắt máy hãy tắt máy ảo trước và tắt máy tính sau

# Cần hỗ trợ thêm vui lòng chat telegram: @net_247
