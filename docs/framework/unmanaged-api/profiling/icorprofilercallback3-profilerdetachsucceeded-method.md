---
title: ICorProfilerCallback3::ProfilerDetachSucceeded 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3.ProfilerDetachSucceeded Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3::ProfilerDetachSucceeded
helpviewer_keywords:
- ProfilerDetachSucceeded method [.NET Framework profiling]
- ICorProfilerCallback3::ProfilerDetachSucceeded method [.NET Framework profiling]
ms.assetid: 05164966-16ce-4cc9-a530-43a640c00711
topic_type:
- apiref
ms.openlocfilehash: b96a8930c24275546b0aac9fa650cf5447ef4ef2
ms.sourcegitcommit: b11efd71c3d5ce3d9449c8d4345481b9f21392c6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2020
ms.locfileid: "76865410"
---
# <a name="icorprofilercallback3profilerdetachsucceeded-method"></a>ICorProfilerCallback3::ProfilerDetachSucceeded 方法
通知探查器公共语言运行时 (CLR) 将要卸载探查器 DLL。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ProfilerDetachSucceeded();  
```  
  
## <a name="return-value"></a>返回值  
 将忽略来自此回调的返回值。  
  
## <a name="remarks"></a>备注  
 在所有线程均退出探查器的代码之后，发出`ProfilerDetachSucceeded` 回调。 当调用此方法时，探查器应执行任何不适合用于其析构函数的的最后执行的任务，例如通知其 UI 或日志记录组件。 但是，探查器不能在此回调期间（如[ICorProfilerInfo](icorprofilerinfo-interface.md)或 `IMetaData*` 接口）对 CLR 提供的接口调用函数。  
  
 CLR 在 Windows 应用程序事件日志中创建条目，用于表示分离操作成功。  
  
 探查器从此回调返回后，CLR 将释放探查器对象并卸载探查器 DLL。 因此，探查器不可执行任何会导致探查器 DLL 从此回调返回后其内部进行执行的操作。 例如，它不能创建线程或注册计时器回调。  
  
## <a name="requirements"></a>需求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>另请参阅

- [元数据接口](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [ICorProfilerInfo3 接口](icorprofilerinfo3-interface.md)
- [Profiling 接口](profiling-interfaces.md)
- [分析](index.md)
