---
title: "ICorProfilerCallback::RemotingServerInvocationReturned メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.RemotingServerInvocationReturned
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::RemotingServerInvocationReturned
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned method [.NET Framework profiling]
- RemotingServerInvocationReturned method [.NET Framework profiling]
ms.assetid: a4de6805-e159-4280-99e5-3390c86166d0
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: e4b1becc695b001402482256ef6adad3b339495e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackremotingserverinvocationreturned-method"></a><span data-ttu-id="7ce15-102">ICorProfilerCallback::RemotingServerInvocationReturned メソッド</span><span class="sxs-lookup"><span data-stu-id="7ce15-102">ICorProfilerCallback::RemotingServerInvocationReturned Method</span></span>
<span data-ttu-id="7ce15-103">リモート メソッド呼び出しの要求に応答でメソッドを呼び出すプロセスを完了したことをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="7ce15-103">Notifies the profiler that the process has finished invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ce15-104">構文</span><span class="sxs-lookup"><span data-stu-id="7ce15-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationReturned();  
```  
  
## <a name="requirements"></a><span data-ttu-id="7ce15-105">要件</span><span class="sxs-lookup"><span data-stu-id="7ce15-105">Requirements</span></span>  
 <span data-ttu-id="7ce15-106">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="7ce15-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7ce15-107">**ヘッダー** : CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7ce15-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7ce15-108">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7ce15-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7ce15-109">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7ce15-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ce15-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ce15-110">See Also</span></span>  
 [<span data-ttu-id="7ce15-111">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7ce15-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)