---
title: 派生类无法引发基类事件
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc30029
- bc30029
helpviewer_keywords:
- BC30029
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
caps.latest.revision: 9
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 70dde8b96980adfd618e38b9ce142cdec56a6b13
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="derived-classes-cannot-raise-base-class-events"></a><span data-ttu-id="5107d-102">派生类无法引发基类事件</span><span class="sxs-lookup"><span data-stu-id="5107d-102">Derived classes cannot raise base class events</span></span>
<span data-ttu-id="5107d-103">只能从在其中声明的声明空间，可以引发一个事件。</span><span class="sxs-lookup"><span data-stu-id="5107d-103">An event can be raised only from the declaration space in which it is declared.</span></span> <span data-ttu-id="5107d-104">因此，一个类不能引发从任何其他类，甚至一个派生自的事件。</span><span class="sxs-lookup"><span data-stu-id="5107d-104">Therefore, a class cannot raise events from any other class, even one from which it is derived.</span></span>  
  
 <span data-ttu-id="5107d-105">**错误 ID:** BC30029</span><span class="sxs-lookup"><span data-stu-id="5107d-105">**Error ID:** BC30029</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="5107d-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="5107d-106">To correct this error</span></span>  
  
-   <span data-ttu-id="5107d-107">移动`Event`语句或`RaiseEvent`语句，使它们处于同一个类。</span><span class="sxs-lookup"><span data-stu-id="5107d-107">Move the `Event` statement or the `RaiseEvent` statement so they are in the same class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5107d-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5107d-108">See Also</span></span>  
 [<span data-ttu-id="5107d-109">Event 语句</span><span class="sxs-lookup"><span data-stu-id="5107d-109">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)  
 [<span data-ttu-id="5107d-110">RaiseEvent 语句</span><span class="sxs-lookup"><span data-stu-id="5107d-110">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
