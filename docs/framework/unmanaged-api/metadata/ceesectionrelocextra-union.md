---
title: "CeeSectionRelocExtra 共用体"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CeeSectionRelocExtra Union
api_location: mscoree.dll
api_type: COM
f1_keywords: CeeSectionRelocExtra
helpviewer_keywords: CeeSectionRelocExtra union [.NET Framework metadata]
ms.assetid: d9568cf6-7f98-4cd6-ab36-0a2bd509afcc
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c5b584ced996b31be6656082af3f64a19b1f223c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="c7a55-102">CeeSectionRelocExtra 共用体</span><span class="sxs-lookup"><span data-stu-id="c7a55-102">CeeSectionRelocExtra Union</span></span>
<span data-ttu-id="c7a55-103">によって使用されるアドレスのオフセットを表す、 [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)セクションを再配置するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="c7a55-103">Represents an address offset that is used by the [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7a55-104">構文</span><span class="sxs-lookup"><span data-stu-id="c7a55-104">Syntax</span></span>  
  
```  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="c7a55-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="c7a55-105">Members</span></span>  
  
|<span data-ttu-id="c7a55-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="c7a55-106">Member</span></span>|<span data-ttu-id="c7a55-107">説明</span><span class="sxs-lookup"><span data-stu-id="c7a55-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="c7a55-108">セクションの上位アドレスを調整します。</span><span class="sxs-lookup"><span data-stu-id="c7a55-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c7a55-109">要件</span><span class="sxs-lookup"><span data-stu-id="c7a55-109">Requirements</span></span>  
 <span data-ttu-id="c7a55-110">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="c7a55-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7a55-111">**ヘッダー:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c7a55-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c7a55-112">**ライブラリ:** MsCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7a55-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c7a55-113">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7a55-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7a55-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7a55-114">See Also</span></span>  
 [<span data-ttu-id="c7a55-115">メタデータ共用体</span><span class="sxs-lookup"><span data-stu-id="c7a55-115">Metadata Unions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-unions.md)