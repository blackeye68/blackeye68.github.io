---
layout: post
title:  "Kỹ thuật lập trình: Kiến trúc MVC"
author: blackeye
categories: [ .net, identity, tim-hieu]
image: assets/images/8.jpg
dotnet: true
---

# MVC Architecture - Kiến trúc MVC
- Đây là một design pattern.
- MVC là viết tắt của **Model, View và Controller**.
- MVC tách ứng dụng ra làm 3 phần chính là: Model, View và Controller nên nó được gọi là MVC.
- Hình biểu diễn:
![]({{site.baseurl}}/assets/images/dotnetcore/mvc-architecture.png)

- Giải thích ảnh mô hình:
    + Khi một user gửi request từ View (giao diện) bắn lên Controller và Controller sẽ xử lý request và sau đó thao tác dữ liệu thông qua Model sau đó nó sẽ gửi lại (response) kết quả cho View để hiển thị.
    + View được hiển thị nhờ Model là nơi vừa chứa dữ liệu, vừa là nơi truy xuất dữ liệu để giúp chúng ta hiển thị nên View.
- MVC Architecture
    + **Model**: Model represents shape of the data and business logic. It maintains the data of the application. Model objects retrieve and store model state in a database.
        * > Model is a data and business logic.
    + **View**: View is a user interface. View display data using model to the user and also enables them to modify the data.
        * > View is a User Interface.
    + **Controller**: Controller handles the user request. Typically, user interact with View, which in-tern raises appropriate URL request, this request will be handled by a controller. The controller renders the appropriate view with the model data as a response.
        * > Controller is a request handler.
    
- Hình biểu diễn người dùng tương tác với MVC:
![]({{site.baseurl}}/assets/images/dotnetcore/request-handling-in-mvc.png)


