---
title: "使用组合键进行联接"
description: "如何使用组合键进行联接。"
keywords: .NET, .NET Core, C#
author: stevehoag
manager: wpickett
ms.author: wiwagn
ms.date: 12/1/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: da70b54d-3213-45eb-8437-fbe75cbcf935
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: f504c9dabcd7ca2d198d58c6d81e1fde1052e3be
ms.lasthandoff: 03/13/2017

---
# <a name="join-by-using-composite-keys"></a>使用组合键进行联接

此示例演示如何执行想要使用多个键来定义匹配的联接操作。 使用组合键来完成此操作。 以匿名类型或包含要比较值的命名类型的形式来创建组合键。 若要跨方法边界传递查询变量，请使用替代该键的 <xref:System.Object.Equals%2A> 和 <xref:System.Object.GetHashCode%2A> 的命名类型。 属性的名称以及属性出现的顺序在每个键中必须相同。  
  
## <a name="example"></a>示例  
 以下示例演示如何使用组合键联接 3 个表中的数据：  
  
```csharp  
var query = from o in db.Orders  
    from p in db.Products  
    join d in db.OrderDetails   
        on new {o.OrderID, p.ProductID} equals new {d.OrderID,        d.ProductID} into details  
        from d in details  
        select new {o.OrderID, p.ProductID, d.UnitPrice};  
```  
  
 组合键上的类型推理取决于这些键中属性的名称，以及属性出现的顺序。 如果源序列中属性的名称不同，则必须在键中分配新名称。 例如，如果 `Orders` 表和 `OrderDetails` 表为各自的列分别使用不同的名称，则可通过在匿名类型中分配相同的名称来创建组合键：  
  
```csharp  
join...on new {Name = o.CustomerName, ID = o.CustID} equals   
    new {Name = d.CustName, ID = d.CustID }  
```  
  
 还可以在 `group` 子句中使用组合键。  

## <a name="see-also"></a>请参阅  
 [LINQ 查询表达式](index.md)   
 [join 子句](../language-reference/keywords/join-clause.md)   
 [group 子句](../language-reference/keywords/group-clause.md)
