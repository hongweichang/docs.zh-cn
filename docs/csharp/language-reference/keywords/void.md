---
title: "void（C# 参考）"
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- void_CSharpKeyword
- void
helpviewer_keywords:
- void keyword [C#]
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: a71cac30132417abce60cdde54322b5f2067d39d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="void-c-reference"></a>void（C# 参考）
当用作一种方法的返回类型时，`void` 将指定该方法不返回值。

方法的参数列表中不允许有 `void`。 无参数且不返回值的方法的声明方式如下：

```csharp
public void SampleMethod()
{
    // Body of the method.
}
```

`void` 还可用于在不安全的上下文中将指针声明为未知类型。 有关详细信息，请参阅[指针类型](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)。

`void` 是 .NET Framework <xref:System.Void?displayProperty=nameWithType> 类型的别名。

## <a name="c-language-specification"></a>C# 语言规范
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>请参阅
 [C# 参考](../../../csharp/language-reference/index.md)  
 [C# 编程指南](../../../csharp/programming-guide/index.md)  
 [C# 关键字](../../../csharp/language-reference/keywords/index.md)  
 [引用类型](../../../csharp/language-reference/keywords/reference-types.md)  
 [值类型](../../../csharp/language-reference/keywords/value-types.md)  
 [方法](../../../csharp/programming-guide/classes-and-structs/methods.md)  
 [不安全代码和指针](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
