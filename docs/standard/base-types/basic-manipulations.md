---
title: 如何：在 .NET Framework 中执行基本字符串操作
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology: dotnet-standard
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- strings [.NET Framework], examples
ms.assetid: 121d1eae-251b-44c0-8818-57da04b8215e
caps.latest.revision: 7
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8d3d5351a0a639a3f0b674640bcaaf7321ca0d76
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-perform-basic-string-manipulations-in-net"></a><span data-ttu-id="086f6-102">如何：执行 .NET 中的基本字符串控制</span><span class="sxs-lookup"><span data-stu-id="086f6-102">How to: Perform Basic String Manipulations in .NET</span></span>
<span data-ttu-id="086f6-103">下面的示例使用[基本字符串操作](../../../docs/standard/base-types/basic-string-operations.md)主题中介绍的一些方法，构造模拟现实应用执行字符串控制的类。</span><span class="sxs-lookup"><span data-stu-id="086f6-103">The following example uses some of the methods discussed in the [Basic String Operations](../../../docs/standard/base-types/basic-string-operations.md) topics to construct a class that performs string manipulations in a manner that might be found in a real-world application.</span></span> <span data-ttu-id="086f6-104">`MailToData` 类将个人的姓名和地址存储在单独的属性中，并提供一种将 `City`、`State` 和 `Zip` 字段合并成向用户显示的单个字符串的方式。</span><span class="sxs-lookup"><span data-stu-id="086f6-104">The `MailToData` class stores the name and address of an individual in separate properties and provides a way to combine the `City`, `State`, and `Zip` fields into a single string for display to the user.</span></span> <span data-ttu-id="086f6-105">此外，该类允许用户以单个字符串的形式输入将城市、州/省和邮政编码信息；应用程序会自动分析此字符串，并将正确的信息输入到相应的属性中。</span><span class="sxs-lookup"><span data-stu-id="086f6-105">Furthermore, the class allows the user to enter the city, state, and ZIP Code information as a single string; the application automatically parses the single string and enters the proper information into the corresponding property.</span></span>  
  
 <span data-ttu-id="086f6-106">为简单起见，此示例使用带命令行接口的控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="086f6-106">For simplicity, this example uses a console application with a command-line interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="086f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="086f6-107">Example</span></span>  
 [!code-csharp[Conceptual.String.BasicOps#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.string.basicops/cs/basicops.cs#1)]
 [!code-vb[Conceptual.String.BasicOps#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.string.basicops/vb/basicops.vb#1)]  
  
 <span data-ttu-id="086f6-108">执行上面的代码时，系统会要求用户输入其姓名和地址。</span><span class="sxs-lookup"><span data-stu-id="086f6-108">When the preceding code is executed, the user is asked to enter his or her name and address.</span></span> <span data-ttu-id="086f6-109">应用程序将这些信息放入相应的属性并向用户显示这些信息，同时创建一个显示城市、州/省和邮政编码信息的字符串。</span><span class="sxs-lookup"><span data-stu-id="086f6-109">The application places the information in the appropriate properties and displays the information back to the user, creating a single string that displays the city, state, and ZIP Code information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="086f6-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="086f6-110">See Also</span></span>  
 [<span data-ttu-id="086f6-111">基本字符串操作</span><span class="sxs-lookup"><span data-stu-id="086f6-111">Basic String Operations</span></span>](../../../docs/standard/base-types/basic-string-operations.md)
