---
title: "ICLRHostProtectionManager::SetProtectedCategories メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRHostProtectionManager.SetProtectedCategories
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRHostProtectionManager::SetProtectedCategories
helpviewer_keywords:
- SetProtectedCategories method [.NET Framework hosting]
- ICLRHostProtectionManager::SetProtectedCategories method [.NET Framework hosting]
ms.assetid: fa21dc7b-5da7-440b-b59e-9180e5181f9d
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 984a88a9b75a03f421f1dd3f834665fee932876a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="iclrhostprotectionmanagersetprotectedcategories-method"></a><span data-ttu-id="a26d6-102">ICLRHostProtectionManager::SetProtectedCategories メソッド</span><span class="sxs-lookup"><span data-stu-id="a26d6-102">ICLRHostProtectionManager::SetProtectedCategories Method</span></span>
<span data-ttu-id="a26d6-103">部分的に信頼されたコードでの実行を禁止するマネージ型とメンバーのカテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="a26d6-103">Specifies which categories of managed types and members should be blocked from running in partially trusted code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a26d6-104">構文</span><span class="sxs-lookup"><span data-stu-id="a26d6-104">Syntax</span></span>  
  
```  
HRESULT SetProtectedCategories (  
    [in] EApiCategories  categories  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a26d6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a26d6-105">Parameters</span></span>  
 `categories`  
 <span data-ttu-id="a26d6-106">[in]組み合わせた[EApiCategories](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)部分的に信頼されたコードでの実行を禁止するマネージ型とメンバーのカテゴリを示す値。</span><span class="sxs-lookup"><span data-stu-id="a26d6-106">[in] A combination of [EApiCategories](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md) values, indicating which categories of managed types and members should be blocked from running in partially trusted code.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a26d6-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="a26d6-107">Return Value</span></span>  
  
|<span data-ttu-id="a26d6-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a26d6-108">HRESULT</span></span>|<span data-ttu-id="a26d6-109">説明</span><span class="sxs-lookup"><span data-stu-id="a26d6-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a26d6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a26d6-110">S_OK</span></span>|<span data-ttu-id="a26d6-111">`SetProtectedCategories`正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="a26d6-111">`SetProtectedCategories` returned successfully.</span></span>|  
|<span data-ttu-id="a26d6-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a26d6-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a26d6-113">共通言語ランタイム (CLR) が、プロセスに読み込まれていませんまたは CLR は、状態をマネージ コードを実行またはできないの呼び出しは正常に処理します。</span><span class="sxs-lookup"><span data-stu-id="a26d6-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a26d6-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a26d6-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a26d6-115">呼び出しがタイムアウトしました。</span><span class="sxs-lookup"><span data-stu-id="a26d6-115">The call timed out.</span></span>|  
|<span data-ttu-id="a26d6-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a26d6-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a26d6-117">呼び出し元は、ロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="a26d6-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a26d6-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a26d6-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a26d6-119">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="a26d6-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a26d6-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a26d6-120">E_FAIL</span></span>|<span data-ttu-id="a26d6-121">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a26d6-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a26d6-122">メソッドには、E_FAIL が返された、後に、CLR はプロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a26d6-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a26d6-123">メソッドのホストに以降の呼び出しでは、HOST_E_CLRNOTAVAILABLE を返します。</span><span class="sxs-lookup"><span data-stu-id="a26d6-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a26d6-124">コメント</span><span class="sxs-lookup"><span data-stu-id="a26d6-124">Remarks</span></span>  
 <span data-ttu-id="a26d6-125">各`EApiCategories`値がマネージ型とメンバーの一覧を参照します。</span><span class="sxs-lookup"><span data-stu-id="a26d6-125">Each `EApiCategories` value refers to a list of managed types and members.</span></span> <span data-ttu-id="a26d6-126">`EApiCategories`列挙型、および`SetProtectedCategories`メソッドは直接関連マネージに<xref:System.Security.Permissions.HostProtectionAttribute>によって記述されたカテゴリに対応する機能を公開するマネージ型とメンバーを示すために使用されるクラス`EApiCategories`です。</span><span class="sxs-lookup"><span data-stu-id="a26d6-126">The `EApiCategories` enumeration and the `SetProtectedCategories` method are directly related to the managed <xref:System.Security.Permissions.HostProtectionAttribute> class, which is used to mark managed types and members that expose capabilities corresponding to the categories described by `EApiCategories`.</span></span> <span data-ttu-id="a26d6-127">詳細については、次を参照してください。<xref:System.Security.Permissions.HostProtectionAttribute>と<xref:System.Security.Permissions.HostProtectionResource>列挙体は、に直接対応`EApiCategories`です。</span><span class="sxs-lookup"><span data-stu-id="a26d6-127">For more information, see <xref:System.Security.Permissions.HostProtectionAttribute> and the <xref:System.Security.Permissions.HostProtectionResource> enumeration, which directly corresponds to `EApiCategories`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a26d6-128">要件</span><span class="sxs-lookup"><span data-stu-id="a26d6-128">Requirements</span></span>  
 <span data-ttu-id="a26d6-129">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="a26d6-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a26d6-130">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a26d6-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a26d6-131">**ライブラリ:** MSCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="a26d6-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a26d6-132">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a26d6-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a26d6-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a26d6-133">See Also</span></span>  
 <xref:System.Security.Permissions.HostProtectionAttribute>  
 <xref:System.Security.Permissions.HostProtectionResource>  
 [<span data-ttu-id="a26d6-134">EApiCategories 列挙型</span><span class="sxs-lookup"><span data-stu-id="a26d6-134">EApiCategories Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)  
 [<span data-ttu-id="a26d6-135">ICLRControl インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a26d6-135">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="a26d6-136">ICLRHostProtectionManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a26d6-136">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)