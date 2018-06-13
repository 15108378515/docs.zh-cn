---
title: 如何：指定专用存储字段
ms.date: 03/30/2017
ms.assetid: 5a40e816-cc6e-43a0-b32a-9caaa0ab6912
ms.openlocfilehash: d8a9bacd88b08384e7619dc64ab86cb0651ac44d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361593"
---
# <a name="how-to-specify-private-storage-fields"></a><span data-ttu-id="230e9-102">如何：指定专用存储字段</span><span class="sxs-lookup"><span data-stu-id="230e9-102">How to: Specify Private Storage Fields</span></span>
<span data-ttu-id="230e9-103">使用[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>属性<xref:System.Data.Linq.Mapping.DataAttribute>特性来指定基础存储字段的名称。</span><span class="sxs-lookup"><span data-stu-id="230e9-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> property on the <xref:System.Data.Linq.Mapping.DataAttribute> attribute to designate the name of an underlying storage field.</span></span>  
  
 <span data-ttu-id="230e9-104">有关代码示例，请参见<xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>。</span><span class="sxs-lookup"><span data-stu-id="230e9-104">For code examples, see <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A>.</span></span>  
  
### <a name="to-specify-the-name-of-an-underlying-storage-field"></a><span data-ttu-id="230e9-105">指定基础存储字段的名称</span><span class="sxs-lookup"><span data-stu-id="230e9-105">To specify the name of an underlying storage field</span></span>  
  
1.  <span data-ttu-id="230e9-106">将 <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> 属性 (Property) 添加到 <xref:System.Data.Linq.Mapping.ColumnAttribute> 属性 (Attribute)。</span><span class="sxs-lookup"><span data-stu-id="230e9-106">Add the <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2.  <span data-ttu-id="230e9-107">指定字段的名称作为 <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> 属性的值。</span><span class="sxs-lookup"><span data-stu-id="230e9-107">Assign the name of the field as the value of the <xref:System.Data.Linq.Mapping.DataAttribute.Storage%2A> property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="230e9-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="230e9-108">See Also</span></span>  
 [<span data-ttu-id="230e9-109">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="230e9-109">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [<span data-ttu-id="230e9-110">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="230e9-110">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
