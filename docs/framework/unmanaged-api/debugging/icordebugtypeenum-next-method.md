---
title: ICorDebugTypeEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugTypeEnum::Next
helpviewer_keywords:
- ICorDebugTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugTypeEnum interface [.NET Framework debugging]
ms.assetid: d0fdeba3-c195-4ece-8caf-79b1f40025d2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9812fa4248533ccb898c98082e42e288c091f776
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420579"
---
# <a name="icordebugtypeenumnext-method"></a><span data-ttu-id="f8d07-102">ICorDebugTypeEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="f8d07-102">ICorDebugTypeEnum::Next Method</span></span>
<span data-ttu-id="f8d07-103">获取由指定的"ICorDebugType"实例数`celt`从枚举中的当前位置开始。</span><span class="sxs-lookup"><span data-stu-id="f8d07-103">Gets the number of "ICorDebugType" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8d07-104">语法</span><span class="sxs-lookup"><span data-stu-id="f8d07-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugType *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f8d07-105">参数</span><span class="sxs-lookup"><span data-stu-id="f8d07-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="f8d07-106">[in]数`ICorDebugType`要检索的实例。</span><span class="sxs-lookup"><span data-stu-id="f8d07-106">[in] The number of `ICorDebugType` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="f8d07-107">[out]一个指针，其中每个指向数组`ICorDebugType`对象。</span><span class="sxs-lookup"><span data-stu-id="f8d07-107">[out] An array of pointers, each of which points to an `ICorDebugType` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="f8d07-108">[out]指向数`ICorDebugType`实际返回的实例。</span><span class="sxs-lookup"><span data-stu-id="f8d07-108">[out] Pointer to the number of `ICorDebugType` instances actually returned.</span></span> <span data-ttu-id="f8d07-109">此值可能为 null 如果`celt`是之一。</span><span class="sxs-lookup"><span data-stu-id="f8d07-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8d07-110">要求</span><span class="sxs-lookup"><span data-stu-id="f8d07-110">Requirements</span></span>  
 <span data-ttu-id="f8d07-111">**平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f8d07-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8d07-112">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f8d07-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f8d07-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f8d07-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f8d07-114">**.NET framework 版本：** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8d07-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8d07-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8d07-115">See Also</span></span>  
 
