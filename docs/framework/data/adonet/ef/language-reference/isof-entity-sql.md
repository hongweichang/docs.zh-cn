---
title: ISOF (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5b2b0d34-d0a7-4bcd-baf2-58aa8456d00b
caps.latest.revision: "4"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 78bfcef336ad265b98069ed540f9156cf9cb65bd
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="isof-entity-sql"></a>ISOF (Entity SQL)
确定表达式的类型是否为指定类型或指定类型的某个子类型。  
  
## <a name="syntax"></a>语法  
  
```  
expression IS [ NOT ] OF ( [ ONLY ] type )  
```  
  
## <a name="arguments"></a>自变量  
 `expression`  
 要确定其类型的任何有效查询表达式。  
  
 NOT  
 对 IS OF 的 EDM.Boolean 结果取反。  
  
 ONLY  
 指定仅当 `true` 的类型为 `expression`，而不是其任何子类型时，IS OF 才返回 `type`。  
  
 `type`  
 要针对其测试 `expression` 的类型。 该类型必须由命名空间进行限定。  
  
## <a name="return-value"></a>返回值  
 如果 `true` 的类型为 T 且 T 为基类型或 `expression` 的派生类型，则返回 `type`；如果 `expression` 在运行时为 null，则返回 null；否则返回 `false`。  
  
## <a name="remarks"></a>备注  
 表达式`expression IS NOT OF (type)`和`expression IS NOT OF (ONLY type)`语法上等效于`NOT (expression IS OF (type))`和`NOT (expression IS OF (ONLY type))`分别。  
  
 下表显示了 `IS OF` 运算符在某些典型和非常见模式下的行为。 所有异常都在调用提供程序之前从客户端引发：  
  
|模式|行为|  
|-------------|--------------|  
|null IS OF (EntityType)|引发|  
|null IS OF (ComplexType)|引发|  
|null IS OF (RowType)|引发|  
|TREAT (null AS EntityType) IS OF (EntityType)|返回 DBNull。|  
|TREAT (null AS ComplexType) IS OF (ComplexType)|引发|  
|TREAT (null AS RowType) IS OF (RowType)|引发|  
|EntityType IS OF (EntityType)|返回 true/false|  
|ComplexType IS OF (ComplexType)|引发|  
|RowType IS OF (RowType)|引发|  
  
## <a name="example"></a>示例  
 下面的 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询使用 IS OF 运算符确定一个查询表达式的类型，然后使用 TREAT 运算符将一个类型为 Course 的对象转换为类型为 OnsiteCourse 的对象的集合。 查询基于[School 模型](http://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac)。  
  
 [!code-csharp[DP EntityServices Concepts 2#TREAT_ISOF](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#treat_isof)]  
  
## <a name="see-also"></a>请参阅  
 [实体 SQL 引用](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
