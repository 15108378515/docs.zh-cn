---
title: 表概述
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flow content elements [WPF], Table
- documents [WPF], tables
- tables [WPF]
ms.assetid: 5e1105f4-8fc4-473a-ba55-88c8e71386e6
ms.openlocfilehash: 631a14ae8eb17713186f7db66700026cc476024e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33549365"
---
# <a name="table-overview"></a>表概述
<xref:System.Windows.Documents.Table> 是支持的流文档内容的基于网格的演示文稿的块级别元素。 此元素极具灵活性，因此很有用，但也因此显得更加复杂，从而不容易理解和正确使用。  
  
 本主题包含以下各节：  
  
-   [表基础](#table_basics)  
  
-   [表与网格有什么区别？](#table_vs_Grid)  
  
-   [基本表结构](#basic_table_structure)  
  
-   [表包含](#table_containment)  
  
-   [行分组](#row_groupings)  
  
-   [背景呈现优先级](#rendering_precedence)  
  
-   [跨行或列 ](#spanning_rows_or_columns)  
  
-   [使用代码生成表 ](#building_a_table_with_code)  
  
-   [相关主题] 
  
<a name="table_basics"></a>   
## <a name="table-basics"></a>表基础  
  
<a name="table_vs_Grid"></a>   
### <a name="how-is-table-different-then-grid"></a>表与网格有什么区别？  
 <xref:System.Windows.Documents.Table> 和<xref:System.Windows.Controls.Grid>共享一些常见的功能，但每个最适合于不同的方案。 A<xref:System.Windows.Documents.Table>旨在用于在流内容中 (请参阅[流文档概述](../../../../docs/framework/wpf/advanced/flow-document-overview.md)有关流内容的详细信息)。 网格最适合在表单内（主要在流内容以外的任意位置）使用。 在<xref:System.Windows.Documents.FlowDocument>，<xref:System.Windows.Documents.Table>支持流分页、 列回流等内容时选择的内容行为<xref:System.Windows.Controls.Grid>却没有。 A<xref:System.Windows.Controls.Grid>另一方面最佳使用外部<xref:System.Windows.Documents.FlowDocument>包括的原因有很多<xref:System.Windows.Controls.Grid>添加基于一个行和列的索引，元素<xref:System.Windows.Documents.Table>却没有。 <xref:System.Windows.Controls.Grid>元素允许的子内容，允许多个元素中的单个"单元格。"存在分层 <xref:System.Windows.Documents.Table> 不支持分层。 子元素的<xref:System.Windows.Controls.Grid>进行绝对定位相对于其"单元格"边界的区域。 <xref:System.Windows.Documents.Table> 不支持此功能。 最后，<xref:System.Windows.Controls.Grid>需要较少的资源则<xref:System.Windows.Documents.Table>因此请考虑使用<xref:System.Windows.Controls.Grid>以提高性能。  
  
<a name="basic_table_structure"></a>   
### <a name="basic-table-structure"></a>基本表结构  
 <xref:System.Windows.Documents.Table> 提供基于网格的表示形式，包括列 (由表示<xref:System.Windows.Documents.TableColumn>元素) 和行 (由表示<xref:System.Windows.Documents.TableRow>元素)。 <xref:System.Windows.Documents.TableColumn> 元素未承载内容;它们只需定义列和列的特性。 <xref:System.Windows.Documents.TableRow> 元素必须承载于<xref:System.Windows.Documents.TableRowGroup>元素，它定义的表的行分组。 <xref:System.Windows.Documents.TableCell> 元素，其中包含由表中显示的实际内容，必须承载于<xref:System.Windows.Documents.TableRow>元素。 <xref:System.Windows.Documents.TableCell> 只能包含派生自的元素<xref:System.Windows.Documents.Block>。  有效的子元素<xref:System.Windows.Documents.TableCell>包括。  
  
-   <xref:System.Windows.Documents.BlockUIContainer>  
  
-   <xref:System.Windows.Documents.List>  
  
-   <xref:System.Windows.Documents.Paragraph>  
  
-   <xref:System.Windows.Documents.Section>  
  
-   <xref:System.Windows.Documents.Table>  
  
> [!NOTE]
>  <xref:System.Windows.Documents.TableCell> 元素可能不会直接承载文本内容。 有关流的包含规则详细信息之类的内容元素<xref:System.Windows.Documents.TableCell>，请参阅[流文档概述](../../../../docs/framework/wpf/advanced/flow-document-overview.md)。  
  
> [!NOTE]
>  <xref:System.Windows.Documents.Table> 类似于<xref:System.Windows.Controls.Grid>元素但具有更多功能，因此，需要更大的资源开销。  
  
 下面的示例定义的简单 2x3 表[!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)]。  
  
 [!code-xaml[TableSnippets2#_Table_BasicLayout](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_basiclayout)]  
  
 下图显示了此示例的呈现效果。  
  
 ![屏幕快照：呈现一个基本表](../../../../docs/framework/wpf/advanced/media/basictablerrender.png "BasicTablerRender")  
  
<a name="table_containment"></a>   
### <a name="table-containment"></a>表包容  
 <xref:System.Windows.Documents.Table> 派生自<xref:System.Windows.Documents.Block>元素，并遵循常见规则<xref:System.Windows.Documents.Block>级别元素。  A<xref:System.Windows.Documents.Table>元素可能包含任何以下元素：  
  
-   <xref:System.Windows.Documents.FlowDocument>  
  
-   <xref:System.Windows.Documents.TableCell>  
  
-   <xref:System.Windows.Controls.ListBoxItem>  
  
-   <xref:System.Windows.Controls.ListViewItem>  
  
-   <xref:System.Windows.Documents.Section>  
  
-   <xref:System.Windows.Documents.Floater>  
  
-   <xref:System.Windows.Documents.Figure>  
  
<a name="row_groupings"></a>   
### <a name="row-groupings"></a>行分组  
 <xref:System.Windows.Documents.TableRowGroup>元素提供对任意行进行分组表中的一种方法; 表中的每行必须属于的行分组。  行分组中的行通常具有相同的用途，并可作为一个组来设置样式。  行分组的一个常见使用方式是用于将特定用途的行（如标题行、标头和页脚行）与表中所含的主内容分隔开来。  
  
 下面的示例使用[!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)]定义具有带样式的页眉和页脚行的表。  
  
 [!code-xaml[TableSnippets2#_Table_RowGroups](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_rowgroups)]  
  
 下图显示了此示例的呈现效果。  
  
 ![屏幕快照：表行组](../../../../docs/framework/wpf/advanced/media/table-rowgroups.png "Table_RowGroups")  
  
<a name="rendering_precedence"></a>   
### <a name="background-rendering-precedence"></a>背景呈现优先级  
 表元素以下列顺序呈现（按 Z 顺序从最低到最高排列）。 此顺序不能更改。 例如，对于这些元素，没有可用于替换此已有顺序的“Z 顺序”属性。  
  
1.  <xref:System.Windows.Documents.Table>  
  
2.  <xref:System.Windows.Documents.TableColumn>  
  
3.  <xref:System.Windows.Documents.TableRowGroup>  
  
4.  <xref:System.Windows.Documents.TableRow>  
  
5.  <xref:System.Windows.Documents.TableCell>  
  
 请参考以下示例，该示例对表内每个元素的背景色进行定义。  
  
 [!code-xaml[TableSnippets2#_Table_ZOrder](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_zorder)]  
  
 下图显示了此示例的呈现方式（仅显示背景色）。  
  
 ![屏幕快照：表 Z 顺序](../../../../docs/framework/wpf/advanced/media/table-zorder.png "Table_ZOrder")  
  
<a name="spanning_rows_or_columns"></a>   
### <a name="spanning-rows-or-columns"></a>跨行或列  
 表格单元格可能配置为通过使用跨多个行或列<xref:System.Windows.Documents.TableCell.RowSpan%2A>或<xref:System.Windows.Documents.TableCell.ColumnSpan%2A>属性，分别。  
  
 请参考以下示例，该示例中有一个跨三列的单元格。  
  
 [!code-xaml[TableSnippets2#_Table_ColumnSpan](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_columnspan)]  
  
 下图显示了此示例的呈现效果。  
  
 ![屏幕快照：跨全部三列的单元格](../../../../docs/framework/wpf/advanced/media/table-columnspan.png "Table_ColumnSpan")  
  
<a name="building_a_table_with_code"></a>   
## <a name="building-a-table-with-code"></a>使用代码生成表  
 下面的示例演示如何以编程方式创建<xref:System.Windows.Documents.Table>和填充其内容。 表的内容分配到五个行 (由表示<xref:System.Windows.Documents.TableRow>中所含对象<xref:System.Windows.Documents.Table.RowGroups%2A>对象) 和六个列 (由表示<xref:System.Windows.Documents.TableColumn>对象)。 各行用于不同的显示目的，其中，标题行用于显示整个表的标题，标头行用于描述表中的数据列，而页脚行则包含摘要信息。  请注意，“标题”行、“标头”行和“页脚”行并非表格所固有的，它们只是具有不同特征的行。 表格单元格包含实际的内容，它可以包含文本、 图像或几乎任何其他[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)]元素。  
  
 首先，<xref:System.Windows.Documents.FlowDocument>创建到主机<xref:System.Windows.Documents.Table>，和一个新<xref:System.Windows.Documents.Table>被创建并添加到的内容<xref:System.Windows.Documents.FlowDocument>。  
  
 [!code-csharp[TableSnippets#_TableCreate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tablecreate)]
 [!code-vb[TableSnippets#_TableCreate](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tablecreate)]  
  
 接下来，六个<xref:System.Windows.Documents.TableColumn>对象会创建并添加到表的<xref:System.Windows.Documents.Table.Columns%2A>集合中的，同时应用一些格式设置。  
  
> [!NOTE]
>  请注意，表的<xref:System.Windows.Documents.Table.Columns%2A>集合使用标准的从零开始索引。  
  
 [!code-csharp[TableSnippets#_TableCreateColumns](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tablecreatecolumns)]
 [!code-vb[TableSnippets#_TableCreateColumns](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tablecreatecolumns)]  
  
 接下来，创建一个标题行，并将其添加到表中，同时应用某些格式设置。  标题行包含一个单元格，该单元格跨表中的全部六列。  
  
 [!code-csharp[TableSnippets#_TableAddTitleRow](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddtitlerow)]
 [!code-vb[TableSnippets#_TableAddTitleRow](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddtitlerow)]  
  
 接下来，创建一个标头行并将其添加到表中，同时创建标头行中的单元格并填充其内容。  
  
 [!code-csharp[TableSnippets#_TableAddHeaderRow](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddheaderrow)]
 [!code-vb[TableSnippets#_TableAddHeaderRow](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddheaderrow)]  
  
 接下来，创建一个数据行并将其添加到表中，同时创建此行中的单元格并填充其内容。  生成此行的过程与生成标头行的过程类似，只是应用的格式设置略有不同。  
  
 [!code-csharp[TableSnippets#_TableAddDataRow](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableadddatarow)]
 [!code-vb[TableSnippets#_TableAddDataRow](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableadddatarow)]  
  
 最后，创建、添加脚注行并设置其格式。  与标题行类似，脚注包含的单元格的跨度为表中的全部六列。  
  
 [!code-csharp[TableSnippets#_TableAddFooterRow](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddfooterrow)]
 [!code-vb[TableSnippets#_TableAddFooterRow](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddfooterrow)]  
  
## <a name="see-also"></a>请参阅  
 [流文档概述](../../../../docs/framework/wpf/advanced/flow-document-overview.md)  
 [使用 XAML 定义表](../../../../docs/framework/wpf/advanced/how-to-define-a-table-with-xaml.md)  
 [WPF 中的文档](../../../../docs/framework/wpf/advanced/documents-in-wpf.md)  
 [使用流内容元素](../../../../docs/framework/wpf/advanced/how-to-use-flow-content-elements.md)
