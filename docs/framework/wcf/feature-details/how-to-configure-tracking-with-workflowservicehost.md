---
title: "如何：使用 WorkflowServiceHost 配置跟踪"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ed1485fe-7529-4351-bca3-8bb915260b17
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 1b9bba3c589ca0232171bab58c26b19c7312a313
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-configure-tracking-with-workflowservicehost"></a>如何：使用 WorkflowServiceHost 配置跟踪
本主题说明如何为 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] 中承载的 <xref:System.ServiceModel.Activities.WorkflowServiceHost>工作流配置跟踪。 可以通过指定服务行为使用 Web.config 文件进行配置。  
  
### <a name="configure-tracking-in-configuration"></a>在配置中配置跟踪  
  
1.  在配置文件中使用 <<xref:System.Activities.Tracking.EtwTrackingParticipant>> 元素添加 `behavior`，如下面的示例所示。  
  
    ```xml  
    <behaviors>  
       <serviceBehaviors>  
         <behavior>  
           <etwTracking profileName="Sample Tracking Profile" />  
         </behavior>              
       </serviceBehaviors>  
    <behaviors>  
    ```  
  
    > [!NOTE]
    >  上面的配置示例使用的是简化配置。 [!INCLUDE[crdefault](../../../../includes/crdefault-md.md)][简化了配置](../../../../docs/framework/wcf/simplified-configuration.md)。  
  
     上面的配置示例添加一个 <xref:System.Activities.Tracking.EtwTrackingParticipant>，并指定一个跟踪配置文件名称。 跟踪配置文件是在 <`trackingProfile`> 元素的 <`tracking`> 元素中创建的。 跟踪配置文件包含跟踪查询，这些查询允许跟踪参与者订阅工作流实例的状态在运行时发生更改时发出的工作流事件。 下面的示例演示如何创建跟踪配置文件。  
  
    ```xml  
    <system.serviceModel>  
        <tracking>   
         <trackingProfile name="Sample Tracking Profile">  
            <workflow activityDefinitionId="*">  
               <workflowInstanceQueries>  
                 <workflowInstanceQuery>  
                    <states>  
                       <state name="Started"/>  
                       <state name="Completed"/>  
                    </states>  
                </workflowInstanceQuery>  
             </workflowInstanceQueries>  
           </workflow>  
         </trackingProfile>   
       </tracking>  
    </system.serviceModel>  
    ```  
  
     [!INCLUDE[crabout](../../../../includes/crabout-md.md)]跟踪配置文件，请参阅[跟踪配置文件](../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)。  
  
     [!INCLUDE[crabout](../../../../includes/crabout-md.md)]跟踪一般情况下，请参阅[工作流跟踪](../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)。  
  
### <a name="configure-tracking-in-code"></a>在代码中配置跟踪  
  
1.  在代码中使用 <xref:System.Activities.Tracking.EtwTrackingParticipant> 行为添加 <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior>，如下面的示例所示。  
  
    ```csharp  
    host.Description.Behaviors.Add(new EtwTrackingBehavior { ProfileName = "Sample Tracking Profile" });  
    ```  
  
     上面的代码示例添加一个 <xref:System.Activities.Tracking.EtwTrackingParticipant>，并指定一个跟踪配置文件名称。 跟踪配置文件是在 <`trackingProfile`> 元素的 <`tracking`> 元素中创建的，如上一节所示。  
  
     [!INCLUDE[crabout](../../../../includes/crabout-md.md)]跟踪配置文件，请参阅[跟踪配置文件](../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)。  
  
     [!INCLUDE[crabout](../../../../includes/crabout-md.md)]跟踪一般情况下，请参阅[工作流跟踪](../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)。 有关配置跟踪以编程方式的示例请参阅[工作流配置跟踪](../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md)。  
  
## <a name="see-also"></a>请参阅  
 [WCF 服务的简化配置](../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)  
 [工作流服务](../../../../docs/framework/wcf/feature-details/workflow-services.md)  
 [跟踪配置文件](../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
