---
title: "EClrUnhandledException 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- EClrUnhandledException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrUnhandledException
helpviewer_keywords:
- EClrUnhandledException enumeration [.NET Framework hosting]
ms.assetid: d231044e-2b53-4836-93f9-8117ff0e5c3a
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: a8fcc9254499724d94153c445943fdaf78d12a10
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="eclrunhandledexception-enumeration"></a>EClrUnhandledException 枚举
介绍可用于管理用户代码中处理的异常的选项。  
  
## <a name="syntax"></a>语法  
  
```  
typedef enum {  
    eRuntimeDeterminedPolicy,  
    eHostDeterminedPolicy  
} EClrUnhandledException;  
```  
  
## <a name="members"></a>成员  
  
|成员|描述|  
|------------|-----------------|  
|`eRuntimeDeterminedPolicy`|指定的默认行为发生。 该过程被撤销。|  
|`eHostDeterminedPolicy`|指定公共语言运行时 (CLR) 将忽略未经处理的异常，并让宿主确定任何进一步的操作。|  
  
## <a name="remarks"></a>备注  
 若要指定 CLR 行为类似于早期版本，使用`eHostDeterminedPolicy`成员。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** MSCorEE.h  
  
 **库：** MSCorEE.dll  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [EClrFailure 枚举](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)  
 [EClrOperation 枚举](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)  
 [ICLRPolicyManager 接口](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [SetUnhandledExceptionPolicy 方法](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setunhandledexceptionpolicy-method.md)  
 [IHostPolicyManager 接口](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)  
 [承载枚举](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
