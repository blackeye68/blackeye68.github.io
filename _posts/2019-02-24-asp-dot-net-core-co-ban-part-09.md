---
layout: post
title:  "ASP.NET Core cơ bản - Phần 09: Tìm hiểu về Dependency Injection"
author: blackeye
categories: [ .net-core, co-ban, khai-niem, part-09 ]
image: assets/images/7.jpg
dotnet: true
---

# **OVERVIEW**
- What is Dependency Injection ?
- Using Framework-Provided Services
- Service Lifetimes and Registration Options
- Request Services
- Designing Your Services For Dependency Injection
- Replacing the default services container
- Recommendations

## What is Dependency Injection?
- Dependency injection (DI) is a technique for achieving loose coupling between objects and their collaborators, or dependencies.
- This follows the ``Dependency Inversion Principle``, which states that "high level modules should not depend on low level modules; both should depend on abstractions."
- Extracting dependencies into interfaces and providing implementations of these interfaces as parameters is also an example of the ```Strategy design pattern```.

## 