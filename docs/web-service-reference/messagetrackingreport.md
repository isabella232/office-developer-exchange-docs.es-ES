---
title: MessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingReport
api_type:
- schema
ms.assetid: 2740bcf6-f86d-4756-a0f2-24ed6e9b75f7
description: El elemento MessageTrackingReport contiene un único mensaje que se devuelve en una operación GetMessageTrackingReport.
ms.openlocfilehash: aa55bb9e4f81a4cc0586d7258720aefd743923fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539362"
---
# <a name="messagetrackingreport"></a>MessageTrackingReport

El **elemento MessageTrackingReport** contiene un único mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).
  
```XML
<MessageTrackingReport>
   <Sender/>
   <PurportedSender/>
   <Subject/>
   <SubmitTime/>
   <OriginalRecipients/>
   <RecipientTrackingEvents/>
   <Properties/>
</MessageTrackingReport>
```

 **MessageTrackingReportType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contiene información de contacto del remitente del mensaje de correo electrónico.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contiene información de contacto del supuesto remitente de un mensaje de correo electrónico.  <br/> |
|[Asunto](subject.md) <br/> |Contiene el asunto del mensaje de correo electrónico.  <br/> |
|[SubmitTime](submittime.md) <br/> |Contiene la hora del día en que se envió el mensaje de correo electrónico.  <br/> |
|[OriginalRecipients](originalrecipients.md) <br/> |Contiene una lista de los destinatarios del mensaje de correo electrónico.  <br/> |
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Contiene una lista de uno o más eventos de seguimiento para los destinatarios.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contiene una lista de una o más propiedades de seguimiento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Contiene el resultado de una única [solicitud de operación GetMessageTrackingReport.](getmessagetrackingreport-operation.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)
  
[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
  
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

