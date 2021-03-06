---
title: ICorDebugILFrame4 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame4
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 1e739183-3e05-49e5-846f-4075256e41de
topic_type:
- apiref
ms.openlocfilehash: 7f1c5d7a6fdae3e4c5a66c9aa4a82911105f4597
ms.sourcegitcommit: 13e79efdbd589cad6b1de634f5d6b1262b12ab01
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2020
ms.locfileid: "76788503"
---
# <a name="icordebugilframe4-interface"></a>ICorDebugILFrame4 接口
[仅在 .NET Framework 4.5.2 及更高版本中受支持]  
  
 提供使你能够访问中间语言 (IL) 代码的堆栈帧中的局部变量和代码的方法。 一个用于指定调试器是否可以访问在探查器 ReJIT 检测中添加的变量和代码的参数。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[EnumerateLocalVariablesEx 方法](icordebugilframe4-enumeratelocalvariablesex-method.md)|返回在当前帧中可用的局部变量的列表。|  
|[GetCodeEx 方法](icordebugilframe4-getcodeex-method.md)|返回此堆栈帧正在运行的代码。|  
|[GetLocalVariableEx 方法](icordebugilframe4-getlocalvariableex-method.md)|返回 IL 帧中的局部变量的值。|  
  
## <a name="remarks"></a>备注  
 除了[EnumerateLocalVariables](icordebugilframe-enumeratelocalvariables-method.md)、 [GetCode](icordebugframe-getcode-method.md)和[GetLocalVariable](icordebugilframe-getlocalvariable-method.md)方法提供的功能外，这些方法还提供功能。 每个方法都包含一个 `flags` 参数，该参数可指定探查器的 ReJIT 请求定义的附加局部变量或代码是否可见。  
  
## <a name="requirements"></a>需求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>另请参阅

- [调试接口](debugging-interfaces.md)
- [调试](index.md)
