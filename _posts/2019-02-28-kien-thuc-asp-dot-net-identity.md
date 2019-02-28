---
layout: post
title:  "Tìm hiểu ASP.NET Identity"
author: blackeye
categories: [ .net, identity, tim-hieu]
image: assets/images/8.jpg
dotnet: true
---

# Overview
- ASP.NET Identity là một hệ thống chứng thực cấp quyền (membershop system) giúp ta thêm chức năng login, logout, signup vào trong ứng dụng của chúng ta. 
- Tiền thân của ASP.NET Identity là ASP.NET Membership sau khi ra đời đã có nhiều điểm yếu. ASP.NET Identity đã khắc phục và ra mắt nhiều tính năng mạnh mẽ.
- Được ra mắt lần đầu trong Project Template của Visual 2013.
- Nó là 1 giải pháp dùng chung cho nhiều nhà phát triển giúp chúng ta không phải code lại nữa như vậy sẽ giúp ta phát triển ứng dụng nhanh hơn.
- Nó cung cấp cho chúng ta giải pháp bảo mật, mã hóa, tích hợp với các chức năng login với google, facebook, twitter...
- Chúng ta có thể cấu hình ASP.NET Identity sử dụng SQL Server database (hoặc các cơ sở dữ liệu quan hệ khác) để lưu trữ tên người dùng, mật khẩu và dữ liệu thông tin hồ sơ. Hoặc chúng ta cũng có thể lưu trữ trên Azure Cloud.

## Các đặc điểm
- Là cơ chế dùng chung cho tất cả các ứng dụng Web bao gồm ASP.NET MVC, Web API, WebForm và SignalR.
- Dễ dàng thêm mới các trường dữ liệu khác vào user
- Dễ dàng Unit test
- Quản lý quyền
- Hỗ trợ login với các Social dễ dàng
- Độc lập với Web vì sử dụng cơ chế **OWIN**.
- Cài đặt dễ dàng từ Nuget

## Các bước thực hiện cài đặt DI Autofac (càiđặt trong ASP.NET MVC)
1. Cài đặt 3 thưu viện
    1. Microsoft.AspNet.Identity.EntityFramework
    2. Microsoft.AspNet.Identity.Core
    3. Microsoft.AspNet.Identity.OWIN
2. Tạo mới class User kế thừa từ IdentityUser
3. Tạo mới Role kế thừa từ IdentityRole
4. Kế thừa lớp DbContext từ dentityDbContext<User>
5. Cấu hình authentication từ file Startup.cs
6. Thực hiện Migration vào database
7. Tạo class quản lý authen

## Giới thiệu về cấu trúc tổ chức thư mục của ASP.NET Identity (ASP.NET MVC)
Khi project được tạo xong các bạn sẽ thấy 1 số files được tạo sẵn trong project như sau:

* **App_Start/IdentityConfig.cs**: chứa các lệnh để cấu hình ASP.NET Identity
* **Controller/AccountController**: controller chứa các action method có tác dụng xác thực người dùng như Login, Register, ForgotPassword, ...
* **Controller/ManageController**: controller chứa các action method có tác dụng quản lý user (khi user đã login vào web) như ChangePassword, SetPassword, ...
* **Model/AccountViewModels**: chứa các View Model hiển thị trong các view của AccountController
* **Model/ManageViewModels**: chứa các View Model hiển thị trong các view của ManageController
* **Model/IdentityModels**: chứa class ApplicationUser để quản lý thông tin user và class ApplicationDbContext để quản lý kết nối với database ở dạng Entity Framework Code First (các bạn nên có kiến thức căn bản về Entity Framework Code First) để có thể bổ sung thêm các field cho user hoặc loại bỏ bớt các field mà bạn không cần thiết 1 cách dễ dàng và ít bỡ ngỡ.

## Chức năng đăng ký thành viên (Register) (ASP.NET MVC)
Mình giải thích 1 số thuộc tính bạn cần biết:
* **RequiredLength**: độ dài tối thiểu của password
* **RequireNonLetterOrDigit**:  bắt buộc password chứa ký tự đặc biệt hoặc ký tự số
* **RequireDigit**: bắt buộc chứa ký tự số
* **RequireLowercase**: bắt buộc chứa ký tự in thường
* **RequireUppercase**: bắt buộc chứa ký tự in HOA

Các bạn có thể tùy ý cấu hình theo ý muốn nhé. Ở đây mình chỉ muốn đặt ràng buộc cho mật khẩu là tối thiểu 6 ký tự bao gồm cả ký tự số thì đoạn code mình sẽ sửa lại như sau:

    // Configure validation logic for passwords
                manager.PasswordValidator = new PasswordValidator
                {
                    RequiredLength = 6,
                    RequireNonLetterOrDigit = false
                    RequireDigit = true,
                    RequireLowercase = false,
                    RequireUppercase = false,
                };
    Sau khi sửa xong mình tiến hành build lại project và load lại trang register. Sau đó nhập thông tin như sau:
    **Email: tuannguyen@gmail.com**
    **Password: iloveyouok123**
    **Confirm password: iloveyouok123**

## ASP.NET Identity Architecture - Kiến trúc của ASP.NET Identity

![]({{site.baseurl}}/assets/images/dotnetcore/identity-architech.png)


![]({{site.baseurl}}/assets/images/dotnetcore/identity-library.png)

