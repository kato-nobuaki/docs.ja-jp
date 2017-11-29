---
title: "ICorProfilerCallback4::GetReJITParameters メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback4.GetReJITParameters
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback4::GetReJITParameters
helpviewer_keywords:
- ICorProfilerCallback4::GetReJITParameters method [.NET Framework profiling]
- GetReJITParameters method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 0e9bfe07-9f20-498c-b568-9017c8f6056c
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: acecbe10fd79394b27e6264c337d584d9fb259b1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback4getrejitparameters-method"></a><span data-ttu-id="612d2-102">ICorProfilerCallback4::GetReJITParameters メソッド</span><span class="sxs-lookup"><span data-stu-id="612d2-102">ICorProfilerCallback4::GetReJITParameters Method</span></span>
<span data-ttu-id="612d2-103">新しい再コンパイルされたメソッドの本体の代替コード生成フラグを設定するコード プロファイラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="612d2-103">Allows the code profiler to set alternate code generation flags for a new recompiled method body.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="612d2-104">構文</span><span class="sxs-lookup"><span data-stu-id="612d2-104">Syntax</span></span>  
  
```  
HRESULT GetReJITParameters(     [in] ModuleID moduleId,     [in] mdMethodDef methodId,     [in] ICorProfilerFunctionControl *pFunctionControl);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="612d2-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="612d2-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="612d2-106">[in]CLR の JIT 再コンパイルのパラメーターが必要なメソッドを含むモジュール。</span><span class="sxs-lookup"><span data-stu-id="612d2-106">[in] The module that contains the method for which the CLR needs JIT recompilation parameters.</span></span>  
  
 `methodId`  
 <span data-ttu-id="612d2-107">[in]`MethodDef`の CLR の JIT 再コンパイルのパラメーターが必要なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="612d2-107">[in] The `MethodDef` of the method for which the CLR needs JIT recompilation parameters.</span></span>  
  
 `pFunctionControl`  
 <span data-ttu-id="612d2-108">[in]ポインター、 [ICorProfilerFunctionControl](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-interface.md)プロファイラーを使用して再コンパイルされるメソッドの JIT 再コンパイルの情報を提供するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="612d2-108">[in] A pointer to an [ICorProfilerFunctionControl](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-interface.md) interface that the profiler can use to provide JIT recompilation information for the method being recompiled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="612d2-109">コメント</span><span class="sxs-lookup"><span data-stu-id="612d2-109">Remarks</span></span>  
 <span data-ttu-id="612d2-110">CLR の問題、`GetReJITParameters`コールバック プロファイラーは、特定のメソッドを再コンパイルするためのパラメーターを指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="612d2-110">The CLR issues a `GetReJITParameters` callback so that the profiler can specify the parameters for recompiling a given method.</span></span> <span data-ttu-id="612d2-111">`GetReJITParameters`関数ごとのコールバックは 1 回だけ発行されます。 その関数のすべてのインスタンスに、プロファイラーによって指定されたパラメーターを適用します。</span><span class="sxs-lookup"><span data-stu-id="612d2-111">The `GetReJITParameters` callback is issued only once per function; the parameters supplied by the profiler apply to all instances of that function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="612d2-112">要件</span><span class="sxs-lookup"><span data-stu-id="612d2-112">Requirements</span></span>  
 <span data-ttu-id="612d2-113">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="612d2-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="612d2-114">**ヘッダー** : CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="612d2-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="612d2-115">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="612d2-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="612d2-116">**.NET framework のバージョン:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="612d2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="612d2-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="612d2-117">See Also</span></span>  
 [<span data-ttu-id="612d2-118">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="612d2-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="612d2-119">ICorProfilerCallback4 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="612d2-119">ICorProfilerCallback4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)  
 [<span data-ttu-id="612d2-120">JITCompilationStarted メソッド</span><span class="sxs-lookup"><span data-stu-id="612d2-120">JITCompilationStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcompilationstarted-method.md)  
 [<span data-ttu-id="612d2-121">ReJITCompilationStarted メソッド</span><span class="sxs-lookup"><span data-stu-id="612d2-121">ReJITCompilationStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-rejitcompilationstarted-method.md)