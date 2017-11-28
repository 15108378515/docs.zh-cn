---
title: "ICorPublish::GetProcess 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorPublish.GetProcess
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorPublish::GetProcess
helpviewer_keywords:
- ICorPublish::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorPublish interface [.NET Framework debugging]
ms.assetid: c5143805-2eb7-45b8-85ed-c8fb34df1084
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 4c5fd66fb3ba5eba1b01451b77472a94bc16dfef
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icorpublishgetprocess-method"></a><span data-ttu-id="f80cd-102">ICorPublish::GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="f80cd-102">ICorPublish::GetProcess Method</span></span>
<span data-ttu-id="f80cd-103">获取[ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)实例，它表示具有指定标识符的过程。</span><span class="sxs-lookup"><span data-stu-id="f80cd-103">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f80cd-104">语法</span><span class="sxs-lookup"><span data-stu-id="f80cd-104">Syntax</span></span>  
  
```  
HRESULT GetProcess(  
    [in] unsigned              pid,   
    [out] ICorPublishProcess   **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f80cd-105">参数</span><span class="sxs-lookup"><span data-stu-id="f80cd-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="f80cd-106">[in]进程的标识符。</span><span class="sxs-lookup"><span data-stu-id="f80cd-106">[in] The identifier of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="f80cd-107">[out]指向的地址的指针`ICorPublishProcess`表示进程的实例。</span><span class="sxs-lookup"><span data-stu-id="f80cd-107">[out] A pointer to the address of an `ICorPublishProcess` instance that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f80cd-108">备注</span><span class="sxs-lookup"><span data-stu-id="f80cd-108">Remarks</span></span>  
 <span data-ttu-id="f80cd-109">`GetProcess`如果进程不存在，或未托管的进程进行调试由当前用户将失败。</span><span class="sxs-lookup"><span data-stu-id="f80cd-109">`GetProcess` fails if the process doesn't exist, or isn't a managed process that can be debugged by the current user.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f80cd-110">要求</span><span class="sxs-lookup"><span data-stu-id="f80cd-110">Requirements</span></span>  
 <span data-ttu-id="f80cd-111">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f80cd-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f80cd-112">**标头：** CorPub.idl、 CorPub.h</span><span class="sxs-lookup"><span data-stu-id="f80cd-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="f80cd-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f80cd-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f80cd-114">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f80cd-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f80cd-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f80cd-115">See Also</span></span>  
 [<span data-ttu-id="f80cd-116">ICorPublish 接口</span><span class="sxs-lookup"><span data-stu-id="f80cd-116">ICorPublish Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-interface.md)
