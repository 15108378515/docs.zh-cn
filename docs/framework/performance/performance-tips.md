---
title: .NET 性能提示
ms.date: 03/30/2017
helpviewer_keywords:
- C# language, performance
- performance [C#]
- Visual Basic, performance
- performance [Visual Basic]
ms.assetid: ae275793-857d-4102-9095-b4c2a02d57f4
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 3d5d91db9256cdfb3aa0062d66333f13797ee1bb
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/02/2018
ms.locfileid: "48025248"
---
# <a name="net-performance-tips"></a>.NET 性能提示
术语“性能”通常指程序的执行速度。 有时通过遵循源代码中的一些基本规则便可以提高执行速度。 在某些程序中，十分重要的一点是需要仔细检查代码并使用探查器确保程序尽可能快地运行。 而在其他程序中，由于代码在编写时便运行得足够快，因此不必执行此类优化。 本文列出了一些性能可能遭受影响的常见领域以及相关改进建议，并提供其他性能主题的链接。 有关规划和测量性能的详细信息，请参阅[性能](../../../docs/framework/performance/index.md)  
  
## <a name="boxing-and-unboxing"></a>装箱和取消装箱  
 如果值类型必须被频繁装箱，那么在这些情况下最好避免使用值类型（例如在诸如 <xref:System.Collections.ArrayList?displayProperty=nameWithType> 的非泛型集合类中）。 可通过使用泛型集合（例如 <xref:System.Collections.Generic.List%601?displayProperty=nameWithType>）来避免装箱值类型。 装箱和取消装箱过程需要进行大量的计算。 对值类型进行装箱时，必须创建一个全新的对象。 这可能比简单的引用赋值用时最多长 20 倍。 取消装箱的过程所需时间可达赋值操作的四倍。 有关详细信息，请参阅[装箱和取消装箱](~/docs/csharp/programming-guide/types/boxing-and-unboxing.md)。  
  
## <a name="strings"></a>字符串  
 在连接大量字符串变量时，例如在紧凑循环中，请使用 <xref:System.Text.StringBuilder?displayProperty=nameWithType> 而不是 C# [+ 运算符](~/docs/csharp/language-reference/operators/addition-operator.md)或 Visual Basic [串联运算符](~/docs/visual-basic/language-reference/operators/concatenation-operators.md)。 有关详细信息，请参阅[如何连接多个字符串](../../csharp/how-to/concatenate-multiple-strings.md)和 [Visual Basic 中的串联运算符](~/docs/visual-basic/programming-guide/language-features/operators-and-expressions/concatenation-operators.md)。  
  
## <a name="destructors"></a>析构函数  
 不应使用空的析构函数。 如果类包含析构函数，则 Finalize 队列中会创建一个条目。 调用析构函数时，将调用垃圾回收器来处理此队列。 如果析构函数为空，只会导致性能损失。 有关详细信息，请参阅[析构函数](~/docs/csharp/programming-guide/classes-and-structs/destructors.md)和[对象生存期：如何创建和销毁对象](~/docs/visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)。  
  
## <a name="other-resources"></a>其他资源  
  
-   [编写更快的托管代码：了解代价](https://go.microsoft.com/fwlink/?LinkId=99294)  
  
-   [编写高性能的托管应用程序：入门](https://go.microsoft.com/fwlink/?LinkId=99295)  
  
-   [垃圾回收器基础知识和性能提示](https://go.microsoft.com/fwlink/?LinkId=99296)  
  
-   [.NET 应用程序的性能提示和技巧](https://go.microsoft.com/fwlink/?LinkId=99297)  

-   [Rico Mariani 关于性能问题的见解](https://go.microsoft.com/fwlink/?LinkId=115679)  

-   [Vance Morrison 的博客](https://blogs.msdn.microsoft.com/vancem/)
  
## <a name="see-also"></a>请参阅  
 [性能](../../../docs/framework/performance/index.md)  
 [编程概念](https://msdn.microsoft.com/library/65c12cca-af4f-4017-886e-2dbc00a189d6)  
 [Visual Basic 编程指南](../../visual-basic/programming-guide/index.md)  
 [C# 编程指南](https://msdn.microsoft.com/library/ac0f23a2-6bf3-4077-be99-538ae5fd3bc5)
