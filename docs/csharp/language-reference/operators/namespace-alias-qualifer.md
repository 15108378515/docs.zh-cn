---
title: ":: 运算符（C# 参考）| Microsoft Docs"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ::_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
caps.latest.revision: 21
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
ms.openlocfilehash: 12a0265d430a5a110d8c73107a48b36e0ab15405
ms.contentlocale: zh-cn
ms.lasthandoff: 03/13/2017

---
# <a name="-operator-c-reference"></a>:: 运算符（C# 参考）
命名空间别名限定符（`::`）用于查找标识符。 它始终位于两个标识符之间，如本示例所示：  
  
 [!code-cs[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  
  
## <a name="remarks"></a>备注  
 命名空间别名限定符可以为 `global`。 这将调用全局命名空间（而不是别名命名空间）中的查找。  
  
## <a name="for-more-information"></a>更多信息  
 有关如何使用 `::` 运算符的示例，请参阅以下部分：  
  
-   [如何：使用全局命名空间别名](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a>C# 语言规范  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [C# 参考](../../../csharp/language-reference/index.md)   
 [C# 编程指南](../../../csharp/programming-guide/index.md)   
 [C# 运算符](../../../csharp/language-reference/operators/index.md)   
 [命名空间关键字](../../../csharp/language-reference/keywords/namespace-keywords.md)   
 [。运算符](../../../csharp/language-reference/operators/member-access-operator.md)   
 [外部别名](../../../csharp/language-reference/keywords/extern-alias.md)
