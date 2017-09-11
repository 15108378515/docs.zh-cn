---
title: "如何：检索元素的浅值 (C#)"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: 924a2699-72f6-4be1-aaa6-de62f8ec73b9
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: aad07fdba1d3df2b72f867e6845536300031146b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="how-to-retrieve-the-shallow-value-of-an-element-c"></a><span data-ttu-id="993fc-102">如何：检索元素的浅值 (C#)</span><span class="sxs-lookup"><span data-stu-id="993fc-102">How to: Retrieve the Shallow Value of an Element (C#)</span></span>
<span data-ttu-id="993fc-103">本主题说明如何获取元素的浅值。</span><span class="sxs-lookup"><span data-stu-id="993fc-103">This topic shows how to get the shallow value of an element.</span></span> <span data-ttu-id="993fc-104">浅值只是特定元素的值，与深值相反，包括串联成一个单一字符串的所有子元素的值。</span><span class="sxs-lookup"><span data-stu-id="993fc-104">The shallow value is the value of the specific element only, as opposed to the deep value, which includes the values of all descendent elements concatenated into a single string.</span></span>  
  
 <span data-ttu-id="993fc-105">使用强制转换或 <xref:System.Xml.Linq.XElement.Value%2A?displayProperty=fullName> 属性检索元素值时，您可以检索深值。</span><span class="sxs-lookup"><span data-stu-id="993fc-105">When you retrieve an element value by using either casting or the <xref:System.Xml.Linq.XElement.Value%2A?displayProperty=fullName> property, you retrieve the deep value.</span></span> <span data-ttu-id="993fc-106">要检索浅值，您可以使用 `ShallowValue` 扩展方法，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="993fc-106">To retrieve the shallow value, you can use the `ShallowValue` extension method, as shown in the follwing example.</span></span> <span data-ttu-id="993fc-107">当根据内容选择元素时，检索浅值十分有用。</span><span class="sxs-lookup"><span data-stu-id="993fc-107">Retrieving the shallow value is useful when you want to select elements based on their content.</span></span>  
  
 <span data-ttu-id="993fc-108">下面的示例声明了检索元素浅值的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="993fc-108">The following example declares an extension method that retrieves the shallow value of an element.</span></span> <span data-ttu-id="993fc-109">然后在查询中使用该扩展方法列出包含计算得出的值的所有元素。</span><span class="sxs-lookup"><span data-stu-id="993fc-109">It then uses the extension method in a query to list all elements that contain a calculated value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="993fc-110">示例</span><span class="sxs-lookup"><span data-stu-id="993fc-110">Example</span></span>  
 <span data-ttu-id="993fc-111">下面的文本文件 Report.xml 是此示例的源。</span><span class="sxs-lookup"><span data-stu-id="993fc-111">The following text file, Report.xml, is the source for this example.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<Report>  
  <Section>  
    <Heading>  
      <Column Name="CustomerId">=Customer.CustomerId.Heading</Column>  
      <Column Name="Name">=Customer.Name.Heading</Column>  
    </Heading>  
    <Detail>  
      <Column Name="CustomerId">=Customer.CustomerId</Column>  
      <Column Name="Name">=Customer.Name</Column>  
    </Detail>  
  </Section>  
</Report>  
```  
  
```csharp  
public static class MyExtensions  
{  
    public static string ShallowValue(this XElement xe)  
    {  
        return xe  
               .Nodes()  
               .OfType<XText>()  
               .Aggregate(new StringBuilder(),  
                          (s, c) => s.Append(c),  
                          s => s.ToString());  
    }  
}  
  
class Program  
{  
    static void Main(string[] args)  
    {  
        XElement root = XElement.Load("Report.xml");  
  
        IEnumerable<XElement> query = from el in root.Descendants()  
                                      where el.ShallowValue().StartsWith("=")  
                                      select el;  
  
        foreach (var q in query)  
        {  
            Console.WriteLine("{0}{1}{2}",  
                q.Name.ToString().PadRight(8),  
                q.Attribute("Name").ToString().PadRight(20),  
                q.ShallowValue());  
        }  
    }  
}  
```  
  
 <span data-ttu-id="993fc-112">该示例产生下面的输出：</span><span class="sxs-lookup"><span data-stu-id="993fc-112">This example produces the following output:</span></span>  
  
```  
Column  Name="CustomerId"   =Customer.CustomerId.Heading  
Column  Name="Name"         =Customer.Name.Heading  
Column  Name="CustomerId"   =Customer.CustomerId  
Column  Name="Name"         =Customer.Name  
```  
  
## <a name="see-also"></a><span data-ttu-id="993fc-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="993fc-113">See Also</span></span>  
 [<span data-ttu-id="993fc-114">LINQ to XML 轴 (C#)</span><span class="sxs-lookup"><span data-stu-id="993fc-114">LINQ to XML Axes (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-axes.md)

