---
title: 访问计算机资源 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- computer resources [Visual Basic]
- My.Computer object [Visual Basic], tasks
- computer resources [Visual Basic], accessing
ms.assetid: 75b81c88-f7c0-46e0-95c8-0c006d2120f9
ms.openlocfilehash: 7128a71f28d1755a14fcda5f09bee11202ab4154
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2018
ms.locfileid: "43001899"
---
# <a name="accessing-computer-resources-visual-basic"></a><span data-ttu-id="a0ea5-102">访问计算机资源 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0ea5-102">Accessing computer resources (Visual Basic)</span></span>

<span data-ttu-id="a0ea5-103">`My.Computer` 对象是 `My` 中的三个中心对象之一，提供对信息和常用功能的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-103">The `My.Computer` object is one of the three central objects in `My`, providing access to information and commonly used functionality.</span></span> <span data-ttu-id="a0ea5-104">`My.Computer` 提供用于访问运行应用程序的计算机的方法、属性和事件。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-104">`My.Computer` provides methods, properties, and events for accessing the computer on which the application is running.</span></span> <span data-ttu-id="a0ea5-105">其对象包括：</span><span class="sxs-lookup"><span data-stu-id="a0ea5-105">Its objects include:</span></span>  
  
-   <xref:Microsoft.VisualBasic.Devices.Audio>
-   <span data-ttu-id="a0ea5-106">剪贴板 (<xref:Microsoft.VisualBasic.MyServices.ClipboardProxy>)</span><span class="sxs-lookup"><span data-stu-id="a0ea5-106">Clipboard (<xref:Microsoft.VisualBasic.MyServices.ClipboardProxy>)</span></span>
-   <xref:Microsoft.VisualBasic.Devices.Clock>
-   <xref:Microsoft.VisualBasic.FileIO.FileSystem>
-   <xref:Microsoft.VisualBasic.Devices.ServerComputer.Info%2A>
-   <xref:Microsoft.VisualBasic.Devices.Keyboard>
-   <xref:Microsoft.VisualBasic.Devices.Mouse>
-   <xref:Microsoft.VisualBasic.Devices.Network>
-   <xref:Microsoft.VisualBasic.Devices.Ports>
-   <span data-ttu-id="a0ea5-107">注册表 (<xref:Microsoft.VisualBasic.MyServices.RegistryProxy>)</span><span class="sxs-lookup"><span data-stu-id="a0ea5-107">Registry (<xref:Microsoft.VisualBasic.MyServices.RegistryProxy>)</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a0ea5-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="a0ea5-108">In this section</span></span>

<span data-ttu-id="a0ea5-109">[播放声音](../../../../visual-basic/developing-apps/programming/computer-resources/playing-sounds.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-109">[Playing Sounds](../../../../visual-basic/developing-apps/programming/computer-resources/playing-sounds.md) </span></span>  
<span data-ttu-id="a0ea5-110">列出与 `My.Computer.Audio` 关联的任务，例如在后台播放声音。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-110">Lists tasks associated with `My.Computer.Audio`, such as playing a sound in the background.</span></span>

<span data-ttu-id="a0ea5-111">[将数据存储到剪贴板以及从剪贴板读取数据](../../../../visual-basic/developing-apps/programming/computer-resources/storing-data-to-and-reading-from-the-clipboard.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-111">[Storing Data to and Reading from the Clipboard](../../../../visual-basic/developing-apps/programming/computer-resources/storing-data-to-and-reading-from-the-clipboard.md) </span></span>  
<span data-ttu-id="a0ea5-112">列出与 `My.Computer.Clipboard` 关联的任务，例如从剪贴板读取数据或向剪贴板写入数据。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-112">Lists tasks associated with `My.Computer.Clipboard`, such as reading data from or writing data to the Clipboard.</span></span>

<span data-ttu-id="a0ea5-113">[获取有关计算机的信息](../../../../visual-basic/developing-apps/programming/computer-resources/getting-information-about-the-computer.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-113">[Getting Information about the Computer](../../../../visual-basic/developing-apps/programming/computer-resources/getting-information-about-the-computer.md) </span></span>  
<span data-ttu-id="a0ea5-114">列出与 `My.Computer.Info` 关联的任务，例如确定计算机的全名或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-114">Lists tasks associated with `My.Computer.Info`, such as determining a computer's full name or IP addresses.</span></span>

<span data-ttu-id="a0ea5-115">[访问键盘](../../../../visual-basic/developing-apps/programming/computer-resources/accessing-the-keyboard.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-115">[Accessing the Keyboard](../../../../visual-basic/developing-apps/programming/computer-resources/accessing-the-keyboard.md) </span></span>  
<span data-ttu-id="a0ea5-116">列出与 `My.Computer.Keyboard` 关联的任务，例如确定 Caps Lock 键是否已启用。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-116">Lists tasks associated with `My.Computer.Keyboard`, such as determining whether CAPS LOCK is on.</span></span>

<span data-ttu-id="a0ea5-117">[访问鼠标](../../../../visual-basic/developing-apps/programming/computer-resources/accessing-the-mouse.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-117">[Accessing the Mouse](../../../../visual-basic/developing-apps/programming/computer-resources/accessing-the-mouse.md) </span></span>  
<span data-ttu-id="a0ea5-118">列出与 `My.Computer.Mouse` 关联的任务，例如确定鼠标是否存在。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-118">Lists tasks associated with `My.Computer.Mouse`, such as determining whether a mouse is present.</span></span>

<span data-ttu-id="a0ea5-119">[执行网络操作](../../../../visual-basic/developing-apps/programming/computer-resources/performing-network-operations.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-119">[Performing Network Operations](../../../../visual-basic/developing-apps/programming/computer-resources/performing-network-operations.md) </span></span>  
<span data-ttu-id="a0ea5-120">列出与 `My.Computer.Network` 关联的任务，例如上传或下载文件。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-120">Lists tasks associated with `My.Computer.Network`, such as uploading or downloading files.</span></span>

<span data-ttu-id="a0ea5-121">[访问计算机的端口](../../../../visual-basic/developing-apps/programming/computer-resources/accessing-the-computer-s-ports.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-121">[Accessing the Computer's Ports](../../../../visual-basic/developing-apps/programming/computer-resources/accessing-the-computer-s-ports.md) </span></span>  
<span data-ttu-id="a0ea5-122">列出与 `My.Computer.Ports` 关联的任务，例如显示可用的串行端口或向串行端口发送字符串。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-122">Lists tasks associated with `My.Computer.Ports`, such as showing available serial ports or sending strings to serial ports.</span></span>

<span data-ttu-id="a0ea5-123">[读取和写入注册表](../../../../visual-basic/developing-apps/programming/computer-resources/reading-from-and-writing-to-the-registry.md) </span><span class="sxs-lookup"><span data-stu-id="a0ea5-123">[Reading from and Writing to the Registry](../../../../visual-basic/developing-apps/programming/computer-resources/reading-from-and-writing-to-the-registry.md) </span></span>  
<span data-ttu-id="a0ea5-124">列出与 `My.Computer.Registry` 关联的任务，例如从注册表项读取数据或向注册表项写入数据。</span><span class="sxs-lookup"><span data-stu-id="a0ea5-124">Lists tasks associated with `My.Computer.Registry`, such as reading data from or writing data to registry keys.</span></span>