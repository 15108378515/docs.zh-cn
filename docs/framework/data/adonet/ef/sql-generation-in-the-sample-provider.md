---
title: "示例提供程序中的 SQL 生成"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 58a49f7bf5d385466810a3c59bda748ef66d5840
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="sql-generation-in-the-sample-provider"></a><span data-ttu-id="7fc9b-102">示例提供程序中的 SQL 生成</span><span class="sxs-lookup"><span data-stu-id="7fc9b-102">SQL Generation in the Sample Provider</span></span>
<span data-ttu-id="7fc9b-103">[实体框架示例提供程序](http://go.microsoft.com/fwlink/?LinkId=180616)演示的 ADO.NET 数据提供程序支持的新组件[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]。</span><span class="sxs-lookup"><span data-stu-id="7fc9b-103">The [Entity Framework Sample Provider](http://go.microsoft.com/fwlink/?LinkId=180616) demonstrates the new components of ADO.NET Data Providers that support the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span>  <span data-ttu-id="7fc9b-104">它使用 SQL Server 2005 数据库，并实现为 System.Data.SqlClient ADO.NET 2.0 数据提供程序的一个包装。</span><span class="sxs-lookup"><span data-stu-id="7fc9b-104">It works with a SQL Server 2005 database and is implemented as a wrapper for the System.Data.SqlClient ADO.NET 2.0 Data Provider.</span></span>  
  
 <span data-ttu-id="7fc9b-105">该示例提供程序的 SQL 生成模块（位于 SQL Generation 文件夹下，不包括 DmlSqlGenerator.cs 文件）采用一个输入 DbQueryCommandTree，并且生成单个 SQL SELECT 语句。</span><span class="sxs-lookup"><span data-stu-id="7fc9b-105">The SQL Generation module of the Sample Provider (located under the SQL Generation folder, except for the file DmlSqlGenerator.cs) takes an input DbQueryCommandTree and produces a single SQL SELECT statement.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7fc9b-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="7fc9b-106">In This Section</span></span>  
 <span data-ttu-id="7fc9b-107">本节包括下列主题：</span><span class="sxs-lookup"><span data-stu-id="7fc9b-107">This section includes the following topics:</span></span>  
  
 [<span data-ttu-id="7fc9b-108">体系结构和设计</span><span class="sxs-lookup"><span data-stu-id="7fc9b-108">Architecture and Design</span></span>](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [<span data-ttu-id="7fc9b-109">演练： SQL 生成</span><span class="sxs-lookup"><span data-stu-id="7fc9b-109">Walkthrough: SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a><span data-ttu-id="7fc9b-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7fc9b-110">See Also</span></span>  
 [<span data-ttu-id="7fc9b-111">SQL 生成</span><span class="sxs-lookup"><span data-stu-id="7fc9b-111">SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
