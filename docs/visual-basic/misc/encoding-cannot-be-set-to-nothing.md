---
title: "编码不能设置为 Nothing。"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
ms.assetid: 59f7c731-8291-4a85-bf51-c225e48cdc84
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 42baef6e0634849004290dce3db32e47f103282d
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="encoding-cannot-be-set-to-nothing"></a><span data-ttu-id="4bb61-102">编码不能设置为 Nothing。</span><span class="sxs-lookup"><span data-stu-id="4bb61-102">Encoding cannot be set to Nothing</span></span>
<span data-ttu-id="4bb61-103">尝试读取或写入文件失败，因为已将参数 `encoding` 设置为 `Nothing` ，但需要有效值。</span><span class="sxs-lookup"><span data-stu-id="4bb61-103">An attempt to read from or write to a file has failed because the parameter `encoding` has been set to `Nothing` but requires a valid value.</span></span>  
  
 <span data-ttu-id="4bb61-104"><xref:System.Text.Encoding> 用于确定写入文件时使用何种编码。</span><span class="sxs-lookup"><span data-stu-id="4bb61-104"><xref:System.Text.Encoding> is used to determine what encoding to use when writing to a file.</span></span> <span data-ttu-id="4bb61-105">默认为 UTF-8。</span><span class="sxs-lookup"><span data-stu-id="4bb61-105">The default is UTF-8.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4bb61-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4bb61-106">To correct this error</span></span>  
  
-   <span data-ttu-id="4bb61-107">为 `encoding` 参数提供有效值。</span><span class="sxs-lookup"><span data-stu-id="4bb61-107">Supply a valid value for the `encoding` parameter.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bb61-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="4bb61-108">See Also</span></span>  
 [<span data-ttu-id="4bb61-109">文件编码</span><span class="sxs-lookup"><span data-stu-id="4bb61-109">File Encodings</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/file-encodings.md)  
 [<span data-ttu-id="4bb61-110">从文件读取</span><span class="sxs-lookup"><span data-stu-id="4bb61-110">Reading from Files</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/reading-from-files.md)  
 [<span data-ttu-id="4bb61-111">写入文件</span><span class="sxs-lookup"><span data-stu-id="4bb61-111">Writing to Files</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)  
 [<span data-ttu-id="4bb61-112">My.Computer.FileSystem.ReadAllText</span><span class="sxs-lookup"><span data-stu-id="4bb61-112">My.Computer.FileSystem.ReadAllText</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A)  
 [<span data-ttu-id="4bb61-113">My.Computer.FileSystem.WriteAllText</span><span class="sxs-lookup"><span data-stu-id="4bb61-113">My.Computer.FileSystem.WriteAllText</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A)
