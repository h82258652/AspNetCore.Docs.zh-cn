---
title: ASP.NET Core Web SDK
author: Rick-Anderson
description: Microsoft.NET.Sdk.Web 概述。
ms.author: riande
ms.date: 01/25/2020
no-loc:
- Blazor
- Identity
- Let's Encrypt
- Razor
- SignalR
uid: razor-pages/web-sdk
ms.openlocfilehash: 2797f0b3003b8ad89093fe1115dee2acc8650c73
ms.sourcegitcommit: 70e5f982c218db82aa54aa8b8d96b377cfc7283f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2020
ms.locfileid: "82777158"
---
# <a name="aspnet-core-web-sdk"></a>ASP.NET Core Web SDK

### <a name="overview"></a>概述

`Microsoft.NET.Sdk.Web` 是一个用于构建 ASP.NET Core 应用的 [MSBuild 项目 SDK](https://docs.microsoft.com/visualstudio/msbuild/how-to-use-project-sdk)。 无需此 SDK 即可构建 ASP.NET Core 应用，不过该 Web SDK：

* 旨在提供一流的体验。
* 是大多数用户的理想之选。

在项目中使用该 Web.SDK：

  ```xml
  <Project Sdk="Microsoft.NET.Sdk.Web">
    <!-- omitted for brevity -->
  </Project>
  ```

通过使用该 Web SDK 启用的功能：

* 面向 .NET Core 3.0 或更高版本的项目隐式引用：

  * [ASP.NET Core 共享框架](xref:fundamentals/metapackage-app)。
  * 专用于构建 ASP.NET Core 应用的[分析器](/visualstudio/extensibility/getting-started-with-roslyn-analyzers)。
* 该 Web SDK 会导入 MSBuild 目标，允许使用发布配置文件并使用 WebDeploy 进行发布。

### <a name="properties"></a>属性

| Property | 描述 |
| -------- | ----------- |
| `DisableImplicitFrameworkReferences` | 禁用对 `Microsoft.AspNetCore.App` 共享框架的隐式引用。 |
| `DisableImplicitAspNetCoreAnalyzers` | 禁用对 ASP.NET Core 分析器的隐式引用。 |
| `DisableImplicitComponentsAnalyzers` | 在构建 Blazor（服务器）应用程序时禁用对 Razor 组件分析器的隐式引用。 |
