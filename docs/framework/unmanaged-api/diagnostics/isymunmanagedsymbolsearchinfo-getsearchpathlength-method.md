---
title: "ISymUnmanagedSymbolSearchInfo::GetSearchPathLength 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ISymUnmanagedSymbolSearchInfo.GetSearchPathLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength
helpviewer_keywords:
- GetSearchPathLength method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength method [.NET Framework debugging]
ms.assetid: 274e73cf-8333-47ba-ac12-70214e2b0112
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 3525e33dc311ee87e05ea467197090378e420fa5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpathlength-method"></a><span data-ttu-id="cfa6c-102">ISymUnmanagedSymbolSearchInfo::GetSearchPathLength 方法</span><span class="sxs-lookup"><span data-stu-id="cfa6c-102">ISymUnmanagedSymbolSearchInfo::GetSearchPathLength Method</span></span>
<span data-ttu-id="cfa6c-103">获取搜索路径长度。</span><span class="sxs-lookup"><span data-stu-id="cfa6c-103">Gets the search path length.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfa6c-104">语法</span><span class="sxs-lookup"><span data-stu-id="cfa6c-104">Syntax</span></span>  
  
```  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cfa6c-105">参数</span><span class="sxs-lookup"><span data-stu-id="cfa6c-105">Parameters</span></span>  
 `pcchPath`  
 <span data-ttu-id="cfa6c-106">[out]指向的指针`ULONG32`接收大小，以字符为单位，包含搜索路径长度所需的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="cfa6c-106">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the search path length.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cfa6c-107">返回值</span><span class="sxs-lookup"><span data-stu-id="cfa6c-107">Return Value</span></span>  
 <span data-ttu-id="cfa6c-108">如果该方法成功; 则为 S_OK否则为 E_FAIL 或某些其他错误代码。</span><span class="sxs-lookup"><span data-stu-id="cfa6c-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cfa6c-109">惠?</span><span class="sxs-lookup"><span data-stu-id="cfa6c-109">Requirements</span></span>  
 <span data-ttu-id="cfa6c-110">**标头：** CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="cfa6c-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfa6c-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="cfa6c-111">See Also</span></span>  
 [<span data-ttu-id="cfa6c-112">ISymUnmanagedSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="cfa6c-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
