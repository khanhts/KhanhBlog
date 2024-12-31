+++
title = "Tương tác giữa JavaScript và CSS"
date = "2024-12-24"
tags = ["Hugo", "Web Development", "Tutorial"]
author = "Trương Sĩ Gia Khánh"
image = "/images/cssjs.jpg"
+++

## JavaScript và CSS

![JavaScript và CSS](/KhanhBlog/images/cssjs.jpg)

JavaScript có thể tương tác với CSS bằng cách thay đổi các thuộc tính kiểu dáng (CSS properties) của các phần tử HTML trong trang web. Điều này được thực hiện thông qua đối tượng style trong DOM (Document Object Model), cho phép JavaScript thay đổi kiểu dáng của phần tử ngay lập tức mà không cần phải sửa trực tiếp trong các file CSS.

**1. Thay đổi các thuộc tính CSS qua JavaScript**

JavaScript có thể truy cập và thay đổi các thuộc tính CSS của một phần tử thông qua đối tượng style của phần tử đó. Đối tượng style này cho phép bạn sửa các thuộc tính CSS trực tiếp của phần tử mà không cần thay đổi file CSS bên ngoài.

**2. Thay đổi các thuộc tính CSS động (như hover, transition, animation)**

Một số thuộc tính CSS như *:hover*, *:focus*, hoặc các hiệu ứng chuyển động và hoạt ảnh (transition, animation) không thể thay đổi trực tiếp bằng JavaScript thông qua thuộc tính style. Tuy nhiên, JavaScript có thể thay đổi các lớp CSS (class) của các phần tử HTML để áp dụng các hiệu ứng này.

**3. Thay đổi các thuộc tính CSS với setAttribute**

Ngoài việc thay đổi trực tiếp các thuộc tính style, bạn cũng có thể thay đổi thuộc tính style thông qua phương thức *setAttribute()*. Phương thức này cho phép bạn thay đổi giá trị của bất kỳ thuộc tính nào của phần tử HTML, bao gồm thuộc tính style.

**4. CSS Animations và Transitions trong JavaScript**

JavaScript có thể điều khiển các hiệu ứng CSS Animation và CSS Transition bằng cách thay đổi các thuộc tính liên quan đến hoạt ảnh hoặc chuyển đổi.

**5. Kết luận**

JavaScript tương tác với CSS thông qua các phương thức DOM để thay đổi các thuộc tính CSS của phần tử HTML trong thời gian thực. Một số cách tương tác cơ bản bao gồm:

- Thay đổi trực tiếp các thuộc tính CSS: Dùng đối tượng style.
- Thêm, xóa, và chuyển đổi lớp CSS: Dùng classList.
- Sử dụng setAttribute để thay đổi các thuộc tính style.
- Thực hiện các hiệu ứng CSS động: Bằng cách sử dụng CSS transition hoặc animation kết hợp với JavaScript.
- JavaScript mở rộng khả năng của CSS và giúp xây dựng những trang web động và tương tác cao hơn.