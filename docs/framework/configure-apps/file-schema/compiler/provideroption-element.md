---
title: "&lt;providerOption&gt;元素"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- provideroption
helpviewer_keywords:
- <provideroption> element
- providerOptions
- provideroption element
ms.assetid: 014f2e0b-c0b5-4fc4-92d3-73f02978b2a1
caps.latest.revision: 
author: mcleblanc
ms.author: markl
manager: markl
ms.workload:
- dotnet
ms.openlocfilehash: f28b7b43f2f782744a0dbc81bd0b91bbbcd8abba
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="ltprovideroptiongt-element"></a>&lt;providerOption&gt;元素
指定语言提供程序的编译器版本属性。  
  
 \<配置元素 >  
\<system.codedom Element>  
\<编译器元素 >  
\<编译器 > 元素  
\<providerOption > 元素  
  
## <a name="syntax"></a>语法  
  
```xml  
<providerOption  
  name="option-name"  
  value="option-value"  
/>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|`name`|必需的特性。<br /><br /> 指定的选项; 的名称例如，"CompilerVersion"。|  
|`value`|必需的特性。<br /><br /> 指定选项; 的值例如，"v3.5"。|  
  
### <a name="child-elements"></a>子元素  
 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<configuration> 元素](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|公共语言运行库和 .NET Framework 应用程序所使用的每个配置文件中的根元素。|  
|[\<system.codedom> Element](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|指定可用语言提供程序的编译器配置设置。|  
|[\<编译器 > 元素](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|编译器配置元素，则容器包含零个或多`<compiler>`元素。|  
|[\<compiler> Element](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)|指定语言提供程序的编译器配置属性。|  
  
## <a name="remarks"></a>备注  
 在.NET Framework 版本 3.5 中，代码文档对象模型 (CodeDOM) 的代码提供程序可以支持提供程序特定选项使用`<providerOption>`元素。  
  
 .NET Framework 3.5 包含更新的.NET Framework 2.0 程序集，并提供包含新类型的新版本 3.5 程序集。 Microsoft C# 和 Visual Basic 的代码提供程序包含在.NET Framework 2.0 程序集，但已更新，以支持版本 3.5 编译器。 默认情况下，更新的代码提供程序生成为版本 2.0 编译器的代码。 你可以使用`<providerOption>`元素以将目标编译器版本更改为 3.5。 若要执行此操作，指定"CompilerVersion"`name`属性和"v3.5"为`value`属性。 你必须在前面与小写的"v"的版本号。  
  
 你可以进行版本规范全局添加`<providerOption>`到.NET Framework 2.0 Machine.config 或根 Web.config 文件的元素。 如果您更新默认编译器版本为 3.5 在 Machine.config 文件中，你可以将其更改回为 2.0 基于每个应用程序使用`<providerOption>`应用程序配置文件中的元素。  
  
 CodeDOM 代码提供程序实施者可以处理通过提供的构造函数的自定义选项`providerOptions`类型的参数<xref:System.Collections.Generic.IDictionary%602>。  
  
## <a name="example"></a>示例  
 下面的示例演示如何指定应使用 3.5 版的 C# 代码提供程序。  
  
```xml  
<configuration>  
  <system.codedom>  
    <compilers>  
      <!-- zero or more compiler elements -->  
      <compiler  
        language="c#;cs;csharp"  
        extension=".cs"  
        type="Microsoft.CSharp.CSharpCodeProvider, System,   
          Version=2.0.3600.0, Culture=neutral,   
          PublicKeyToken=b77a5c561934e089"  
        compilerOptions="/optimize"  
        warningLevel="1" >  
          <providerOption  
            name="CompilerVersion"  
            value="v3.5" />  
      </compiler>  
    </compilers>  
  </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a>请参阅  
 <xref:System.CodeDom.Compiler.CompilerInfo>  
 <xref:System.CodeDom.Compiler.CodeDomProvider>  
 [配置文件架构](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [\<编译器 > 元素](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)  
 [指定完全限定的类型名称](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)  
 [编译器进行编译 （ASP.NET 设置架构） 使用的编译器元素](http://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e)
