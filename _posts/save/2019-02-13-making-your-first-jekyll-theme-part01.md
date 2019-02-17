---
layout: post
title:  "Cùng làm theme Jekyll đầu tiên của bạn - Phần 01"
author: blackeye
categories: [ jekyll, series, learn, static website ]
image: assets/images/8.jpg
---
(nguồn: [Making your first Jekyll theme: Part 1](https://www.siteleaf.com/blog/making-your-first-jekyll-theme-part-1/) )

Về bản chất, bất kỳ trang web có cấu trúc tốt nào có nội dung có thể chỉnh sửa dễ dàng là "có thể làm giao diện - themeable" - một lớp hoặc giao diện trình bày nội dung theo cách mà chủ sở hữu hoặc người tạo dự định; Jekyll không khác biệt điều đó. Các trang, bài đăng và bất kỳ hình thức nội dung được định dạng nào khác có thể được tách biệt khỏi các tệp khuôn mẫu.

Giao diện cho Jekyll đã xuất hiện được một thời gian, nhưng quá trình cài đặt là một chủ đề hơi rắc rối. Các tệp nội dung và các tệp khuôn mẫu sẽ phải được sao chép cẩn thận. Nhưng, với việc giới thiệu các giao diện dựa trên [Gem-base themes](https://jekyllrb.com/docs/themes/), giờ đây các giao diện có thể được cài đặt với một vài dòng mã.

## Làm thế nào để chủ đề hoạt động? #
Các giao diện Jekyll cho phép bạn chứa tất cả các mã tạo khuôn mẫu và trình bày trong một Ruby gem, giống như cách các plugin Jekyll được chứa. Điều này có nghĩa là thiết kế có thể dễ dàng được áp dụng cho một trang web, được sử dụng trên nhiều trang web và codebase của trang web bị lộn xộn bởi lớp trình bày.

    root/
    ├── _posts/
    │   └── my-amazing-post-14-09-2017.md
    ├── index.html
    ├── Gemfile
    ├── _config.yml
    ├── 404.md
    └── about.md
    Ví dụ về cấu trúc trang web Jekyll khi sử dụng một giao diện Gem


