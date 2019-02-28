---
layout: post
title:  "ASP.NET Core cơ bản - Phần 05: ASP.NET Middleware"
author: blackeye
categories: [ .net-core, co-ban, khai-niem ]
image: assets/images/6.jpg
dotnet: true
---

## What is Middleware ?
* Middleware is sofeware that is assembled into an application pipeline to handle requests and responses.
    - Middleware là phần mềm lắp ghép vào đường ống củng của ứng dụng để bắt những request và response.
* This means that they are effectively "gateway" classes that can decide whether or not to continue allowing the request to be processed by other Middleware components further down the stream.

## Configuring Middleware
* Adding middleware to an application happens in the Configure method of the startup class for an application.
* The Configure method is injectable, meaning you can [ask for any other services you need](), but the one service you'll always need is the IApplicationBuilder service.
* Most middleware will live in a NeGet package.
* Each NuGet package will include extension methods for IApplicationBuilder to add a middleware component using a simple method call.
* Notice the extension methods all start will the word _Use_.
* The order that middleware components are added in the Configure method defines the order in which they are invoked on requests, and the reverse order for the response.

![]()



## Build-in middleware

| Middleware                   | Description                                                      |
|------------------------------|------------------------------------------------------------------|
| [Authentication]()           | Provides authentication support.                                 |
| [CORS]()                     | Configures Cross-Origin Resource Sharing.                        |
| [Response Caching]()         | Provides support for caching responses                           |
| [Response Compression]()     | Provides support for compressing responses.                      |
| [Routing]()                  | Defines and constrains request routes.                           |
| [Session]()                  | Provides support for managing user session.                      |
| [Static Files]()             | Provides support for serving static files and directory browing. |
| [URL Rewriting Middleware]() | Provides support for rewriting URLs and redirecting request.     |

## Creating Middleware
* First, _Invoke_ will receive an _HttpContext_ object with access to the request and the response.
* You can inspect incoming headers and create outgong headers.
* You can read the request body or write into the response.
* The logic inside Invoke can decide if you want to call the next piece of middleware or handle the response entirely in the current middleware.
* Note the name _Invoke_ is the method ASP.NET will automatically look for (no interface implementation required), and is injectable.

## Run, Map, and Use
* Run is a convention, and some middleware components may expose Run[Middleware] methods that run at the end of the pipeline.
* [Map] branches the request pipeline based on matches of the given request path
* [MapWhen] branches the request pipeline based on the result of the given predicate.

### Migrating module code to middleware
* IHttpModule --> Middleware
* IHttpHandler --> Middleware

## Advantages - Ưu điểm
* The ability to explicitly configure every component of the HTTP processing pipeline makes it easy to know what is happening inside an application.
* The application is also as lean as possible because we can install only the features an application requires.
* Middleware is on reason why ASP.NET Core can perform better and use less memory than its predecessors.

## Disadvantages - Nhược điểm
* Time consuming to move existed HTTP modules to middleware when migrate from older version to .NET Core.
* Middleware components are highly asynchronous and often follow functional programming idioms. Also, there are no interfaces to guide middleware develoment as most of the contracts rely on convention instead of the compiler. All of these changes make some developers uncomfortable.
* Difficulty when find match middleware in Nuget before make decision to create new middleware.

## Summary
* Expect to see middleware play an increasingly importand role in the future.
* Not only will Microsoft and others create more middleware, but also expect the sophistication of middleware to increase.
* Future middleware will not only continue to replace IIS features like URL re-writing, but also change our application architecture by enabling additional frameworks and the ability to compose new behavior into an application.
* Don't underestimate the importance of porting existing logic into middleware and the impact of a middleware on an application's behavior.