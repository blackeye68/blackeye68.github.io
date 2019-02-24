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
* This means that they are effectively "gateway" classes that can decide whether or not to continue allowing the request to be processed by other Middleware components further down the stream.

## Build-in middleware