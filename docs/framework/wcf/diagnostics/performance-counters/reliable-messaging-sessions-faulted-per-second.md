---
title: Reliable Messaging Sessions Faulted Per Second（每秒出错的可靠消息会话数）
ms.date: 03/30/2017
ms.assetid: 8f8ca2eb-1be4-4b6a-aa78-fcd3ee145fe8
ms.openlocfilehash: c77d6a5f12dcce15dba94e2f63025a219ebcc6fd
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2018
ms.locfileid: "43873986"
---
# <a name="reliable-messaging-sessions-faulted-per-second"></a><span data-ttu-id="f086f-102">Reliable Messaging Sessions Faulted Per Second（每秒出错的可靠消息会话数）</span><span class="sxs-lookup"><span data-stu-id="f086f-102">Reliable Messaging Sessions Faulted Per Second</span></span>
<span data-ttu-id="f086f-103">计数器名称：Reliable Messaging Sessions Faulted Per Second（每秒出错的可靠消息会话数）。</span><span class="sxs-lookup"><span data-stu-id="f086f-103">Counter Name: Reliable Messaging Sessions Faulted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="f086f-104">描述</span><span class="sxs-lookup"><span data-stu-id="f086f-104">Description</span></span>  
 <span data-ttu-id="f086f-105">此服务每秒出错的可靠消息会话的数目。</span><span class="sxs-lookup"><span data-stu-id="f086f-105">Number of reliable messaging sessions that are faulted in this service in a second.</span></span>  
  
 <span data-ttu-id="f086f-106">此计数器为性能计数器类型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)，使用以下公式计算其值。</span><span class="sxs-lookup"><span data-stu-id="f086f-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="f086f-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="f086f-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
