---
layout: post
title:  "ASP.NET Core cơ bản - Phần 04: Application Startup - Khởi động ứng dụng"
author: blackeye
categories: [ .net-core, co-ban, khai-niem ]
image: assets/images/6.jpg
dotnet: true
---
## Startup Class
* ASP.NET Core apps require a Startup class. By convention, the Startup class is named "Startup".
* You specify the startup class name in the Main programs WebHostBuilderExtensions UseStartup<TStartup> method.
* You can define separate Startup classes for different environments, and the appropriate one will be selected at runtime.
* The Startup class constructor can accept dependencies that are provided through dependency injection.
* The Startup class must include a Configure method and can optionally include a ConfigureServices method, both of which are called when the application starts.

## The Configure Method - Phương thức cấu hình
* The Configure method is used to specify how the ASP.NET application will respond to HTTP requests.
* The request pipeline is configured by adding middleware components to an IApplicationBuilder instance that is provided by dependency injection.

## The ConfigureServices method
* The ConfigureServices method is optional; but if used, it's called before the Configure method by the runtime (some features are added before they're wired up to the request pipeline).
* For features that require substantial setup there are Add[Service] extension methods on IServiceCollection

## Services Available in Startup
* ASP.NET Core dependency injection provides application services during an application's startup.
* You can request these services by including the appropriate interface as a parameter on your Startup class's constructor or one of its Configure or ConfigureServices methods.
* Looking at each method in the Startup class in the order in which thay are called, the following services may be requested as parameters:
    + In the constructor: IHostingEnvironment, ILoggerFactory.
    + In the ConfigureServices method: IServiceCollection.
    + In the Configure method: IApplicationBuilder, IHostingEnvironment, ILoggerFactory, IApplicationLifetime.