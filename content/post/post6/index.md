+++
title = "Xử lý sự kiện thông qua JS"
date = "2024-12-15"
tags = ["Hugo", "Web Development", "Tutorial"]
author = "Trương Sĩ Gia Khánh"
image = "/images/jsehandler.jpg"
+++

## Thế nào là sự kiện và áp dụng JS như thế nào?

![JS eventHandler](/images/jsehandler.jpg)

JavaScript (JS) là ngôn ngữ lập trình chủ yếu được sử dụng để xử lý các sự kiện trong web và tăng cường độ tương tác của trang web. Trong môi trường web, "sự kiện" thường ám chỉ những hành động hoặc phản ứng mà người dùng thực hiện trên trang web, ví dụ như nhấp chuột, di chuột, nhập liệu vào form, hoặc cuộn trang. JavaScript cho phép các nhà phát triển xây dựng những hành vi tương tác động và thay đổi ngay lập tức nội dung trang mà không cần phải tải lại trang, từ đó làm tăng trải nghiệm người dùng.

**1. Khái niệm về sự kiện trong JavaScript**

Một sự kiện (event) là một hành động được thực hiện bởi người dùng hoặc do hệ thống kích hoạt trong trình duyệt, ví dụ:

*Nhấp chuột* (click)

*Di chuột qua* (mouseover, mouseout)

*Nhấn phím* (keydown, keyup, input)

*Thay đổi giá trị trong form* (change, input)

*Cuộn trang* (scroll)

*Chọn* (select), v.v.

Các sự kiện này có thể được JavaScript "lắng nghe" và xử lý để thực hiện một hành động cụ thể khi sự kiện đó xảy ra.

**2. Cách thức hoạt động của sự kiện trong JavaScript**

JavaScript có thể xử lý sự kiện bằng cách "lắng nghe" và phản hồi khi sự kiện đó xảy ra. Việc xử lý sự kiện trong JavaScript thường bao gồm 3 bước chính:

1. Chọn phần tử HTML (element) mà bạn muốn lắng nghe sự kiện.
2. Đăng ký một "event listener" cho phần tử đó, tức là lắng nghe khi một sự kiện xảy ra.
3. Xử lý sự kiện (event handler) khi sự kiện được kích hoạt.



