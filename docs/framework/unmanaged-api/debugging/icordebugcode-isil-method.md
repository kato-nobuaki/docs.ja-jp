---
title: "ICorDebugCode::IsIL メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugCode.IsIL
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugCode::IsIL
helpviewer_keywords:
- ICorDebugCode::IsIL method [.NET Framework debugging]
- IsIL method [.NET Framework debugging]
ms.assetid: 132ef8cc-d938-43f3-b8f2-e3b97c0ceb33
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 07b0490e322c70763a37b86fbb02e2f8b99bd768
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugcodeisil-method"></a><span data-ttu-id="2b00c-102">ICorDebugCode::IsIL メソッド</span><span class="sxs-lookup"><span data-stu-id="2b00c-102">ICorDebugCode::IsIL Method</span></span>
<span data-ttu-id="2b00c-103">この"ICorDebugCode"が Microsoft intermediate language (MSIL) にコンパイルされたコードを表すかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2b00c-103">Gets a value that indicates whether this "ICorDebugCode" represents code that was compiled in Microsoft intermediate language (MSIL).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b00c-104">構文</span><span class="sxs-lookup"><span data-stu-id="2b00c-104">Syntax</span></span>  
  
```  
HRESULT IsIL (  
    [out] BOOL       *pbIL  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2b00c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2b00c-105">Parameters</span></span>  
 `pbIL`  
 <span data-ttu-id="2b00c-106">[out]`true`この`ICorDebugCode`、それ以外の MSIL にコンパイルされるコードを表す`false`です。</span><span class="sxs-lookup"><span data-stu-id="2b00c-106">[out] `true` if this `ICorDebugCode` represents code that was compiled in MSIL; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b00c-107">要件</span><span class="sxs-lookup"><span data-stu-id="2b00c-107">Requirements</span></span>  
 <span data-ttu-id="2b00c-108">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="2b00c-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b00c-109">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2b00c-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2b00c-110">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2b00c-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2b00c-111">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b00c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b00c-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b00c-112">See Also</span></span>  
 