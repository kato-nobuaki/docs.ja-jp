---
title: "ISymUnmanagedScope インターフェイス"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedScope
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedScope
helpviewer_keywords: ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 3db7a220-cfe9-4810-8ca8-a094bb8e0f5b
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d25d62dd42e3e93124c9a3bd8945be265f192663
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="isymunmanagedscope-interface"></a><span data-ttu-id="b3baa-102">ISymUnmanagedScope インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b3baa-102">ISymUnmanagedScope Interface</span></span>
<span data-ttu-id="b3baa-103">メソッド内での構文のスコープを表します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-103">Represents a lexical scope within a method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b3baa-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-104">Methods</span></span>  
  
|<span data-ttu-id="b3baa-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-105">Method</span></span>|<span data-ttu-id="b3baa-106">説明</span><span class="sxs-lookup"><span data-stu-id="b3baa-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b3baa-107">GetChildren メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-107">GetChildren Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)|<span data-ttu-id="b3baa-108">このスコープの子を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-108">Gets the children of this scope.</span></span>|  
|[<span data-ttu-id="b3baa-109">GetEndOffset メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-109">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getendoffset-method.md)|<span data-ttu-id="b3baa-110">このスコープの終了オフセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-110">Gets the end offset for this scope.</span></span>|  
|[<span data-ttu-id="b3baa-111">GetLocalCount メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-111">GetLocalCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocalcount-method.md)|<span data-ttu-id="b3baa-112">このスコープ内で定義されているローカル変数の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-112">Gets a count of the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="b3baa-113">GetLocals メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-113">GetLocals Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocals-method.md)|<span data-ttu-id="b3baa-114">このスコープ内で定義されているローカル変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-114">Gets the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="b3baa-115">GetMethod メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-115">GetMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getmethod-method.md)|<span data-ttu-id="b3baa-116">このスコープに含まれているメソッドを取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-116">Gets the method that contains this scope.</span></span>|  
|[<span data-ttu-id="b3baa-117">GetNamespaces メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-117">GetNamespaces Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getnamespaces-method.md)|<span data-ttu-id="b3baa-118">このスコープ内で使用されている名前空間を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-118">Gets the namespaces that are being used within this scope.</span></span>|  
|[<span data-ttu-id="b3baa-119">GetParent メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-119">GetParent Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getparent-method.md)|<span data-ttu-id="b3baa-120">このスコープの親スコープを取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-120">Gets the parent scope of this scope.</span></span>|  
|[<span data-ttu-id="b3baa-121">GetStartOffset メソッド</span><span class="sxs-lookup"><span data-stu-id="b3baa-121">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getstartoffset-method.md)|<span data-ttu-id="b3baa-122">このスコープの開始オフセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="b3baa-122">Gets the start offset for this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b3baa-123">要件</span><span class="sxs-lookup"><span data-stu-id="b3baa-123">Requirements</span></span>  
 <span data-ttu-id="b3baa-124">**ヘッダー:** CorSym.idl、CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b3baa-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3baa-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3baa-125">See Also</span></span>  
 [<span data-ttu-id="b3baa-126">シンボル ストア診断インターフェイスします。</span><span class="sxs-lookup"><span data-stu-id="b3baa-126">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="b3baa-127">ISymUnmanagedScope2 インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b3baa-127">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)