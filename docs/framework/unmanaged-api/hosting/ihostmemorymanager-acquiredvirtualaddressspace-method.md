---
title: "IHostMemoryManager::AcquiredVirtualAddressSpace メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostMemoryManager.AcquiredVirtualAddressSpace
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostMemoryManager::AcquiredVirtualAddressSpace
helpviewer_keywords:
- IHostMemoryManager::AcquiredVirtualAddressSpace method [.NET Framework hosting]
- AcquiredVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: ef2f83c2-127e-4c38-8385-306c03cd2167
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 480dba9257c34af2cd1bc11aba4a07a4fbbe1162
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="ihostmemorymanageracquiredvirtualaddressspace-method"></a><span data-ttu-id="f3250-102">IHostMemoryManager::AcquiredVirtualAddressSpace メソッド</span><span class="sxs-lookup"><span data-stu-id="f3250-102">IHostMemoryManager::AcquiredVirtualAddressSpace Method</span></span>
<span data-ttu-id="f3250-103">共通言語ランタイム (CLR) が、オペレーティング システムから指定されたメモリを取得したことをホストに通知します。</span><span class="sxs-lookup"><span data-stu-id="f3250-103">Notifies the host that the common language runtime (CLR) has acquired the specified memory from the operating system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3250-104">構文</span><span class="sxs-lookup"><span data-stu-id="f3250-104">Syntax</span></span>  
  
```  
HRESULT AcquiredVirtualAddressSpace(  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f3250-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3250-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="f3250-106">[in]メモリの開始アドレス。</span><span class="sxs-lookup"><span data-stu-id="f3250-106">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="f3250-107">[in]メモリのバイト単位のサイズ。</span><span class="sxs-lookup"><span data-stu-id="f3250-107">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f3250-108">コメント</span><span class="sxs-lookup"><span data-stu-id="f3250-108">Remarks</span></span>  
 <span data-ttu-id="f3250-109">`AcquiredVirtualAddressSpace`メソッドはコールバック メソッドであり、ホスト アプリケーションの作成者によって実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3250-109">The `AcquiredVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="f3250-110">これは、CLR によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3250-110">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3250-111">要件</span><span class="sxs-lookup"><span data-stu-id="f3250-111">Requirements</span></span>  
 <span data-ttu-id="f3250-112">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="f3250-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3250-113">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f3250-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f3250-114">**ライブラリ:** MSCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="f3250-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f3250-115">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3250-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3250-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3250-116">See Also</span></span>  
 [<span data-ttu-id="f3250-117">IHostMemoryManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f3250-117">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)