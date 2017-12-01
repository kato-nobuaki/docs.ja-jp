---
title: "ISymUnmanagedENCUpdate::UpdateSymbolStore2 メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedENCUpdate.UpdateSymbolStore2
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedENCUpdate::UpdateSymbolStore2
helpviewer_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2 method [.NET Framework debugging]
- UpdateSymbolStore2 method [.NET Framework debugging]
ms.assetid: 35588317-6184-485c-ab41-4b15fc1765d9
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 1c0ff6d48bc749b1d8850f94fb1dc1adf3de8e37
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedencupdateupdatesymbolstore2-method"></a><span data-ttu-id="00072-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 メソッド</span><span class="sxs-lookup"><span data-stu-id="00072-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 Method</span></span>
<span data-ttu-id="00072-103">により、コンパイラが行情報が要件を満たしていれば、プログラム データベース (PDB) のストリームから変更されていない関数を省略できます。</span><span class="sxs-lookup"><span data-stu-id="00072-103">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided the line information meets the requirements.</span></span> <span data-ttu-id="00072-104">PDB の行の古い情報と、関数のすべての行の 1 つのデルタは、正しい行情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="00072-104">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00072-105">構文</span><span class="sxs-lookup"><span data-stu-id="00072-105">Syntax</span></span>  
  
```  
HRESULT UpdateSymbolStore2(  
    [in]  IStream      *pIStream,  
    [in]  SYMLINEDELTA* pDeltaLines,  
    [in]  ULONG         cDeltaLines);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="00072-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="00072-106">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="00072-107">[in]ポインター、<xref:IStream>行情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="00072-107">[in] A pointer to an <xref:IStream> that contains the line information.</span></span>  
  
 `pDeltaLines`  
 <span data-ttu-id="00072-108">[in]ポインター、 [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md)に変更された行を含む構造体。</span><span class="sxs-lookup"><span data-stu-id="00072-108">[in] A pointer to a [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure that contains the lines that have changed.</span></span>  
  
 `cDeltaLines`  
 <span data-ttu-id="00072-109">[in]A`ULONG`が変更された行の数を表すです。</span><span class="sxs-lookup"><span data-stu-id="00072-109">[in] A `ULONG` that represents the number of lines that have changed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="00072-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="00072-110">Return Value</span></span>  
 <span data-ttu-id="00072-111">メソッドが成功した場合は S_OK、それ以外の場合、E_FAIL またはその他のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="00072-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00072-112">要件</span><span class="sxs-lookup"><span data-stu-id="00072-112">Requirements</span></span>  
 <span data-ttu-id="00072-113">**ヘッダー:** CorSym.idl、CorSym.h</span><span class="sxs-lookup"><span data-stu-id="00072-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00072-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="00072-114">See Also</span></span>  
 [<span data-ttu-id="00072-115">ISymUnmanagedENCUpdate インターフェイス</span><span class="sxs-lookup"><span data-stu-id="00072-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)