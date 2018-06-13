---
title: '&#39;&lt;membername&gt; &#39;继承的接口之间不明确&#39; &lt;interfacename1&gt; &#39;和&#39; &lt;interfacename2&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30685
- bc30685
helpviewer_keywords:
- BC30685
ms.assetid: 756add7a-23d5-4b4f-a48d-8297d6459c73
ms.openlocfilehash: 23d1a11bcee2a4faae40f2683d109d5820ee5f9c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33585296"
---
# <a name="39ltmembernamegt39-is-ambiguous-across-the-inherited-interfaces-39ltinterfacename1gt39-and-39ltinterfacename2gt39"></a><span data-ttu-id="7533c-102">&#39;&lt;membername&gt; &#39;继承的接口之间不明确&#39; &lt;interfacename1&gt; &#39;和&#39; &lt;interfacename2&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="7533c-102">&#39;&lt;membername&gt;&#39; is ambiguous across the inherited interfaces &#39;&lt;interfacename1&gt;&#39; and &#39;&lt;interfacename2&gt;&#39;</span></span>
<span data-ttu-id="7533c-103">接口继承自多个接口具有相同名称的两个或多个成员。</span><span class="sxs-lookup"><span data-stu-id="7533c-103">The interface inherits two or more members with the same name from multiple interfaces.</span></span>  
  
 <span data-ttu-id="7533c-104">**错误 ID:** BC30685</span><span class="sxs-lookup"><span data-stu-id="7533c-104">**Error ID:** BC30685</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7533c-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="7533c-105">To correct this error</span></span>  
  
-   <span data-ttu-id="7533c-106">你想要使用; 的基接口将值强制转换例如：</span><span class="sxs-lookup"><span data-stu-id="7533c-106">Cast the value to the base interface that you want to use; for example:</span></span>  
  
    ```  
    Interface Left  
        Sub MySub()  
    End Interface  
  
    Interface Right  
        Sub MySub()  
    End Interface  
  
    Interface LeftRight  
        Inherits Left, Right  
    End Interface  
  
    Module test  
        Sub Main()  
            Dim x As LeftRight  
            ' x.MySub()  'x is ambiguous.  
            CType(x, Left).MySub() ' Cast to base type.  
            CType(x, Right).MySub() ' Call the other base type.  
        End Sub  
    End Module  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7533c-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="7533c-107">See Also</span></span>  
 [<span data-ttu-id="7533c-108">接口</span><span class="sxs-lookup"><span data-stu-id="7533c-108">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
