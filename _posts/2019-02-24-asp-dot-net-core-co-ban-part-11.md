---
layout: post
title:  "ASP.NET Core cơ bản - Phần 11: Configuration - Cấu hình"
author: blackeye
categories: [ .net-core, co-ban, khai-niem ]
image: assets/images/6.jpg
dotnet: true
---

## Overview
* The Configuration API provides a way of configuring an app based on a list of name-value pairs.
* Configuration is read at runtime from multiple sources.
* The name-value pairs can be grouped into a multi-level hierarchy.
    + File formats (INI, JSON, and XML).
    + Command-line arguments.
    + Environment variables.
    + In-memory .NET objects.
    + An encrypted user store.
    + Azure Key Vault.
    + Custom providers, which you install or create

### Simple configuration
* Reading configuration from file. 