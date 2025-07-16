==== Hướng dẫn sử dụng phần mềm tạo proxy 2D Proxy Server ====

Để vào trang quản lý truy cập qua IP Public http://IP_PUBLIC:8000 hoặc tên miền được hỗ trợ , nội dung web được lưu hoàn toàn trên máy cài phần mềm, không qua server của chúng tôi, pm hoạt động thì web và proxy mới hoạt động, tên miền được hỗ trợ sẽ trỏ thẳng về IP Public của máy cài pm giúp tiện truy cập khi IP Public bị thay đổi (Mỗi lần chạy lại phần mềm IP Public sẽ thay đổi hoặc do IP động nhà mạng sau một thời gian sẽ có thay đổi)

Có thể truy cập proxy từ bên ngoài qua tên miền được hỗ trợ hoặc IP PUBLIC

Trên máy cài phần mềm có thể sử dụng IP LOCAL

Quý khách đổi mật khẩu mặc định vào trang quản lý, đổi key tài khoản, đổi key proxy, đổi mật khẩu của proxy để bảo mật và tự quản lý

=================================================

API TÍCH HỢP

Một số tham số chung dùng trong các API cần thay thế:

TOKEN thay bằng: Token tài khoản sẽ áp dụng cho tất cả proxy của tài khoản (truy cập thông tin tài khoản để lấy) hoặc 
Key cụ thể của 1 proxy sẽ áp dụng cho proxy (mỗi proxy có key cụ thể)

HOST thay bằng: xxx.2dproxy.com hoặc IP_PUBLIC hoặc IP_LOCAL

1. API Lấy Proxy
http://HOST:8000/api/get_proxy?access_key=TOKEN

Có thể lấy proxy theo định dạng ví dụ:

Muốn lấy danh sách proxy theo định dạng ip:port:username:password hoặc thay đổi vị trí các thông tin theo mong muốn. Ví dụ:

http://HOST:8000/api/get_proxy?access_key=TOKEN&format=HOST_PROXY|PORT_PROXY|username|password&delimiter=:

Tham số HOST_PROXY thay bằng: host_public hoặc host_local tùy theo chạy local hoặc public

Tham số PORT_PROXY thay bằng: port_http hoặc port_socks5 tùy loại proxy muốn lấy

Tham số delimiter=:  : ở đây là ký tự mong muốn để ngăn cách giữa các thông tin

2. API Đổi IP của Proxy
http://HOST:8000/api/change_ip?access_key=TOKEN

====================================================

Lưu ý: 
- Với phần mềm chạy trên máy ảo, máy ảo phải chạy để duy trì hoạt động của proxy và máy chính mới có mạng, mới khởi động phần mềm có thể mất vài phút để tạo kết nối và máy chính mới có mạng, Nếu tắt máy hãy tắt máy ảo trước và tắt máy tính sau.
- Trong quá trình sử dụng nếu có proxy nào lỗi thì hãy restart port đó
- Trường hợp bị tắt nguồn đột ngột như mất điện dịch vụ đang chạy có thể bị lỗi nếu proxy lên hoặc không đủ Total Proxy Quý khách vào từng card mạng trong phần Networks -> Tick Restart -> Cập nhật lại và kiểm tra lại sau vài phút xem proxy đã lên chưa
- Để đổi IP nhanh hơn đặt Total IP: là số phiên của gói đa phiên LỚN HƠN Total Proxy, phần mềm sẽ lấy từ Total IP để gán vào các slot theo số lượng Total Proxy nên nếu có IP dư trước đó việc đổi IP sẽ nhanh hơn
- Pm dùng 1 phiên để tạo IP Public và ra mạng cho thiết bị sau nó nên số proxy tạo đc sẽ -1
- Để xác thực phần mềm và hỗ trợ kỹ thuật chúng tôi chỉ truy cập từ xa vào pm kiểm tra khi có vấn đề
- Do nhiều yếu tố khách quan khi cài trên máy khách với bản phần mềm chạy trên windows như virus làm hỏng file, đụng độ phần mềm, phần cứng thay đổi, thao tác chỉnh sửa hay cài đặt các ứng dụng khác làm ảnh hưởng tới hoạt động của phần mềm nên chúng tôi chỉ hỗ trợ xử lý vấn đề trong 7 ngày đầu khách chạy
- Chúng tôi chỉ bán phần mềm cho khách hàng sử dụng theo chức năng của phần mềm nghiêm cấm mọi hành vi phá hoại, crack, dùng kỹ thuật can thiệp ăn cắp mã nguồn vi phạm quyền sở hữu trí tuệ chất xám của chúng tôi
  
# Cần hỗ trợ thêm vui lòng chat telegram: @net_247
