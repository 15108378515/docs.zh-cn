---
title: "-main（C# 编译器选项）"
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- /main
dev_langs:
- CSharp
helpviewer_keywords:
- -main compiler option [C#]
- main compiler option [C#]
- /main compiler option [C#]
ms.assetid: 975cf4d5-36ac-4530-826c-4aad0c7f2049
caps.latest.revision: 14
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: eee7ef4698f4b6bf7c90ff8e22a1a3ae106bec35
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="main-c-compiler-options"></a><span data-ttu-id="fb37d-102">/main（C# 编译器选项）</span><span class="sxs-lookup"><span data-stu-id="fb37d-102">/main (C# Compiler Options)</span></span>
<span data-ttu-id="fb37d-103">如果多个类包含 **Main** 方法，此选项将指定包含程序入口点的类。</span><span class="sxs-lookup"><span data-stu-id="fb37d-103">This option specifies the class that contains the entry point to the program, if more than one class contains a **Main** method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb37d-104">语法</span><span class="sxs-lookup"><span data-stu-id="fb37d-104">Syntax</span></span>  
  
```console  
/main:class  
```  
  
## <a name="arguments"></a><span data-ttu-id="fb37d-105">自变量</span><span class="sxs-lookup"><span data-stu-id="fb37d-105">Arguments</span></span>  
 `class`  
 <span data-ttu-id="fb37d-106">此类型包含 **Main** 方法。</span><span class="sxs-lookup"><span data-stu-id="fb37d-106">The type that contains the **Main** method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fb37d-107">备注</span><span class="sxs-lookup"><span data-stu-id="fb37d-107">Remarks</span></span>  
 <span data-ttu-id="fb37d-108">如果编译包含具有 [Main](../../../csharp/programming-guide/main-and-command-args/index.md) 方法的多个类型，则可以指定哪个类型包含你想用作程序入口点的 **Main** 方法。</span><span class="sxs-lookup"><span data-stu-id="fb37d-108">If your compilation includes more than one type with a [Main](../../../csharp/programming-guide/main-and-command-args/index.md) method, you can specify which type contains the **Main** method that you want to use as the entry point into the program.</span></span>  
  
 <span data-ttu-id="fb37d-109">此选项用于编译 .exe 文件。</span><span class="sxs-lookup"><span data-stu-id="fb37d-109">This option is for use when compiling an .exe file.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="fb37d-110">在 Visual Studio 开发环境中设置此编译器选项</span><span class="sxs-lookup"><span data-stu-id="fb37d-110">To set this compiler option in the Visual Studio development environment</span></span>  
  
1.  <span data-ttu-id="fb37d-111">打开项目的“属性”页。</span><span class="sxs-lookup"><span data-stu-id="fb37d-111">Open the project's **Properties** page.</span></span>  
  
2.  <span data-ttu-id="fb37d-112">单击“应用程序”属性页。</span><span class="sxs-lookup"><span data-stu-id="fb37d-112">Click the **Application** property page.</span></span>  
  
3.  <span data-ttu-id="fb37d-113">修改“启动对象”属性。</span><span class="sxs-lookup"><span data-stu-id="fb37d-113">Modify the **Startup object** property.</span></span>  
  
     <span data-ttu-id="fb37d-114">若要以编程方式设置此编译器选项，请参阅 <xref:VSLangProj80.ProjectProperties3.StartupObject%2A>。</span><span class="sxs-lookup"><span data-stu-id="fb37d-114">To set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.StartupObject%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fb37d-115">示例</span><span class="sxs-lookup"><span data-stu-id="fb37d-115">Example</span></span>  
 <span data-ttu-id="fb37d-116">编译 `t2.cs` 和 `t3.cs`，指出 **Main** 方法可在 `Test2` 中找到：</span><span class="sxs-lookup"><span data-stu-id="fb37d-116">Compile `t2.cs` and `t3.cs`, specifying that the **Main** method will be found in `Test2`:</span></span>  
  
```console  
csc t2.cs t3.cs /main:Test2  
```  
  
## <a name="see-also"></a><span data-ttu-id="fb37d-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="fb37d-117">See Also</span></span>  
 <span data-ttu-id="fb37d-118">[（C# 编译器选项）](../../../csharp/language-reference/compiler-options/index.md) </span><span class="sxs-lookup"><span data-stu-id="fb37d-118">[C# Compiler Options](../../../csharp/language-reference/compiler-options/index.md) </span></span>  
 [<span data-ttu-id="fb37d-119">管理项目和解决方案属性</span><span class="sxs-lookup"><span data-stu-id="fb37d-119">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)

