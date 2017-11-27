---
title: "NOTIFY_FILTER 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: NOTIFY_FILTER
api_location: diasymreader.dll
api_type: COM
f1_keywords: NOTIFY_FILTER
helpviewer_keywords: NOTIFY_FILTER enumeration [.NET Framework debugging]
ms.assetid: 4789d08f-8683-45d3-ac30-73d48c61e470
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9db03458aab60d28efe52edfd9830da7862fcb8c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="notifyfilter-enumeration"></a><span data-ttu-id="b8cf4-102">NOTIFY_FILTER 枚举</span><span class="sxs-lookup"><span data-stu-id="b8cf4-102">NOTIFY_FILTER Enumeration</span></span>
<span data-ttu-id="b8cf4-103">标识调试器函数的回调。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-103">Identifies callbacks for debugger functions.</span></span> <span data-ttu-id="b8cf4-104">有关详细信息，请参阅[inotifysource2:: Setnotifyfilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-104">For more information, see the [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8cf4-105">语法</span><span class="sxs-lookup"><span data-stu-id="b8cf4-105">Syntax</span></span>  
  
```  
enum tagNOTIFY_FILTER  
{  
    NOTIFY_FILTER_ONSYNCCALLOUT    = 0x1,  
    NOTIFY_FILTER_ONSYNCCALLENTER  = 0x2,  
    NOTIFY_FILTER_ONSYNCCALLEXIT   = 0x4,  
    NOTIFY_FILTER_ONSYNCCALLRETURN = 0x8,  
    NOTIFY_FILTER_ALLSYNC = NOTIFY_FILTER_ONSYNCCALLOUT | NOTIFY_FILTER_ONSYNCCALLENTER | NOTIFY_FILTER_ONSYNCCALLEXIT | NOTIFY_FILTER_ONSYNCCALLRETURN,  
    NOTIFY_FILTER_ALL              = 0xffffffff,  
    NOTIFY_FILTER_NONE             = 0  
};  
```  
  
## <a name="members"></a><span data-ttu-id="b8cf4-106">成员</span><span class="sxs-lookup"><span data-stu-id="b8cf4-106">Members</span></span>  
  
|<span data-ttu-id="b8cf4-107">成员</span><span class="sxs-lookup"><span data-stu-id="b8cf4-107">Member</span></span>|<span data-ttu-id="b8cf4-108">描述</span><span class="sxs-lookup"><span data-stu-id="b8cf4-108">Description</span></span>|  
|------------|-----------------|  
|`NOTIFY_FILTER_ONSYNCCALLOUT`|<span data-ttu-id="b8cf4-109">指示[inotifysink2:: Onsynccallout](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallout-method.md)应该调用方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-109">Indicates that the [INotifySink2::OnSyncCallOut](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallout-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLENTER`|<span data-ttu-id="b8cf4-110">指示[inotifysink2:: Onsynccallenter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallenter-method.md)应该调用方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-110">Indicates that the [INotifySink2::OnSyncCallEnter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallenter-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLEXIT`|<span data-ttu-id="b8cf4-111">指示[inotifysink2:: Onsynccallexit](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallexit-method.md)应该调用方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-111">Indicates that the [INotifySink2::OnSyncCallExit](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallexit-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLRETURN`|<span data-ttu-id="b8cf4-112">指示[inotifysink2:: Onsynccallreturn](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallreturn-method.md)应该调用方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-112">Indicates that the [INotifySink2::OnSyncCallReturn](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallreturn-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ALLSYNC`|<span data-ttu-id="b8cf4-113">指示所有[INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)应调用方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-113">Indicates that all of the [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) methods should be invoked.</span></span>|  
|`NOTIFY_FILTER_ALL`|<span data-ttu-id="b8cf4-114">激活所有现有和将来的通知。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-114">Activates all existing and future notifications.</span></span>|  
|`NOTIFY_FILTER_NONE`|<span data-ttu-id="b8cf4-115">指示应调用任何通知方法。</span><span class="sxs-lookup"><span data-stu-id="b8cf4-115">Indicates that no notification methods should be invoked.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b8cf4-116">要求</span><span class="sxs-lookup"><span data-stu-id="b8cf4-116">Requirements</span></span>  
 <span data-ttu-id="b8cf4-117">**标头：** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="b8cf4-117">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8cf4-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8cf4-118">See Also</span></span>  
 [<span data-ttu-id="b8cf4-119">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="b8cf4-119">Diagnostics Symbol Store Enumerations</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)
