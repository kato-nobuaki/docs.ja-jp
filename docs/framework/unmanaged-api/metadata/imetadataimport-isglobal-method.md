---
title: "IMetaDataImport::IsGlobal メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.IsGlobal
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::IsGlobal
helpviewer_keywords:
- IsGlobal method [.NET Framework metadata]
- IMetaDataImport::IsGlobal method [.NET Framework metadata]
ms.assetid: 44cf6908-f555-4ae8-b2cf-24bd974bf2fe
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 09f7d437e09063bf621990dec4f2903139af8238
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportisglobal-method"></a><span data-ttu-id="c09c7-102">IMetaDataImport::IsGlobal メソッド</span><span class="sxs-lookup"><span data-stu-id="c09c7-102">IMetaDataImport::IsGlobal Method</span></span>
<span data-ttu-id="c09c7-103">指定したメタデータ トークンによって表されるフィールド、メソッド、または型がグローバル スコープを保持しているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c09c7-103">Gets a value indicating whether the field, method, or type represented by the specified metadata token has global scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c09c7-104">構文</span><span class="sxs-lookup"><span data-stu-id="c09c7-104">Syntax</span></span>  
  
```  
HRESULT IsGlobal (  
   [in]  mdToken     pd,  
   [out] int         *pbGlobal  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c09c7-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c09c7-105">Parameters</span></span>  
 `pd`  
 <span data-ttu-id="c09c7-106">[in]型、フィールド、またはメソッドを表すメタデータ トークン。</span><span class="sxs-lookup"><span data-stu-id="c09c7-106">[in] A metadata token that represents a type, field, or method.</span></span>  
  
 `pbGlobal`  
 <span data-ttu-id="c09c7-107">[out] の場合は、1 オブジェクトがグローバル スコープです。それ以外の場合、0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="c09c7-107">[out] 1 if the object has global scope; otherwise, 0 (zero).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c09c7-108">要件</span><span class="sxs-lookup"><span data-stu-id="c09c7-108">Requirements</span></span>  
 <span data-ttu-id="c09c7-109">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="c09c7-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c09c7-110">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c09c7-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c09c7-111">**ライブラリ:** MsCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="c09c7-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c09c7-112">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c09c7-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c09c7-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="c09c7-113">See Also</span></span>  
 [<span data-ttu-id="c09c7-114">IMetaDataImport インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c09c7-114">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="c09c7-115">IMetaDataImport2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c09c7-115">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)