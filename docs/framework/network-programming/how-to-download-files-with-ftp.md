---
title: "如何：使用 FTP 下载文件"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 892548b8-954a-4f6a-9bca-2ae620c3700f
caps.latest.revision: "5"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: 6309bf4885b7a0f2ab7cedfb48af70dc76bf31f4
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-download-files-with-ftp"></a><span data-ttu-id="d51a9-102">如何：使用 FTP 下载文件</span><span class="sxs-lookup"><span data-stu-id="d51a9-102">How to: Download Files with FTP</span></span>
<span data-ttu-id="d51a9-103">此示例演示如何从 FTP 服务器下载文件。</span><span class="sxs-lookup"><span data-stu-id="d51a9-103">This sample shows how to download a file from an FTP server.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d51a9-104">示例</span><span class="sxs-lookup"><span data-stu-id="d51a9-104">Example</span></span>  
  
```csharp  
using System;  
using System.IO;  
using System.Net;  
using System.Text;  
  
namespace Examples.System.Net  
{  
    public class WebRequestGetExample  
    {  
        public static void Main ()  
        {  
            // Get the object used to communicate with the server.  
            FtpWebRequest request = (FtpWebRequest)WebRequest.Create("ftp://www.contoso.com/test.htm");  
            request.Method = WebRequestMethods.Ftp.DownloadFile;  
  
            // This example assumes the FTP site uses anonymous logon.  
            request.Credentials = new NetworkCredential ("anonymous","janeDoe@contoso.com");  
  
            FtpWebResponse response = (FtpWebResponse)request.GetResponse();  
  
            Stream responseStream = response.GetResponseStream();  
            StreamReader reader = new StreamReader(responseStream);  
            Console.WriteLine(reader.ReadToEnd());  
  
            Console.WriteLine("Download Complete, status {0}", response.StatusDescription);  
  
            reader.Close();  
            response.Close();    
        }  
    }  
}  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d51a9-105">编译代码</span><span class="sxs-lookup"><span data-stu-id="d51a9-105">Compiling the Code</span></span>  
 <span data-ttu-id="d51a9-106">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="d51a9-106">This example requires:</span></span>  
  
-   <span data-ttu-id="d51a9-107">引用 System.Net 命名空间。</span><span class="sxs-lookup"><span data-stu-id="d51a9-107">References to the **System.Net** namespace.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="d51a9-108">可靠编程</span><span class="sxs-lookup"><span data-stu-id="d51a9-108">Robust Programming</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="d51a9-109">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="d51a9-109">.NET Framework Security</span></span>
