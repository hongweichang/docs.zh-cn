---
title: "ForwardTranslateAccelerator 函数 （WPF 非托管 API 参考）"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- cpp
api_name:
- ForwardTranslateAccelerator
api_location:
- PresentationHost_v0400.dll
ms.assetid: fff47a86-9d9f-4176-9530-10e1876e393f
caps.latest.revision: 
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: cca9c78eaf13e04d22fce9f61ce4a7ab9ee09769
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="forwardtranslateaccelerator-function-wpf-unmanaged-api-reference"></a>ForwardTranslateAccelerator 函数 （WPF 非托管 API 参考）
此 API 支持的 Windows Presentation Foundation (WPF) 基础结构，不宜在代码中直接使用。  
  
 Windows Presentation Foundation (WPF) 基础结构用于 windows 管理。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ForwardTranslateAccelerator(  
   MSG* pMsg,   
   VARIANT_BOOL appUnhandled  
)  
```  
  
#### <a name="parameters"></a>参数  
 pMsg  
 一条消息指向的指针。  
  
 appUnhandled  
 `true`当应用程序已被授予一个机会处理输入的消息，但不是处理它;否则为`false`。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[.NET Framework 系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **DLL:**  
  
 在.NET Framework 3.0 和 3.5: PresentationHostDLL.dll  
  
 在.NET Framework 4 及更高版本： PresentationHost_v0400.dll  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [WPF 非托管 API 参考](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
