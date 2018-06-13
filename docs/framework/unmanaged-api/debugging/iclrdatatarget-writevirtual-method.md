---
title: ICLRDataTarget::WriteVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.WriteVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::WriteVirtual
helpviewer_keywords:
- ICLRDataTarget::WriteVirtual method [.NET Framework debugging]
- WriteVirtual method [.NET Framework debugging]
ms.assetid: d627e8b7-a605-40ac-b9bb-da9a3f1b66d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e55bc18c7a41e235d1ba6274067c45c26dc7262a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405443"
---
# <a name="iclrdatatargetwritevirtual-method"></a><span data-ttu-id="5dddf-102">ICLRDataTarget::WriteVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="5dddf-102">ICLRDataTarget::WriteVirtual Method</span></span>
<span data-ttu-id="5dddf-103">从指定的缓冲区写入指定的虚拟内存地址的数据。</span><span class="sxs-lookup"><span data-stu-id="5dddf-103">Writes data from the specified buffer to the specified virtual memory address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5dddf-104">语法</span><span class="sxs-lookup"><span data-stu-id="5dddf-104">Syntax</span></span>  
  
```  
HRESULT WriteVirtual (  
    [in] CLRDATA_ADDRESS    address,  
    [in, size_is(bytesRequested)]   
        BYTE                *buffer,  
    [in] ULONG32            bytesRequested,  
    [out] ULONG32           *bytesWritten  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5dddf-105">参数</span><span class="sxs-lookup"><span data-stu-id="5dddf-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="5dddf-106">[in]将存储的虚拟内存地址 CLRDATA_ADDRESS。</span><span class="sxs-lookup"><span data-stu-id="5dddf-106">[in] A CLRDATA_ADDRESS that stores the virtual memory address.</span></span>  
  
 `buffer`  
 <span data-ttu-id="5dddf-107">[in]指向存储的数据要写入的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="5dddf-107">[in] A pointer to a buffer that stores the data to be written.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="5dddf-108">[in]要写入的字节数。</span><span class="sxs-lookup"><span data-stu-id="5dddf-108">[in] The number of bytes to be written.</span></span>  
  
 `bytesWritten`  
 <span data-ttu-id="5dddf-109">[out]指向实际写入的字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="5dddf-109">[out] A pointer to the actual number of bytes that were written.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5dddf-110">要求</span><span class="sxs-lookup"><span data-stu-id="5dddf-110">Requirements</span></span>  
 <span data-ttu-id="5dddf-111">**平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5dddf-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5dddf-112">**标头：** ClrData.idl、 ClrData.h</span><span class="sxs-lookup"><span data-stu-id="5dddf-112">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="5dddf-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5dddf-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5dddf-114">**.NET framework 版本：** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5dddf-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5dddf-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="5dddf-115">See Also</span></span>  
 [<span data-ttu-id="5dddf-116">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="5dddf-116">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
