---
title: "如何：定义转换运算符 (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: b0f9e63ba039a48226186fa4ce118d3e47b5673e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a><span data-ttu-id="e2469-102">如何：定义转换运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e2469-102">How to: Define a Conversion Operator (Visual Basic)</span></span>
<span data-ttu-id="e2469-103">如果已定义类或结构，则可以定义的类或结构类型和另一个数据类型之间的类型转换运算符 (如`Integer`， `Double`，或`String`)。</span><span class="sxs-lookup"><span data-stu-id="e2469-103">If you have defined a class or structure, you can define a type conversion operator between the type of your class or structure and another data type (such as `Integer`, `Double`, or `String`).</span></span>  
  
 <span data-ttu-id="e2469-104">定义类型转换为[CType 函数](../../../../visual-basic/language-reference/functions/ctype-function.md)类或结构中的过程。</span><span class="sxs-lookup"><span data-stu-id="e2469-104">Define the type conversion as a [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) procedure within the class or structure.</span></span> <span data-ttu-id="e2469-105">所有转换过程都必须`Public Shared`，和每个必须指定[Widening](../../../../visual-basic/language-reference/modifiers/widening.md)或[Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md)。</span><span class="sxs-lookup"><span data-stu-id="e2469-105">All conversion procedures must be `Public Shared`, and each one must specify either [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) or [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).</span></span>  
  
 <span data-ttu-id="e2469-106">在类或结构上定义一个运算符也称为*重载*运算符。</span><span class="sxs-lookup"><span data-stu-id="e2469-106">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2469-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2469-107">Example</span></span>  
 <span data-ttu-id="e2469-108">下面的示例定义一个称为结构之间的转换运算符`digit`和`Byte`。</span><span class="sxs-lookup"><span data-stu-id="e2469-108">The following example defines conversion operators between a structure called `digit` and a `Byte`.</span></span>  
  
 [!code-vb[VbVbcnProcedures#27](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_1.vb)]  
  
 <span data-ttu-id="e2469-109">你可以测试结构`digit`替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="e2469-109">You can test the structure `digit` with the following code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#28](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="e2469-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2469-110">See Also</span></span>  
 [<span data-ttu-id="e2469-111">运算符过程</span><span class="sxs-lookup"><span data-stu-id="e2469-111">Operator Procedures</span></span>](./operator-procedures.md)  
 [<span data-ttu-id="e2469-112">如何：定义运算符</span><span class="sxs-lookup"><span data-stu-id="e2469-112">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)  
 [<span data-ttu-id="e2469-113">如何：调用运算符过程</span><span class="sxs-lookup"><span data-stu-id="e2469-113">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)  
 [<span data-ttu-id="e2469-114">如何：使用定义运算符的类</span><span class="sxs-lookup"><span data-stu-id="e2469-114">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)  
 [<span data-ttu-id="e2469-115">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="e2469-115">Operator Statement</span></span>](../../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="e2469-116">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="e2469-116">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)  
 [<span data-ttu-id="e2469-117">如何：声明结构</span><span class="sxs-lookup"><span data-stu-id="e2469-117">How to: Declare a Structure</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)  
 [<span data-ttu-id="e2469-118">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="e2469-118">Implicit and Explicit Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)  
 [<span data-ttu-id="e2469-119">扩大转换和收缩转换</span><span class="sxs-lookup"><span data-stu-id="e2469-119">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
