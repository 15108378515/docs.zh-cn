---
title: WCF 的 &lt;bookmarkResumptionQueries&gt;
ms.date: 03/30/2017
ms.assetid: ed086712-1dc7-4932-a592-d1116a0155f3
ms.openlocfilehash: 8a83f521e444838b6495221c00211710dd99ab6b
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="ltbookmarkresumptionqueriesgt-of-wcf"></a><span data-ttu-id="e436a-102">WCF 的 &lt;bookmarkResumptionQueries&gt;</span><span class="sxs-lookup"><span data-stu-id="e436a-102">&lt;bookmarkResumptionQueries&gt; of WCF</span></span>
<span data-ttu-id="e436a-103">表示一个查询集合，这些查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="e436a-103">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="e436a-104">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="e436a-104">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="e436a-105">有关跟踪配置文件查询的详细信息，请参阅[跟踪配置文件](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="e436a-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="e436a-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="e436a-106">\<system.serviceModel></span></span>  
<span data-ttu-id="e436a-107">\<跟踪 ></span><span class="sxs-lookup"><span data-stu-id="e436a-107">\<tracking></span></span>  
<span data-ttu-id="e436a-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="e436a-108">\<trackingProfile></span></span>  
<span data-ttu-id="e436a-109">\<工作流 ></span><span class="sxs-lookup"><span data-stu-id="e436a-109">\<workflow></span></span>  
<span data-ttu-id="e436a-110">\<bookmarkResumptionQueries ></span><span class="sxs-lookup"><span data-stu-id="e436a-110">\<bookmarkResumptionQueries></span></span>  
<span data-ttu-id="e436a-111">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="e436a-111">\<bookmarkResumptionQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e436a-112">语法</span><span class="sxs-lookup"><span data-stu-id="e436a-112">Syntax</span></span>  
  
```xml
<tracking>   <trackingProfile name="Name">       <workflow>          <bookmarkResumptionQueries>             <bookmarkResumptionQuery name="String" />          </bookmarkResumptionQueries>       </workflow>   </trackingProfile></tracking>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e436a-113">特性和元素</span><span class="sxs-lookup"><span data-stu-id="e436a-113">Attributes and Elements</span></span>  
 <span data-ttu-id="e436a-114">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e436a-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e436a-115">特性</span><span class="sxs-lookup"><span data-stu-id="e436a-115">Attributes</span></span>  
 <span data-ttu-id="e436a-116">无。</span><span class="sxs-lookup"><span data-stu-id="e436a-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="e436a-117">子元素</span><span class="sxs-lookup"><span data-stu-id="e436a-117">Child Elements</span></span>  
  
|<span data-ttu-id="e436a-118">元素</span><span class="sxs-lookup"><span data-stu-id="e436a-118">Element</span></span>|<span data-ttu-id="e436a-119">描述</span><span class="sxs-lookup"><span data-stu-id="e436a-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e436a-120">\<bookmarkResumptionQuery ></span><span class="sxs-lookup"><span data-stu-id="e436a-120">\<bookmarkResumptionQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/bookmarkresumptionquery.md)|<span data-ttu-id="e436a-121">一个查询，用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="e436a-121">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="e436a-122">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="e436a-122">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e436a-123">父元素</span><span class="sxs-lookup"><span data-stu-id="e436a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="e436a-124">元素</span><span class="sxs-lookup"><span data-stu-id="e436a-124">Element</span></span>|<span data-ttu-id="e436a-125">描述</span><span class="sxs-lookup"><span data-stu-id="e436a-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e436a-126">\<工作流 ></span><span class="sxs-lookup"><span data-stu-id="e436a-126">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="e436a-127">一个配置元素，包含 `activityDefinitionId` 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="e436a-127">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e436a-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="e436a-128">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="e436a-129">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="e436a-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="e436a-130">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="e436a-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
