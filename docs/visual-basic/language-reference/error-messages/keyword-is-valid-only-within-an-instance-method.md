---
title: '&#39;&lt;关键字&gt;&#39;只能在实例方法内有效'
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: 2d9e26aa7dccf1b9c6390a20a59b10a0d248969d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="39ltkeywordgt39-is-valid-only-within-an-instance-method"></a>&#39;&lt;关键字&gt;&#39;只能在实例方法内有效
`Me`， `MyClass`，和`MyBase`关键字引用特定的类实例。 你无法使用其内部共享`Function`或`Sub`过程。  
  
 **错误 ID:** BC30043  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
-   从过程中删除关键字或删除`Shared`从过程声明的关键字。  
  
## <a name="see-also"></a>请参阅  
 [对象变量赋值](../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)  
 [Me、My、MyBase 和 MyClass](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)  
 [继承的基础知识](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
