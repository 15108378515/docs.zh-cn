---
title: 如何：创建自定义活动设计器
ms.date: 03/30/2017
ms.assetid: 2f3aade6-facc-44ef-9657-a407ef8b9b31
ms.openlocfilehash: 86cd3544e9117cca273b6c8dde8454672f14a36a
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "48777677"
---
# <a name="how-to-create-a-custom-activity-designer"></a>如何：创建自定义活动设计器

通常实现自定义活动设计器，以便其相关活动可与其他活动（这些活动的设计器可与它们一起放置到设计图面上）组合在一起。 此功能要求自定义活动设计器提供"放置区"可以放置任意活动的位置以及管理得到的设计图面上的元素集合的方法。 本主题介绍如何创建一个包含上述放置区的自定义活动设计器，以及如何创建一个可提供管理设计器元素集合所需的编辑功能的自定义活动设计器。

 自定义活动设计器通常继承自 <xref:System.Activities.Presentation.ActivityDesigner>，后者是任何无特定设计器的活动的默认基活动设计器类型。 此类型提供与属性网格交互以及配置管理颜色和图标等基本方面的设计时体验。

 <xref:System.Activities.Presentation.ActivityDesigner> 采用两个帮助器控件，即 <xref:System.Activities.Presentation.WorkflowItemPresenter> 和 <xref:System.Activities.Presentation.WorkflowItemsPresenter>，以便更易于开发自定义活动设计器。 这两个控件处理常用功能，例如，拖放子元素，删除、选择和添加这些子元素。 <xref:System.Activities.Presentation.WorkflowItemPresenter>允许单个子级 UI 元素内，提供"放置区"，它同时<xref:System.Activities.Presentation.WorkflowItemsPresenter>可以提供支持多个 UI 元素，包括附加功能，例如排序、 移动、 删除和添加的子元素。

 在实现自定义活动设计器的过程需要强调的其他关键部分是，考虑如何使用 [!INCLUDE[avalon2](../../../includes/avalon2-md.md)] 数据绑定将可视化编辑操作绑定到为记住我们在设计器中编辑的内容而存储的实例。 这是通过模型项树实现的，它还负责启用更改通知和跟踪事件（例如状态的更改）。

 本主题概述了两个过程。

1.  第一个过程介绍如何使用 <xref:System.Activities.Presentation.WorkflowItemPresenter> 创建一个自定义活动设计器，用于提供接收其他活动的放置区。 此过程基于[自定义复合设计器 — 工作流项演示器](../../../docs/framework/windows-workflow-foundation/samples/custom-composite-designers-workflow-item-presenter.md)示例。

2.  第二个过程介绍如何使用 <xref:System.Activities.Presentation.WorkflowItemsPresenter> 创建一个自定义活动设计器，用于提供编辑包含的元素的集合所需的功能。 此过程基于[自定义复合设计器 — 工作流项演示器](../../../docs/framework/windows-workflow-foundation/samples/custom-composite-designers-workflow-items-presenter.md)示例。

## <a name="to-create-a-custom-activity-designer-with-a-drop-zone-using-workflowitempresenter"></a>使用 WorkflowItemPresenter 创建带有放置区的自定义活动设计器

1.  启动 Visual Studio 2010。

2.  上**文件**菜单，依次指向**新建**，然后选择**项目...**.

     **“新建项目”** 对话框随即打开。

3.  在中**已安装的模板**窗格中，选择**Windows**从首选的语言类别。

4.  在中**模板**窗格中，选择**WPF 应用程序**。

5.  在中**名称**框中，输入`UsingWorkflowItemPresenter`。

6.  在中**位置**框中，输入想要保存你的项目，或者单击的目录**浏览**以导航到它。

7.  在中**解决方案**框中，接受默认值。

8.  单击 **“确定”**。

9. 右击 MainWindows.xaml 文件中的，然后**解决方案资源管理器**，选择**删除**，并确认**确定**中**Microsoft Visual Studio**对话框。

10. 右击 UsingWorkflowItemPresenter 项目中的**解决方案资源管理器**，选择**添加**，然后**新项...** 若要打开**添加新项**对话框中，然后选择**WPF**从类别**已安装的模板**左侧部分。

11. 选择**Window (WPF)** 模板，其命名`RehostingWFDesigner`，然后单击**添加**。

12. 打开 RehostingWFDesigner.xaml 文件，将下面的代码粘贴到其中以定义应用程序的 UI。

    ```xml
    <Window x:Class=" UsingWorkflowItemPresenter.RehostingWFDesigner"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:sapt="clr-namespace:System.Activities.Presentation.Toolbox;assembly=System.Activities.Presentation"
            xmlns:sys="clr-namespace:System;assembly=mscorlib"
            Title="Window1" Height="600" Width="900">
        <Window.Resources>
            <sys:String x:Key="AssemblyName">System.Activities, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35</sys:String>
        </Window.Resources>
        <Grid>
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="2*"/>
                <ColumnDefinition Width="7*"/>
                <ColumnDefinition Width="3*"/>
            </Grid.ColumnDefinitions>
            <Border Grid.Column="0">
                <sapt:ToolboxControl Name="Toolbox">
                    <sapt:ToolboxCategory CategoryName="Basic">
                        <sapt:ToolboxItemWrapper AssemblyName="{StaticResource AssemblyName}" >
                            <sapt:ToolboxItemWrapper.ToolName>
                                System.Activities.Statements.Sequence
                            </sapt:ToolboxItemWrapper.ToolName>
                           </sapt:ToolboxItemWrapper>
                        <sapt:ToolboxItemWrapper  AssemblyName="{StaticResource AssemblyName}">
                            <sapt:ToolboxItemWrapper.ToolName>
                                System.Activities.Statements.WriteLine
                            </sapt:ToolboxItemWrapper.ToolName>

                        </sapt:ToolboxItemWrapper>
                        <sapt:ToolboxItemWrapper  AssemblyName="{StaticResource AssemblyName}">
                            <sapt:ToolboxItemWrapper.ToolName>
                                System.Activities.Statements.If
                            </sapt:ToolboxItemWrapper.ToolName>

                        </sapt:ToolboxItemWrapper>
                        <sapt:ToolboxItemWrapper  AssemblyName="{StaticResource AssemblyName}">
                            <sapt:ToolboxItemWrapper.ToolName>
                                System.Activities.Statements.While
                            </sapt:ToolboxItemWrapper.ToolName>

                        </sapt:ToolboxItemWrapper>
                    </sapt:ToolboxCategory>
                </sapt:ToolboxControl>
            </Border>
            <Border Grid.Column="1" Name="DesignerBorder"/>
            <Border Grid.Column="2" Name="PropertyBorder"/>
        </Grid>
    </Window>
    ```

13. 若要将活动设计器与活动类型相关联，您必须向元数据存储注册活动设计器。 为此，请将 `RegisterMetadata` 方法添加到 `RehostingWFDesigner` 类中。 在 `RegisterMetadata` 方法的范围内，创建一个 <xref:System.Activities.Presentation.Metadata.AttributeTableBuilder> 对象，并调用 <xref:System.Activities.Presentation.Metadata.AttributeTableBuilder.AddCustomAttributes%2A> 方法以向其添加特性。 调用 <xref:System.Activities.Presentation.Metadata.MetadataStore.AddAttributeTable%2A> 方法以向元数据存储添加 <xref:System.Activities.Presentation.Metadata.AttributeTable>。 下面的代码包含设计器的重新承载逻辑。 它注册元数据，将 `SimpleNativeActivity` 放入工具箱中，并创建工作流。 将此代码放入 RehostingWFDesigner.xaml.cs 文件中。

    ```
    using System;
    using System.Activities.Core.Presentation;
    using System.Activities.Presentation;
    using System.Activities.Presentation.Metadata;
    using System.Activities.Presentation.Toolbox;
    using System.Activities.Statements;
    using System.ComponentModel;
    using System.Windows;

    namespace UsingWorkflowItemPresenter
    {
        // Interaction logic for RehostingWFDesigner.xaml
        public partial class RehostingWFDesigner
        {
            public RehostingWFDesigner()
            {
                InitializeComponent();
            }

            protected override void OnInitialized(EventArgs e)
            {
                base.OnInitialized(e);
                // register metadata
                (new DesignerMetadata()).Register();
                RegisterCustomMetadata();
                // add custom activity to toolbox
                Toolbox.Categories.Add(new ToolboxCategory("Custom activities"));
                Toolbox.Categories[1].Add(new ToolboxItemWrapper(typeof(SimpleNativeActivity)));

                // create the workflow designer
                WorkflowDesigner wd = new WorkflowDesigner();
                wd.Load(new Sequence());
                DesignerBorder.Child = wd.View;
                PropertyBorder.Child = wd.PropertyInspectorView;

            }

            void RegisterCustomMetadata()
            {
                AttributeTableBuilder builder = new AttributeTableBuilder();
                builder.AddCustomAttributes(typeof(SimpleNativeActivity), new DesignerAttribute(typeof(SimpleNativeDesigner)));
                MetadataStore.AddAttributeTable(builder.CreateTable());
            }
        }
    }
    ```

14. 右键单击解决方案资源管理器中的引用目录，然后选择**添加引用...** 若要打开**添加引用**对话框。

15. 单击 **.NET**选项卡上，找到名为程序集**System.Activities.Core.Presentation**，选择它，然后单击**确定**。

16. 使用相同的过程，添加对下列程序集的引用：

    1.  System.Data.DataSetExtensions.dll

    2.  System.Activities.Presentation.dll

    3.  System.ServiceModel.Activities.dll

17. 打开 App.xaml 文件并将 StartUpUri 的值更改为"RehostingWFDesigner.xaml"。

18. 右击 UsingWorkflowItemPresenter 项目中的**解决方案资源管理器**，选择**添加**，然后**新项...** 若要打开**添加新项**对话框中，然后选择**工作流**类别窗体**已安装的模板**左侧部分。

19. 选择**活动设计器**模板，其命名`SimpleNativeDesigner`，然后单击**添加**。

20. 打开 SimpleNativeDesigner.xaml 文件，并将下列代码粘贴到其中。 请注意，此代码使用 <xref:System.Activities.Presentation.ActivityDesigner> 作为根元素，并演示如何使用绑定将 <xref:System.Activities.Presentation.WorkflowItemPresenter> 集成到设计器中，以便可以在复合活动设计器中显示子类型。

    > [!NOTE]
    >  <xref:System.Activities.Presentation.ActivityDesigner> 的架构只允许向自定义活动设计器定义中添加一个子元素；不过，这个元素可以是 `StackPanel`、`Grid` 或某些其他复合 UI 元素。

    ```xml
    <sap:ActivityDesigner x:Class=" UsingWorkflowItemPresenter.SimpleNativeDesigner"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:sap="clr-namespace:System.Activities.Presentation;assembly=System.Activities.Presentation"
        xmlns:sapv="clr-namespace:System.Activities.Presentation.View;assembly=System.Activities.Presentation">
        <sap:ActivityDesigner.Resources>
            <DataTemplate x:Key="Collapsed">
                <StackPanel>
                    <TextBlock>This is the collapsed view</TextBlock>
                </StackPanel>
            </DataTemplate>
            <DataTemplate x:Key="Expanded">
                <StackPanel>
                    <TextBlock>Custom Text</TextBlock>
                    <sap:WorkflowItemPresenter Item="{Binding Path=ModelItem.Body, Mode=TwoWay}"
                                            HintText="Please drop an activity here" />
                </StackPanel>
            </DataTemplate>
            <Style x:Key="ExpandOrCollapsedStyle" TargetType="{x:Type ContentPresenter}">
                <Setter Property="ContentTemplate" Value="{DynamicResource Collapsed}"/>
                <Style.Triggers>
                    <DataTrigger Binding="{Binding Path=ShowExpanded}" Value="true">
                        <Setter Property="ContentTemplate" Value="{DynamicResource Expanded}"/>
                    </DataTrigger>
                </Style.Triggers>
            </Style>
        </sap:ActivityDesigner.Resources>
        <Grid>
            <ContentPresenter Style="{DynamicResource ExpandOrCollapsedStyle}" Content="{Binding}" />
        </Grid>
    </sap:ActivityDesigner>
    ```

21. 右击 UsingWorkflowItemPresenter 项目中的**解决方案资源管理器**，选择**添加**，然后**新项...** 若要打开**添加新项**对话框中，然后选择**工作流**类别窗体**已安装的模板**左侧部分。

22. 选择**代码活动**模板，其命名`SimpleNativeActivity`，然后单击**添加**。

23. 通过在 SimpleNativeActivity.cs 文件中输入下面的代码，实现 `SimpleNativeActivity` 类。

    ```
    using System.Activities;

    namespace UsingWorkflowItemPresenter
    {
        public sealed class SimpleNativeActivity : NativeActivity
        {
            // this property contains an activity that will be scheduled in the execute method
    // the WorkflowItemPresenter in the designer is bound to this to enable editing
    // of the value
            public Activity Body { get; set; }

            protected override void CacheMetadata(NativeActivityMetadata metadata)
            {
               metadata.AddChild(Body);
               base.CacheMetadata(metadata);

            }

            protected override void Execute(NativeActivityContext context)
            {
                context.ScheduleActivity(Body);
            }
        }
    }
    ```

24. 选择**生成解决方案**从**生成**菜单。

25. 选择**启动但不调试**从**调试**菜单以打开重新承载的自定义设计窗口。

### <a name="to-create-a-custom-activity-designer-using-workflowitemspresenter"></a>使用 WorkflowItemsPresenter 创建自定义活动设计器

1.  第二个自定义活动设计器的过程是首次进行一些修改，其中第一个是第二个应用程序命名的 parallels `UsingWorkflowItemsPresenter`。 另外，此应用程序不会定义新的自定义活动。

2.  主要差别包含在 CustomParallelDesigner.xaml 和 RehostingWFDesigner.xaml.cs 文件中。 下面是 CustomParallelDesigne.xaml 文件中定义 UI 的代码。

    ```xml
    <sap:ActivityDesigner x:Class=" UsingWorkflowItemsPresenter.CustomParallelDesigner"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:sap="clr-namespace:System.Activities.Presentation;assembly=System.Activities.Presentation"
        xmlns:sapv="clr-namespace:System.Activities.Presentation.View;assembly=System.Activities.Presentation">
        <sap:ActivityDesigner.Resources>
            <DataTemplate x:Key="Collapsed">
                <TextBlock>This is the Collapsed View</TextBlock>
            </DataTemplate>
            <DataTemplate x:Key="Expanded">
                <StackPanel>
                    <TextBlock HorizontalAlignment="Center">This is the</TextBlock>
                    <TextBlock HorizontalAlignment="Center">extended view</TextBlock>
                    <sap:WorkflowItemsPresenter HintText="Drop Activities Here"
                                        Items="{Binding Path=ModelItem.Branches}">
                        <sap:WorkflowItemsPresenter.SpacerTemplate>
                            <DataTemplate>
                                <Ellipse Width="10" Height="10" Fill="Black"/>
                            </DataTemplate>
                        </sap:WorkflowItemsPresenter.SpacerTemplate>
                        <sap:WorkflowItemsPresenter.ItemsPanel>
                            <ItemsPanelTemplate>
                                <StackPanel Orientation="Horizontal"/>
                            </ItemsPanelTemplate>
                        </sap:WorkflowItemsPresenter.ItemsPanel>
                    </sap:WorkflowItemsPresenter>
                </StackPanel>
            </DataTemplate>
            <Style x:Key="ExpandOrCollapsedStyle" TargetType="{x:Type ContentPresenter}">
                <Setter Property="ContentTemplate" Value="{DynamicResource Collapsed}"/>
                <Style.Triggers>
                    <DataTrigger Binding="{Binding Path=ShowExpanded}" Value="true">
                        <Setter Property="ContentTemplate" Value="{DynamicResource Expanded}"/>
                    </DataTrigger>
                </Style.Triggers>
            </Style>
        </sap:ActivityDesigner.Resources>
        <Grid>
            <ContentPresenter Style="{DynamicResource ExpandOrCollapsedStyle}" Content="{Binding}"/>
        </Grid>
    </sap:ActivityDesigner>
    ```

3.  下面是 RehostingWFDesigner.xaml.cs 文件中提供重新承载逻辑的代码。

    ```
    using System;
    using System.Activities.Core.Presentation;
    using System.Activities.Presentation;
    using System.Activities.Presentation.Metadata;
    using System.Activities.Statements;
    using System.ComponentModel;
    using System.Windows;

    namespaceUsingWorkflowItemsPresenter
    {
        public partial class RehostingWfDesigner : Window
        {
            public RehostingWfDesigner()
            {
                InitializeComponent();
            }

            protected override void OnInitialized(EventArgs e)
            {
                base.OnInitialized(e);
                // register metadata
                (new DesignerMetadata()).Register();
                RegisterCustomMetadata();

                // create the workflow designer
                WorkflowDesigner wd = new WorkflowDesigner();
                wd.Load(new Sequence());
                DesignerBorder.Child = wd.View;
                PropertyBorder.Child = wd.PropertyInspectorView;

            }

            void RegisterCustomMetadata()
            {
                AttributeTableBuilder builder = new AttributeTableBuilder();
                builder.AddCustomAttributes(typeof(Parallel), new DesignerAttribute(typeof(CustomParallelDesigner)));
                MetadataStore.AddAttributeTable(builder.CreateTable());
            }
        }
    }
    ```

## <a name="see-also"></a>请参阅

- <xref:System.Activities.Presentation.ActivityDesigner>
- <xref:System.Activities.Presentation.WorkflowItemPresenter>
- <xref:System.Activities.Presentation.WorkflowItemsPresenter>
- <xref:System.Activities.Presentation.WorkflowViewElement>
- <xref:System.Activities.Presentation.Model.ModelItem>
- [自定义工作流设计体验](../../../docs/framework/windows-workflow-foundation/customizing-the-workflow-design-experience.md)