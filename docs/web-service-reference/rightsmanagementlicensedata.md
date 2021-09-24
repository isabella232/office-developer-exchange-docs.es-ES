---
title: RightsManagementLicenseData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 38f0b7f4-2338-4e90-af67-e0951e8edfa3
description: El elemento RightsManagementLicenseData especifica información sobre la licencia de administración de derechos de un elemento.
ms.openlocfilehash: 8875e9bad425224f86b6de5149f87a36c2a2581e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523471"
---
# <a name="rightsmanagementlicensedata"></a>RightsManagementLicenseData

El **elemento RightsManagementLicenseData** especifica información sobre la licencia de administración de derechos de un elemento. 
  
```XML
<RightsManagementLicenseData>
   <RightsManagedMessageDecryptionStatus/>
   <RmsTemplateId/>
   <TemplateName/>
   <TemplateDescription/>
   <EditAllowed/>
   <ReplyAllowed/>
   <ReplyAllAllowed/>
   <ForwardAllowed/>
   <ModifyRecipientsAllowed/>
   <ExtractAllowed/>
   <PrintAllowed/>
   <ExportAllowed/>
   <ProgrammaticAccessAllowed/>
   <IsOwner/>
   <ContentOwner/>
   <ContentExpiryDate/>
</RightsManagementLicenseData>
```

 **RightsManagementLicenseDataType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md)  |  [RMSTemplateId](rmstemplateid.md)  |  [TemplateName](templatename.md)  |  [TemplateDescription](templatedescription.md)  |  [EditAllowed](editallowed.md)  |  [ReplyAllowed](replyallowed.md)  |  [ReplyAllAllowed](replyallallowed.md)  |  [ForwardAllowed](forwardallowed.md)  |  [ModifyRecipientsAllowed](modifyrecipientsallowed.md)  |  [ExtractAllowed](extractallowed.md)  |  [PrintAllowed](printallowed.md)  |  [ExportAllowed](exportallowed.md)  |  [ProgrammaticAccessAllowed](programmaticaccessallowed.md)  |  [IsOwner](isowner.md)  |  [ContentOwner](contentowner.md)  |  [ContentExpiryDate](contentexpirydate.md)
  
### <a name="parent-elements"></a>Elementos principales

[Elemento](item.md)  |  [Mensaje](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Tarea](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

