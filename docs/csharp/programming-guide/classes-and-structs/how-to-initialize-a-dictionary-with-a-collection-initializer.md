---
title: 如何：使用集合初始值设定项初始化字典（C# 编程指南）
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- collection initializers [C#], with Dictionary
ms.assetid: 25283922-f8ee-40dc-a639-fac30804ec71
caps.latest.revision: ''
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 8b8de5fb85a839d52ad00ad552ef823d9817e9b7
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/26/2018
---
# <a name="how-to-initialize-a-dictionary-with-a-collection-initializer-c-programming-guide"></a>如何：使用集合初始值设定项初始化字典（C# 编程指南）
<xref:System.Collections.Generic.Dictionary`2> 包含键/值对集合。 其 <xref:System.Collections.Generic.Dictionary`2.Add*> 方法采用两个参数，一个用于键，一个用于值。 若要初始化 <xref:System.Collections.Generic.Dictionary`2> 或其 `Add` 方法采用多个参数的任何集合，请将每组参数括在大括号中，如下面的示例中所示。  
  
## <a name="example"></a>示例  
 在下面的代码示例中，使用类型 `StudentName` 的实例初始化 <xref:System.Collections.Generic.Dictionary`2>。  
  
 [!code-csharp[csProgGuideLINQ#34](../../../csharp/programming-guide/arrays/codesnippet/CSharp/how-to-initialize-a-dictionary-with-a-collection-initializer_1.cs)]  
  
 请注意，集合中的每个元素有两对大括号。 最内层的大括号中的是 `StudentName` 的对象初始值设定项，最外层的大括号中的是要添加到 `students`<xref:System.Collections.Generic.Dictionary`2> 的键/值对的初始值设定项。 最后，字典的整个集合初始值设定项被括在大括号中。  
  
## <a name="compiling-the-code"></a>编译代码  
 若要运行此代码，请将该类复制并粘贴到已经在 [!INCLUDE[vs_current_short](~/includes/vs-current-short-md.md)] 中创建的 Visual C# 控制台应用程序项目中。 默认情况下，此项目面向 [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] 3.5 版，并且具有对 System.Core.dll 的引用和一个用于 System.Linq 的 using 指令。 如果项目中缺少其中一个或多个要求，则可以手动添加它们。  
  
## <a name="see-also"></a>另请参阅  
 [C# 编程指南](../../../csharp/programming-guide/index.md)  
 [对象和集合初始值设定项](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)
