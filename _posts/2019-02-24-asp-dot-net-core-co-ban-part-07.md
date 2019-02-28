---
layout: post
title:  "ASP.NET Core cơ bản - Phần 07:  Bắt lỗi trong ứng dụng [Exception handling]"
author: blackeye
categories: [ .net-core, co-ban, khai-niem, part-09 ]
image: assets/images/10.jpg
dotnet: true
---
# Overview
- When errors occur in your ASP.NET Core app, you can handle them in a variety of ways, as described in this article.

## Configuring a custom exception handling page
- It's a good idea to configure an exception handler page to use when the app is no running in the Development environment.

    ![]()

## Configuring status code pages
- By default, your app will not provide a rich status code page of HTTP status codes such as 500 (Internal Server Error) or 404 (Not Found). You can configure the StatusCodePagesMiddleware by adding a line to the Configure method.
- The middleware supports several different extension methods. One takes a lambda expression, another takes a content type and format string.

    ![]()

## Configuring status code pages
- There are also redirect extension methods. One sends a 302 status code to the client, and one returns the original status code to the client but also executes the handler for the redirect URL.
- app.UseStatusCodePagesWithRedirects("/error/{0}");

## The developer exception page
- To configure an app to display a page that shows detailed information about exceptions, install the Microsoft.AspNetCore.Diagnostics
- Enable the developer exception page **only when the app is running in the Development environment**

## Exception-handling code
- Code in exception handling pages can throw exceptions. It's often a good idea for production error pages to consist of purely static content.

## Server exception handling
- In addition to the exception handling logic in your app, the server hosting your app will perform some exception handling.
- If the server catches an exception before the headers have been sent it sends a 500 Internal Server Error response with no body.
- If it catches an exception after the headers have been sent, it closes the connection.
- Request that are not handled by your app will be handled by the server, and any exception that occurs will be handled by the server's exception handling.

## ASP.NET MVC error handling
- MVC apps have some additional options for handling errors, such as configuring exception filters and performing model validation.
    * Exceptions Filters. - Lọc các Exception
    * Handling Model State Errors