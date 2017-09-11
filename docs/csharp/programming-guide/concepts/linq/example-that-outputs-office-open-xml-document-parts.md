---
title: "输出 Office Open XML 文档部件的示例 (C#)"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: 6cd37055-89b4-42e8-bf27-5a29717e35f3
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: e7b2135a0894e1fa5a553552fa128809d740dea2
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="example-that-outputs-office-open-xml-document-parts-c"></a><span data-ttu-id="7d27d-102">输出 Office Open XML 文档部件的示例 (C#)</span><span class="sxs-lookup"><span data-stu-id="7d27d-102">Example that Outputs Office Open XML Document Parts (C#)</span></span>
<span data-ttu-id="7d27d-103">本主题演示如何打开 Office Open XML 文档并访问其中的部分。</span><span class="sxs-lookup"><span data-stu-id="7d27d-103">This topic shows how to open an Office Open XML document and access parts within it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d27d-104">示例</span><span class="sxs-lookup"><span data-stu-id="7d27d-104">Example</span></span>  
 <span data-ttu-id="7d27d-105">下面的示例打开 Office Open XML 文档，并将文档部分和样式部分输出到控制台。</span><span class="sxs-lookup"><span data-stu-id="7d27d-105">The following example opens an Office Open XML document, and prints the document part and the style part to the console.</span></span>  
  
 <span data-ttu-id="7d27d-106">本示例使用 WindowsBase 程序集中的类。</span><span class="sxs-lookup"><span data-stu-id="7d27d-106">This example uses classes from the WindowsBase assembly.</span></span> <span data-ttu-id="7d27d-107">它使用 <xref:System.IO.Packaging?displayProperty=fullName> 命名空间中的类型。</span><span class="sxs-lookup"><span data-stu-id="7d27d-107">It uses types in the <xref:System.IO.Packaging?displayProperty=fullName> namespace.</span></span>  
  
```csharp  
const string fileName = "SampleDoc.docx";  
  
const string documentRelationshipType =  
  "http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument";  
const string stylesRelationshipType =  
  "http://schemas.openxmlformats.org/officeDocument/2006/relationships/styles";  
const string wordmlNamespace =  
  "http://schemas.openxmlformats.org/wordprocessingml/2006/main";  
XNamespace w = wordmlNamespace;  
  
using (Package wdPackage = Package.Open(fileName, FileMode.Open, FileAccess.Read))  
{  
    PackageRelationship docPackageRelationship =  
      wdPackage.GetRelationshipsByType(documentRelationshipType).FirstOrDefault();  
    if (docPackageRelationship != null)  
    {  
        Uri documentUri = PackUriHelper.ResolvePartUri(new Uri("/", UriKind.Relative),  
          docPackageRelationship.TargetUri);  
        PackagePart documentPart = wdPackage.GetPart(documentUri);  
  
        //  Load the document XML in the part into an XDocument instance.  
        XDocument xdoc = XDocument.Load(XmlReader.Create(documentPart.GetStream()));  
  
        Console.WriteLine("TargetUri:{0}", docPackageRelationship.TargetUri);  
        Console.WriteLine("==================================================================");  
        Console.WriteLine(xdoc.Root);  
        Console.WriteLine();  
  
        //  Find the styles part. There will only be one.  
        PackageRelationship styleRelation =  
          documentPart.GetRelationshipsByType(stylesRelationshipType).FirstOrDefault();  
        if (styleRelation != null)  
        {  
            Uri styleUri = PackUriHelper.ResolvePartUri(documentUri, styleRelation.TargetUri);  
            PackagePart stylePart = wdPackage.GetPart(styleUri);  
  
            //  Load the style XML in the part into an XDocument instance.  
            XDocument styleDoc = XDocument.Load(XmlReader.Create(stylePart.GetStream()));  
  
            Console.WriteLine("TargetUri:{0}", styleRelation.TargetUri);  
            Console.WriteLine("==================================================================");  
            Console.WriteLine(styleDoc.Root);  
            Console.WriteLine();  
        }  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="7d27d-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7d27d-108">See Also</span></span>  
 [<span data-ttu-id="7d27d-109">Office Open XML WordprocessingML 文档的详细信息 (C#)</span><span class="sxs-lookup"><span data-stu-id="7d27d-109">Details of Office Open XML WordprocessingML Documents (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/details-of-office-open-xml-wordprocessingml-documents.md)

