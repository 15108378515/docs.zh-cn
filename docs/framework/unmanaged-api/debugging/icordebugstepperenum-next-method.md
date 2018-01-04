---
title: "ICorDebugStepperEnum::Next 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugStepperEnum.Next
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 42a7a2323e25d149f5c8e2a1c3d2278557571938
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugstepperenumnext-method"></a><span data-ttu-id="205d3-102">ICorDebugStepperEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="205d3-102">ICorDebugStepperEnum::Next Method</span></span>
<span data-ttu-id="205d3-103">获取指定的数量的 ICorDebugStepper 实例的枚举，从当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="205d3-103">Gets the specified number of ICorDebugStepper instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="205d3-104">语法</span><span class="sxs-lookup"><span data-stu-id="205d3-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="205d3-105">参数</span><span class="sxs-lookup"><span data-stu-id="205d3-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="205d3-106">[in]数`ICorDebugStepper`要检索的实例。</span><span class="sxs-lookup"><span data-stu-id="205d3-106">[in] The number of `ICorDebugStepper` instances to be retrieved.</span></span>  
  
 `steppers`  
 <span data-ttu-id="205d3-107">[out]一个指针，其中每个指向数组`ICorDebugStepper`对象。</span><span class="sxs-lookup"><span data-stu-id="205d3-107">[out] An array of pointers, each of which points to an `ICorDebugStepper` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="205d3-108">[out]指向数`ICorDebugStepper`实际返回的实例。</span><span class="sxs-lookup"><span data-stu-id="205d3-108">[out] Pointer to the number of `ICorDebugStepper` instances actually returned.</span></span> <span data-ttu-id="205d3-109">此值可能为 null 如果`celt`是之一。</span><span class="sxs-lookup"><span data-stu-id="205d3-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="205d3-110">惠?</span><span class="sxs-lookup"><span data-stu-id="205d3-110">Requirements</span></span>  
 <span data-ttu-id="205d3-111">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="205d3-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="205d3-112">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="205d3-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="205d3-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="205d3-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="205d3-114">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="205d3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
