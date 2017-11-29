---
title: "ICorDebugFunction3::GetActiveReJitRequestILCode メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: ICorDebugFunction3.GetActiveReJitRequestILCode
api_location: mscordbi.dll
api_type: COM
ms.assetid: 88584574-ade5-45b2-9778-489ed5c4dd7f
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6459297a2a04728ca87801bfc8484acec384a45c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugfunction3getactiverejitrequestilcode-method"></a><span data-ttu-id="d9060-102">ICorDebugFunction3::GetActiveReJitRequestILCode メソッド</span><span class="sxs-lookup"><span data-stu-id="d9060-102">ICorDebugFunction3::GetActiveReJitRequestILCode Method</span></span>
<span data-ttu-id="d9060-103">[.NET Framework 4.5.2 以降のバージョンでのみでサポート]</span><span class="sxs-lookup"><span data-stu-id="d9060-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="d9060-104">インターフェイス ポインターを取得、 [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)アクティブな ReJIT 要求から、IL を格納しています。</span><span class="sxs-lookup"><span data-stu-id="d9060-104">Gets an interface pointer to an [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9060-105">構文</span><span class="sxs-lookup"><span data-stu-id="d9060-105">Syntax</span></span>  
  
```cpp
HRESULT GetActiveReJitRequestILCode(  
   ICorDebugILCode **ppReJitedILCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d9060-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9060-106">Parameters</span></span>  
 `ppReJitedILCode`  
 <span data-ttu-id="d9060-107">アクティブな ReJIT 要求からの、IL へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9060-107">A pointer to the IL from an active ReJIT request.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9060-108">コメント</span><span class="sxs-lookup"><span data-stu-id="d9060-108">Remarks</span></span>  
 <span data-ttu-id="d9060-109">この `ICorDebugFunction3` オブジェクトによって表示されるメソッドがアクティブな ReJIT 要求を持っている場合、`ppReJitedILCode` は IL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d9060-109">If the method represented by this `ICorDebugFunction3` object has an active ReJIT request, `ppReJitedILCode` returns a pointer to its IL.</span></span> <span data-ttu-id="d9060-110">一般的なケースでは、そのアクティブな要求がないかどうか`ppReJitedILCode`は**null**です。</span><span class="sxs-lookup"><span data-stu-id="d9060-110">If there is no active request, which is a common case, then `ppReJitedILCode` is **null**.</span></span>  
  
 <span data-ttu-id="d9060-111">実行が戻った後にだけ、ReJIT 要求がアクティブになった、 [icorprofilercallback 4::getrejitparameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md)メソッドの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="d9060-111">A ReJIT request becomes active just after execution returns from the [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) method call.</span></span> <span data-ttu-id="d9060-112">これは、まだ JIT コンパイルされていない可能性があり、スレッドはコードの元のバージョンで実行中の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d9060-112">It may not yet be JIT-compiled, and threads may still be executing in the original version of the code.</span></span> <span data-ttu-id="d9060-113">プロファイラーの呼び出し中に、ReJIT 要求がアクティブで、 [icorprofilerinfo 4::requestrevert](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-requestrevert-method.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="d9060-113">A ReJIT request becomes inactive during the profiler's call to the [ICorProfilerInfo4::RequestRevert](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-requestrevert-method.md) method.</span></span> <span data-ttu-id="d9060-114">LI が戻された後であっても、スレッドは JIT 再コンパイル (ReJIT) されたコードで実行中の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d9060-114">Even after the IL is reverted, a thread can still be executing in the JIT-recompiled (ReJIT) code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9060-115">要件</span><span class="sxs-lookup"><span data-stu-id="d9060-115">Requirements</span></span>  
 <span data-ttu-id="d9060-116">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="d9060-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9060-117">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d9060-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d9060-118">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d9060-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d9060-119">**.NET framework のバージョン:**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9060-119">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9060-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9060-120">See Also</span></span>  
 [<span data-ttu-id="d9060-121">ICorDebugFunction3 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d9060-121">ICorDebugFunction3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-interface.md)  
 [<span data-ttu-id="d9060-122">デバッグのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="d9060-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="d9060-123">ReJIT: ハウツー ガイド</span><span class="sxs-lookup"><span data-stu-id="d9060-123">ReJIT: A How-To Guide</span></span>](http://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)