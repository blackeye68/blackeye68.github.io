---
layout: post
title:  "ASP.NET Core cơ bản - Phần 01: Một số khải niệm cơ bản trong .NET CORE"
author: blackeye
categories: [ .net-core, co-ban, khai-niem ]
image: assets/images/6.jpg
dotnet: true
---

## Nội dung kiến thức - Contents:
- Fundamentals (Cơ bản)
    + A ASP.NET Core app is simply a console app that creates a web server in its Main method
- Startup
- Services
    + A services is a component that is intended for common consumption in an application.
    + Services are made available through dependency injection (DI).
    + ASP.NET Core includes a simple built - in inversion of control (IoC) container that supports constructor injection by default.
    + The built-in container can be easily replaced with your container of choice.
- **Middleware**
    + ASP.NET Core middleware performs asynchoronous logic on an HttpContex and then either invokes the next middleware in the sequence or terminates the request directly.
    + You generally "Use" middleware by taking a dependency on a NuGet package and invoking a corresponding UseXYZ extension method on the IApplicationBuilder in the Configure.
    + ASP.NET Core comes with a rick set of built-in middleware:
        * Satatic files
        * Routing
        * Authentication
- Servers
- Content Root
- Web root
- Configuration
- Environments
- .NET Core and .NET Framework runtime

## Thực hành - Practice:
- Cách tạo 1 .NET CORE project với Visual Studio:
- 
