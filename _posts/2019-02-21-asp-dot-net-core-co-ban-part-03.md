---
layout: post
title:  "ASP.NET Core cơ bản - Phần 03: Một số khải niệm cơ bản trong .NET CORE"
author: blackeye
categories: [ .net-core, co-ban, khai-niem ]
image: assets/images/6.jpg
dotnet: true
---

## Nội dung kiến thức - Contents:
- **Fundamentals (Cơ bản)**
    + A ASP.NET Core app is simply a console app that creates a web server in its Main method.

- **Startup**
    + The UseStartup method on WebHostBuilder specifies the Startup class for your app.

- **Services**
    + A services is a component that is intended for common consumption in an application.
    + Services are made available through dependency injection (DI).
    + ASP.NET Core includes a simple built - in inversion of control (IoC) container that supports constructor injection by default.
    + The built-in container can be easily replaced with your container of choice.

- **Middleware**
    + ASP.NET Core middleware performs asynchoronous logic on an HttpContex and then either invokes the next middleware in the sequence or terminates the request directly.
    + You generally "Use" middleware by taking a dependency on a NuGet package and invoking a corresponding UseXYZ extension method on the IApplicationBuilder in the Configure.
    + ASP.NET Core comes with a rick set of built-in middleware:
        * Static files
        * Routing
        * Authentication

- **Servers**
* The ASP.NET Core hosting model does not directly listen for requests; rather it relies on an HTTP server implementation to forward the request to the application.
* The forwarded request is wrapped as a set of feature interfaces that the application then composes into an HttpContext.
* ASP.NET Core includes a managed cross-platform web server, called Kestrel that you would typically run behind a production web server like IIS or nginx.

- **Content Root**
* The content root is the base path to any content used by the app, such as its views and web content.
* By default the content root is the same as application base path for the executable hosting the app; an alternative location can be specified with _WebHostBuilder_.

- **Web root**
* The web root of your app is the directory in your project for public, static resources like css, js, and image files.
* The static files middleware will only serve files from the web root directory (and sub-directories) by default.
* The web root path defaults to _/wwwroot_, but you can specify a different location using the _WebHostBuilder_.

- **Configuration**
* ASP.NET Core uses a new configuration model for handling simple name-value pairs. The new configuration model is not based on System.
* Configuration or web.config; rather, it pulls from an ordered set of configuaration provides.
* The build-in configuration provides support a variety of file formats (XML, JSON, INI) and environment variables to enable environment-based configuration.
* You can also write your own custom configuration provides

- **Environments**
* Environments, like "Development" and "Production", are a first-class notion in ASP.NET Core and can be set using environment variables.
* For more information, see Working with Multiple Environments.

- **.NET Core and .NET Framework runtime**

- **When to choose .NET Core**
* You have cross-platform needs.
* You are targeting microservices.
* You are using Docker containers.
* You need high performance and scalable systems.
* You need side by side of .NET versions by application.

## Thực hành - Practice:
- Cách tạo 1 .NET CORE project với Visual Studio:
- 


## Khái niệm
1. **Dependency injection** là gì ? và khi nào nên sử dụng nó ?

    `Dependency injection là một kĩ thuật trong đó một object (hoặc một static method) cung cấp các dependencies của một object khác. Một dependency là một object mà có thể sử dụng (một service). Tuy nhiên định nghĩa trên vẫn khá là khó hiểu, vậy nên hãy cùng tìm hiểu để hiểu rõ hơn về nó nào.`

Dependency hay dependent nghĩa là phụ thuộc vào hỗ trợ của một cái gì, việc gì đó. Ví dụ như nếu chúng ta phụ thuộc quá nhiều vào smartphone, thì có thể hiểu là chúng ta đã dependent lên smartphone.

Trước khi nói về dependency injection, hãy hiểu xem dependency trong lập trình nghĩa là gì trc'.

Khi mà class A sử dụng một số chức năng của class class B, thì có thể nói là class A có quan hệ phụ thuộc với class B.

    ![]({{site.baseurl}}/assets/images/di/....jpg)

Trong java, trc' khi ta có thể sử dụng method của class khác, ta phải khởi tạo một object của class đấy (hay A cần phải tạo 1 thực thể của B).

Vậy ta có thể hiểu, việc chuyển giao nhiệm vụ khởi tạo object đó cho một ai khác và trực tiếp sử dụng các dependency đó được gọi là dependency injection. 

    ![]({{site.baseurl}}/assets/images/di/....jpg)

Tại sao chúng ta cần sử dụng dependency injection?
Ví dụ chúng ta có một class Car, trong đó có chứa một vài object khác như Wheel, Battery...

    class Car{
    private Wheels wheel = new MRFWheels();
    private Battery battery = new ExcideBattery();
    ...
    ...
    }

Ở đây, class Car chịu trách nhiệm khởi tạo tất cả các dependency object. Nhưng chuyện gì sẽ xảy ra nếu chúng ta muốn bỏ MRFWheel và thay thế bằng YokohamaWheel.

Chúng ta sẽ cần tạo một class Car mới với YokohamaWheel, tuy nhiên khi sử dụng dependency injection, chúng ta có thể đổi Wheel ở runtime vì dependency có thể đc đẩy vào (inject) ở runtime thay vì complile time.

Bạn có thể hiểu là dependency injection là một người trung gian chịu trách nhiệm tạo ra các loại wheel khác nhau, rồi cung cấp chúng cho class Car. Việc đó làm cho class Car ko phải phụ thuộc vào Wheel cụ thể nào hay Battery cụ thể nào nữa.

**Về cơ bản có 3 loại dependency injection:**
* **Constructor injection**: các dependency đc cung cấp thông qua constructor của class.
* **Setter injection**: client tạo ra một setter method để các class khác có thể sử dụng chúng để cấp dependency.
* **Interface injection**: dependency sẽ cung cấp một hàm injector để inject nó vào bất kì client nào đc truyền vào. Các client phải implement một interface mà có một setter method dành cho việc nhận dependency.

    class Car{
    private Wheels wheel;
    private Battery battery;
    
    /*Ở đâu đó trong project, ta khởi tạo những objects mà đc yêu cầu bởi class này
        Có 2 cách để implement dependency injection
        1. Dựa vào constructor
        2. Dựa vào Setter method
    */
    
    // Dựa vào constructor
    Car(Wheel wh, Battery bt) {
        this.wh = wh;
        this.bt = bt;
    }
    
    // Dựa vào Setter method
    void setWheel(Batter bt){
        this.bt = bt;
    }
    ...  
    ...
    }

Vậy trách nhiệm của dependency injection là:
- Tạo ra các object.
- Biết được class nào cần những object đấy.
- Cung cấp cho những class đó những object chúng cần.
Bằng cách này, nếu trong tương lai object đó có sự thay đổi thì dependency injection có nhiệm vụ cấp lại những object cần thiết cho class.

2. **API** là gì ?

3. **Boilerplate code** là gì ?

4. 

## Phân tích ASP.NET Core
- **class Startup** là gì ? : 

- Middleware nằm giữa resquest và response