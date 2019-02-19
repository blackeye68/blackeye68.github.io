---
layout: post
title:  "Kiến thức về ngôn ngữ Markdown-Phần 02: Bảng tóm tắt về cú pháp Markdown"
author: blackeye
categories: [ markdown, phan2, kienthuc ]
image: assets/images/5.jpg
jekyll: true
---

# Tài liệu tổng hợp
Bảng tóm tắt kèm ví dụ tham chiếu nhanh các cú pháp cơ bản của Markdown

### Tổng quan
This Markdown cheat sheet provides a quick overview of all the Markdown syntax elements. It can’t cover every edge case, so if you need more information about any of these elements, refer to our reference guides for basic syntax and extended syntax.

### Cú pháp đơn giản
Đây là những thành phần được nêu trong tài liệu thiết kế ban đầu của John Gruber. Tất cả các ứng dụng Markdown đều hỗ trợ các thành phần này.


| Element	              | Markdown Syntax |
| --------------------- | --------------- |
| Heading	              | `# H1`          |
|                       | `## H2`         |
|                       | `### H3`        |
|Bold	                  |**bold text**    |
|Italic	                |*italicized text*|
|Blockquote	            |> blockquote     |
|Ordered List           |1. First item    |
|                       |2. Second item   |
|                       |3. Third item    |
|Unordered List         |	- First item    |
|                       |- Second item    |
|                       |- Third item     |
|Code	                  |`code`           |
|Horizontal Rule	      |---              |
|Link	                  |[title](https://www.example.com) |
|Image	                | ![alt text](image.jpg)          |

### Cú pháp mở rộng
Các thành phần này mở rộng cú pháp cơ bản bằng cách thêm các tính năng bổ sung. Không phải tất cả các ứng dụng Markdown đều hỗ trợ các thành phần này.

|Element               |	Markdown Syntax   |
|--------------------  | ----------------   |
Table	               | Syntax | Description | 
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
|Fenced Code Block	    | ```               |
|                        |{
|                     | "firstName": "John",
|                 | "lastName": "Smith",
|                     |"age": 25
|                    |}
|                   |```
|Footnote	Here's a sentence with a footnote.| [^1] 
|                             |  [^1]: This is the footnote.|
|Heading ID	### My Great Heading {#custom-id}
|Definition List	         |term
|                          |: definition
|Strikethrough	               |~~The world is flat.~~|
|Task List|      	- [x] Write the press release  |
|                 |- [ ] Update the website   |
|                 |- [ ] Contact the media    |

