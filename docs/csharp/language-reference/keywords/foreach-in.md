---
title: "foreach，in（C# 参考）| Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- foreach
- foreach_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- foreach keyword [C#]
- foreach statement [C#]
- in keyword [C#]
ms.assetid: 5a9c5ddc-5fd3-457a-9bb6-9abffcd874ec
caps.latest.revision: 29
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: aa5408dbe214af2c21edd394f74fb8b675f2a099
ms.contentlocale: zh-cn
ms.lasthandoff: 03/13/2017

---
# <a name="foreach-in-c-reference"></a>foreach，in（C# 参考）
`foreach` 语句为实现 <xref:System.Collections.IEnumerable?displayProperty=fullName> 或 <xref:System.Collections.Generic.IEnumerable%601?displayProperty=fullName> 接口的数组或对象集合中的每个元素重复一组嵌入语句。 `foreach` 语句用于循环访问集合以获取所需信息，但不用于添加或删除源集合中的项，以避免不可预知的副作用。 如果需要添加或删除源集合中的项，请使用 [for](../../../csharp/language-reference/keywords/for.md) 循环。  
  
 为数组或集合中的每个元素继续执行嵌入的语句。 为集合中的所有元素完成迭代后，控制将传递给 `foreach` 块之后的下一语句。  
  
 在 `foreach` 块中的任何点上，可以使用[中断](../../../csharp/language-reference/keywords/break.md)关键字中断该循环，或者可以使用[继续](../../../csharp/language-reference/keywords/continue.md)关键字单步执行到循环中的下一次迭代。  
  
 `foreach` 循环还可以通过 [goto](../../../csharp/language-reference/keywords/goto.md)、[return](../../../csharp/language-reference/keywords/return.md) 或 [throw](../../../csharp/language-reference/keywords/throw.md) 语句退出。  
  
 有关 `foreach` 关键字和代码示例的详细信息，请参阅下列主题：  
  
 [对数组使用 foreach](../../../csharp/programming-guide/arrays/using-foreach-with-arrays.md)  
  
 [如何：使用 foreach 访问集合类](../../../csharp/programming-guide/classes-and-structs/how-to-access-a-collection-class-with-foreach.md)  
  
## <a name="example"></a>示例  
 下面的代码演示了三个示例：  
  
-   显示整数数组内容的典型 `foreach` 循环  
  
-   执行相同操作的 [for](../../../csharp/language-reference/keywords/for.md) 循环  
  
-   维护数组中元素数计数的 `foreach` 循环  
  
 [!code-cs[csrefKeywordsIteration#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/foreach-in_1.cs)]  
  
## <a name="c-language-specification"></a>C# 语言规范  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>另请参阅  
 [C# 参考](../../../csharp/language-reference/index.md)   
 [C# 编程指南](../../../csharp/programming-guide/index.md)   
 [C# 关键字](../../../csharp/language-reference/keywords/index.md)   
 [迭代语句](../../../csharp/language-reference/keywords/iteration-statements.md)   
 [for](../../../csharp/language-reference/keywords/for.md)
