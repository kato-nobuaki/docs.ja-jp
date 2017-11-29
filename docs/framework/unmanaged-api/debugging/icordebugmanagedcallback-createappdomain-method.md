---
title: "ICorDebugManagedCallback::CreateAppDomain メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback.CreateAppDomain
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback::CreateAppDomain
helpviewer_keywords:
- CreateAppDomain method [.NET Framework debugging]
- ICorDebugManagedCallback::CreateAppDomain method [.NET Framework debugging]
ms.assetid: 48d410d7-6749-4125-a8fd-f9562c7088e9
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6d2cb90f780d4d680e6c81ebd9579341d5a3b1fa
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugmanagedcallbackcreateappdomain-method"></a><span data-ttu-id="5948a-102">ICorDebugManagedCallback::CreateAppDomain メソッド</span><span class="sxs-lookup"><span data-stu-id="5948a-102">ICorDebugManagedCallback::CreateAppDomain Method</span></span>
<span data-ttu-id="5948a-103">アプリケーション ドメインが作成されたことをデバッガーに通知します。</span><span class="sxs-lookup"><span data-stu-id="5948a-103">Notifies the debugger that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5948a-104">構文</span><span class="sxs-lookup"><span data-stu-id="5948a-104">Syntax</span></span>  
  
```  
HRESULT CreateAppDomain (  
    [in] ICorDebugProcess   *pProcess,  
    [in] ICorDebugAppDomain *pAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5948a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5948a-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="5948a-106">[in]アプリケーション ドメインが作成されたプロセスを表す ICorDebugProcess オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5948a-106">[in] A pointer to an ICorDebugProcess object that represents the process in which the application domain was created.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="5948a-107">[in]ICorDebugAppDomain を表すオブジェクトが作成されたアプリケーション ドメインへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5948a-107">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that has been created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5948a-108">要件</span><span class="sxs-lookup"><span data-stu-id="5948a-108">Requirements</span></span>  
 <span data-ttu-id="5948a-109">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="5948a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5948a-110">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5948a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5948a-111">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5948a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5948a-112">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5948a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5948a-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="5948a-113">See Also</span></span>  
 [<span data-ttu-id="5948a-114">ICorDebugManagedCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5948a-114">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)