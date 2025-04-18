---
title: Đóng gói ứng dụng bằng container
status: Completed
category: Technology
tags: ["application", "", ""]
---

Containerization là quá trình đóng gói mã nguồn ứng dụng cùng mọi thư viện và phụ thuộc cần thiết để chạy mã vào một tệp thực thi gọn nhẹ — gọi là [container image](/container-image/).
## Vấn đề được giải quyết  

Trước khi [container](/container/) trở nên phổ biến, các tổ chức thường dựa vào [máy ảo](/virtual-machine/) (VM) để điều phối nhiều ứng dụng trên cùng một [máy chủ vật lý](/bare-metal-machine/).  
VM có kích thước lớn hơn container đáng kể và cần một hypervisor để vận hành.  
Việc lưu trữ, sao lưu và truyền các template VM cồng kềnh khiến quá trình tạo chúng chậm chạp.  
Ngoài ra, VM dễ gặp configuration drift (sai lệch cấu hình) — vi phạm nguyên tắc [hạ tầng bất biến](/immutable-infrastructure/).

## Lợi ích 

Container image rất nhẹ (không giống VM truyền thống) và quá trình container hóa chỉ cần một tệp liệt kê các phụ thuộc.  
Tệp này có thể được quản lý phiên bản và quy trình build được tự động hóa, giúp tổ chức tập trung vào các ưu tiên khác trong khi hệ thống tự động xử lý việc build.  
Một container image được lưu với định danh duy nhất gắn liền chính xác với nội dung và cấu hình của nó.  
Khi container được lên lịch chạy lại, chúng luôn trở về trạng thái ban đầu, loại bỏ hoàn toàn sai lệch cấu hình.
