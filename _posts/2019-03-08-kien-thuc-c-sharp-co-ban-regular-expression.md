---
layout: post
title:  "Kiến thức C# cơ bản: Regular Expression"
author: blackeye
categories: [ .net, identity, tim-hieu]
image: assets/images/8.jpg
dotnet: true
---
(nguồn tham khảo [^nguon])

# Regular Expression - Biểu thức chính quy
## Concept - Khái niệm:
- **Regular Expression** là một ngôn ngữ cực mạnh dùng mô tả văn bản cũng như thao tác trên văn bản. Một **RE** thường được ứng dụng lên một chuỗi, nghĩa là lên một nhóm ký tự.
- RE gồm 2 phần:
    + _literal_(trực kiện).
    + _metacharacters_(siêu ký tự)
- Các siêu ký tự (metacharacters) thường dùng (vô cùng quan trọng)
    * \d: ký tự chữ số tương đương [0-9]
    * \D: ký tự không phải chữ số
    * \s: ký tự khoảng trắng tương đương [\f\n\r\t\v]
    * \S: ký tự không phải khoảng trắng tương đương [^\f\n\r\t\v]
    * \w: ký tự word (gồm chữ cái và chữ số, dấu gạch dưới_) tương đương [a-zA-Z_0-9]
    * \W: ký tự không phải ký tự word tương đương [^a-zA-Z_0-9]
    * ^: bắt đầu 1 chuỗi hay 1 dòng.
    * $: kết thúc


## Examples - Ví dụ:



[nguon]: [Bài 22: Làm việc với Regular Expression - Khóa C# cơ bản - Tedu](https://www.youtube.com/watch?v=mfMn1HCK7UM&feature=youtu.be)
- 