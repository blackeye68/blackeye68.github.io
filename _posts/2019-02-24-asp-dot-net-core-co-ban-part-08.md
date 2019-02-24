---
layout: post
title:  "ASP.NET Core cơ bản - Phần 08: How to migrate ASP.NET Core 1.x to 2.0 ?"
author: blackeye
categories: [ .net-core, co-ban, khai-niem, part-08 ]
image: assets/images/7.jpg
dotnet: true
---

## What differences between 1.x and 2.0?
+ Razor Pages
+ ASP.NET Core metapackage
+ .NET Standard 2.0
+ Configuration update
+ Logging update
+ Authentication update
+ Identity update
+ Automatic use of anti-forgery tokens
+ Automatic precompilation
+ Razor support for C# 7.1

## Step by Step
+ Open ASP.NET Core solution 1.1
+ Open edit project file
+ Edit target framework
+ Change packages versions
+ Edit startup file
+ Edit program file
+ Run command restore
+ Rebuild and fix using