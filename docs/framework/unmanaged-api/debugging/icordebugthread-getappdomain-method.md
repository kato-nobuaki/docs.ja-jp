---
title: "ICorDebugThread::GetAppDomain メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread.GetAppDomain
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread::GetAppDomain
helpviewer_keywords:
- GetAppDomain method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetAppDomain method [.NET Framework debugging]
ms.assetid: 415b3d34-8b35-4b60-a318-140646cc83f8
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d23ba10d40cb8b1f06cc5b24299de6445f45feaa
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugthreadgetappdomain-method"></a><span data-ttu-id="0e9d9-102">ICorDebugThread::GetAppDomain メソッド</span><span class="sxs-lookup"><span data-stu-id="0e9d9-102">ICorDebugThread::GetAppDomain Method</span></span>
<span data-ttu-id="0e9d9-103">この ICorDebugThread を現在実行しているアプリケーション ドメインへのインターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="0e9d9-103">Gets an interface pointer to the application domain in which this ICorDebugThread is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e9d9-104">構文</span><span class="sxs-lookup"><span data-stu-id="0e9d9-104">Syntax</span></span>  
  
```  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0e9d9-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e9d9-105">Parameters</span></span>  
 `ppAppDomain`  
 <span data-ttu-id="0e9d9-106">[out]現在このスレッドが実行しているアプリケーション ドメインを表す ICorDebugAppDomain オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0e9d9-106">[out] A pointer to an ICorDebugAppDomain object that represents the application domain in which this thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e9d9-107">要件</span><span class="sxs-lookup"><span data-stu-id="0e9d9-107">Requirements</span></span>  
 <span data-ttu-id="0e9d9-108">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="0e9d9-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e9d9-109">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0e9d9-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0e9d9-110">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0e9d9-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0e9d9-111">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e9d9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>