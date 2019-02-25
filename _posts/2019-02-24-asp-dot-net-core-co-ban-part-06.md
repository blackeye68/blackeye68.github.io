---
layout: post
title:  "ASP.NET Core cơ bản - Phần 06: Working with Static Files"
author: blackeye
categories: [ .net-core, co-ban, khai-niem, part-06 ]
image: assets/images/6.jpg
dotnet: true
---


## **OVERVIEW**
- Static files, such as HTML, CSS image, and Javascript, are assets that an ASP.NET Core app can serve directly to clients.

### **Serving static files**
- Static files are typically located in the web root (<content-root>/wwwroot) folder.
- You generally set the content root to be the current directory so that your project's web root will be found while in development.
    - [http://<app>/images/<imageFileName>]()
    - [http://localhost:9189/images/banner3.svg]()
    - web root defaults to the wwwroot directory, but you can set the web root directory with UseWebRoot.

## **Serving static files**
- Suppose you have a project hierarchy where the static files you wish to serve are outside the web root.

## **Static file authorization**
- The static file module provides **no** authorization checks. Any files served by it, including those under _wwwroot_ are publicly available.
- To serve files based on authorization:
    + Store theme outsite of _wwwroot_ and any directory accessible to the static file middleware and 
    + Serve them through a controller action, returning a FileResult where authorization is applied

### **UseFileServer**
- UseFileServer combines the functionality of UseStaticFiles, UseDefaultFiles, and UseDirectoryBrowser.
- The following code enables static files and the default file to be served, but does not allow directory browsing: