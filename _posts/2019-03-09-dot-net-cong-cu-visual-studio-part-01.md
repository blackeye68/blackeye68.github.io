---
layout: post
title:  "Lập trình Microsoft .Net Visual Studio 2017 - Part 01 - Cài đặt"
author: blackeye
categories: [ .net, identity, tim-hieu]
image: assets/images/8.jpg
dotnet: true
---

# Install Visual Studio 2017 - Cài đặt Visual Studio 2017
Đầu tiên bạn phải vào trang chủ của Microsoft để download công cụ cài đặt **Visual Studio** là: **Visual Studio Installer** - [tại link](https://visualstudio.microsoft.com/downloads/).

![]({{site.baseur}}/assets/images/)

Sau khi tải bộ cài đặt công cụ cài đặt **Visual Studio Installer** ta click vào file cài đặt để tiến hành cài đặt bộ cài đặt **Visual Studio Installer**

![]({{site.baseur}}/assets/images/)

việc cài đặt này có thể diễn ra trong một khoảng thời gian khá lâu vì tốc độ tải về tương đối chậm (ở trên máy mình - kéo dài đến 45' cho 63'82 MB)

Sau khi cài xong bộ cài đặt **Visual Studio Installer** thì dùng bộ cài này để cài đặt **Visual Studio 2017** và các thành phần của nó như: .Net Core, .Net Framework, ...

> Kinh nghiệm: Khi mới cài đặt Visual Studio 2017 nên chọn các phần cài cơ bản thôi, không nên cài thừa như vậy sẽ rất nặng máy mà cài lại lâu. Ta có thể chọn các phần tối thiểu để cài sau đó nếu cần đến thì lại mởi Visual Studio Installer để cài thêm sau.

## Kinh nghiệm sửa:
- Khi cài lại Visual Studio 2017 hoặc gặp lỗi cần cài đi cài lại Visual Studio 2017 mà không uninstall hoặc repair... được có thể do bạn chưa xóa được hết các cài đặt cũ hoặc xóa kiểu thủ công... Để giải quyết được ta phải vào thư mục của [C:\Program Files (x86)\Microsoft Visual Studio\Installer\resources\app\layout\]() - thường là vậy - của Visaul Studio Installer rồi chạy file **AppCleaner.exe** (Tối nhất là chạy với chế độ Administrator) --> Nó giúp ta xóa triệut để Visual Studio 2017 để sau đó ta có thể tải file cài đặt về và cài lại.







