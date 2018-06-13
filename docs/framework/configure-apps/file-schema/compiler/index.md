---
title: 编译器和语言提供程序设置架构
ms.date: 03/30/2017
helpviewer_keywords:
- configuration settings [.NET Framework], compilers
- compiler configuration elements, schema
- compiler configuration elements
- language providers
- compiler configuration settings, schema
- configuration schema [.NET Framework], compiler settings
- language providers, settings schema
- compiler configuration settings
ms.assetid: c020b139-8699-4f0d-9ac9-70d0c5b2a8c8
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: beb38c00c7055d8edfff6f574ec454902e3a9b14
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
ms.locfileid: "32753685"
---
# <a name="compiler-and-language-provider-settings-schema"></a><span data-ttu-id="6d8e3-102">编译器和语言提供程序设置架构</span><span class="sxs-lookup"><span data-stu-id="6d8e3-102">Compiler and Language Provider Settings Schema</span></span>
<span data-ttu-id="6d8e3-103">编译器和语言提供程序设置指定可用语言提供程序的编译器配置元素。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-103">Compiler and language provider settings specify compiler configuration elements for available language providers.</span></span> <span data-ttu-id="6d8e3-104">每个编译器配置元素指定代码提供程序类型名称、编译器参数、支持语言名称以及支持的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-104">Each compiler configuration element specifies the code provider type name, compiler parameters, supported language names, and supported file extensions.</span></span>  
  
 <span data-ttu-id="6d8e3-105">.NET Framework 在计算机配置文件 (Machine.config) 中定义初始编译器设置。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-105">The .NET Framework defines the initial compiler settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="6d8e3-106">开发人员和编译器供应商可以添加新 <xref:System.CodeDom.Compiler.CodeDomProvider> 实现的配置设置。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-106">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="6d8e3-107">使用 <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> 方法，以编程方式枚举计算机上的语言提供程序和编译器配置设置。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-107">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>  
  
 [<span data-ttu-id="6d8e3-108">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="6d8e3-108">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="6d8e3-109">\<system.codedom></span><span class="sxs-lookup"><span data-stu-id="6d8e3-109">\<system.codedom></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)  
  
 [<span data-ttu-id="6d8e3-110">\<compilers></span><span class="sxs-lookup"><span data-stu-id="6d8e3-110">\<compilers></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)  
  
 [<span data-ttu-id="6d8e3-111">\<compiler></span><span class="sxs-lookup"><span data-stu-id="6d8e3-111">\<compiler></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)  
  
|<span data-ttu-id="6d8e3-112">元素</span><span class="sxs-lookup"><span data-stu-id="6d8e3-112">Element</span></span>|<span data-ttu-id="6d8e3-113">描述</span><span class="sxs-lookup"><span data-stu-id="6d8e3-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6d8e3-114">\<system.codedom></span><span class="sxs-lookup"><span data-stu-id="6d8e3-114">\<system.codedom></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|<span data-ttu-id="6d8e3-115">指定可用语言提供程序的编译器配置设置。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-115">Specifies compiler configuration settings for available language providers.</span></span>|  
|[<span data-ttu-id="6d8e3-116">\<compilers></span><span class="sxs-lookup"><span data-stu-id="6d8e3-116">\<compilers></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|<span data-ttu-id="6d8e3-117">编译器配置元素的容器；包含零个或多个 [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-117">Container for compiler configuration elements; contains zero or more [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) elements.</span></span>|  
|[<span data-ttu-id="6d8e3-118">\<compiler></span><span class="sxs-lookup"><span data-stu-id="6d8e3-118">\<compiler></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)|<span data-ttu-id="6d8e3-119">指定语言提供程序的编译器配置属性。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-119">Specifies the compiler configuration attributes for a language provider.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6d8e3-120">示例</span><span class="sxs-lookup"><span data-stu-id="6d8e3-120">Example</span></span>  
 <span data-ttu-id="6d8e3-121">以下示例说明典型的编译器配置元素。</span><span class="sxs-lookup"><span data-stu-id="6d8e3-121">The following example illustrates a typical compiler configuration element.</span></span>  
  
```xml  
<configuration>  
   <system.codedom>  
     <compilers>  
       <!-- zero or more compiler elements -->  
       <compiler  
          language="c#;cs;csharp"  
          extension=".cs"  
          type="Microsoft.CSharp.CSharpCodeProvider, System, Version=1.0.5000.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"  
          compilerOptions=""  
          warningLevel="1" />  
     </compilers>  
   </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6d8e3-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d8e3-122">See Also</span></span>  
 <xref:System.CodeDom.Compiler.CompilerInfo>  
 <xref:System.CodeDom.Compiler.CodeDomProvider>  
 [<span data-ttu-id="6d8e3-123">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="6d8e3-123">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="6d8e3-124">\<compiler> Element</span><span class="sxs-lookup"><span data-stu-id="6d8e3-124">\<compiler> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)
