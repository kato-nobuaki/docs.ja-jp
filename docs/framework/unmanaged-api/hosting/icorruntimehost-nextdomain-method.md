---
title: "ICorRuntimeHost::NextDomain メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorRuntimeHost.NextDomain
api_location: mscoree.dll
api_type: COM
f1_keywords: ICorRuntimeHost::NextDomain
helpviewer_keywords:
- ICorRuntimeHost::NextDomain method [.NET Framework hosting]
- NextDomain method [.NET Framework hosting]
ms.assetid: fe07a05b-f6d6-44b5-ab01-b9a6eb15c350
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: de7d90ed55cf27aa0b1679b5e55d9f28902b6aeb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="icorruntimehostnextdomain-method"></a><span data-ttu-id="364fe-102">ICorRuntimeHost::NextDomain メソッド</span><span class="sxs-lookup"><span data-stu-id="364fe-102">ICorRuntimeHost::NextDomain Method</span></span>
<span data-ttu-id="364fe-103">列挙体の次のドメインへのインターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="364fe-103">Gets an interface pointer to the next domain in the enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="364fe-104">構文</span><span class="sxs-lookup"><span data-stu-id="364fe-104">Syntax</span></span>  
  
```  
HRESULT NextDomain (  
    [in] HCORENUM hEnum,  
    [out] void** pAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="364fe-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="364fe-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="364fe-106">[in]列挙子を呼び出すことによって取得された[EnumDomains](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-enumdomains-method.md)です。</span><span class="sxs-lookup"><span data-stu-id="364fe-106">[in] The enumerator that was obtained through a call to [EnumDomains](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-enumdomains-method.md).</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="364fe-107">[out]インターフェイス ポインター、<xref:System._AppDomain?displayProperty=nameWithType>以上ドメインがない場合は、列挙型、または null の場合の次のドメインを表す型。</span><span class="sxs-lookup"><span data-stu-id="364fe-107">[out] An interface pointer to the <xref:System._AppDomain?displayProperty=nameWithType> type that represents the next domain in the enumeration, or null, if no more domains exist.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="364fe-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="364fe-108">Return Value</span></span>  
  
|<span data-ttu-id="364fe-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="364fe-109">HRESULT</span></span>|<span data-ttu-id="364fe-110">説明</span><span class="sxs-lookup"><span data-stu-id="364fe-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="364fe-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="364fe-111">S_OK</span></span>|<span data-ttu-id="364fe-112">操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="364fe-112">The operation was successful.</span></span>|  
|<span data-ttu-id="364fe-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="364fe-113">S_FALSE</span></span>|<span data-ttu-id="364fe-114">完了するには、操作が失敗したか、列挙体のない複数のドメインがあります。</span><span class="sxs-lookup"><span data-stu-id="364fe-114">The operation failed to complete, or there are no more domains in the enumeration.</span></span>|  
|<span data-ttu-id="364fe-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="364fe-115">E_FAIL</span></span>|<span data-ttu-id="364fe-116">未知の致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="364fe-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="364fe-117">メソッドには、E_FAIL が返されます、共通言語ランタイム (CLR) は、プロセスで使用可能なできなくします。</span><span class="sxs-lookup"><span data-stu-id="364fe-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="364fe-118">Api をホストに以降の呼び出しでは、HOST_E_CLRNOTAVAILABLE を返します。</span><span class="sxs-lookup"><span data-stu-id="364fe-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="364fe-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="364fe-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="364fe-120">CLR が、プロセスに読み込まれていませんまたは CLR は、状態をマネージ コードを実行またはできないの呼び出しは正常に処理します。</span><span class="sxs-lookup"><span data-stu-id="364fe-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="364fe-121">要件</span><span class="sxs-lookup"><span data-stu-id="364fe-121">Requirements</span></span>  
 <span data-ttu-id="364fe-122">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="364fe-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="364fe-123">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="364fe-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="364fe-124">**ライブラリ:** MSCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="364fe-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="364fe-125">**.NET framework のバージョン:** 1.0、1.1</span><span class="sxs-lookup"><span data-stu-id="364fe-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="364fe-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="364fe-126">See Also</span></span>  
 <xref:System._AppDomain>  
 <xref:System.AppDomain>  
 [<span data-ttu-id="364fe-127">ICorRuntimeHost インターフェイス</span><span class="sxs-lookup"><span data-stu-id="364fe-127">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)