---
title: 如何：应用 PropertyNameChanged 模式
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property changes (using code)
- data binding [Windows Forms], custom controls
- PropertyNameChanged pattern [Windows Forms], applying
ms.assetid: aa47ddf6-5223-40c4-833f-a78992194836
ms.openlocfilehash: 775a27b1b4ba8143e297a3c4d323356a304073a0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33536740"
---
# <a name="how-to-apply-the-propertynamechanged-pattern"></a>如何：应用 PropertyNameChanged 模式
下面的代码示例演示如何应用*PropertyName*Changed 模式的自定义控件。 实现与 Windows 窗体数据绑定引擎使用的自定义控件时，则适用此模式。  
  
## <a name="example"></a>示例  
 [!code-csharp[System.Windows.Forms.ChangeNotification#3](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/CS/Form1.cs#3)]
 [!code-vb[System.Windows.Forms.ChangeNotification#3](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a>编译代码  
 编译前面的代码示例：  
  
-   将代码粘贴到空代码文件中。 你必须使用包含一个 Windows 窗体上的自定义控件`Main`方法。  
  
## <a name="see-also"></a>请参阅  
 [如何：实现 INotifyPropertyChanged 接口](../../../docs/framework/winforms/how-to-implement-the-inotifypropertychanged-interface.md)  
 [Windows 窗体数据绑定中的更改通知](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)  
 [Windows 窗体数据绑定](../../../docs/framework/winforms/windows-forms-data-binding.md)
