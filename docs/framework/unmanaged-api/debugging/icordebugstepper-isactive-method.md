---
title: "ICorDebugStepper::IsActive メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugStepper.IsActive
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugStepper::IsActive
helpviewer_keywords:
- IsActive method, ICorDebugStepper interface [.NET Framework debugging]
- ICorDebugStepper::IsActive method [.NET Framework debugging]
ms.assetid: 8b35e7a9-b40e-40a9-8d8e-b82e823fc575
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 25e4b59c59ee4340c14da22143f49c645e1dcc7b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugstepperisactive-method"></a><span data-ttu-id="05359-102">ICorDebugStepper::IsActive メソッド</span><span class="sxs-lookup"><span data-stu-id="05359-102">ICorDebugStepper::IsActive Method</span></span>
<span data-ttu-id="05359-103">この ICorDebugStepper が現在の手順を実行中かどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="05359-103">Gets a value that indicates whether this ICorDebugStepper is currently executing a step.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05359-104">構文</span><span class="sxs-lookup"><span data-stu-id="05359-104">Syntax</span></span>  
  
```  
HRESULT IsActive (  
    [out] BOOL   *pbActive  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="05359-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="05359-105">Parameters</span></span>  
 `pbActive`  
 <span data-ttu-id="05359-106">[out]返します`true`ステッパは、ステップ; を現在実行中の場合、それを返します`false`です。</span><span class="sxs-lookup"><span data-stu-id="05359-106">[out] Returns `true` if the stepper is currently executing a step; otherwise, returns `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="05359-107">コメント</span><span class="sxs-lookup"><span data-stu-id="05359-107">Remarks</span></span>  
 <span data-ttu-id="05359-108">デバッガーが受信するまで、ステップのアクションがアクティブなまま、 [icordebugmanagedcallback::stepcomplete](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-stepcomplete-method.md)を呼び出すと、自動的に非アクティブ化するステッパです。</span><span class="sxs-lookup"><span data-stu-id="05359-108">Any step action remains active until the debugger receives a [ICorDebugManagedCallback::StepComplete](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-stepcomplete-method.md) call, which automatically deactivates the stepper.</span></span> <span data-ttu-id="05359-109">ステッパ可能性がありますも非アクティブ化処理の途中で呼び出すことによって[icordebugstepper::deactivate](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-deactivate-method.md)状態に達すると、コールバックの前にします。</span><span class="sxs-lookup"><span data-stu-id="05359-109">A stepper may also be deactivated prematurely by calling [ICorDebugStepper::Deactivate](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-deactivate-method.md) before the callback condition is reached.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05359-110">要件</span><span class="sxs-lookup"><span data-stu-id="05359-110">Requirements</span></span>  
 <span data-ttu-id="05359-111">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="05359-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05359-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="05359-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="05359-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="05359-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="05359-114">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05359-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>