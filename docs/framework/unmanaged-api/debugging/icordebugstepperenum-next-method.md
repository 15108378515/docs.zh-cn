---
title: ICorDebugStepperEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8bd62e4c5476aacf736f2ddfea008790861d931c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419612"
---
# <a name="icordebugstepperenumnext-method"></a><span data-ttu-id="3aaf4-102">ICorDebugStepperEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="3aaf4-102">ICorDebugStepperEnum::Next Method</span></span>
<span data-ttu-id="3aaf4-103">获取指定的数量的 ICorDebugStepper 实例的枚举，从当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="3aaf4-103">Gets the specified number of ICorDebugStepper instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3aaf4-104">语法</span><span class="sxs-lookup"><span data-stu-id="3aaf4-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3aaf4-105">参数</span><span class="sxs-lookup"><span data-stu-id="3aaf4-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="3aaf4-106">[in]数`ICorDebugStepper`要检索的实例。</span><span class="sxs-lookup"><span data-stu-id="3aaf4-106">[in] The number of `ICorDebugStepper` instances to be retrieved.</span></span>  
  
 `steppers`  
 <span data-ttu-id="3aaf4-107">[out]一个指针，其中每个指向数组`ICorDebugStepper`对象。</span><span class="sxs-lookup"><span data-stu-id="3aaf4-107">[out] An array of pointers, each of which points to an `ICorDebugStepper` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="3aaf4-108">[out]指向数`ICorDebugStepper`实际返回的实例。</span><span class="sxs-lookup"><span data-stu-id="3aaf4-108">[out] Pointer to the number of `ICorDebugStepper` instances actually returned.</span></span> <span data-ttu-id="3aaf4-109">此值可能为 null 如果`celt`是之一。</span><span class="sxs-lookup"><span data-stu-id="3aaf4-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3aaf4-110">要求</span><span class="sxs-lookup"><span data-stu-id="3aaf4-110">Requirements</span></span>  
 <span data-ttu-id="3aaf4-111">**平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3aaf4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3aaf4-112">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3aaf4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3aaf4-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3aaf4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3aaf4-114">**.NET framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3aaf4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
