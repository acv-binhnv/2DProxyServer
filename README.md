==== Hướng dẫn sử dụng phần mềm tạo proxy 2D Proxy Server ====

Để vào trang quản lý truy cập http://xxx.2dproxy.com:8000 hoặc 
qua IP Public http://IP_PUBLIC:8000 , nội dung web được lưu hoàn toàn trên máy cài pm không qua server của chúng tôi, pm hoạt động web và proxy mới hoạt động, tên miền được hỗ trợ sẽ trỏ thẳng về IP Public của máy cài pm giúp tiện truy cập khi IP Public bị thay đổi (Mỗi lần chạy lại phần mềm IP Public sẽ thay đổi hoặc do IP động nhà mạng sau một thời gian sẽ có thay đổi)

Có thể truy cập proxy từ bên ngoài qua tên miền xxx.2dproxy.com hoặc IP PUBLIC

Thiết bị cùng mạng Lan nội bộ có thể sử dụng IP LOCAL

Quý khách đổi mật khẩu mặc định vào trang quản lý, đổi key tài khoản, đổi key proxy, đổi mật khẩu của proxy để bảo mật và tự quản lý


API TÍCH HỢP
1. API Lấy Proxy
http://HOST:8000/api/get_proxy?access_key=TOKEN

Có thể lấy proxy theo định dạng ví dụ:

Muốn lấy danh sách proxy theo định dạng ip:port:username:password thì chạy api dưới

http://HOST:8000/api/get_proxy?access_key=TOKEN&format=HOST_PROXY|PORT_PROXY|username|password&delimiter=:

HOST_PROXY thay bằng: host_public hoặc host_local

PORT_PROXY thay bằng: port_http hoặc port_socks5

2. API Đổi IP của Proxy
http://HOST:8000/api/change_ip?access_key=TOKEN

TOKEN thay bằng: Token tài khoản sẽ áp dụng cho tất cả proxy của tài khoản (truy cập thông tin tài khoản để lấy) hoặc 
Key cụ thể của 1 proxy sẽ áp dụng cho proxy (mỗi proxy có key cụ thể)

HOST thay bằng: xxx.2dproxy.com hoặc IP_PUBLIC hoặc IP_LOCAL

Lưu ý: 
- Với phần mềm chạy trên máy ảo, máy ảo phải chạy để duy trì hoạt động của proxy và máy chính mới có mạng, mới khởi động phần mềm có thể mất vài phút để tạo kết nối và máy chính mới có mạng, Nếu tắt máy hãy tắt máy ảo trước và tắt máy tính sau.
- Trong quá trình sử dụng nếu có proxy nào lỗi thì hãy restart port đó
- Trường hợp bị tắt nguồn đột ngột như mất điện dịch vụ đang chạy có thể bị lỗi nếu không thấy proxy lên hoặc không đủ theo số Tootal Proxy Quý khách vào từng card mạng trong phần Networks -> Ticks Restart -> Cập nhật lại và kiểm tra lại sau vài phút xem proxy đã lên chưa
- Để đổi IP nhanh hơn quý khách quý khách đặt Total IP: là tổng phiên (ip) lấy từ nhà mạng LỚN HƠN Total Proxy, phần mềm sẽ lấy từ tổng ip để gán vào các slot proxy sẵn nên nếu có IP dư trước đó việc đổi IP sẽ nhanh hơn

# Cần hỗ trợ thêm vui lòng chat telegram: @net_247
