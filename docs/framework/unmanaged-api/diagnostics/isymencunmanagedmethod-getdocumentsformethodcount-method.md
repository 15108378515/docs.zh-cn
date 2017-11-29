---
title: "ISymENCUnmanagedMethod::GetDocumentsForMethodCount 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymENCUnmanagedMethod.GetDocumentsForMethodCount
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymENCUnmanagedMethod::GetDocumentsForMethodCount
helpviewer_keywords:
- GetDocumentsForMethodCount method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount method [.NET Framework debugging]
ms.assetid: cc1a823a-3ff3-4a33-b641-96edc93d2b17
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 49b849ced80d526ed529bad1eaa766d5a2a19d51
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="isymencunmanagedmethodgetdocumentsformethodcount-method"></a><span data-ttu-id="30e10-102">ISymENCUnmanagedMethod::GetDocumentsForMethodCount 方法</span><span class="sxs-lookup"><span data-stu-id="30e10-102">ISymENCUnmanagedMethod::GetDocumentsForMethodCount Method</span></span>
<span data-ttu-id="30e10-103">获取此方法的行中的文档数。</span><span class="sxs-lookup"><span data-stu-id="30e10-103">Gets the number of documents that this method has lines in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30e10-104">语法</span><span class="sxs-lookup"><span data-stu-id="30e10-104">Syntax</span></span>  
  
```  
HRESULT GetDocumentsForMethodCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="30e10-105">参数</span><span class="sxs-lookup"><span data-stu-id="30e10-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="30e10-106">[out]指向的指针`ULONG32`接收包含文档所需的缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="30e10-106">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the documents.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="30e10-107">返回值</span><span class="sxs-lookup"><span data-stu-id="30e10-107">Return Value</span></span>  
 <span data-ttu-id="30e10-108">如果该方法成功; 则为 S_OK否则为 E_FAIL 或某些其他错误代码。</span><span class="sxs-lookup"><span data-stu-id="30e10-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30e10-109">要求</span><span class="sxs-lookup"><span data-stu-id="30e10-109">Requirements</span></span>  
 <span data-ttu-id="30e10-110">**标头：** CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="30e10-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30e10-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30e10-111">See Also</span></span>  
 [<span data-ttu-id="30e10-112">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="30e10-112">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
