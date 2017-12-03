---
title: '&lt;persistableType&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 56443902885e191d93897096e55742f7665ba00a
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="c6086-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="c6086-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="c6086-103">指定所有永久类型。</span><span class="sxs-lookup"><span data-stu-id="c6086-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="c6086-104">\<系统。ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="c6086-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="c6086-105">\<comContracts ></span><span class="sxs-lookup"><span data-stu-id="c6086-105">\<comContracts></span></span>  
<span data-ttu-id="c6086-106">\<comContract ></span><span class="sxs-lookup"><span data-stu-id="c6086-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6086-107">语法</span><span class="sxs-lookup"><span data-stu-id="c6086-107">Syntax</span></span>  
  
```xml  
<comContracts>  
  <comContract>  
      <persistableTypes>  
         <persistableType id="string"  
            name="string">  
         </persistableType>  
      </persistableTypes>  
  </comContract>  
</comContracts>  
```  
  
## <a name="type"></a><span data-ttu-id="c6086-108">类型</span><span class="sxs-lookup"><span data-stu-id="c6086-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c6086-109">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c6086-109">Attributes and Elements</span></span>  
 <span data-ttu-id="c6086-110">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6086-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c6086-111">特性</span><span class="sxs-lookup"><span data-stu-id="c6086-111">Attributes</span></span>  
  
|<span data-ttu-id="c6086-112">特性</span><span class="sxs-lookup"><span data-stu-id="c6086-112">Attribute</span></span>|<span data-ttu-id="c6086-113">描述</span><span class="sxs-lookup"><span data-stu-id="c6086-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c6086-114">id</span><span class="sxs-lookup"><span data-stu-id="c6086-114">id</span></span>|<span data-ttu-id="c6086-115">一个必需的属性，包含一个指定持久类型唯一标识符的字符串。</span><span class="sxs-lookup"><span data-stu-id="c6086-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="c6086-116">name</span><span class="sxs-lookup"><span data-stu-id="c6086-116">name</span></span>|<span data-ttu-id="c6086-117">一个可选属性，包含一个指定持久类型名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="c6086-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c6086-118">子元素</span><span class="sxs-lookup"><span data-stu-id="c6086-118">Child Elements</span></span>  
 <span data-ttu-id="c6086-119">无</span><span class="sxs-lookup"><span data-stu-id="c6086-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c6086-120">父元素</span><span class="sxs-lookup"><span data-stu-id="c6086-120">Parent Elements</span></span>  
  
|<span data-ttu-id="c6086-121">元素</span><span class="sxs-lookup"><span data-stu-id="c6086-121">Element</span></span>|<span data-ttu-id="c6086-122">描述</span><span class="sxs-lookup"><span data-stu-id="c6086-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c6086-123">\<persistableTypes ></span><span class="sxs-lookup"><span data-stu-id="c6086-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="c6086-124">一个 `persistableType` 元素集合。</span><span class="sxs-lookup"><span data-stu-id="c6086-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c6086-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6086-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>  
 [<span data-ttu-id="c6086-126">\<comContracts ></span><span class="sxs-lookup"><span data-stu-id="c6086-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="c6086-127">与 COM + 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="c6086-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="c6086-128">如何： 配置 COM + 服务设置</span><span class="sxs-lookup"><span data-stu-id="c6086-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
