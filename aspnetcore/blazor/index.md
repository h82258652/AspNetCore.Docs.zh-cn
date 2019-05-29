---
title: ASP.NET Core 中的 Blazor 简介
author: guardrex
description: 了解 ASP.NET Core Blazor，用户可以借助它在 ASP.NET Core 应用中使用 .NET 生成交互式客户端 Web UI。
monikerRange: '>= aspnetcore-3.0'
ms.author: riande
ms.custom: mvc, seoapril2019
ms.date: 05/01/2019
uid: blazor/index
ms.openlocfilehash: bd7d2d3e6702844627f19dfbbbad5c52389a52e5
ms.sourcegitcommit: dd9c73db7853d87b566eef136d2162f648a43b85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2019
ms.locfileid: "65085784"
---
# <a name="introduction-to-blazor"></a><span data-ttu-id="96aa2-103">Blazor 简介</span><span class="sxs-lookup"><span data-stu-id="96aa2-103">Introduction to Blazor</span></span>

<span data-ttu-id="96aa2-104">作者：[Daniel Roth](https://github.com/danroth27) 和 [Luke Latham](https://github.com/guardrex)</span><span class="sxs-lookup"><span data-stu-id="96aa2-104">By [Daniel Roth](https://github.com/danroth27) and [Luke Latham](https://github.com/guardrex)</span></span>

<span data-ttu-id="96aa2-105">*欢迎使用 Blazor！*</span><span class="sxs-lookup"><span data-stu-id="96aa2-105">*Welcome to Blazor!*</span></span>

<span data-ttu-id="96aa2-106">Blazor 是一个用于使用 .NET 生成交互式客户端 Web UI 的框架：</span><span class="sxs-lookup"><span data-stu-id="96aa2-106">Blazor is a framework for building interactive client-side web UI with .NET:</span></span>

* <span data-ttu-id="96aa2-107">使用 C# 代替 JavaScript 来创建丰富的交互式 UI。</span><span class="sxs-lookup"><span data-stu-id="96aa2-107">Create rich interactive UIs using C# instead of JavaScript.</span></span>
* <span data-ttu-id="96aa2-108">共享使用 .NET 编写的服务器端和客户端应用逻辑。</span><span class="sxs-lookup"><span data-stu-id="96aa2-108">Share server-side and client-side app logic written with .NET.</span></span>
* <span data-ttu-id="96aa2-109">将 UI 呈现为 HTML 和 CSS，以支持众多浏览器，其中包括移动浏览器。</span><span class="sxs-lookup"><span data-stu-id="96aa2-109">Render the UI as HTML and CSS for wide browser support, including mobile browsers.</span></span>

<span data-ttu-id="96aa2-110">使用 .NET 进行客户端 Web 开发可提供以下优势：</span><span class="sxs-lookup"><span data-stu-id="96aa2-110">Using .NET for client-side web development offers the following advantages:</span></span>

* <span data-ttu-id="96aa2-111">使用 C# 代替 JavaScript 来编写代码。</span><span class="sxs-lookup"><span data-stu-id="96aa2-111">Write code in C# instead of JavaScript.</span></span>
* <span data-ttu-id="96aa2-112">利用现有的 .NET 库生态系统。</span><span class="sxs-lookup"><span data-stu-id="96aa2-112">Leverage the existing .NET ecosystem of .NET libraries.</span></span>
* <span data-ttu-id="96aa2-113">在服务器和客户端之间共享应用逻辑。</span><span class="sxs-lookup"><span data-stu-id="96aa2-113">Share app logic across the server and client.</span></span>
* <span data-ttu-id="96aa2-114">受益于 .NET 的性能、可靠性和安全性。</span><span class="sxs-lookup"><span data-stu-id="96aa2-114">Benefit from .NET's performance, reliability, and security.</span></span>
* <span data-ttu-id="96aa2-115">始终高效支持 Windows、Linux 和 macOS 上的 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="96aa2-115">Stay productive with Visual Studio on Windows, Linux, and macOS.</span></span>
* <span data-ttu-id="96aa2-116">以一组稳定、功能丰富且易用的通用语言、框架和工具为基础来进行生成。</span><span class="sxs-lookup"><span data-stu-id="96aa2-116">Build on a common set of languages, frameworks, and tools that are stable, feature-rich, and easy to use.</span></span>

## <a name="components"></a><span data-ttu-id="96aa2-117">组件数</span><span class="sxs-lookup"><span data-stu-id="96aa2-117">Components</span></span>

<span data-ttu-id="96aa2-118">Blazor 应用基于组件。</span><span class="sxs-lookup"><span data-stu-id="96aa2-118">Blazor apps are based on *components*.</span></span> <span data-ttu-id="96aa2-119">Blazor 中的组件是指 UI 元素，例如，页面、对话框或数据输入窗体。</span><span class="sxs-lookup"><span data-stu-id="96aa2-119">A component in Blazor is an element of UI, such as a page, dialog, or data entry form.</span></span> <span data-ttu-id="96aa2-120">组件处理用户事件，并定义灵活的 UI 呈现逻辑。</span><span class="sxs-lookup"><span data-stu-id="96aa2-120">Components handle user events and define flexible UI rendering logic.</span></span> <span data-ttu-id="96aa2-121">组件可以嵌套和重用。</span><span class="sxs-lookup"><span data-stu-id="96aa2-121">Components can be nested and reused.</span></span>

<span data-ttu-id="96aa2-122">组件是内置于 .NET 程序集的 .NET 类，可以作为 [NuGet 包](/nuget/what-is-nuget)进行共享和分发。</span><span class="sxs-lookup"><span data-stu-id="96aa2-122">Components are .NET classes built into .NET assemblies that can be shared and distributed as [NuGet packages](/nuget/what-is-nuget).</span></span> <span data-ttu-id="96aa2-123">组件类通常以 Razor 标记页（文件扩展名为 .razor）的形式编写。</span><span class="sxs-lookup"><span data-stu-id="96aa2-123">The component class is usually written in the form of a Razor markup page with a *.razor* file extension.</span></span>

<span data-ttu-id="96aa2-124">Blazor 中的组件有时被称为 Razor 组件。</span><span class="sxs-lookup"><span data-stu-id="96aa2-124">Components in Blazor are sometimes referred to as *Razor components*.</span></span> <span data-ttu-id="96aa2-125">[Razor](xref:mvc/views/razor) 是用于将 HTML 标记与专为提高开发人员工作效率而设计的 C# 代码结合在一起的语法。</span><span class="sxs-lookup"><span data-stu-id="96aa2-125">[Razor](xref:mvc/views/razor) is a syntax for combining HTML markup with C# code designed for developer productivity.</span></span> <span data-ttu-id="96aa2-126">借助 Razor，可以使用 [IntelliSense](/visualstudio/ide/using-intellisense) 支持在同一文件中的 HTML 标记和 C# 之间切换。</span><span class="sxs-lookup"><span data-stu-id="96aa2-126">Razor allows you to switch between HTML markup and C# in the same file with [IntelliSense](/visualstudio/ide/using-intellisense) support.</span></span> <span data-ttu-id="96aa2-127">Razor Pages 和 MVC 也使用 Razor。</span><span class="sxs-lookup"><span data-stu-id="96aa2-127">Razor Pages and MVC also use Razor.</span></span> <span data-ttu-id="96aa2-128">与围绕请求/响应模型生成的 Razor Pages 和 MVC 不同，组件专门用于处理客户端 UI 逻辑和构成。</span><span class="sxs-lookup"><span data-stu-id="96aa2-128">Unlike Razor Pages and MVC, which are built around a request/response model, components are used specifically for client-side UI logic and composition.</span></span>

<span data-ttu-id="96aa2-129">以下 Razor 标记演示组件 (Dialog.razor)，该组件可以嵌套在另一个组件中：</span><span class="sxs-lookup"><span data-stu-id="96aa2-129">The following Razor markup demonstrates a component (*Dialog.razor*), which can be nested within another component:</span></span>

```cshtml
<div>
    <h1>@Title</h1>

    @ChildContent

    <button onclick="@OnYes">Yes!</button>
</div>

@functions {
    [Parameter]
    private string Title { get; set; }

    [Parameter]
    private RenderFragment ChildContent { get; set; }

    private void OnYes()
    {
        Console.WriteLine("Write to the console in C#!");
    }
}
```

<span data-ttu-id="96aa2-130">对话框的正文内容 (`ChildContent`) 和标题 (`Title`) 由在其 UI 中使用此组件的组件提供。</span><span class="sxs-lookup"><span data-stu-id="96aa2-130">The dialog's body content (`ChildContent`) and title (`Title`) are provided by the component that uses this component in its UI.</span></span> <span data-ttu-id="96aa2-131">`OnYes` 是由按钮的 `onclick` 事件触发的 C# 方法。</span><span class="sxs-lookup"><span data-stu-id="96aa2-131">`OnYes` is a C# method triggered by the button's `onclick` event.</span></span>

<span data-ttu-id="96aa2-132">Blazor 使用 UI 构成的自然 HTML 标记。</span><span class="sxs-lookup"><span data-stu-id="96aa2-132">Blazor uses natural HTML tags for UI composition.</span></span> <span data-ttu-id="96aa2-133">HTML 元素指定组件，并且标记的特性将值传递给组件的属性。</span><span class="sxs-lookup"><span data-stu-id="96aa2-133">HTML elements specify components, and a tag's attributes pass values to a component's properties.</span></span> <span data-ttu-id="96aa2-134">`ChildContent` 和 `Title` 由使用对话框组件 (Index.razor) 的组件设置：</span><span class="sxs-lookup"><span data-stu-id="96aa2-134">`ChildContent` and `Title` are set by the component that uses the Dialog component (*Index.razor*):</span></span>

```cshtml
@page "/"

<h1>Hello, world!</h1>

Welcome to your new app.

<Dialog Title="Blazor">
    Do you want to <i>learn more</i> about Blazor?
</Dialog>
```

<span data-ttu-id="96aa2-135">在浏览器中访问父级 (Index.razor) 时，将呈现该对话框：</span><span class="sxs-lookup"><span data-stu-id="96aa2-135">The dialog is rendered when the parent (*Index.razor*) is accessed in a browser:</span></span>

![浏览器中呈现的对话框组件](index/_static/dialog.png)

<span data-ttu-id="96aa2-137">如果在应用中使用此组件，[Visual Studio](/visualstudio/ide/using-intellisense) 和 [Visual Studio Code](https://code.visualstudio.com/docs/editor/intellisense) 中的 IntelliSense 可加快使用语法和参数补全的开发。</span><span class="sxs-lookup"><span data-stu-id="96aa2-137">When this component is used in the app, IntelliSense in [Visual Studio](/visualstudio/ide/using-intellisense) and [Visual Studio Code](https://code.visualstudio.com/docs/editor/intellisense) speeds development with syntax and parameter completion.</span></span>

<span data-ttu-id="96aa2-138">组件呈现为浏览器 DOM 的内存中表现形式，称为“呈现树”，然后可以使用它以灵活高效的方式更新 UI。</span><span class="sxs-lookup"><span data-stu-id="96aa2-138">Components render into an in-memory representation of the browser DOM called a *render tree* that's used to update the UI in a flexible and efficient way.</span></span>

## <a name="blazor-client-side"></a><span data-ttu-id="96aa2-139">Blazor 客户端</span><span class="sxs-lookup"><span data-stu-id="96aa2-139">Blazor client-side</span></span>

<span data-ttu-id="96aa2-140">Blazor 客户端是一个单页应用框架，用于使用 .NET 生成交互式客户端 Web 应用。</span><span class="sxs-lookup"><span data-stu-id="96aa2-140">Blazor client-side is a single-page app framework for building interactive client-side web apps with .NET.</span></span> <span data-ttu-id="96aa2-141">Blazor 客户端使用开放的 Web 标准（没有插件或代码转换），并且适用于所有新式 Web 浏览器（包括移动浏览器）。</span><span class="sxs-lookup"><span data-stu-id="96aa2-141">Blazor client-side uses open web standards without plugins or code transpilation and works in all modern web browsers, including mobile browsers.</span></span>

<span data-ttu-id="96aa2-142">通过 [WebAssembly](http://webassembly.org)（缩写为 wasm），可在 Web 浏览器内运行 .NET 代码。</span><span class="sxs-lookup"><span data-stu-id="96aa2-142">Running .NET code inside web browsers is made possible by [WebAssembly](http://webassembly.org) (abbreviated *wasm*).</span></span> <span data-ttu-id="96aa2-143">WebAssembly 是开放的 Web 标准，支持用于无插件的 Web 浏览器。</span><span class="sxs-lookup"><span data-stu-id="96aa2-143">WebAssembly is an open web standard and supported in web browsers without plugins.</span></span> <span data-ttu-id="96aa2-144">WebAssembly 是针对快速下载和最大执行速度优化的压缩字节码格式。</span><span class="sxs-lookup"><span data-stu-id="96aa2-144">WebAssembly is a compact bytecode format optimized for fast download and maximum execution speed.</span></span>

<span data-ttu-id="96aa2-145">WebAssembly 代码可通过 JavaScript（称为 JavaScript 互操作性或 JavaScript 互操作）访问浏览器的完整功能。</span><span class="sxs-lookup"><span data-stu-id="96aa2-145">WebAssembly code can access the full functionality of the browser via JavaScript, called *JavaScript interoperability* (or *JavaScript interop*).</span></span> <span data-ttu-id="96aa2-146">在浏览器中通过 WebAssembly 执行的 .NET 代码在与 JavaScript 相同的受信任沙盒中运行，这几乎可以阻止应用在客户端计算机上执行恶意操作。</span><span class="sxs-lookup"><span data-stu-id="96aa2-146">.NET code executed via WebAssembly in the browser runs in the same trusted sandbox as JavaScript, which virtually eliminates the opportunity for an app to perform malicious actions on the client machine.</span></span>

![Blazor 客户端使用 WebAssembly 在浏览器中运行 .NET 代码。](index/_static/blazor-client-side.png)

<span data-ttu-id="96aa2-148">生成 Blazor 客户端应用并在浏览器中运行时：</span><span class="sxs-lookup"><span data-stu-id="96aa2-148">When a Blazor client-side app is built and run in a browser:</span></span>

* <span data-ttu-id="96aa2-149">C# 代码文件和 Razor 文件将被编译为 .NET 程序集。</span><span class="sxs-lookup"><span data-stu-id="96aa2-149">C# code files and Razor files are compiled into .NET assemblies.</span></span>
* <span data-ttu-id="96aa2-150">该程序集和 .NET 运行时将被下载到浏览器。</span><span class="sxs-lookup"><span data-stu-id="96aa2-150">The assemblies and the .NET runtime are downloaded to the browser.</span></span>
* <span data-ttu-id="96aa2-151">Blazor 客户端启动 .NET 运行时并配置运行时，为应用加载程序集。</span><span class="sxs-lookup"><span data-stu-id="96aa2-151">Blazor client-side bootstraps the .NET runtime and configures the runtime to load the assemblies for the app.</span></span> <span data-ttu-id="96aa2-152">Blazor 客户端运行时使用 JavaScript 互操作处理文档对象模型 (DOM) 操作和浏览器 API 调用。</span><span class="sxs-lookup"><span data-stu-id="96aa2-152">The Blazor client-side runtime uses JavaScript interop to handle Document Object Model (DOM) manipulation and browser API calls.</span></span>

<span data-ttu-id="96aa2-153">已发布应用的大小（其有效负载大小）是应用可用性的关键性能因素。</span><span class="sxs-lookup"><span data-stu-id="96aa2-153">The size of the published app, its *payload size*, is a critical performance factor for an app's useability.</span></span> <span data-ttu-id="96aa2-154">大型应用需要相对较长的时间才能下载到浏览器，这会损害用户体验。</span><span class="sxs-lookup"><span data-stu-id="96aa2-154">A large app takes a relatively long time to download to a browser, which hurts the user experience.</span></span> <span data-ttu-id="96aa2-155">Blazor 客户端优化有效负载大小，以缩短下载时间：</span><span class="sxs-lookup"><span data-stu-id="96aa2-155">Blazor client-side optimizes payload size to reduce download times:</span></span>

* <span data-ttu-id="96aa2-156">在[中间语言 (IL) 链接器](xref:host-and-deploy/blazor/configure-linker)发布应用时，会从应用删除未使用的代码。</span><span class="sxs-lookup"><span data-stu-id="96aa2-156">Unused code is stripped out of the app when it's published by the [Intermediate Language (IL) Linker](xref:host-and-deploy/blazor/configure-linker).</span></span>
* <span data-ttu-id="96aa2-157">压缩 HTTP 响应。</span><span class="sxs-lookup"><span data-stu-id="96aa2-157">HTTP responses are compressed.</span></span>
* <span data-ttu-id="96aa2-158">.NET 运行时和程序集缓存在浏览器中。</span><span class="sxs-lookup"><span data-stu-id="96aa2-158">The .NET runtime and assemblies are cached in the browser.</span></span>

<span data-ttu-id="96aa2-159">有关选择托管模型的详细信息和指南，请参阅 <xref:blazor/hosting-models>。</span><span class="sxs-lookup"><span data-stu-id="96aa2-159">For more information and guidance on choosing a hosting model, see <xref:blazor/hosting-models>.</span></span>

## <a name="blazor-server-side"></a><span data-ttu-id="96aa2-160">Razor 服务器端</span><span class="sxs-lookup"><span data-stu-id="96aa2-160">Blazor server-side</span></span>

<span data-ttu-id="96aa2-161">Razor 将组件呈现逻辑从 UI 更新的应用方式中分离出来。</span><span class="sxs-lookup"><span data-stu-id="96aa2-161">Blazor decouples component rendering logic from how UI updates are applied.</span></span> <span data-ttu-id="96aa2-162">Razor 服务器端在 ASP.NET Core 应用中添加了对在服务器上托管 Razor 组件的支持。</span><span class="sxs-lookup"><span data-stu-id="96aa2-162">Blazor server-side provides support for hosting Razor components on the server in an ASP.NET Core app.</span></span> <span data-ttu-id="96aa2-163">可通过 [SignalR](xref:signalr/introduction) 连接处理 UI 更新。</span><span class="sxs-lookup"><span data-stu-id="96aa2-163">UI updates are handled over a [SignalR](xref:signalr/introduction) connection.</span></span>

<span data-ttu-id="96aa2-164">运行时处理从浏览器向服务器发送 UI 事件，并在运行组件后，将服务器发送的 UI 更新重新应用到浏览器。</span><span class="sxs-lookup"><span data-stu-id="96aa2-164">The runtime handles sending UI events from the browser to the server and applies UI updates sent by the server back to the browser after running the components.</span></span>

<span data-ttu-id="96aa2-165">被 Razor 服务器端用于与浏览器进行通信的组件还可用于处理 JavaScript 互操作调用。</span><span class="sxs-lookup"><span data-stu-id="96aa2-165">The connection used by Blazor server-side to communicate with the browser is also used to handle JavaScript interop calls.</span></span>

![Razor 服务器端在服务器上运行 .NET 代码，并通过 SignalR 连接与客户端上的文档对象模型进行交互](index/_static/blazor-server-side.png)

<span data-ttu-id="96aa2-167">有关选择托管模型的详细信息和指南，请参阅 <xref:blazor/hosting-models>。</span><span class="sxs-lookup"><span data-stu-id="96aa2-167">For more information and guidance on choosing a hosting model, see <xref:blazor/hosting-models>.</span></span>

## <a name="javascript-interop"></a><span data-ttu-id="96aa2-168">JavaScript 互操作</span><span class="sxs-lookup"><span data-stu-id="96aa2-168">JavaScript interop</span></span>

<span data-ttu-id="96aa2-169">对于需要第三方 JavaScript 库和浏览器 API 的应用，组件与 JavaScript 进行互操作。</span><span class="sxs-lookup"><span data-stu-id="96aa2-169">For apps that require third-party JavaScript libraries and browser APIs, components interoperate with JavaScript.</span></span> <span data-ttu-id="96aa2-170">组件能够使用 JavaScript 能够使用的任何库或 API。</span><span class="sxs-lookup"><span data-stu-id="96aa2-170">Components are capable of using any library or API that JavaScript is able to use.</span></span> <span data-ttu-id="96aa2-171">C# 代码可以调用到 JavaScript 代码，而 JavaScript 代码可以调用到 C# 代码。</span><span class="sxs-lookup"><span data-stu-id="96aa2-171">C# code can call into JavaScript code, and JavaScript code can call into C# code.</span></span> <span data-ttu-id="96aa2-172">有关更多信息，请参见<xref:blazor/javascript-interop>。</span><span class="sxs-lookup"><span data-stu-id="96aa2-172">For more information, see <xref:blazor/javascript-interop>.</span></span>

## <a name="code-sharing-and-net-standard"></a><span data-ttu-id="96aa2-173">代码共享和 .NET Standard</span><span class="sxs-lookup"><span data-stu-id="96aa2-173">Code sharing and .NET Standard</span></span>

<span data-ttu-id="96aa2-174">Blazor 实现 [.NET Standard 2.0](/dotnet/standard/net-standard)。</span><span class="sxs-lookup"><span data-stu-id="96aa2-174">Blazor implements [.NET Standard 2.0](/dotnet/standard/net-standard).</span></span> <span data-ttu-id="96aa2-175">.NET Standard 是正式的 .NET API 规范，常见于 .NET 实现中。</span><span class="sxs-lookup"><span data-stu-id="96aa2-175">.NET Standard is a formal specification of .NET APIs that are common across .NET implementations.</span></span> <span data-ttu-id="96aa2-176">.NET Standard 类库可以在不同 .NET 平台之间共享，例如 Blazor、.NET Framework、.NET Core、Xamarin、Mono 和 Unity。</span><span class="sxs-lookup"><span data-stu-id="96aa2-176">.NET Standard class libraries can be shared across different .NET platforms, such as Blazor, .NET Framework, .NET Core, Xamarin, Mono, and Unity.</span></span>

<span data-ttu-id="96aa2-177">不适用于 Web 浏览器内部的 API（例如，访问文件系统、打开套接字和线程处理）将引发 <xref:System.PlatformNotSupportedException>。</span><span class="sxs-lookup"><span data-stu-id="96aa2-177">APIs that aren't applicable inside a web browser (for example, accessing the file system, opening a socket, and threading) throw a <xref:System.PlatformNotSupportedException>.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96aa2-178">其他资源</span><span class="sxs-lookup"><span data-stu-id="96aa2-178">Additional resources</span></span>

* [<span data-ttu-id="96aa2-179">WebAssembly</span><span class="sxs-lookup"><span data-stu-id="96aa2-179">WebAssembly</span></span>](http://webassembly.org/)
* [<span data-ttu-id="96aa2-180">C# 指南</span><span class="sxs-lookup"><span data-stu-id="96aa2-180">C# Guide</span></span>](/dotnet/csharp/)
* <xref:mvc/views/razor>
* [<span data-ttu-id="96aa2-181">HTML</span><span class="sxs-lookup"><span data-stu-id="96aa2-181">HTML</span></span>](https://www.w3.org/html/)