---
title: "ICorDebug 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebug
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebug
helpviewer_keywords: ICorDebug interface [.NET Framework debugging]
ms.assetid: 33f431d7-ab1a-494d-8af2-20ab15aba194
topic_type: apiref
caps.latest.revision: "20"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 62a29133252277cbf614a1916af6fa4c6905a920
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icordebug-interface"></a><span data-ttu-id="96030-102">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="96030-102">ICorDebug Interface</span></span>
<span data-ttu-id="96030-103">提供允许开发人员调试应用程序在公共语言运行时 (CLR) 环境中的方法。</span><span class="sxs-lookup"><span data-stu-id="96030-103">Provides methods that allow developers to debug applications in the common language runtime (CLR) environment.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="96030-104">在 Windows 95、 Windows 98 或 Windows ME，或在非 x86 平台 （例如 IA64 和 AMD64） 上不支持混合模式 （托管和本机代码） 调试。</span><span class="sxs-lookup"><span data-stu-id="96030-104">Mixed-mode (managed and native code) debugging is not supported on Windows 95, Windows 98, or Windows ME, or on non-x86 platforms (such as IA64 and AMD64).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="96030-105">方法</span><span class="sxs-lookup"><span data-stu-id="96030-105">Methods</span></span>  
  
|<span data-ttu-id="96030-106">方法</span><span class="sxs-lookup"><span data-stu-id="96030-106">Method</span></span>|<span data-ttu-id="96030-107">描述</span><span class="sxs-lookup"><span data-stu-id="96030-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="96030-108">CanLaunchOrAttach 方法</span><span class="sxs-lookup"><span data-stu-id="96030-108">CanLaunchOrAttach Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-canlaunchorattach-method.md)|<span data-ttu-id="96030-109">确定是否可以在当前的计算机和运行时配置的上下文中启动新的进程或附加到给定的进程。</span><span class="sxs-lookup"><span data-stu-id="96030-109">Determines whether launching a new process or attaching to the given process is possible within the context of the current machine and runtime configuration.</span></span>|  
|[<span data-ttu-id="96030-110">CreateProcess 方法</span><span class="sxs-lookup"><span data-stu-id="96030-110">CreateProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md)|<span data-ttu-id="96030-111">将启动一个进程和调试器的控制之下其主线程。</span><span class="sxs-lookup"><span data-stu-id="96030-111">Launches a process and its primary thread under the control of the debugger.</span></span>|  
|[<span data-ttu-id="96030-112">DebugActiveProcess 方法</span><span class="sxs-lookup"><span data-stu-id="96030-112">DebugActiveProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-debugactiveprocess-method.md)|<span data-ttu-id="96030-113">将调试器附加到现有的进程。</span><span class="sxs-lookup"><span data-stu-id="96030-113">Attaches the debugger to an existing process.</span></span>|  
|[<span data-ttu-id="96030-114">EnumerateProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="96030-114">EnumerateProcesses Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-enumerateprocesses-method.md)|<span data-ttu-id="96030-115">获取正在调试的进程的枚举数。</span><span class="sxs-lookup"><span data-stu-id="96030-115">Gets an enumerator for the processes that are being debugged.</span></span>|  
|[<span data-ttu-id="96030-116">GetProcess 方法</span><span class="sxs-lookup"><span data-stu-id="96030-116">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-getprocess-method.md)|<span data-ttu-id="96030-117">返回"ICorDebugProcess"的对象与给定的进程 id。</span><span class="sxs-lookup"><span data-stu-id="96030-117">Returns the "ICorDebugProcess" object with the given process ID.</span></span>|  
|[<span data-ttu-id="96030-118">Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="96030-118">Initialize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-initialize-method.md)|<span data-ttu-id="96030-119">初始化 `ICorDebug` 对象。</span><span class="sxs-lookup"><span data-stu-id="96030-119">Initializes the `ICorDebug` object.</span></span>|  
|[<span data-ttu-id="96030-120">SetManagedHandler 方法</span><span class="sxs-lookup"><span data-stu-id="96030-120">SetManagedHandler Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-setmanagedhandler-method.md)|<span data-ttu-id="96030-121">指定托管事件的事件处理程序对象。</span><span class="sxs-lookup"><span data-stu-id="96030-121">Specifies the event handler object for managed events.</span></span>|  
|[<span data-ttu-id="96030-122">SetUnmanagedHandler 方法</span><span class="sxs-lookup"><span data-stu-id="96030-122">SetUnmanagedHandler Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-setunmanagedhandler-method.md)|<span data-ttu-id="96030-123">指定非托管事件的事件处理程序对象。</span><span class="sxs-lookup"><span data-stu-id="96030-123">Specifies the event handler object for unmanaged events.</span></span>|  
|[<span data-ttu-id="96030-124">Terminate 方法</span><span class="sxs-lookup"><span data-stu-id="96030-124">Terminate Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-terminate-method.md)|<span data-ttu-id="96030-125">终止`ICorDebug`对象。</span><span class="sxs-lookup"><span data-stu-id="96030-125">Terminates the `ICorDebug` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="96030-126">备注</span><span class="sxs-lookup"><span data-stu-id="96030-126">Remarks</span></span>  
 <span data-ttu-id="96030-127">`ICorDebug`表示调试器进程的事件处理循环。</span><span class="sxs-lookup"><span data-stu-id="96030-127">`ICorDebug` represents an event processing loop for a debugger process.</span></span> <span data-ttu-id="96030-128">调试器必须等待[icordebugmanagedcallback:: Exitprocess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md)从在发布此接口之前正在调试的所有进程的回调。</span><span class="sxs-lookup"><span data-stu-id="96030-128">The debugger must wait for the [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback from all processes being debugged before releasing this interface.</span></span>  
  
 <span data-ttu-id="96030-129">`ICorDebug`对象是控制所有进一步托管调试的初始对象。</span><span class="sxs-lookup"><span data-stu-id="96030-129">The `ICorDebug` object is the initial object to control all further managed debugging.</span></span> <span data-ttu-id="96030-130">在.NET framework 1.0 和 1.1 版中，此对象是`CoClass`从 com。 创建对象</span><span class="sxs-lookup"><span data-stu-id="96030-130">In the .NET Framework versions 1.0 and 1.1, this object was a `CoClass` object created from COM.</span></span> <span data-ttu-id="96030-131">在.NET Framework 2.0 版中，此对象将不再`CoClass`对象。</span><span class="sxs-lookup"><span data-stu-id="96030-131">In the .NET Framework version 2.0, this object is no longer a `CoClass` object.</span></span> <span data-ttu-id="96030-132">它必须由创建[CreateDebuggingInterfaceFromVersion](../../../../docs/framework/unmanaged-api/hosting/createdebugginginterfacefromversion-function.md)函数，这是多区别版本。</span><span class="sxs-lookup"><span data-stu-id="96030-132">It must be created by the [CreateDebuggingInterfaceFromVersion](../../../../docs/framework/unmanaged-api/hosting/createdebugginginterfacefromversion-function.md) function, which is more version-aware.</span></span> <span data-ttu-id="96030-133">此新的创建函数使客户端可以获取的特定实现`ICorDebug`，这也模拟了调试 API 的特定版本。</span><span class="sxs-lookup"><span data-stu-id="96030-133">This new creation function enables clients to get a specific implementation of `ICorDebug`, which also emulates a specific version of the debugging API.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="96030-134">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="96030-134">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96030-135">要求</span><span class="sxs-lookup"><span data-stu-id="96030-135">Requirements</span></span>  
 <span data-ttu-id="96030-136">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="96030-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96030-137">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="96030-137">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="96030-138">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="96030-138">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="96030-139">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96030-139">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96030-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="96030-140">See Also</span></span>  
 [<span data-ttu-id="96030-141">调试接口</span><span class="sxs-lookup"><span data-stu-id="96030-141">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)