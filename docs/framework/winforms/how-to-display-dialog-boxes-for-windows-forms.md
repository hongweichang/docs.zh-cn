---
title: "如何：显示 Windows 窗体的对话框"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, displaying
- Windows Forms dialog boxes [Windows Forms], displaying
- Windows Forms, calling one form from another
- dialog boxes [Windows Forms], displaying for Windows Forms
ms.assetid: aaac1b38-c651-495a-8d3d-5a9bfb32fee3
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 46e4d019bbd586c0ed46794f55c65da7bcc657f1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-display-dialog-boxes-for-windows-forms"></a>如何：显示 Windows 窗体的对话框
与应用程序中显示的任何其他形式相同的方式显示一个对话框。 运行应用程序时，启动窗体将自动加载。 若要使第二个窗体或应用程序中显示的对话框中，编写代码以加载并显示它。 同样，若要使窗体或对话框框中消失，编写代码以卸载或隐藏它。  
  
### <a name="to-display-a-dialog-box"></a>若要显示的对话框  
  
1.  导航到你想要打开对话框中的事件处理程序。 这可能发生时选择菜单命令，当单击的按钮，或任何其他事件发生时。  
  
2.  事件处理程序中，添加代码以打开对话框。 在此示例中，按钮单击事件用于显示对话框中：  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       Dim dlg1 as new Form()  
       dlg1.ShowDialog()  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)   
    {  
       Form dlg1 = new Form();  
       dlg1.ShowDialog();  
    }  
    ```  
  
    ```cpp  
    private:   
      void button1_Click(System::Object ^ sender,  
        System::EventArgs ^ e)  
      {  
        Form ^ dlg1 = gcnew Form();  
        dlg1->ShowDialog();  
      }  
    ```
