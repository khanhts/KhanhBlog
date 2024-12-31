+++
title = "Tạo Socket bằng Java"
date = "2024-12-12"
tags = ["Hugo", "Web Development", "Tutorial"]
author = "Trương Sĩ Gia Khánh"
image = "/KhanhBlog/images/javasocket.jpg"
+++

## Socket trong Java

![Java Socket](/KhanhBlog/images/javasocket.jpg)

Socket trong Java là một cơ chế để giao tiếp giữa các ứng dụng, cho phép các ứng dụng trên các máy tính khác nhau kết nối và trao đổi dữ liệu qua mạng. Java cung cấp một API java.net để làm việc với các socket và giao tiếp qua mạng, hỗ trợ cả giao tiếp TCP (Transmission Control Protocol) và UDP (User Datagram Protocol).

**1. Socket là gì?**

Socket là một điểm cuối trong một kết nối mạng, được sử dụng để gửi và nhận dữ liệu qua mạng. Trong giao tiếp mạng, một ứng dụng (client) mở một socket và kết nối đến một máy chủ (server), máy chủ cũng mở một socket để chờ kết nối từ client. Sau khi kết nối thành công, dữ liệu có thể được truyền giữa client và server thông qua các socket này. Trong Java, socket chủ yếu được sử dụng với giao thức TCP/IP (mạng có kết nối và đảm bảo độ tin cậy).

**2. Các thành phần cơ bản trong Socket Programming**

**Server Socket** (Máy chủ): Máy chủ tạo một ServerSocket để lắng nghe các kết nối đến từ client. ServerSocket sẽ chờ cho đến khi có một client kết nối, sau đó tạo một Socket để giao tiếp với client.

**Client Socket** (Máy khách): Client mở một Socket và kết nối đến server thông qua địa chỉ IP và cổng (port) của server.

**3. Các lớp trong Java để làm việc với Socket**

*Socket*: Dùng để kết nối tới một địa chỉ máy chủ trên mạng và gửi/nhận dữ liệu.

*ServerSocket*: Lớp này dùng để tạo một server chờ kết nối từ client.

*InetAddress*: Lớp này đại diện cho một địa chỉ IP trong mạng.

*IOException*: Được sử dụng để xử lý các lỗi nhập/xuất trong quá trình giao tiếp qua mạng.

**4. Kết luận**

Socket TCP trong Java giúp thực hiện giao tiếp có kết nối, đáng tin cậy giữa client và server. ServerSocket được sử dụng để lắng nghe kết nối, còn Socket để thực hiện giao tiếp.

UDP trong Java (thông qua DatagramSocket) là một giao thức không kết nối, thích hợp cho các ứng dụng yêu cầu tốc độ cao mà không cần đảm bảo độ tin cậy.

Socket programming trong Java là một phần quan trọng trong việc xây dựng các ứng dụng phân tán, hệ thống mạng và các ứng dụng thời gian thực.

