---
title: "ICorDebugEval2::NewStringWithLength 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugEval2.NewStringWithLength
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugEval2::NewStringWithLength
helpviewer_keywords:
- NewStringWithLength method [.NET Framework debugging]
- ICorDebugEval2::NewStringWithLength method [.NET Framework debugging]
ms.assetid: d5f54a34-6335-4708-b407-a756ec70fab4
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: b794482e491dc9825b0311cf1731d159082bd1f1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugeval2newstringwithlength-method"></a><span data-ttu-id="ad976-102">ICorDebugEval2::NewStringWithLength 方法</span><span class="sxs-lookup"><span data-stu-id="ad976-102">ICorDebugEval2::NewStringWithLength Method</span></span>
<span data-ttu-id="ad976-103">具有指定内容创建指定的长度的字符串。</span><span class="sxs-lookup"><span data-stu-id="ad976-103">Creates a string of the specified length, with the specified contents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad976-104">语法</span><span class="sxs-lookup"><span data-stu-id="ad976-104">Syntax</span></span>  
  
```  
HRESULT NewStringWithLength (  
    [in] LPCWSTR               string,  
    [in] UINT                  uiLength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad976-105">参数</span><span class="sxs-lookup"><span data-stu-id="ad976-105">Parameters</span></span>  
 `string`  
 <span data-ttu-id="ad976-106">[in]指向的字符串值的指针。</span><span class="sxs-lookup"><span data-stu-id="ad976-106">[in] A pointer to the string value.</span></span>  
  
 `uiLength`  
 <span data-ttu-id="ad976-107">[in]字符串的长度。</span><span class="sxs-lookup"><span data-stu-id="ad976-107">[in] Length of the string.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ad976-108">备注</span><span class="sxs-lookup"><span data-stu-id="ad976-108">Remarks</span></span>  
 <span data-ttu-id="ad976-109">如果字符串的尾随 null 字符预计会在托管的字符串中，调用方`NewStringWithLength`方法必须确保字符串长度包含尾随的 null 字符。</span><span class="sxs-lookup"><span data-stu-id="ad976-109">If the string's trailing null character is expected to be in the managed string, the caller of the `NewStringWithLength` method must ensure that the string length includes the trailing null character.</span></span>  
  
 <span data-ttu-id="ad976-110">始终在线程当前执行的应用程序域中创建字符串。</span><span class="sxs-lookup"><span data-stu-id="ad976-110">The string is always created in the application domain in which the thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad976-111">要求</span><span class="sxs-lookup"><span data-stu-id="ad976-111">Requirements</span></span>  
 <span data-ttu-id="ad976-112">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ad976-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad976-113">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ad976-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ad976-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ad976-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ad976-115">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad976-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
